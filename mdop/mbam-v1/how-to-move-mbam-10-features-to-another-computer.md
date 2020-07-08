---
title: Como Mover os Recursos do MBAM 1.0 para Outro Computador
description: Como Mover os Recursos do MBAM 1.0 para Outro Computador
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796127"
---
# Como Mover os Recursos do MBAM 1.0 para Outro Computador


Este tópico descreve as etapas que você deve seguir para mover um ou mais recursos de administração e monitoramento do Microsoft BitLocker (MBAM) para um computador diferente. Ao mover mais de um recurso do MBAM para outro computador, você deve movê-los na seguinte ordem:

1.  Recuperação e banco de dados de hardware

2.  Banco de dados de auditoria e conformidade

3.  Relatórios de conformidade e auditoria

4.  Administração e monitoramento

## Para mover o banco de dados de recuperação e de hardware


Você pode usar o procedimento a seguir para mover o banco de dados de hardware e recuperação do MBAM de um computador para outro (você pode mover este recurso de servidor MBAM do servidor A para o servidor B):

****

1.  Interrompa todas as instâncias do site de administração e monitoramento do MBAM.

2.  Execute a configuração do MBAM no servidor B.

3.  Faça backup do banco de dados de recuperação do MBAM e do hardware no servidor A.

4.  Recuperação de MBAM e banco de dados de hardware do servidor A para B

5.  Restaurar o banco de dados de recuperação e hardware do MBAM no servidor B

6.  Configurar o acesso ao banco de dados de recuperação e hardware do MBAM no servidor B

7.  Atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM

8.  Retomar todas as instâncias do Web site de administração e monitoramento do MBAM

**Para interromper todas as instâncias do site de administração e monitoramento do MBAM**

1.  Use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM. O site MBAM é denominado **Administração e monitoramento do Microsoft BitLocker**.

2.  Para automatizar esse procedimento, você pode usar um comando no prompt de comando semelhante ao seguinte usando o Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Observação**  
    Para executar este prompt de comando do PowerShell, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell. Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.



**Para executar a configuração do MBAM no servidor B**

1.  Execute a configuração do MBAM no servidor B e selecione o banco de dados de recuperação e de hardware para instalação.

2.  Para automatizar esse procedimento, você pode usar um comando no prompt de comando semelhante ao seguinte usando o Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e da instância para a qual o banco de dados de recuperação e de hardware será movido.

    -   $DOMAIN $ \ \ $SERVERNAME $-Insira os nomes do servidor e do domínio de cada aplicativo MBAM e o servidor de monitoramento que entrarão em contato com o banco de dados de recuperação e de hardware. Se houver vários nomes de domínio e servidor, use um ponto-e-vírgula para separar cada um deles na lista. Por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $. Além disso, cada nome de servidor deve ser seguido de um **$** . Por exemplo, MyDomain\\MyServerName1 $ MyDomain\\MyServerName2 $.



**Para fazer backup do banco de dados no servidor A**

1.  Para fazer backup do banco de dados de recuperação e do hardware no servidor A, use o SQL Server Management Studio e a tarefa chamada **fazer backup..**.. Por padrão, o nome do banco de dados é **MBAM recuperação e banco de dados de hardware**.

