---
title: Como mover os bancos de dados do MBAM 2.5
description: Como mover os bancos de dados do MBAM 2.5
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795990"
---
# Como mover os bancos de dados do MBAM 2.5

Use estes procedimentos para mover os seguintes bancos de dados de um computador para outro; do servidor A para o servidor B, por exemplo:

-   Banco de dados de auditoria e conformidade

-   Banco de dados de recuperação

>[!NOTE]
>É importante que os bancos de dados sejam restaurados para o computador B antes de executar o assistente de configuração do MBAM para atualizá-los/configurá-los.

Se os bancos de dados não estiverem presentes, o assistente de configuração criará bancos de dados novos e vazios. Quando os bancos de dados existentes forem restaurados, esse processo irá interromper a configuração do MBAM.

Restaure os bancos de dados primeiro e, em seguida, execute o assistente de configuração do MBAM, escolha a opção banco de dados, e o assistente de configuração será "conectado" aos bancos de dados restaurados; atualizá-los, se necessário, como parte do processo.

**Se estiver movendo vários recursos, mova-os na seguinte ordem:**

1.  Banco de dados de recuperação

2.  Banco de dados de auditoria e conformidade

3.  Relatórios

4.  Site de administração e monitoramento

5.  Portal de autoatendimento

>[!Note]
>Para executar os exemplos de scripts do Windows PowerShell fornecidos neste tópico, você deve atualizar a política de execução do Windows PowerShell para permitir que os scripts sejam executados. Consulte [executando scripts do Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obter instruções.

## Mover o banco de dados de recuperação

As etapas de alto nível para mover o banco de dados de recuperação são:

1.  Parar todas as instâncias do site de administração e monitoramento do MBAM

2.  Fazer backup do banco de dados de recuperação no servidor A

3.  Mover o banco de dados de recuperação do servidor a para o servidor B

4.  Restaurar o banco de dados de recuperação no servidor B

5.  Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão

6.  Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B

7.  Retomar a instância do site de administração e monitoramento

### Como mover o banco de dados de recuperação

**Interrompa todas as instâncias do site de administração e monitoramento do MBAM.** Em cada servidor que está executando o site do servidor de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site de administração e monitoramento.

Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para executar esse comando, você deve adicionar o módulo serviços de informações da Internet (IIS) para Windows PowerShell à instância atual do Windows PowerShell.

### Fazer backup do banco de dados de recuperação no servidor A

1.  Use a tarefa de **backup** no SQL Server Management Studio para fazer backup do banco de dados de recuperação no servidor A.  Por padrão, o nome do banco de dados é **MBAM banco de dados de recuperação**.

2.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL e altere o banco de dados de recuperação do MBAM para usar o modo de recuperação completa:

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

3.  Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente:

    **$Password $** -senha usada para criptografar o arquivo de chave privada.

4.  No Windows PowerShell, execute o script armazenado no arquivo e semelhante ao seguinte:

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente:

    **$ServerName $ \ $SQLINSTANCENAME $** -nome e instância do servidor do qual será feito o backup do banco de dados de recuperação.

### Mover o banco de dados de recuperação do servidor a para o servidor B

Use o Windows Explorer para mover o arquivo **dados. bak do banco de dados de recuperação do MBAM** do servidor a para o servidor B.

Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
Use as informações da tabela a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.

| **Parâmetro**        | **Descrição**  |
|----------------------|------------------|
| $SERVERNAME $       | Nome do servidor para o qual os arquivos serão copiados. |
| $DESTINATIONSHARE $ | Nome do compartilhamento e do caminho para o qual os arquivos serão copiados. |


### Restaurar o banco de dados de recuperação no servidor B

1.  Restaure o banco de dados de recuperação no servidor B usando a tarefa **restaurar banco de dados** no SQL Server Management Studio.

2.  Quando a tarefa anterior terminar, selecione **do dispositivo**e, em seguida, selecione o arquivo de backup do banco de dados.

3.  Use o comando **Adicionar** para selecionar o arquivo **dados. bak do banco de dados de recuperação do MBAM** e clique em **OK** para concluir o processo de restauração.

4.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

    FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

    WITH REPLACE
    ```

5.  Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.

    **$Password $** -senha usada para criptografar o arquivo de chave privada.

6.  No Windows PowerShell, execute o script armazenado no arquivo e semelhante ao seguinte:

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.

    **$ServerName $ \ $SQLINSTANCENAME $** -nome do servidor e instância para os quais o banco de dados de recuperação será restaurado.

### Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão

1. Verifique se o logon de usuário do Microsoft SQL Server que permite o acesso ao banco de dados de recuperação no banco de dados restaurado está mapeado para a conta do Access que você forneceu durante o processo de configuração.

   >[!NOTE]
   >Se o logon não for o mesmo, crie um logon usando o SQL Server Management Studio e mapeie-o para o usuário de banco de dados existente.

2. No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os sites do MBAM.

3. Edite a seguinte chave do registro:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. Atualize o valor da **fonte de dados** com o nome do servidor e da instância (por exemplo, \ $ServerName \ $ \ \ \ \ $SQLINSTANCENAME) à qual o banco de dados de recuperação foi movido.

5. Atualize o valor **inicial do catálogo** com o nome do banco de dados recuperado.

6. Para automatizar esse processo, você pode usar o prompt de comando do Windows PowerShell para inserir uma linha de comando no servidor de administração e monitoramento semelhante à seguinte:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   >Esta cadeia de conexão é compartilhada por todos os aplicativos Web MBAM locais. Portanto, ele precisa ser atualizado apenas uma vez por servidor.


7. Use a tabela a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.

   |Parâmetro|Descrição|
   |---------|-----------|
   |$SERVERNAME $/\ $SQLINSTANCENAME $|Nome do servidor e instância do SQL Server em que o banco de dados de recuperação está localizado.|
   |$DATABASE $|Nome do banco de dados de recuperação.|


### Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B

1.  Instale o software de servidor MBAM 2,5 no servidor B. Para obter detalhes, consulte [instalando o software de servidor MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso de **banco de dados de recuperação** . Para obter detalhes sobre como configurar os bancos de dados, consulte [como configurar os bancos de dados do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Você também pode usar o cmdlet **Enable-MbamDatabase** do Windows PowerShell para configurar o banco de dados de recuperação.


### Retomar a instância do site de administração e monitoramento

No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site de administração e monitoramento.

Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para executar esse comando, você deve adicionar o módulo do IIS para Windows PowerShell à instância atual do Windows PowerShell.

## Mover o banco de dados de auditoria e conformidade

As etapas de alto nível para mover o banco de dados de auditoria e conformidade são:

1.  Parar todas as instâncias do site de administração e monitoramento do MBAM

2.  Fazer backup do banco de dados de conformidade e auditoria no servidor A

3.  Mover o banco de dados de auditoria e conformidade do servidor A para o servidor B

4.  Restaurar o banco de dados de auditoria e conformidade no servidor B

5.  Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão

6.  Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B

7.  Retomar a instância do site de administração e monitoramento

### Como migrar o banco de dados de auditoria e conformidade

**Interrompa todas as instâncias do site de administração e monitoramento do MBAM.**  Em cada servidor que está executando o site do servidor de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site de administração e monitoramento.

Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para executar esse comando, você deve adicionar o módulo serviços de informações da Internet (IIS) para Windows PowerShell à instância atual do Windows PowerShell.

### Fazer backup do banco de dados de conformidade e auditoria no servidor A

1.  Use a tarefa de **backup** no SQL Server Management Studio para fazer backup do banco de dados de auditoria e conformidade no servidor A. Por padrão, o nome do banco de dados é **MBAM banco de dados de status de conformidade**.

2.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  Execute o script que está armazenado no arquivo. SQL usando um comando do Windows PowerShell semelhante ao seguinte:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  Usando o valor a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente:

    **$ServerName $ \ $SQLINSTANCENAME $** -nome e instância do servidor do qual será feito o backup do banco de dados de auditoria e conformidade.

### Mover o banco de dados de auditoria e conformidade do servidor A para o servidor B * *

1.  Use o Windows Explorer para mover o arquivo **dados. bak do banco de dados de status de conformidade do MBAM** do servidor a para o servidor B.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  Usando a tabela a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.

    | **Parâmetro**        | **Descrição**                                               |
    |----------------------|---------------------------------------------------------------|
    | $SERVERNAME $       | Nome do servidor para o qual os arquivos serão copiados.         |
    | $DESTINATIONSHARE $ | Nome do compartilhamento e do caminho para o qual os arquivos serão copiados. |


### Restaurar o banco de dados de auditoria e conformidade no servidor B

1.  Restaure o banco de dados de auditoria e conformidade no servidor B usando a tarefa **restaurar banco de dados** no SQL Server Management Studio.

2.  Quando a tarefa anterior terminar, selecione **do dispositivo**e, em seguida, selecione o arquivo de backup do banco de dados.

3.  Use o comando **Adicionar** para selecionar o arquivo **dados. bak do status de conformidade do MBAM** e clique em **OK** para concluir o processo de restauração.

4.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  No Windows PowerShell, execute o script armazenado no arquivo e semelhante ao seguinte:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  Usando o valor a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.

    **$ServerName $ \ $SQLINSTANCENAME $** -nome e instância do servidor ao qual o banco de dados de auditoria e conformidade será restaurado.

### Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão

1. Verifique se o logon de usuário do Microsoft SQL Server que permite a conformidade e o acesso ao banco de dados de auditoria no banco de dados restaurado está mapeado para a conta de acesso que você forneceu durante o processo de configuração.

   >[!NOTE]
   >Se o logon não for o mesmo, crie um logon usando o SQL Server Management Studio e mapeie-o para o usuário de banco de dados existente.

2. No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão do site.

3. Edite a seguinte chave do registro:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. Atualize o valor da **fonte de dados** com o nome do servidor e da instância (por exemplo, \ $ServerName \ $ \ \ \ \ $SQLINSTANCENAME) à qual o banco de dados de recuperação foi movido.

5. Atualize o valor **inicial do catálogo** com o nome do banco de dados recuperado.

6. Para automatizar esse processo, você pode usar o prompt de comando do Windows PowerShell para inserir uma linha de comando no servidor de administração e monitoramento semelhante à seguinte:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >Esta cadeia de conexão é compartilhada por todos os aplicativos Web MBAM locais. Portanto, ele precisa ser atualizado apenas uma vez por servidor.


7. Usando a tabela a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.

   |Parâmetro | Descrição |
   |---------|------------|
   |$SERVERNAME $ \ $SQLINSTANCENAME $ | Nome do servidor e instância do SQL Server em que o banco de dados de recuperação está localizado.|
   |$DATABASE $|Nome do banco de dados recuperado.|

### Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B

1.  Instale o software de servidor MBAM 2,5 no servidor B. Para obter detalhes, consulte [instalando o software de servidor MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso **conformidade e banco de dados de auditoria** . Para obter detalhes sobre como configurar os bancos de dados, consulte [como configurar os bancos de dados do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Você também pode usar o cmdlet **Enable-MbamDatabase** do Windows PowerShell para configurar o banco de dados de auditoria e conformidade.


### Retomar a instância do site de administração e monitoramento

No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site de administração e monitoramento.

Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para executar esse comando, você deve adicionar o módulo do IIS para Windows PowerShell à instância atual do Windows PowerShell.
