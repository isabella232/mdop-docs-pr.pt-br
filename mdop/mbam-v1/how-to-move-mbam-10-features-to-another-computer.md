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
# <span data-ttu-id="91c20-103">Como Mover os Recursos do MBAM 1.0 para Outro Computador</span><span class="sxs-lookup"><span data-stu-id="91c20-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="91c20-104">Este tópico descreve as etapas que você deve seguir para mover um ou mais recursos de administração e monitoramento do Microsoft BitLocker (MBAM) para um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="91c20-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="91c20-105">Ao mover mais de um recurso do MBAM para outro computador, você deve movê-los na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="91c20-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="91c20-106">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="91c20-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="91c20-107">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="91c20-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="91c20-108">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="91c20-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="91c20-109">Administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="91c20-109">Administration and Monitoring</span></span>

## <span data-ttu-id="91c20-110">Para mover o banco de dados de recuperação e de hardware</span><span class="sxs-lookup"><span data-stu-id="91c20-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="91c20-111">Você pode usar o procedimento a seguir para mover o banco de dados de hardware e recuperação do MBAM de um computador para outro (você pode mover este recurso de servidor MBAM do servidor A para o servidor B):</span><span class="sxs-lookup"><span data-stu-id="91c20-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="91c20-112">Interrompa todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="91c20-113">Execute a configuração do MBAM no servidor B.</span><span class="sxs-lookup"><span data-stu-id="91c20-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="91c20-114">Faça backup do banco de dados de recuperação do MBAM e do hardware no servidor A.</span><span class="sxs-lookup"><span data-stu-id="91c20-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="91c20-115">Recuperação de MBAM e banco de dados de hardware do servidor A para B</span><span class="sxs-lookup"><span data-stu-id="91c20-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="91c20-116">Restaurar o banco de dados de recuperação e hardware do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="91c20-117">Configurar o acesso ao banco de dados de recuperação e hardware do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="91c20-118">Atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="91c20-119">Retomar todas as instâncias do Web site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="91c20-120">Para interromper todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="91c20-121">Use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="91c20-122">O site MBAM é denominado **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="91c20-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="91c20-123">Para automatizar esse procedimento, você pode usar um comando no prompt de comando semelhante ao seguinte usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="91c20-124">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-124">Note</span></span>**  
    <span data-ttu-id="91c20-125">Para executar este prompt de comando do PowerShell, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91c20-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="91c20-126">Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="91c20-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="91c20-127">Para executar a configuração do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="91c20-128">Execute a configuração do MBAM no servidor B e selecione o banco de dados de recuperação e de hardware para instalação.</span><span class="sxs-lookup"><span data-stu-id="91c20-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="91c20-129">Para automatizar esse procedimento, você pode usar um comando no prompt de comando semelhante ao seguinte usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="91c20-130">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-130">Note</span></span>**  
    <span data-ttu-id="91c20-131">Substitua os seguintes valores no exemplo acima por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-132">$SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e da instância para a qual o banco de dados de recuperação e de hardware será movido.</span><span class="sxs-lookup"><span data-stu-id="91c20-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="91c20-133">$DOMAIN $ \ \ $SERVERNAME $-Insira os nomes do servidor e do domínio de cada aplicativo MBAM e o servidor de monitoramento que entrarão em contato com o banco de dados de recuperação e de hardware.</span><span class="sxs-lookup"><span data-stu-id="91c20-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="91c20-134">Se houver vários nomes de domínio e servidor, use um ponto-e-vírgula para separar cada um deles na lista.</span><span class="sxs-lookup"><span data-stu-id="91c20-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="91c20-135">Por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="91c20-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="91c20-136">Além disso, cada nome de servidor deve ser seguido de um **$** .</span><span class="sxs-lookup"><span data-stu-id="91c20-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="91c20-137">Por exemplo, MyDomain\\MyServerName1 $ MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="91c20-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="91c20-138">Para fazer backup do banco de dados no servidor A</span><span class="sxs-lookup"><span data-stu-id="91c20-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="91c20-139">Para fazer backup do banco de dados de recuperação e do hardware no servidor A, use o SQL Server Management Studio e a tarefa chamada **fazer backup..**..</span><span class="sxs-lookup"><span data-stu-id="91c20-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="91c20-140">Por padrão, o nome do banco de dados é **MBAM recuperação e banco de dados de hardware**.</span><span class="sxs-lookup"><span data-stu-id="91c20-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="91c20-141">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:</span><span class="sxs-lookup"><span data-stu-id="91c20-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="91c20-142">Modifique a recuperação do MBAM e o banco de dados de hardware para usar o modo de recuperação completo.</span><span class="sxs-lookup"><span data-stu-id="91c20-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="91c20-143">Crie MBAM recuperação e dados de banco de dados de hardware e recuperação de MBAM dispositivos de backup lógicos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="91c20-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="91c20-144">Faça o backup do banco de dados de recuperação e do hardware completo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-144">Back up the full MBAM Recovery and Hardware database.</span></span>

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

    **<span data-ttu-id="91c20-145">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-145">Note</span></span>**  
    <span data-ttu-id="91c20-146">Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-147">$PASSWORD $-Insira uma senha que será usada para criptografar o arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="91c20-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="91c20-148">Execute o arquivo SQL usando o SQL Server PowerShell e um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="91c20-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="91c20-149">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-149">Note</span></span>**  
    <span data-ttu-id="91c20-150">Substitua o valor do exemplo anterior pelos que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-151">$SERVERNAME $ \ \ $SQLINSTANCENAME $-digite o nome do servidor e a instância do qual você deseja fazer backup do banco de dados de recuperação e do hardware.</span><span class="sxs-lookup"><span data-stu-id="91c20-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="91c20-152">Para mover o banco de dados e o certificado do servidor a para o B</span><span class="sxs-lookup"><span data-stu-id="91c20-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="91c20-153">Mova a recuperação do MBAM e dados de banco de dados de hardware. bak do servidor A para o servidor B usando o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="91c20-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="91c20-154">Para mover o certificado para o banco de dados criptografado, será necessário usar as etapas de automação a seguir.</span><span class="sxs-lookup"><span data-stu-id="91c20-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="91c20-155">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="91c20-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="91c20-156">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-156">Note</span></span>**  
    <span data-ttu-id="91c20-157">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-158">$SERVERNAME $-Insira o nome do servidor para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="91c20-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="91c20-159">$DESTINATIONSHARE $-Insira o nome do compartilhamento e o caminho para os quais os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="91c20-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="91c20-160">Para restaurar o banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="91c20-161">Restaure o banco de dados de recuperação e de hardware no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="91c20-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="91c20-162">Depois que a tarefa for executada, escolha o arquivo de backup do banco de dados selecionando a opção **do dispositivo** e, em seguida, use o comando **Adicionar** para escolher o arquivo de recuperação do MBAM e dados de banco de dados de hardware **. bak** .</span><span class="sxs-lookup"><span data-stu-id="91c20-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="91c20-163">Selecione **OK** para concluir o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="91c20-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="91c20-164">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte script SQL:</span><span class="sxs-lookup"><span data-stu-id="91c20-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="91c20-165">Solte o certificado criado pela configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="91c20-166">Adicionar certificado</span><span class="sxs-lookup"><span data-stu-id="91c20-166">Add certificate</span></span>

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

    <span data-ttu-id="91c20-167">Restaure os dados de banco de dados de hardware e recuperação do MBAM e os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="91c20-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="91c20-168">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-168">Note</span></span>**  
    <span data-ttu-id="91c20-169">Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-170">$PASSWORD $-Insira a senha usada para criptografar o arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="91c20-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="91c20-171">Use o Windows PowerShell para inserir uma linha de comando semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="91c20-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="91c20-172">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-172">Note</span></span>**  
    <span data-ttu-id="91c20-173">Substitua o valor do exemplo de oblíquo pelos que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-174">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância para a qual o banco de dados de recuperação e de hardware será restaurado.</span><span class="sxs-lookup"><span data-stu-id="91c20-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="91c20-175">Configurar o acesso ao banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="91c20-176">No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de computador de cada servidor que executa o recurso de administração e monitoramento do MBAM para o grupo local chamado **MBAM recuperação e acesso ao banco de**dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="91c20-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="91c20-177">Para automatizar esse procedimento, você pode usar o Windows PowerShell no servidor B para inserir um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="91c20-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="91c20-178">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-178">Note</span></span>**  
    <span data-ttu-id="91c20-179">Substitua os valores do exemplo anterior pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="91c20-180">$DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e o nome da máquina do servidor de administração e monitoração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="91c20-181">O nome do servidor deve ser seguido por a **$** , por exemplo, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="91c20-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="91c20-182">Para atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="91c20-183">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que estão hospedados no site de administração e monitoramento do Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="91c20-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="91c20-184">Serviço de administração do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="91c20-185">Recuperação de MBAM e serviço de hardware</span><span class="sxs-lookup"><span data-stu-id="91c20-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="91c20-186">Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.</span><span class="sxs-lookup"><span data-stu-id="91c20-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="91c20-187">Selecione a opção **configurationStrings** no controle da lista de seções.</span><span class="sxs-lookup"><span data-stu-id="91c20-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="91c20-188">Escolha a linha nomeada **(coleção)** e abra o **Editor de coleção** selecionando o botão no lado direito da linha.</span><span class="sxs-lookup"><span data-stu-id="91c20-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="91c20-189">No **Editor de coleção**, escolha a linha chamada **KeyRecoveryConnectionString** quando atualizou a configuração para o aplicativo ' MBAMAdministrationService ' ou escolha a linha chamada <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> ConnectionString, ao atualizar a configuração para o "MBAMRecoveryAndHardwareService".</span><span class="sxs-lookup"><span data-stu-id="91c20-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="91c20-190">Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome do servidor e a instância para a qual o banco de dados de recuperação e de hardware foi movido.</span><span class="sxs-lookup"><span data-stu-id="91c20-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="91c20-191">Por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $.</span><span class="sxs-lookup"><span data-stu-id="91c20-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="91c20-192">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell em cada servidor de administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="91c20-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="91c20-193">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-193">Note</span></span>**  
   <span data-ttu-id="91c20-194">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="91c20-195">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de recuperação e de hardware está.</span><span class="sxs-lookup"><span data-stu-id="91c20-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="91c20-196">Para retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="91c20-197">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM, que é chamado de **Administração e administração do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="91c20-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="91c20-198">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="91c20-199">Para mover o recurso de banco de dados de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="91c20-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="91c20-200">Se você optar por mover o recurso de banco de dados de status de conformidade do MBAM de um computador para outro, como do servidor a para o servidor B, você deve usar o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="91c20-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="91c20-201">Parar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="91c20-202">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="91c20-203">Fazer backup do banco de dados no servidor A</span><span class="sxs-lookup"><span data-stu-id="91c20-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="91c20-204">Mover o banco de dados do servidor A para o B</span><span class="sxs-lookup"><span data-stu-id="91c20-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="91c20-205">Restaurar o banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="91c20-206">Configurar o acesso ao banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="91c20-207">Atualizar dados de conexão de banco de dados em servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="91c20-208">Retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="91c20-209">Para interromper todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="91c20-210">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM, que é chamado **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="91c20-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="91c20-211">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="91c20-212">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-212">Note</span></span>**  
    <span data-ttu-id="91c20-213">Para executar esse comando, você deve adicionar o módulo do IIS do PowerShell à instância atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91c20-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="91c20-214">Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="91c20-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="91c20-215">Para executar a configuração do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="91c20-216">Execute a instalação do MBAM no servidor B e selecione o recurso de banco de dados status de conformidade para a instalação.</span><span class="sxs-lookup"><span data-stu-id="91c20-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="91c20-217">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="91c20-218">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-218">Note</span></span>**  
    <span data-ttu-id="91c20-219">Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-220">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de status de conformidade será movido.</span><span class="sxs-lookup"><span data-stu-id="91c20-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="91c20-221">$DOMAIN $ \ \ $SERVERNAME $-Insira os nomes de domínio e os nomes de servidor de cada aplicativo MBAM e monitorando o servidor de monitoramento que entrarão em contato com o banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="91c20-222">Se houver vários nomes de domínio e nomes de servidor, use um ponto-e-vírgula para separar cada um deles na lista.</span><span class="sxs-lookup"><span data-stu-id="91c20-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="91c20-223">Por exemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="91c20-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="91c20-224">Cada nome de servidor deve ser seguido por um **$** conforme mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="91c20-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="91c20-225">Por exemplo, MyDomain\\MyServerName1 $ MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="91c20-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="91c20-226">$DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="91c20-227">Para fazer backup do banco de dados de conformidade no servidor A</span><span class="sxs-lookup"><span data-stu-id="91c20-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="91c20-228">Para fazer backup do banco de dados de conformidade no servidor A, use o SQL Server Management Studio e a tarefa chamada **fazer backup..**..</span><span class="sxs-lookup"><span data-stu-id="91c20-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="91c20-229">Por padrão, o nome do banco de dados é **MBAM banco de dados de status de conformidade**.</span><span class="sxs-lookup"><span data-stu-id="91c20-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="91c20-230">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:</span><span class="sxs-lookup"><span data-stu-id="91c20-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="91c20-231">Execute o arquivo SQL com um comando semelhante ao seguinte, usando o PowerShell do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="91c20-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="91c20-232">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-232">Note</span></span>**  
    <span data-ttu-id="91c20-233">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-234">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância de onde será feito o backup do banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="91c20-235">Para mover o banco de dados do servidor A para o B</span><span class="sxs-lookup"><span data-stu-id="91c20-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="91c20-236">Mova os seguintes arquivos do servidor A para o servidor B, usando o Windows Explorer:</span><span class="sxs-lookup"><span data-stu-id="91c20-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="91c20-237">Dados de banco de dados de status de conformidade do MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="91c20-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="91c20-238">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="91c20-239">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-239">Note</span></span>**  
    <span data-ttu-id="91c20-240">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-241">$SERVERNAME $-Insira o nome do servidor no qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="91c20-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="91c20-242">$DESTINATIONSHARE $-digite o nome do compartilhamento e do caminho para o qual os arquivos serão copiados.</span><span class="sxs-lookup"><span data-stu-id="91c20-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="91c20-243">Para restaurar o banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="91c20-244">Restaure o banco de dados de status de conformidade no servidor B usando o SQL Server Management Studio e a tarefa denominada **restaurar banco de dados..**..</span><span class="sxs-lookup"><span data-stu-id="91c20-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="91c20-245">Depois que a tarefa for executada, selecione o arquivo de backup do banco de dados, selecionando a opção do dispositivo e, em seguida, use o comando adicionar para escolher o arquivo data. bak do status de conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="91c20-246">Clique em OK para concluir o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="91c20-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="91c20-247">Para automatizar esse procedimento, crie um arquivo SQL (. Sql) que contenha o seguinte-SQL script:</span><span class="sxs-lookup"><span data-stu-id="91c20-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="91c20-248">Execute o arquivo SQL com um comando semelhante ao seguinte, usando o PowerShell do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="91c20-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="91c20-249">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-249">Note</span></span>**  
    <span data-ttu-id="91c20-250">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-251">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de status de conformidade será restaurado.</span><span class="sxs-lookup"><span data-stu-id="91c20-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="91c20-252">Para configurar o acesso ao banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="91c20-253">No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas do computador de cada servidor que executa o recurso de administração e monitoramento do MBAM para o grupo local chamado acesso ao banco de dados do **status de conformidade do MBAM**.</span><span class="sxs-lookup"><span data-stu-id="91c20-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="91c20-254">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell no servidor B:</span><span class="sxs-lookup"><span data-stu-id="91c20-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="91c20-255">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-255">Note</span></span>**  
    <span data-ttu-id="91c20-256">Substitua o valor do exemplo anterior pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="91c20-257">$DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="91c20-258">O nome do servidor deve ser seguido de a **$** . Por exemplo, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="91c20-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="91c20-259">$DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="91c20-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="91c20-260">Para atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="91c20-261">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar as informações da cadeia de conexão para os seguintes aplicativos, que estão hospedados no site de administração e monitoramento do Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="91c20-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="91c20-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="91c20-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="91c20-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="91c20-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="91c20-264">Selecione cada aplicativo e use o recurso **Editor de configuração** , localizado na seção **Gerenciamento** do modo de **exibição de recursos**.</span><span class="sxs-lookup"><span data-stu-id="91c20-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="91c20-265">Selecione a opção **configurationStrings** no controle da lista de seções.</span><span class="sxs-lookup"><span data-stu-id="91c20-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="91c20-266">Selecione a linha nomeada **(coleção)** e abra o editor de coleção selecionando o botão no lado direito da linha.</span><span class="sxs-lookup"><span data-stu-id="91c20-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="91c20-267">No **Editor de coleção**, selecione a linha chamada **ComplianceStatusConnectionString**, ao atualizar a configuração do aplicativo MBAMAdministrationService ou a linha chamada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, quando você atualizar a configuração do MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="91c20-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="91c20-268">Atualize o valor da **fonte de dados =** valor da propriedade **configurationStrings** para listar o nome do servidor e o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="91c20-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="91c20-269">Por exemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME, para o qual o banco de dados de recuperação e de hardware foi movido.</span><span class="sxs-lookup"><span data-stu-id="91c20-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="91c20-270">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte em cada servidor de administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="91c20-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="91c20-271">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-271">Note</span></span>**  
    <span data-ttu-id="91c20-272">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-273">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e o nome da instância em que o banco de dados de recuperação e de hardware está localizado.</span><span class="sxs-lookup"><span data-stu-id="91c20-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="91c20-274">Para retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="91c20-275">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="91c20-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="91c20-276">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="91c20-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="91c20-277">PS C:\\ &gt; Start-website "administração e monitoramento do Microsoft BitLocker"</span><span class="sxs-lookup"><span data-stu-id="91c20-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="91c20-278">Para mover os relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="91c20-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="91c20-279">Se você optar por mover os relatórios de conformidade e conformidade do MBAM de um computador para outro (especificamente, se você mover o recurso do servidor a para o servidor B), deverá usar o procedimento e as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="91c20-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="91c20-280">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="91c20-281">Configurar o acesso aos relatórios de conformidade e auditoria no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="91c20-282">Parar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="91c20-283">Atualizar os dados de conexão dos relatórios nos servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="91c20-284">Retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="91c20-285">Para executar a configuração do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="91c20-286">Execute a instalação do MBAM no servidor B e selecione apenas o recurso de conformidade e auditoria para a instalação.</span><span class="sxs-lookup"><span data-stu-id="91c20-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="91c20-287">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="91c20-288">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-288">Note</span></span>**  
    <span data-ttu-id="91c20-289">Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-290">$SERVERNAME $ \ \ $SQLINSTANCENAME $-Insira o nome do servidor e a instância em que o banco de dados de status de conformidade está localizado.</span><span class="sxs-lookup"><span data-stu-id="91c20-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="91c20-291">$DOMAIN $ \ \ $USERNAME $-Insira o nome de domínio e o nome de usuário que serão usados pelo recurso de relatórios de auditoria e conformidade para se conectar ao banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="91c20-292">$PASSWORD $-Insira a senha da conta de usuário que será usada para se conectar ao banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="91c20-293">Para configurar o acesso aos relatórios de conformidade e auditoria no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="91c20-294">No servidor B, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas de usuário que terão acesso aos relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="91c20-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="91c20-295">Adicione as contas de usuário ao grupo local chamado "MBAM Report Users".</span><span class="sxs-lookup"><span data-stu-id="91c20-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="91c20-296">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell no servidor B.</span><span class="sxs-lookup"><span data-stu-id="91c20-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="91c20-297">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-297">Note</span></span>**  
    <span data-ttu-id="91c20-298">Substitua o seguinte valor do exemplo anterior pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="91c20-299">$DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="91c20-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="91c20-300">Para interromper todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="91c20-301">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site do MBAM chamado **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="91c20-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="91c20-302">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="91c20-303">Para atualizar os dados de conexão do banco de dados em servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="91c20-304">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para atualizar a URL dos relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="91c20-305">Selecione o site de **Administração e administração do Microsoft BitLocker** e use o recurso **Editor de configuração** que pode ser encontrado na seção **Gerenciamento** do modo de **exibição de recursos**.</span><span class="sxs-lookup"><span data-stu-id="91c20-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="91c20-306">Selecione a opção **appSettings** do controle da lista de seções.</span><span class="sxs-lookup"><span data-stu-id="91c20-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="91c20-307">Aqui, selecione a linha nomeada **(coleção)** e abra o editor de **coleção** selecionando o botão no lado direito da linha.</span><span class="sxs-lookup"><span data-stu-id="91c20-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="91c20-308">No **Editor de coleção**, selecione a linha chamada "Microsoft. MBAM. Reports. URL".</span><span class="sxs-lookup"><span data-stu-id="91c20-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="91c20-309">Atualize o valor de Microsoft. MBAM. Reports. URL para refletir o nome do servidor para o servidor B. Se o recurso de relatórios de conformidade e auditoria tiver sido instalado em uma instância nomeada do SQL Reporting Services, certifique-se de adicionar ou atualizar o nome da instância para a URL.</span><span class="sxs-lookup"><span data-stu-id="91c20-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="91c20-310">Por exemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....</span><span class="sxs-lookup"><span data-stu-id="91c20-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="91c20-311">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte em cada servidor de administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="91c20-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="91c20-312">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-312">Note</span></span>**  
   <span data-ttu-id="91c20-313">Substitua o valor do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="91c20-314">$SERVERNAME $-Insira o nome do servidor no qual os relatórios de conformidade e auditoria foram instalados.</span><span class="sxs-lookup"><span data-stu-id="91c20-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="91c20-315">$SRSINSTANCENAME $-Insira o nome da instância do SQL Reporting Services à qual os relatórios de conformidade e auditoria foram instalados.</span><span class="sxs-lookup"><span data-stu-id="91c20-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="91c20-316">Para retomar todas as instâncias do site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="91c20-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="91c20-317">Em cada um dos servidores que executam o recurso de administração e monitoramento do MBAM, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site do MBAM chamado **Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="91c20-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="91c20-318">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="91c20-319">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-319">Note</span></span>**  
    <span data-ttu-id="91c20-320">Para executar esse comando, o módulo do IIS do PowerShell deve ser adicionado à instância atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91c20-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="91c20-321">Além disso, você deve atualizar a política de execução do PowerShell para permitir a execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="91c20-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="91c20-322">Para mover o recurso de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="91c20-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="91c20-323">Se você optar por mover o recurso de administração e monitoramento de MBAM de um computador para outro (se você mover o recurso do servidor A para o servidor B), deverá usar o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="91c20-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="91c20-324">O processo inclui as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="91c20-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="91c20-325">Executar a instalação do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="91c20-326">Configurar o acesso ao banco de dados no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="91c20-327">Para executar a configuração do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="91c20-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="91c20-328">Execute a instalação do MBAM no servidor B e selecione apenas o recurso de administração para instalação.</span><span class="sxs-lookup"><span data-stu-id="91c20-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="91c20-329">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91c20-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="91c20-330">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-330">Note</span></span>**  
    <span data-ttu-id="91c20-331">Substitua os valores do exemplo anterior por aqueles que correspondam ao seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="91c20-332">$SERVERNAME $ \ \ $SQLINSTANCENAME $-para o parâmetro COMPLIDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de status de conformidade está localizado.</span><span class="sxs-lookup"><span data-stu-id="91c20-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="91c20-333">Para o parâmetro RECOVERYANDHWDB \ _SQLINSTANCE, insira o nome do servidor e a instância em que o banco de dados de recuperação e de hardware está localizado.</span><span class="sxs-lookup"><span data-stu-id="91c20-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="91c20-334">$DOMAIN $ \ \ $USERNAME $-Insira o domínio e o nome de usuário que serão usados pelo recurso de relatórios de conformidade e auditoria para se conectar ao banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="91c20-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="91c20-335">$ REPORTSSERVERURL $-Insira a URL para o local de origem do site do serviço de relatórios SQL.</span><span class="sxs-lookup"><span data-stu-id="91c20-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="91c20-336">Se os relatórios foram instalados em uma instância padrão do SRS, o formato de URL formatará "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="91c20-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="91c20-337">Se os relatórios foram instalados em uma instância padrão do SRS, o formato da URL será formatado para "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".</span><span class="sxs-lookup"><span data-stu-id="91c20-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="91c20-338">Para configurar o acesso aos bancos de dados</span><span class="sxs-lookup"><span data-stu-id="91c20-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="91c20-339">Em servidores ou servidores em que a recuperação e o hardware, e os bancos de dados de conformidade e auditoria são implantados, use o snap-in usuários e grupos locais do Gerenciador de servidores para adicionar as contas do computador de cada servidor que executa o recurso de administração e monitoramento do MBAM para os grupos locais denominados "recuperação do MBAM e o acesso ao banco de dados de hardware" (servidor de banco de dados de conformidade e auditoria).</span><span class="sxs-lookup"><span data-stu-id="91c20-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="91c20-340">Para automatizar esse procedimento, você pode usar um comando semelhante ao seguinte, usando o Windows PowerShell no servidor em que os bancos de dados de auditoria e conformidade foram implantados.</span><span class="sxs-lookup"><span data-stu-id="91c20-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="91c20-341">No servidor em que os bancos de dados de recuperação e de hardware foram implantados, execute um comando semelhante ao seguinte, usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91c20-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="91c20-342">Observação</span><span class="sxs-lookup"><span data-stu-id="91c20-342">Note</span></span>**  
    <span data-ttu-id="91c20-343">Substitua o valor do exemplo anterior pelos valores aplicáveis para o seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="91c20-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="91c20-344">$DOMAIN $ \ \ $SERVERNAME $ $-digite o nome do domínio e do computador do servidor de administração e monitoração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="91c20-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="91c20-345">O nome do servidor deve ser seguido de a **$** .</span><span class="sxs-lookup"><span data-stu-id="91c20-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="91c20-346">Por exemplo, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="91c20-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="91c20-347">$DOMAIN $ \ \ $REPORTSUSERNAME $-digite o nome da conta de usuário que foi usada para configurar a fonte de dados para os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="91c20-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="91c20-348">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91c20-348">Related topics</span></span>


[<span data-ttu-id="91c20-349">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="91c20-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









