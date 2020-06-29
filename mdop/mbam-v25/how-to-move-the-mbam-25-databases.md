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
# <span data-ttu-id="1b83c-103">Como mover os bancos de dados do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1b83c-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="1b83c-104">Use estes procedimentos para mover os seguintes bancos de dados de um computador para outro; do servidor A para o servidor B, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1b83c-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="1b83c-105">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="1b83c-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="1b83c-106">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="1b83c-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="1b83c-107">É importante que os bancos de dados sejam restaurados para o computador B antes de executar o assistente de configuração do MBAM para atualizá-los/configurá-los.</span><span class="sxs-lookup"><span data-stu-id="1b83c-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="1b83c-108">Se os bancos de dados não estiverem presentes, o assistente de configuração criará bancos de dados novos e vazios.</span><span class="sxs-lookup"><span data-stu-id="1b83c-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="1b83c-109">Quando os bancos de dados existentes forem restaurados, esse processo irá interromper a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b83c-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="1b83c-110">Restaure os bancos de dados primeiro e, em seguida, execute o assistente de configuração do MBAM, escolha a opção banco de dados, e o assistente de configuração será "conectado" aos bancos de dados restaurados; atualizá-los, se necessário, como parte do processo.</span><span class="sxs-lookup"><span data-stu-id="1b83c-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="1b83c-111">Se estiver movendo vários recursos, mova-os na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="1b83c-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="1b83c-112">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="1b83c-112">Recovery Database</span></span>

2.  <span data-ttu-id="1b83c-113">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="1b83c-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="1b83c-114">Relatórios</span><span class="sxs-lookup"><span data-stu-id="1b83c-114">Reports</span></span>

4.  <span data-ttu-id="1b83c-115">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1b83c-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="1b83c-116">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="1b83c-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="1b83c-117">Para executar os exemplos de scripts do Windows PowerShell fornecidos neste tópico, você deve atualizar a política de execução do Windows PowerShell para permitir que os scripts sejam executados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="1b83c-118">Consulte [executando scripts do Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="1b83c-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="1b83c-119">Mover o banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="1b83c-119">Move the Recovery Database</span></span>

<span data-ttu-id="1b83c-120">As etapas de alto nível para mover o banco de dados de recuperação são:</span><span class="sxs-lookup"><span data-stu-id="1b83c-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="1b83c-121">Parar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="1b83c-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="1b83c-122">Fazer backup do banco de dados de recuperação no servidor A</span><span class="sxs-lookup"><span data-stu-id="1b83c-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="1b83c-123">Mover o banco de dados de recuperação do servidor a para o servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="1b83c-124">Restaurar o banco de dados de recuperação no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="1b83c-125">Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão</span><span class="sxs-lookup"><span data-stu-id="1b83c-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="1b83c-126">Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="1b83c-127">Retomar a instância do site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1b83c-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="1b83c-128">Como mover o banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="1b83c-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="1b83c-129">Interrompa todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b83c-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="1b83c-130">Em cada servidor que está executando o site do servidor de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1b83c-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="1b83c-131">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="1b83c-132">Para executar esse comando, você deve adicionar o módulo serviços de informações da Internet (IIS) para Windows PowerShell à instância atual do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1b83c-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="1b83c-133">Fazer backup do banco de dados de recuperação no servidor A</span><span class="sxs-lookup"><span data-stu-id="1b83c-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="1b83c-134">Use a tarefa de **backup** no SQL Server Management Studio para fazer backup do banco de dados de recuperação no servidor A.  Por padrão, o nome do banco de dados é **MBAM banco de dados de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="1b83c-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="1b83c-135">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL e altere o banco de dados de recuperação do MBAM para usar o modo de recuperação completa:</span><span class="sxs-lookup"><span data-stu-id="1b83c-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

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