2.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:

    Modifique a recuperação do MBAM e o banco de dados de hardware para usar o modo de recuperação completo.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    Crie MBAM recuperação e dados de banco de dados de hardware e recuperação de MBAM dispositivos de backup lógicos de recuperação.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    Faça o backup do banco de dados de recuperação e do hardware completo do MBAM.

    ```sql
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
    Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $PASSWORD $-Insira uma senha que será usada para criptografar o arquivo de chave privada.



3.  Execute o arquivo SQL usando o SQL Server PowerShell e um comando semelhante ao seguinte:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o valor do exemplo anterior pelos que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e a instância do qual você deseja fazer backup do banco de dados de recuperação e do hardware.



**Para mover o banco de dados e o certificado do servidor a para o B**

1.  Mova a recuperação do MBAM e dados de banco de dados de hardware. bak do servidor A para o servidor B usando o Windows Explorer.

2.  Para mover o certificado para o banco de dados criptografado, será necessário usar as etapas de automação a seguir. Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Observação**  
    Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $-Insira o nome do servidor para o qual os arquivos serão copiados.

    -   $DESTINATIONSHARE $-Insira o nome do compartilhamento e o caminho para os quais os arquivos serão copiados.



**Para restaurar o banco de dados no servidor B**

1.  Restaure o banco de dados de recuperação e de hardware no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados**.

2.  Depois que a tarefa for executada, escolha o arquivo de backup do banco de dados selecionando a opção **do dispositivo** e, em seguida, use o comando **Adicionar** para escolher o arquivo de recuperação do MBAM e dados de banco de dados de hardware **. bak** .

3.  Selecione **OK** para concluir o processo de restauração.

4.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    Solte o certificado criado pela configuração do MBAM.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    Adicionar certificado

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    Restaure os dados de banco de dados de hardware e recuperação do MBAM e os arquivos de log.

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **Observação**  
    Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $PASSWORD $-Insira a senha usada para criptografar o arquivo de chave privada.



5.  Use o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o valor do exemplo de oblíquo pelos que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância para a qual o banco de dados de recuperação e de hardware será restaurado.



**Configurar o acesso ao banco de dados no servidor B**

1.  No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que executa o recurso de administração e monitoramento do MBAM para o grupo local chamado **MBAM recuperação e acesso ao banco de**dados de hardware.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell no servidor B para inserir um comando semelhante ao seguinte:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Observação**  
    Substitua os valores do exemplo anterior pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e o nome da máquina do servidor de administração e monitoração do MBAM. O nome do servidor deve ser seguido por a **$** , por exemplo, MyDomain\\MyServerName1 $.



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Para atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM**

1. Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que estão hospedados no site de administração e monitoramento do Microsoft BitLocker:

   -   Serviço de administração do MBAM

   -   Recuperação de MBAM e serviço de hardware

2. Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.

3. Selecione a opção **configurationStrings** no controle da lista de seções.

4. Escolha a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.

5. No **Editor de coleção**, escolha a linha chamada **KeyRecoveryConnectionString** quando atualizou a configuração para o aplicativo ' MBAMAdministrationService ' ou escolha a linha chamada <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> ConnectionString, ao atualizar a configuração para o "MBAMRecoveryAndHardwareService".

6. Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome do servidor e a instância para a qual o banco de dados de recuperação e de hardware foi movido. Por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $.

7. Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell em cada servidor de administração e monitoramento:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Observação**  
   Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de recuperação e de hardware está.



**Para retomar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM, que é chamado de **Administração e administração do Microsoft BitLocker**.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Para mover o recurso de banco de dados de status de conformidade


Se você optar por mover o recurso de banco de dados de status de conformidade do MBAM de um computador para outro, como do servidor a para o servidor B, você deve usar o seguinte procedimento:

1.  Parar todas as instâncias do site de administração e monitoramento do MBAM

2.  Executar a instalação do MBAM no servidor B

3.  Fazer backup do banco de dados no servidor A

4.  Mover o banco de dados do servidor A para o B

5.  Restaurar o banco de dados no servidor B

6.  Configurar o acesso ao banco de dados no servidor B

7.  Atualizar dados de conexão de banco de dados em servidores de administração e monitoramento do MBAM

8.  Retomar todas as instâncias do site de administração e monitoramento do MBAM

**Para interromper todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM, que é chamado **Administração e monitoramento do Microsoft BitLocker**.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Observação**  
    Para executar esse comando, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell. Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.



**Para executar a configuração do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione o recurso de banco de dados status de conformidade para a instalação.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **Observação**  
    Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de status de conformidade será movido.

    -   $DOMAIN $ \ \ $SERVERNAME $-Insira os nomes de domínio e os nomes de servidor de cada aplicativo MBAM e monitorando o servidor de monitoramento que entrarão em contato com o banco de dados de status de conformidade. Se houver vários nomes de domínio e nomes de servidor, use um ponto-e-vírgula para separar cada um deles na lista. Por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $. Cada nome de servidor deve ser seguido por um **$** conforme mostrado no exemplo. Por exemplo, MyDomain\\MyServerName1 $ MyDomain\\MyServerName2 $.

    -   $DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de status de conformidade.



**Para fazer backup do banco de dados de conformidade no servidor A**

1.  Para fazer backup do banco de dados de conformidade no servidor A, use o SQL Server Management Studio e a tarefa chamada **fazer backup..**.. Por padrão, o nome do banco de dados é **MBAM banco de dados de status de conformidade**.

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Execute o arquivo SQL com um comando semelhante ao seguinte, usando o PowerShell do SQL Server:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância de onde será feito o backup do banco de dados de status de conformidade.



**Para mover o banco de dados do servidor A para o B**

1.  Mova os seguintes arquivos do servidor A para o servidor B, usando o Windows Explorer:

    -   Dados de banco de dados de status de conformidade do MBAM. bak

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte usando o Windows PowerShell:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Observação**  
    Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $-Insira o nome do servidor no qual os arquivos serão copiados.

    -   $DESTINATIONSHARE $-digite o nome do compartilhamento e do caminho para o qual os arquivos serão copiados.



**Para restaurar o banco de dados no servidor B**

1.  Restaure o banco de dados de status de conformidade no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados..**..

2.  Depois que a tarefa for executada, selecione o arquivo de backup do banco de dados, selecionando a opção do dispositivo e, em seguida, use o comando adicionar para escolher o arquivo data. bak do status de conformidade do MBAM. Clique em OK para concluir o processo de restauração.

3.  Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Execute o arquivo SQL com um comando semelhante ao seguinte, usando o PowerShell do SQL Server:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Observação**  
    Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de status de conformidade será restaurado.



**Para configurar o acesso ao banco de dados no servidor B**

1.  No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas do computador de cada servidor que executa o recurso de administração e monitoramento do MBAM para o grupo local chamado acesso ao banco de dados do **status de conformidade do MBAM**.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell no servidor B:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Observação**  
    Substitua o valor do exemplo anterior pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM. O nome do servidor deve ser seguido de a **$** . Por exemplo, MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**Para atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que estão hospedados no site de administração e monitoramento do Microsoft BitLocker:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.

3.  Selecione a opção **configurationStrings** no controle da lista de seções.

4.  Selecione a linha nomeada **(coleção)** e abra o editor de coleção selecionando o botão no lado direito da linha.

5.  No **Editor de coleção**, selecione a linha chamada **ComplianceStatusConnectionString**, ao atualizar a configuração do aplicativo MBAMAdministrationService ou a linha chamada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, quando você atualizar a configuração do MBAMComplianceStatusService.

6.  Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome do servidor e o nome da instância. Por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME, para o qual o banco de dados de recuperação e de hardware foi movido.

7.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte em cada servidor de administração e monitoramento:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Observação**  
    Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e o nome da instância em que o banco de dados de recuperação e de hardware está localizado.



**Para retomar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:

    **PS C:\\ &gt; Start-website "administração e monitoramento do Microsoft BitLocker"**

## Para mover os relatórios de conformidade e auditoria


Se você optar por mover os relatórios de conformidade e conformidade do MBAM de um computador para outro (especificamente, se você mover o recurso do servidor a para o servidor B), deverá usar o procedimento e as etapas a seguir:

1.  Executar a instalação do MBAM no servidor B

2.  Configurar o acesso aos relatórios de conformidade e auditoria no servidor B

3.  Parar todas as instâncias do site de administração e monitoramento do MBAM

4.  Atualizar os dados de conexão dos relatórios nos servidores de administração e monitoramento do MBAM

5.  Retomar todas as instâncias do site de administração e monitoramento do MBAM

**Para executar a configuração do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione apenas o recurso de conformidade e auditoria para a instalação.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **Observação**  
    Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de status de conformidade está localizado.

    -   $DOMAIN $ \ \ $USERNAME $-Insira o nome de domínio e o nome de usuário que serão usados pelo recurso de relatórios de auditoria e conformidade para se conectar ao banco de dados de status de conformidade.

    -   $PASSWORD $-Insira a senha da conta de usuário que será usada para se conectar ao banco de dados de status de conformidade.



**Para configurar o acesso aos relatórios de conformidade e auditoria no servidor B**

1.  No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de usuário que terão acesso aos relatórios de conformidade e auditoria. Adicione as contas de usuário ao grupo local chamado "MBAM Report Users".

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell no servidor B.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Observação**  
    Substitua o seguinte valor do exemplo anterior pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Para interromper todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM chamado **Administração e monitoramento do Microsoft BitLocker**.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Para atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM**

1. Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar a URL dos relatórios de conformidade.

2. Selecione o site de **Administração e administração do Microsoft BitLocker** e use o recurso **Editor de configuração** que pode ser encontrado na seção **Gerenciamento** do modo de **exibição de recursos**.

3. Selecione a opção **appSettings** do controle da lista de seções.

4. Aqui, selecione a linha nomeada **(coleção)** e abra o editor de **coleção** selecionando o botão no lado direito da linha.

5. No **Editor de coleção**, selecione a linha chamada "Microsoft. MBAM. Reports. URL".

6. Atualize o valor de Microsoft. MBAM. Reports. URL para refletir o nome do servidor para o servidor B. Se o recurso de relatórios de conformidade e auditoria tiver sido instalado em uma instância nomeada do SQL Reporting Services, certifique-se de adicionar ou atualizar o nome da instância para a URL. Por exemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....

7. Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte em cada servidor de administração e monitoramento:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **Observação**  
   Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:

   -   $SERVERNAME $-Insira o nome do servidor no qual os relatórios de conformidade e auditoria foram instalados.

   -   $SRSINSTANCENAME $-Insira o nome da instância do SQL Reporting Services à qual os relatórios de conformidade e auditoria foram instalados.



**Para retomar todas as instâncias do site de administração e monitoramento do MBAM**

1.  Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Observação**  
    Para executar esse comando, o módulo do IIS do PowerShell deve ser adicionado à instância atual do PowerShell. Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.



## Para mover o recurso de administração e monitoramento


Se você optar por mover o recurso de administração e monitoramento de MBAM de um computador para outro (se você mover o recurso do servidor A para o servidor B), deverá usar o procedimento a seguir. O processo inclui as seguintes etapas:

1.  Executar a instalação do MBAM no servidor B

2.  Configurar o acesso ao banco de dados no servidor B

**Para executar a configuração do MBAM no servidor B**

1.  Execute a instalação do MBAM no servidor B e selecione apenas o recurso de administração para instalação.

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **Observação**  
    Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-para o parâmetro COMPLIDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de status de conformidade está localizado. Para o parâmetro RECOVERYANDHWDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de recuperação e de hardware está localizado.

    -   $DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de status de conformidade.

    -   $ REPORTSSERVERURL $-Insira a URL para o local de origem do site do serviço de relatórios SQL. Se os relatórios foram instalados em uma instância padrão do SRS, o formato de URL formatará "http://$SERVERNAME $/ReportServer". Se os relatórios foram instalados em uma instância padrão do SRS, o formato da URL será formatado para "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".



**Para configurar o acesso aos bancos de dados**

1.  Em servidores ou servidores em que a recuperação e o hardware, e os bancos de dados de conformidade e auditoria são implantados, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas do computador de cada servidor que executa o recurso de administração e monitoramento do MBAM para os grupos locais denominados "recuperação do MBAM e o acesso ao banco de dados de hardware" (servidor de banco de dados de conformidade e auditoria).

2.  Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell no servidor em que os bancos de dados de auditoria e conformidade foram implantados.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  No servidor em que os bancos de dados de recuperação e de hardware foram implantados, execute um comando semelhante ao seguinte, usando o Windows PowerShell.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Observação**  
    Substitua o valor do exemplo anterior pelos valores aplicáveis para o seu ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM. O nome do servidor deve ser seguido de a **$** . Por exemplo, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Tópicos relacionados


[Administrando os Recursos do MBAM 1.0](administering-mbam-10-features.md)









