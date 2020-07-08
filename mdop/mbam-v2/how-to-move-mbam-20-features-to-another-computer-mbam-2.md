---
title: Como mover os recursos do MBAM 2.0 para outro computador
description: Como mover os recursos do MBAM 2.0 para outro computador
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799600"
---
# Como mover os recursos do MBAM 2.0 para outro computador


Este tópico descreve as etapas que você deve seguir para mover um ou mais recursos de administração e monitoramento do Microsoft BitLocker (MBAM) para um computador diferente. Ao mover mais de um recurso de administração e monitoramento do Microsoft BitLocker, você deve movê-los na seguinte ordem:

1.  Banco de dados de recuperação

2.  Banco de dados de auditoria e conformidade

3.  Relatórios de conformidade e auditoria

4.  Administração e monitoramento

## Movendo o banco de dados de recuperação


Para mover o banco de dados de recuperação de um computador para outro (por exemplo, do servidor A para o servidor B), use o procedimento a seguir.

1.  Interrompa todas as instâncias do site de administração e monitoramento.

2.  Execute a instalação do MBAM no servidor B.

3.  Faça o backup do banco de dados de recuperação do MBAM no servidor A.

4.  Mova o banco de dados de recuperação do MBAM do servidor A para o B.

5.  Restaure o banco de dados de recuperação do MBAM no servidor B.

6.  Configure o acesso ao banco de dados de recuperação do MBAM no servidor B.

7.  Atualize os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM.

8.  Retome todas as instâncias do site de administração e monitoramento do MBAM.

**Parar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM, que é chamado **Administração e monitoramento do Microsoft BitLocker**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Observação**  
    Para executar essa linha de comando do PowerShell, o módulo do IIS para PowerShell deve ser adicionado à instância atual do PowerShell. Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.



**Executar a instalação do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione apenas o **banco de dados de recuperação** para instalação.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância para a qual o banco de dados de recuperação será movido.

    -   $DOMAIN $ \ \ $SERVERNAME $-Insira os nomes de domínio e servidor de cada servidor de administração e monitoramento do MBAM que entrarão em contato com o banco de dados de recuperação. Use um ponto-e-vírgula para separar cada par de domínio e servidor na lista (por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $). Cada nome de servidor deve ser seguido por um símbolo "$", conforme mostrado no exemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.



**Fazer backup do banco de dados de recuperação no servidor A**

1.  Para fazer backup do banco de dados de recuperação no servidor A, use o SQL Server Management Studio e a tarefa chamada fazer backup. Por padrão, o nome do banco de dados é **MBAM banco de dados de recuperação**.