3.  <span data-ttu-id="1b83c-136">Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="1b83c-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="1b83c-137">**$Password $** -senha usada para criptografar o arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="1b83c-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="1b83c-138">No Windows PowerShell, execute o script armazenado no arquivo e semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="1b83c-139">Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="1b83c-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="1b83c-140">**$ServerName $ \ $SQLINSTANCENAME $** -nome e instância do servidor do qual será feito o backup do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1b83c-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="1b83c-141">Mover o banco de dados de recuperação do servidor a para o servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="1b83c-142">Use o Windows Explorer para mover o arquivo **dados. bak do banco de dados de recuperação do MBAM** do servidor a para o servidor B.</span><span class="sxs-lookup"><span data-stu-id="1b83c-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="1b83c-143">Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="1b83c-144">Use as informações da tabela a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="1b83c-145">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b83c-145">Parameter</span></span>**        | **<span data-ttu-id="1b83c-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b83c-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="1b83c-147">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="1b83c-147">$SERVERNAME$</span></span>       | <span data-ttu-id="1b83c-148">Nome do servidor para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="1b83c-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="1b83c-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="1b83c-150">Nome do compartilhamento e do caminho para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="1b83c-151">Restaurar o banco de dados de recuperação no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="1b83c-152">Restaure o banco de dados de recuperação no servidor B usando a tarefa **restaurar banco de dados** no SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="1b83c-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="1b83c-153">Quando a tarefa anterior terminar, selecione **do dispositivo**e, em seguida, selecione o arquivo de backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="1b83c-154">Use o comando **Adicionar** para selecionar o arquivo **dados. bak do banco de dados de recuperação do MBAM** e clique em **OK** para concluir o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="1b83c-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="1b83c-155">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:</span><span class="sxs-lookup"><span data-stu-id="1b83c-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

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

