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
# <span data-ttu-id="189eb-103">Como mover os recursos do MBAM 2.0 para outro computador</span><span class="sxs-lookup"><span data-stu-id="189eb-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="189eb-104">Este tópico descreve as etapas que você deve seguir para mover um ou mais recursos de administração e monitoramento do Microsoft BitLocker (MBAM) para um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="189eb-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="189eb-105">Ao mover mais de um recurso de administração e monitoramento do Microsoft BitLocker, você deve movê-los na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="189eb-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="189eb-106">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="189eb-106">Recovery Database</span></span>

2.  <span data-ttu-id="189eb-107">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="189eb-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="189eb-108">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="189eb-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="189eb-109">Administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="189eb-109">Administration and Monitoring</span></span>

## <span data-ttu-id="189eb-110">Movendo o banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="189eb-110">Moving the Recovery Database</span></span>


<span data-ttu-id="189eb-111">Para mover o banco de dados de recuperação de um computador para outro (por exemplo, do servidor A para o servidor B), use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="189eb-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="189eb-112">Interrompa todas as instâncias do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="189eb-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="189eb-113">Execute a instalação do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="189eb-114">Faça o backup do banco de dados de recuperação do MBAM no servidor A.</span><span class="sxs-lookup"><span data-stu-id="189eb-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="189eb-115">Mova o banco de dados de recuperação do MBAM do servidor A para o B.</span><span class="sxs-lookup"><span data-stu-id="189eb-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="189eb-116">Restaure o banco de dados de recuperação do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="189eb-117">Configure o acesso ao banco de dados de recuperação do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="189eb-118">Atualize os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="189eb-119">Retome todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="189eb-120">Parar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="189eb-121">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM, que é chamado **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="189eb-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="189eb-122">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="189eb-123">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-123">Note</span></span>**  
    <span data-ttu-id="189eb-124">Para executar essa linha de comando do PowerShell, o módulo do IIS para PowerShell deve ser adicionado à instância atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189eb-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="189eb-125">Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="189eb-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="189eb-126">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="189eb-127">Execute a instalação do MBAM no servidor B e selecione apenas o **banco de dados de recuperação** para instalação.</span><span class="sxs-lookup"><span data-stu-id="189eb-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="189eb-128">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="189eb-129">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-129">Note</span></span>**  
    <span data-ttu-id="189eb-130">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-131">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância para a qual o banco de dados de recuperação será movido.</span><span class="sxs-lookup"><span data-stu-id="189eb-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="189eb-132">$DOMAIN $ \ \ $SERVERNAME $-Insira os nomes de domínio e servidor de cada servidor de administração e monitoramento do MBAM que entrarão em contato com o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="189eb-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="189eb-133">Use um ponto-e-vírgula para separar cada par de domínio e servidor na lista (por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="189eb-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="189eb-134">Cada nome de servidor deve ser seguido por um símbolo "$", conforme mostrado no exemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="189eb-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="189eb-135">$X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="189eb-136">Fazer backup do banco de dados de recuperação no servidor A</span><span class="sxs-lookup"><span data-stu-id="189eb-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="189eb-137">Para fazer backup do banco de dados de recuperação no servidor A, use o SQL Server Management Studio e a tarefa chamada fazer backup.</span><span class="sxs-lookup"><span data-stu-id="189eb-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="189eb-138">Por padrão, o nome do banco de dados é **MBAM banco de dados de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="189eb-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="189eb-139">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:</span><span class="sxs-lookup"><span data-stu-id="189eb-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="189eb-140">Modifique o banco de dados de recuperação do MBAM para usar o modo de recuperação completo.</span><span class="sxs-lookup"><span data-stu-id="189eb-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

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

    **<span data-ttu-id="189eb-141">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-141">Note</span></span>**  
    <span data-ttu-id="189eb-142">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-143">$PASSWORD $-Insira uma senha que será usada para criptografar o arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="189eb-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="189eb-144">Execute o arquivo SQL usando o SQL Server PowerShell e uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="189eb-145">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-145">Note</span></span>**  
    <span data-ttu-id="189eb-146">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-147">$SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e da instância do qual será feito o backup do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="189eb-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="189eb-148">Mover o banco de dados de recuperação e o certificado do servidor a para o servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="189eb-149">Mova o arquivo a seguir do servidor A para o servidor B usando o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="189eb-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="189eb-150">Dados de banco de dados de recuperação MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="189eb-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="189eb-151">Para mover o certificado para o banco de dados criptografado, use as etapas de automação a seguir.</span><span class="sxs-lookup"><span data-stu-id="189eb-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="189eb-152">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="189eb-153">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-153">Note</span></span>**  
    <span data-ttu-id="189eb-154">Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-155">$SERVERNAME $-Insira o nome do servidor para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="189eb-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="189eb-156">$DESTINATIONSHARE $-Insira o nome do compartilhamento e o caminho para os quais os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="189eb-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="189eb-157">Restaurar o banco de dados de recuperação no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="189eb-158">Restaure o banco de dados de recuperação no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="189eb-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="189eb-159">Após a conclusão da tarefa, selecione o arquivo de backup do banco de dados selecionando a opção **do dispositivo** e, em seguida, use o comando **Adicionar** para selecionar o arquivo **Data. bak** do banco de dados de recuperação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="189eb-160">Selecione **OK** para concluir o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="189eb-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="189eb-161">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:</span><span class="sxs-lookup"><span data-stu-id="189eb-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    **<span data-ttu-id="189eb-162">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-162">Note</span></span>**  
    <span data-ttu-id="189eb-163">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-164">$PASSWORD $-Insira uma senha que você usou para criptografar o arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="189eb-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="189eb-165">Você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="189eb-166">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-166">Note</span></span>**  
    <span data-ttu-id="189eb-167">Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-168">$SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e da instância para a qual o banco de dados de recuperação será restaurado.</span><span class="sxs-lookup"><span data-stu-id="189eb-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="189eb-169">Configurar o acesso ao banco de dados de recuperação no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="189eb-170">No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que está executando o recurso de administração e monitoramento do MBAM para o grupo local chamado **MBAM recuperação e acesso ao banco de**dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="189eb-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="189eb-171">Verifique se o acesso ao SQL login **MBAM recuperação e o acesso de BD de hardware** no banco de dados restaurado está mapeado para o nome de logon **$MachineName $ \\MBAM recuperação e acesso ao banco de dados de hardware**.</span><span class="sxs-lookup"><span data-stu-id="189eb-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="189eb-172">Se não estiver mapeado como descrito, crie outro logon com associações de grupo semelhantes e mapeie-o para o nome de logon **$MachineName $ \\MBAM de recuperação e acesso ao banco de dados de hardware**.</span><span class="sxs-lookup"><span data-stu-id="189eb-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="189eb-173">Para automatizar esse procedimento, você pode usar o Windows PowerShell no servidor B para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="189eb-174">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-174">Note</span></span>**  
    <span data-ttu-id="189eb-175">Substitua os seguintes valores no exemplo acima pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="189eb-176">$DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="189eb-177">O nome do servidor deve ser seguido por $, conforme mostrado no exemplo (por exemplo, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="189eb-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="189eb-178">Atualizar os dados de conexão do banco de dados de recuperação nos servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="189eb-179">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que são hospedados no site de administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="189eb-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="189eb-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="189eb-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="189eb-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="189eb-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="189eb-182">Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.</span><span class="sxs-lookup"><span data-stu-id="189eb-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="189eb-183">Selecione a opção **configurationStrings** no controle da **lista de seções** .</span><span class="sxs-lookup"><span data-stu-id="189eb-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="189eb-184">Selecione a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.</span><span class="sxs-lookup"><span data-stu-id="189eb-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="189eb-185">No **Editor de coleção**, selecione a linha chamada **KeyRecoveryConnectionString** ao atualizar a configuração do aplicativo MBAMAdministrationService ou a linha denominada <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> ConnectionString ao atualizar a configuração do MBAMRecoveryAndHardwareService.</span><span class="sxs-lookup"><span data-stu-id="189eb-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="189eb-186">Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome e a instância do servidor (por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $) em que o banco de dados de recuperação foi movido.</span><span class="sxs-lookup"><span data-stu-id="189eb-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="189eb-187">Para automatizar esse procedimento, você pode usar o Windows para inserir uma linha de comando, que é semelhante ao seguinte, em cada servidor de administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="189eb-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="189eb-188">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-188">Note</span></span>**  
   <span data-ttu-id="189eb-189">Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="189eb-190">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de recuperação está.</span><span class="sxs-lookup"><span data-stu-id="189eb-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="189eb-191">Retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="189eb-192">Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM, que é chamado **de administração e administração do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="189eb-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="189eb-193">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="189eb-194">Movendo o recurso de banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="189eb-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="189eb-195">Se você quiser mover o banco de dados de auditoria e conformidade com o MBAM de um computador para outro (ou seja, mover o banco de dados do servidor A para o servidor B), use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="189eb-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="189eb-196">O processo inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="189eb-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="189eb-197">Interrompa todas as instâncias do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="189eb-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="189eb-198">Execute a instalação do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="189eb-199">Fazer backup do banco de dados no servidor A.</span><span class="sxs-lookup"><span data-stu-id="189eb-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="189eb-200">Mover o banco de dados do servidor a para o B.</span><span class="sxs-lookup"><span data-stu-id="189eb-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="189eb-201">Restaure o banco de dados no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="189eb-202">Configure o acesso ao banco de dados no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="189eb-203">Atualize os dados de conexão do banco de dados nos servidores de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="189eb-204">Atualize a cadeia de conexão da fonte de dados relatórios do SSRS com o novo local do banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="189eb-205">Retome todas as instâncias do site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="189eb-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="189eb-206">Interromper todas as instâncias do site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="189eb-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="189eb-207">Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="189eb-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="189eb-208">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="189eb-209">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-209">Note</span></span>**  
    <span data-ttu-id="189eb-210">Para executar essa linha de comando, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189eb-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="189eb-211">Além disso, você deve atualizar a política de execução do PowerShell para permitir que os scripts sejam executados.</span><span class="sxs-lookup"><span data-stu-id="189eb-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="189eb-212">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="189eb-213">Execute a instalação do MBAM no servidor B e selecione apenas o **banco de dados de auditoria e conformidade** para a instalação.</span><span class="sxs-lookup"><span data-stu-id="189eb-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="189eb-214">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="189eb-215">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-215">Note</span></span>**  
    <span data-ttu-id="189eb-216">Observação: substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-217">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de auditoria e conformidade será movido.</span><span class="sxs-lookup"><span data-stu-id="189eb-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="189eb-218">$DOMAIN $ \ \ $SERVERNAME $-Insira os nomes de domínio e servidor de cada servidor de administração e monitoração de MBAM que entrarão em contato com o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="189eb-219">Use um ponto-e-vírgula para separar cada par de domínio e servidor na lista (por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="189eb-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="189eb-220">Cada nome de servidor deve ser seguido por um símbolo "$", conforme mostrado no exemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="189eb-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="189eb-221">$DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="189eb-222">$X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="189eb-223">Fazer backup do banco de dados de conformidade e auditoria no servidor A</span><span class="sxs-lookup"><span data-stu-id="189eb-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="189eb-224">Para fazer backup do banco de dados de auditoria e conformidade no servidor A, use o SQL Server Management Studio e a tarefa chamada **fazer backup**.</span><span class="sxs-lookup"><span data-stu-id="189eb-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="189eb-225">Por padrão, o nome do banco de dados é **MBAM banco de dados de status de conformidade**.</span><span class="sxs-lookup"><span data-stu-id="189eb-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="189eb-226">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:</span><span class="sxs-lookup"><span data-stu-id="189eb-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="189eb-227">Execute o arquivo SQL usando uma linha de comando do Windows PowerShell semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="189eb-228">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-228">Note</span></span>**  
    <span data-ttu-id="189eb-229">Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-230">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que será feito o backup do banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="189eb-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="189eb-231">Mover o banco de dados de auditoria e conformidade do servidor a para o B</span><span class="sxs-lookup"><span data-stu-id="189eb-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="189eb-232">Mova os arquivos a seguir do servidor A para o servidor B usando o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="189eb-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="189eb-233">Dados de banco de dados de status de conformidade do MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="189eb-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="189eb-234">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="189eb-235">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-235">Note</span></span>**  
    <span data-ttu-id="189eb-236">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-237">$SERVERNAME $-Insira o nome do servidor no qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="189eb-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="189eb-238">$DESTINATIONSHARE $-digite o nome do compartilhamento e do caminho para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="189eb-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="189eb-239">Restaurar o banco de dados de auditoria e conformidade no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="189eb-240">Restaure o banco de dados de auditoria e conformidade no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="189eb-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="189eb-241">Após a conclusão da tarefa, selecione o arquivo de backup do banco de dados selecionando a opção **do dispositivo** e, em seguida, use o comando **Adicionar** para selecionar o arquivo data. bak do status de conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="189eb-242">Selecione **OK** para concluir o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="189eb-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="189eb-243">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:</span><span class="sxs-lookup"><span data-stu-id="189eb-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="189eb-244">Execute o arquivo SQL usando uma linha de comando do Windows PowerShell semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="189eb-245">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-245">Note</span></span>**  
    <span data-ttu-id="189eb-246">Substitua o seguinte valor no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-247">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de auditoria e conformidade será restaurado.</span><span class="sxs-lookup"><span data-stu-id="189eb-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="189eb-248">Configurar o acesso ao banco de dados de auditoria e conformidade no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="189eb-249">No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que está executando o recurso de administração e monitoramento do MBAM para o grupo local chamado acesso de banco de dados de **status de conformidade do MBAM**.</span><span class="sxs-lookup"><span data-stu-id="189eb-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="189eb-250">Verifique se o acesso ao banco de dados de **auditoria do MBAM** de login do SQL no banco de dados restaurado está mapeado para o nome de logon **$MachineName $ \ \ MBAM acesso ao banco**de dados de auditoria</span><span class="sxs-lookup"><span data-stu-id="189eb-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="189eb-251">Se não estiver mapeado como descrito, crie outro logon com associações de grupo semelhantes e mapeie-o para o nome de logon **$MachineName $ \ \ MBAM conformidade de banco**de dados de auditoria.</span><span class="sxs-lookup"><span data-stu-id="189eb-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="189eb-252">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando no servidor B semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="189eb-253">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-253">Note</span></span>**  
    <span data-ttu-id="189eb-254">Substitua os seguintes valores no exemplo acima pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="189eb-255">$DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="189eb-256">O nome do servidor deve ser seguido por "$", conforme mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="189eb-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="189eb-257">(por exemplo, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="189eb-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="189eb-258">$DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="189eb-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="189eb-259">Atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="189eb-260">Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que são hospedados no site de administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="189eb-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="189eb-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="189eb-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="189eb-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="189eb-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="189eb-263">Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.</span><span class="sxs-lookup"><span data-stu-id="189eb-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="189eb-264">Selecione a opção **configurationStrings** no controle da **lista de seções** .</span><span class="sxs-lookup"><span data-stu-id="189eb-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="189eb-265">Selecione a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.</span><span class="sxs-lookup"><span data-stu-id="189eb-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="189eb-266">No **Editor de coleção**, selecione a linha chamada **ComplianceStatusConnectionString** ao atualizar a configuração do aplicativo MBAMAdministrationService ou a linha chamada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** ao atualizar a configuração do MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="189eb-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="189eb-267">Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome do servidor e da instância (por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME) ao qual o banco de dados de recuperação foi movido.</span><span class="sxs-lookup"><span data-stu-id="189eb-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="189eb-268">Para automatizar esse procedimento, você pode usar o Windows para inserir uma linha de comando em cada servidor de administração e monitoramento semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="189eb-269">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-269">Note</span></span>**  
    <span data-ttu-id="189eb-270">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-271">$SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e a instância em que o banco de dados de recuperação está localizado.</span><span class="sxs-lookup"><span data-stu-id="189eb-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="189eb-272">Retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="189eb-273">Em cada servidor que está executando o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="189eb-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="189eb-274">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="189eb-275">Mover os relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="189eb-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="189eb-276">Se você quiser mover os relatórios de conformidade e conformidade do MBAM de um computador para outro (ou seja, mover os relatórios do servidor A para o servidor B), use o procedimento a seguir, que inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="189eb-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="189eb-277">Execute a instalação do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="189eb-278">Configure o acesso aos relatórios de conformidade e auditoria no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="189eb-279">Interrompa todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="189eb-280">Atualize os dados de conexão dos relatórios em servidores de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="189eb-281">Retome todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="189eb-282">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="189eb-283">Execute a instalação do MBAM no servidor B e selecione apenas o recurso de **relatórios de auditoria e conformidade** para a instalação.</span><span class="sxs-lookup"><span data-stu-id="189eb-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="189eb-284">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="189eb-285">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-285">Note</span></span>**  
    <span data-ttu-id="189eb-286">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-287">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de conformidade e auditoria está localizado.</span><span class="sxs-lookup"><span data-stu-id="189eb-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="189eb-288">$DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="189eb-289">$PASSWORD $-Insira a senha da conta de usuário que será usada para se conectar ao banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="189eb-290">$X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="189eb-291">Configurar o acesso aos relatórios de conformidade e auditoria no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="189eb-292">No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de usuário que terão acesso aos relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="189eb-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="189eb-293">Adicione as contas de usuário ao grupo local chamado MBAM Report users.</span><span class="sxs-lookup"><span data-stu-id="189eb-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="189eb-294">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando no servidor B semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="189eb-295">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-295">Note</span></span>**  
    <span data-ttu-id="189eb-296">Substitua os seguintes valores no exemplo acima pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="189eb-297">$DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="189eb-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="189eb-298">Parar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="189eb-299">Em cada servidor que está executando o recurso de servidor administração e monitoramento do MBAM, use o console do Gerenciador dos serviços de informações da Internet (IIS) para interromper o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="189eb-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="189eb-300">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="189eb-301">Atualizar os dados de conexão do banco de dados nos servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="189eb-302">Em cada servidor que está executando o recurso de servidor administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar a URL de relatórios de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="189eb-303">Selecione o site de **Administração e monitoramento do Microsoft BitLocker** e use o recurso do **Editor de configuração** que é local na seção **Gerenciamento** do modo de **exibição de recursos**.</span><span class="sxs-lookup"><span data-stu-id="189eb-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="189eb-304">Selecione a opção **appSettings** do controle da **lista de seções** .</span><span class="sxs-lookup"><span data-stu-id="189eb-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="189eb-305">Selecione a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.</span><span class="sxs-lookup"><span data-stu-id="189eb-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="189eb-306">No **Editor de coleção**, selecione a linha chamada **Microsoft. MBAM. Reports. URL**.</span><span class="sxs-lookup"><span data-stu-id="189eb-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="189eb-307">Atualize o valor de **Microsoft. MBAM. Reports. URL** para refletir o nome do servidor para o servidor B. Se o recurso relatórios de auditoria e conformidade foi instalado em uma instância nomeada do SQL Reporting Services, certifique-se de adicionar ou atualizar o nome da instância para a URL (por exemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....)</span><span class="sxs-lookup"><span data-stu-id="189eb-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="189eb-308">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando em cada servidor de administração e monitoramento semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="189eb-309">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-309">Note</span></span>**  
   <span data-ttu-id="189eb-310">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="189eb-311">$SERVERNAME $-digite o nome do nome do servidor ao qual os relatórios de conformidade e auditoria foram instalados.</span><span class="sxs-lookup"><span data-stu-id="189eb-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="189eb-312">$SRSINSTANCENAME $-Insira o nome da instância do SQL Reporting Services à qual os relatórios de conformidade e auditoria foram instalados.</span><span class="sxs-lookup"><span data-stu-id="189eb-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="189eb-313">Retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="189eb-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="189eb-314">Em cada servidor que está executando o recurso de servidor administração e monitoramento do MBAM, use o console do Gerenciador dos serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="189eb-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="189eb-315">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="189eb-316">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-316">Note</span></span>**  
    <span data-ttu-id="189eb-317">Para executar essa linha de comando, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189eb-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="189eb-318">Além disso, você deve atualizar a política de execução do PowerShell para permitir que os scripts sejam executados.</span><span class="sxs-lookup"><span data-stu-id="189eb-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="189eb-319">Movendo o recurso administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="189eb-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="189eb-320">Se você quiser mover o recurso de relatórios de monitoramento e administração do MBAM de um computador para outro (ou seja, mova o recurso do servidor A para o servidor B), use o procedimento a seguir, que inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="189eb-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="189eb-321">Execute a instalação do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="189eb-322">Configure o acesso ao banco de dados no servidor B.</span><span class="sxs-lookup"><span data-stu-id="189eb-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="189eb-323">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="189eb-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="189eb-324">Execute a instalação do MBAM no servidor B e selecione apenas o recurso de **servidor de administração e monitoramento** para a instalação.</span><span class="sxs-lookup"><span data-stu-id="189eb-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="189eb-325">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="189eb-326">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-326">Note</span></span>**  
    <span data-ttu-id="189eb-327">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="189eb-328">$SERVERNAME $ \ \ $SQLINSTANCENAME $-para o parâmetro COMPLIDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de conformidade e auditoria está localizado.</span><span class="sxs-lookup"><span data-stu-id="189eb-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="189eb-329">Para o parâmetro RECOVERYANDHWDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de recuperação está localizado.</span><span class="sxs-lookup"><span data-stu-id="189eb-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="189eb-330">$DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="189eb-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="189eb-331">$ REPORTSSERVERURL $-Insira a URL para o local de origem do site do serviço de relatórios SQL.</span><span class="sxs-lookup"><span data-stu-id="189eb-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="189eb-332">Se os relatórios foram instalados em uma instância padrão do SRS, o formato da URL terá o formato "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="189eb-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="189eb-333">Se os relatórios foram instalados em uma instância padrão do SRS, o formato da URL terá o formato "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".</span><span class="sxs-lookup"><span data-stu-id="189eb-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="189eb-334">$X $-insira **0** se você estiver instalando a topologia autônoma do MBAM ou **1** se estiver instalando a topologia do Gerenciador de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="189eb-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="189eb-335">Configurar o acesso aos bancos de dados</span><span class="sxs-lookup"><span data-stu-id="189eb-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="189eb-336">No servidor ou nos servidores em que o banco de dados de recuperação e o banco de dados de auditoria e conformidade são implantados, use o snap-in de usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que está executando o recurso de servidor de administração de **MBAM e do** **MBAM Access** (servidor de banco de dados de conformidade e auditoria).</span><span class="sxs-lookup"><span data-stu-id="189eb-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="189eb-337">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir uma linha de comando, que é semelhante ao seguinte, no servidor em que o banco de dados de auditoria e conformidade foi implantado.</span><span class="sxs-lookup"><span data-stu-id="189eb-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="189eb-338">No servidor em que o banco de dados de recuperação foi implantado, você pode usar o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="189eb-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="189eb-339">Observação</span><span class="sxs-lookup"><span data-stu-id="189eb-339">Note</span></span>**  
    <span data-ttu-id="189eb-340">Substitua o seguinte valor no exemplo acima pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="189eb-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="189eb-341">$DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração.</span><span class="sxs-lookup"><span data-stu-id="189eb-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="189eb-342">O nome do servidor deve ser seguido por um símbolo "$", conforme mostrado no exemplo (por exemplo, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="189eb-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="189eb-343">$DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="189eb-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="189eb-344">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="189eb-344">Related topics</span></span>


[<span data-ttu-id="189eb-345">Manutenção do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="189eb-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