2.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:

    Modifique o banco de dados de recuperação do MBAM para usar o modo de recuperação completo.

    ```sql
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

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $PASSWORD $-Insira uma senha que será usada para criptografar o arquivo de chave privada.



3.  Execute o arquivo SQL usando o SQL Server PowerShell e uma linha de comando semelhante à seguinte:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e da instância do qual será feito o backup do banco de dados de recuperação.



**Mover o banco de dados de recuperação e o certificado do servidor a para o servidor B**

1.  Mova o arquivo a seguir do servidor A para o servidor B usando o Windows Explorer.

    -   Dados de banco de dados de recuperação MBAM. bak

2.  Para mover o certificado para o banco de dados criptografado, use as etapas de automação a seguir. Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Observação**  
    Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $-Insira o nome do servidor para o qual os arquivos serão copiados.

    -   $DESTINATIONSHARE $-Insira o nome do compartilhamento e o caminho para os quais os arquivos serão copiados.



**Restaurar o banco de dados de recuperação no servidor B**

1.  Restaure o banco de dados de recuperação no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados**.

2.  Após a conclusão da tarefa, selecione o arquivo de backup do banco de dados selecionando a opção **do dispositivo** e, em seguida, use o comando **Adicionar** para selecionar o arquivo **Data. bak** do banco de dados de recuperação do MBAM.

3.  Selecione **OK** para concluir o processo de restauração.

4.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

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

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $PASSWORD $-Insira uma senha que você usou para criptografar o arquivo de chave privada.



5.  Você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e da instância para a qual o banco de dados de recuperação será restaurado.



**Configurar o acesso ao banco de dados de recuperação no servidor B**

1.  No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que está executando o recurso de administração e monitoramento do MBAM para o grupo local chamado **MBAM recuperação e acesso ao banco de**dados de hardware.

2.  Verifique se o acesso ao SQL login **MBAM recuperação e o acesso de BD de hardware** no banco de dados restaurado está mapeado para o nome de logon **$MachineName $ \\MBAM recuperação e acesso ao banco de dados de hardware**. Se não estiver mapeado como descrito, crie outro logon com associações de grupo semelhantes e mapeie-o para o nome de logon **$MachineName $ \\MBAM de recuperação e acesso ao banco de dados de hardware**.

3.  Para automatizar esse procedimento, você pode usar o Windows PowerShell no servidor B para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Observação**  
    Substitua os seguintes valores no exemplo acima pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM. O nome do servidor deve ser seguido por $, conforme mostrado no exemplo (por exemplo, MyDomain\\MyServerName1 $).



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Atualizar os dados de conexão do banco de dados de recuperação nos servidores de administração e monitoramento do MBAM**

1. Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que são hospedados no site de administração e monitoramento:

   -   MBAMAdministrationService

   -   MBAMRecoveryAndHardwareService

2. Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.

3. Selecione a opção **configurationStrings** no controle da **lista de seções** .

4. Selecione a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.

5. No **Editor de coleção**, selecione a linha chamada **KeyRecoveryConnectionString** ao atualizar a configuração do aplicativo MBAMAdministrationService ou a linha denominada <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> ConnectionString ao atualizar a configuração do MBAMRecoveryAndHardwareService.

6. Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome e a instância do servidor (por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $) em que o banco de dados de recuperação foi movido.

7. Para automatizar esse procedimento, você pode usar o Windows para inserir uma linha de comando, que é semelhante ao seguinte, em cada servidor de administração e monitoramento:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Observação**  
   Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de recuperação está.



**Retomar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM, que é chamado **de administração e administração do Microsoft BitLocker**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Movendo o recurso de banco de dados de auditoria e conformidade


Se você quiser mover o banco de dados de auditoria e conformidade com o MBAM de um computador para outro (ou seja, mover o banco de dados do servidor A para o servidor B), use o procedimento a seguir. O processo inclui as seguintes etapas de alto nível:

1.  Interrompa todas as instâncias do site de administração e monitoramento.

2.  Execute a instalação do MBAM no servidor B.

3.  Fazer backup do banco de dados no servidor A.

4.  Mover o banco de dados do servidor a para o B.

5.  Restaure o banco de dados no servidor B.

6.  Configure o acesso ao banco de dados no servidor B.

7.  Atualize os dados de conexão do banco de dados nos servidores de administração e monitoramento do MBAM.

8.  Atualize a cadeia de conexão da fonte de dados relatórios do SSRS com o novo local do banco de dados de auditoria e conformidade.

9.  Retome todas as instâncias do site Administração e monitoramento.

**Interromper todas as instâncias do site de administração e monitoramento**

1.  Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **Observação**  
    Para executar essa linha de comando, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell. Além disso, você deve atualizar a política de execução do PowerShell para permitir que os scripts sejam executados.



**Executar a instalação do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione apenas o **banco de dados de auditoria e conformidade** para a instalação.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **Observação**  
    Observação: substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de auditoria e conformidade será movido.

    -   $DOMAIN $ \ \ $SERVERNAME $-Insira os nomes de domínio e servidor de cada servidor de administração e monitoração de MBAM que entrarão em contato com o banco de dados de auditoria e conformidade. Use um ponto-e-vírgula para separar cada par de domínio e servidor na lista (por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $). Cada nome de servidor deve ser seguido por um símbolo "$", conforme mostrado no exemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de auditoria e conformidade.

    -   $X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.



**Fazer backup do banco de dados de conformidade e auditoria no servidor A**

1.  Para fazer backup do banco de dados de auditoria e conformidade no servidor A, use o SQL Server Management Studio e a tarefa chamada **fazer backup**. Por padrão, o nome do banco de dados é **MBAM banco de dados de status de conformidade**.

2.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

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

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Execute o arquivo SQL usando uma linha de comando do Windows PowerShell semelhante à seguinte:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que será feito o backup do banco de dados de conformidade e auditoria.



**Mover o banco de dados de auditoria e conformidade do servidor a para o B**

1.  Mova os arquivos a seguir do servidor A para o servidor B usando o Windows Explorer.

    -   Dados de banco de dados de status de conformidade do MBAM. bak

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $-Insira o nome do servidor no qual os arquivos serão copiados.

    -   $DESTINATIONSHARE $-digite o nome do compartilhamento e do caminho para o qual os arquivos serão copiados.



**Restaurar o banco de dados de auditoria e conformidade no servidor B**

1.  Restaure o banco de dados de auditoria e conformidade no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados**.

2.  Após a conclusão da tarefa, selecione o arquivo de backup do banco de dados selecionando a opção **do dispositivo** e, em seguida, use o comando **Adicionar** para selecionar o arquivo data. bak do status de conformidade do MBAM. Selecione **OK** para concluir o processo de restauração.

3.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Execute o arquivo SQL usando uma linha de comando do Windows PowerShell semelhante à seguinte:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de auditoria e conformidade será restaurado.



**Configurar o acesso ao banco de dados de auditoria e conformidade no servidor B**

1.  No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que está executando o recurso de administração e monitoramento do MBAM para o grupo local chamado acesso de banco de dados de **status de conformidade do MBAM**.

2.  Verifique se o acesso ao banco de dados de **auditoria do MBAM** de login do SQL no banco de dados restaurado está mapeado para o nome de logon **$MachineName $ \ \ MBAM acesso ao banco**de dados de auditoria Se não estiver mapeado como descrito, crie outro logon com associações de grupo semelhantes e mapeie-o para o nome de logon **$MachineName $ \ \ MBAM conformidade de banco**de dados de auditoria.

3.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando no servidor B semelhante à seguinte:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Observação**  
    Substitua os seguintes valores no exemplo acima pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM. O nome do servidor deve ser seguido por "$", conforme mostrado no exemplo. (por exemplo, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM**

1.  Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que são hospedados no site de administração e monitoramento:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.

3.  Selecione a opção **configurationStrings** no controle da **lista de seções** .

4.  Selecione a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.

5.  No **Editor de coleção**, selecione a linha chamada **ComplianceStatusConnectionString** ao atualizar a configuração do aplicativo MBAMAdministrationService ou a linha chamada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** ao atualizar a configuração do MBAMComplianceStatusService.

6.  Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome do servidor e da instância (por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME) ao qual o banco de dados de recuperação foi movido.

7.  Para automatizar esse procedimento, você pode usar o Windows para inserir uma linha de comando em cada servidor de administração e monitoramento semelhante ao seguinte:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e a instância em que o banco de dados de recuperação está localizado.



**Retomar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Mover os relatórios de conformidade e auditoria


Se você quiser mover os relatórios de conformidade e conformidade do MBAM de um computador para outro (ou seja, mover os relatórios do servidor A para o servidor B), use o procedimento a seguir, que inclui as seguintes etapas de alto nível:

1.  Execute a instalação do MBAM no servidor B.

2.  Configure o acesso aos relatórios de conformidade e auditoria no servidor B.

3.  Interrompa todas as instâncias do site de administração e monitoramento do MBAM.

4.  Atualize os dados de conexão dos relatórios em servidores de administração e monitoramento do MBAM.

5.  Retome todas as instâncias do site de administração e monitoramento do MBAM.

**Executar a instalação do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione apenas o recurso de **relatórios de auditoria e conformidade** para a instalação.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de conformidade e auditoria está localizado.

    -   $DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de auditoria e conformidade.

    -   $PASSWORD $-Insira a senha da conta de usuário que será usada para se conectar ao banco de dados de auditoria e conformidade.

    -   $X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.



**Configurar o acesso aos relatórios de conformidade e auditoria no servidor B**

1.  No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de usuário que terão acesso aos relatórios de conformidade e auditoria. Adicione as contas de usuário ao grupo local chamado MBAM Report users.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando no servidor B semelhante à seguinte:

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Observação**  
    Substitua os seguintes valores no exemplo acima pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Parar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada servidor que está executando o recurso de servidor administração e monitoramento do MBAM, use o console do Gerenciador dos serviços de informações da Internet (IIS) para interromper o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Atualizar os dados de conexão do banco de dados nos servidores de administração e monitoramento do MBAM**

1. Em cada servidor que está executando o recurso de servidor administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar a URL de relatórios de auditoria e conformidade.

2. Selecione o site de **Administração e monitoramento do Microsoft BitLocker** e use o recurso do **Editor de configuração** que é local na seção **Gerenciamento** do modo de **exibição de recursos**.

3. Selecione a opção **appSettings** do controle da **lista de seções** .

4. Selecione a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.

5. No **Editor de coleção**, selecione a linha chamada **Microsoft. MBAM. Reports. URL**.

6. Atualize o valor de **Microsoft. MBAM. Reports. URL** para refletir o nome do servidor para o servidor B. Se o recurso relatórios de auditoria e conformidade foi instalado em uma instância nomeada do SQL Reporting Services, certifique-se de adicionar ou atualizar o nome da instância para a URL (por exemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....)

7. Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando em cada servidor de administração e monitoramento semelhante ao seguinte:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **Observação**  
   Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

   -   $SERVERNAME $-digite o nome do nome do servidor ao qual os relatórios de conformidade e auditoria foram instalados.

   -   $SRSINSTANCENAME $-Insira o nome da instância do SQL Reporting Services à qual os relatórios de conformidade e auditoria foram instalados.



**Retomar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada servidor que está executando o recurso de servidor administração e monitoramento do MBAM, use o console do Gerenciador dos serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Observação**  
    Para executar essa linha de comando, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell. Além disso, você deve atualizar a política de execução do PowerShell para permitir que os scripts sejam executados.



## Movendo o recurso administração e monitoramento


Se você quiser mover o recurso de relatórios de monitoramento e administração do MBAM de um computador para outro (ou seja, mova o recurso do servidor A para o servidor B), use o procedimento a seguir, que inclui as seguintes etapas de alto nível:

1.  Execute a instalação do MBAM no servidor B.

2.  Configure o acesso ao banco de dados no servidor B.

**Executar a instalação do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione apenas o recurso de **servidor de administração e monitoramento** para a instalação.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-para o parâmetro COMPLIDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de conformidade e auditoria está localizado. Para o parâmetro RECOVERYANDHWDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de recuperação está localizado.

    -   $DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de auditoria e conformidade.

    -   $ REPORTSSERVERURL $-Insira a URL para o local de origem do site do serviço de relatórios SQL. Se os relatórios foram instalados em uma instância padrão do SRS, o formato da URL terá o formato "http://$SERVERNAME $/ReportServer". Se os relatórios foram instalados em uma instância padrão do SRS, o formato da URL terá o formato "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".

    -   $X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.



**Configurar o acesso aos bancos de dados**

1.  No servidor ou nos servidores em que o banco de dados de recuperação e o banco de dados de auditoria e conformidade são implantados, use o snap-in de usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que está executando o recurso de servidor de administração de **MBAM e do** **MBAM Access** (servidor de banco de dados de conformidade e auditoria).

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando, que é semelhante ao seguinte, no servidor em que o banco de dados de auditoria e conformidade foi implantado.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  No servidor em que o banco de dados de recuperação foi implantado, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Observação**  
    Substitua o seguinte valor no exemplo acima pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração. O nome do servidor deve ser seguido por um símbolo "$", conforme mostrado no exemplo (por exemplo, MyDomain\\MyServerName1 $).

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Tópicos relacionados


[Manutenção do MBAM 2.0](maintaining-mbam-20-mbam-2.md)