5.  <span data-ttu-id="1b83c-156">Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="1b83c-157">**$Password $** -senha usada para criptografar o arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="1b83c-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="1b83c-158">No Windows PowerShell, execute o script armazenado no arquivo e semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="1b83c-159">Use o valor a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="1b83c-160">**$ServerName $ \ $SQLINSTANCENAME $** -nome do servidor e instância para os quais o banco de dados de recuperação será restaurado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="1b83c-161">Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão</span><span class="sxs-lookup"><span data-stu-id="1b83c-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="1b83c-162">Verifique se o logon de usuário do Microsoft SQL Server que permite o acesso ao banco de dados de recuperação no banco de dados restaurado está mapeado para a conta do Access que você forneceu durante o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="1b83c-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="1b83c-163">Se o logon não for o mesmo, crie um logon usando o SQL Server Management Studio e mapeie-o para o usuário de banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="1b83c-164">No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os sites do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b83c-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="1b83c-165">Edite a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="1b83c-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="1b83c-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="1b83c-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="1b83c-167">Atualize o valor da **fonte de dados** com o nome do servidor e da instância (por exemplo, \ $ServerName \ $ \ \ \ \ $SQLINSTANCENAME) à qual o banco de dados de recuperação foi movido.</span><span class="sxs-lookup"><span data-stu-id="1b83c-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="1b83c-168">Atualize o valor **inicial do catálogo** com o nome do banco de dados recuperado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="1b83c-169">Para automatizar esse processo, você pode usar o prompt de comando do Windows PowerShell para inserir uma linha de comando no servidor de administração e monitoramento semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

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
   ><span data-ttu-id="1b83c-170">Esta cadeia de conexão é compartilhada por todos os aplicativos Web MBAM locais.</span><span class="sxs-lookup"><span data-stu-id="1b83c-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="1b83c-171">Portanto, ele precisa ser atualizado apenas uma vez por servidor.</span><span class="sxs-lookup"><span data-stu-id="1b83c-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="1b83c-172">Use a tabela a seguir para substituir os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="1b83c-173">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b83c-173">Parameter</span></span>|<span data-ttu-id="1b83c-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b83c-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="1b83c-175">$SERVERNAME $/\ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="1b83c-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="1b83c-176">Nome do servidor e instância do SQL Server em que o banco de dados de recuperação está localizado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="1b83c-177">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="1b83c-177">$DATABASE$</span></span>|<span data-ttu-id="1b83c-178">Nome do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1b83c-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="1b83c-179">Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="1b83c-180">Instale o software de servidor MBAM 2,5 no servidor B. Para obter detalhes, consulte [instalando o software de servidor MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="1b83c-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="1b83c-181">No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso de **banco de dados de recuperação** .</span><span class="sxs-lookup"><span data-stu-id="1b83c-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="1b83c-182">Para obter detalhes sobre como configurar os bancos de dados, consulte [como configurar os bancos de dados do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="1b83c-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="1b83c-183">Você também pode usar o cmdlet **Enable-MbamDatabase** do Windows PowerShell para configurar o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1b83c-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="1b83c-184">Retomar a instância do site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1b83c-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="1b83c-185">No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1b83c-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="1b83c-186">Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="1b83c-187">Para executar esse comando, você deve adicionar o módulo do IIS para Windows PowerShell à instância atual do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1b83c-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="1b83c-188">Mover o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="1b83c-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="1b83c-189">As etapas de alto nível para mover o banco de dados de auditoria e conformidade são:</span><span class="sxs-lookup"><span data-stu-id="1b83c-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="1b83c-190">Parar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="1b83c-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="1b83c-191">Fazer backup do banco de dados de conformidade e auditoria no servidor A</span><span class="sxs-lookup"><span data-stu-id="1b83c-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="1b83c-192">Mover o banco de dados de auditoria e conformidade do servidor A para o servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="1b83c-193">Restaurar o banco de dados de auditoria e conformidade no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="1b83c-194">Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão</span><span class="sxs-lookup"><span data-stu-id="1b83c-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="1b83c-195">Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="1b83c-196">Retomar a instância do site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1b83c-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="1b83c-197">Como migrar o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="1b83c-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="1b83c-198">Interrompa todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b83c-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="1b83c-199">Em cada servidor que está executando o site do servidor de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1b83c-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="1b83c-200">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="1b83c-201">Para executar esse comando, você deve adicionar o módulo serviços de informações da Internet (IIS) para Windows PowerShell à instância atual do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1b83c-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="1b83c-202">Fazer backup do banco de dados de conformidade e auditoria no servidor A</span><span class="sxs-lookup"><span data-stu-id="1b83c-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="1b83c-203">Use a tarefa de **backup** no SQL Server Management Studio para fazer backup do banco de dados de auditoria e conformidade no servidor A. Por padrão, o nome do banco de dados é **MBAM banco de dados de status de conformidade**.</span><span class="sxs-lookup"><span data-stu-id="1b83c-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="1b83c-204">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:</span><span class="sxs-lookup"><span data-stu-id="1b83c-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

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

3.  <span data-ttu-id="1b83c-205">Execute o script que está armazenado no arquivo. SQL usando um comando do Windows PowerShell semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="1b83c-206">Usando o valor a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="1b83c-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="1b83c-207">**$ServerName $ \ $SQLINSTANCENAME $** -nome e instância do servidor do qual será feito o backup do banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="1b83c-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="1b83c-208">Mover o banco de dados de auditoria e conformidade do servidor A para o servidor B \* \*</span><span class="sxs-lookup"><span data-stu-id="1b83c-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="1b83c-209">Use o Windows Explorer para mover o arquivo **dados. bak do banco de dados de status de conformidade do MBAM** do servidor a para o servidor B.</span><span class="sxs-lookup"><span data-stu-id="1b83c-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="1b83c-210">Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="1b83c-211">Usando a tabela a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="1b83c-212">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b83c-212">Parameter</span></span>**        | **<span data-ttu-id="1b83c-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b83c-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="1b83c-214">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="1b83c-214">$SERVERNAME$</span></span>       | <span data-ttu-id="1b83c-215">Nome do servidor para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="1b83c-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="1b83c-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="1b83c-217">Nome do compartilhamento e do caminho para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="1b83c-218">Restaurar o banco de dados de auditoria e conformidade no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="1b83c-219">Restaure o banco de dados de auditoria e conformidade no servidor B usando a tarefa **restaurar banco de dados** no SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="1b83c-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="1b83c-220">Quando a tarefa anterior terminar, selecione **do dispositivo**e, em seguida, selecione o arquivo de backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1b83c-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="1b83c-221">Use o comando **Adicionar** para selecionar o arquivo **dados. bak do status de conformidade do MBAM** e clique em **OK** para concluir o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="1b83c-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="1b83c-222">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:</span><span class="sxs-lookup"><span data-stu-id="1b83c-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="1b83c-223">No Windows PowerShell, execute o script armazenado no arquivo e semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="1b83c-224">Usando o valor a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="1b83c-225">**$ServerName $ \ $SQLINSTANCENAME $** -nome e instância do servidor ao qual o banco de dados de auditoria e conformidade será restaurado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="1b83c-226">Configurar o acesso ao banco de dados no servidor B e atualizar dados de conexão</span><span class="sxs-lookup"><span data-stu-id="1b83c-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="1b83c-227">Verifique se o logon de usuário do Microsoft SQL Server que permite a conformidade e o acesso ao banco de dados de auditoria no banco de dados restaurado está mapeado para a conta de acesso que você forneceu durante o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="1b83c-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="1b83c-228">Se o logon não for o mesmo, crie um logon usando o SQL Server Management Studio e mapeie-o para o usuário de banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="1b83c-229">No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão do site.</span><span class="sxs-lookup"><span data-stu-id="1b83c-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="1b83c-230">Edite a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="1b83c-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="1b83c-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="1b83c-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="1b83c-232">Atualize o valor da **fonte de dados** com o nome do servidor e da instância (por exemplo, \ $ServerName \ $ \ \ \ \ $SQLINSTANCENAME) à qual o banco de dados de recuperação foi movido.</span><span class="sxs-lookup"><span data-stu-id="1b83c-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="1b83c-233">Atualize o valor **inicial do catálogo** com o nome do banco de dados recuperado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="1b83c-234">Para automatizar esse processo, você pode usar o prompt de comando do Windows PowerShell para inserir uma linha de comando no servidor de administração e monitoramento semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="1b83c-235">Esta cadeia de conexão é compartilhada por todos os aplicativos Web MBAM locais.</span><span class="sxs-lookup"><span data-stu-id="1b83c-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="1b83c-236">Portanto, ele precisa ser atualizado apenas uma vez por servidor.</span><span class="sxs-lookup"><span data-stu-id="1b83c-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="1b83c-237">Usando a tabela a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1b83c-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="1b83c-238">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b83c-238">Parameter</span></span> | <span data-ttu-id="1b83c-239">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b83c-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="1b83c-240">$SERVERNAME $ \ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="1b83c-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="1b83c-241">Nome do servidor e instância do SQL Server em que o banco de dados de recuperação está localizado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="1b83c-242">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="1b83c-242">$DATABASE$</span></span>|<span data-ttu-id="1b83c-243">Nome do banco de dados recuperado.</span><span class="sxs-lookup"><span data-stu-id="1b83c-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="1b83c-244">Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="1b83c-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="1b83c-245">Instale o software de servidor MBAM 2,5 no servidor B. Para obter detalhes, consulte [instalando o software de servidor MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="1b83c-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="1b83c-246">No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso **conformidade e banco de dados de auditoria** .</span><span class="sxs-lookup"><span data-stu-id="1b83c-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="1b83c-247">Para obter detalhes sobre como configurar os bancos de dados, consulte [como configurar os bancos de dados do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="1b83c-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="1b83c-248">Você também pode usar o cmdlet **Enable-MbamDatabase** do Windows PowerShell para configurar o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="1b83c-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="1b83c-249">Retomar a instância do site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1b83c-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="1b83c-250">No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1b83c-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="1b83c-251">Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b83c-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="1b83c-252">Para executar esse comando, você deve adicionar o módulo do IIS para Windows PowerShell à instância atual do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1b83c-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
