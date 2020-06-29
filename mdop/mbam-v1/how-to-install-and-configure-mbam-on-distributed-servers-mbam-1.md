---
title: Como instalar e configurar o MBAM em servidores distribuídos
description: Como instalar e configurar o MBAM em servidores distribuídos
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799716"
---
# <span data-ttu-id="69c94-103">Como instalar e configurar o MBAM em servidores distribuídos</span><span class="sxs-lookup"><span data-stu-id="69c94-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="69c94-104">Os procedimentos neste tópico descrevem a instalação completa dos recursos do Microsoft BitLocker Administration and Monitoring (MBAM) em servidores distribuídos.</span><span class="sxs-lookup"><span data-stu-id="69c94-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="69c94-105">Cada recurso do servidor tem determinados pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="69c94-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="69c94-106">Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="69c94-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="69c94-107">Além disso, alguns recursos exigem que você forneça determinadas informações durante o processo de instalação para implantar o recurso com êxito.</span><span class="sxs-lookup"><span data-stu-id="69c94-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="69c94-108">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-108">Note</span></span>**  
<span data-ttu-id="69c94-109">Para obter os arquivos de log de instalação, você precisa instalar o MBAM usando o pacote **msiexec** e a opção \*\*/l &lt; Location &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="69c94-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="69c94-110">Os arquivos de log são criados no local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="69c94-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="69c94-111">Arquivos de log de instalação adicionais são criados na pasta% Temp% do usuário que executa a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="69c94-112">Implantar os recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="69c94-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="69c94-113">As etapas a seguir descrevem como instalar os recursos gerais do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="69c94-114">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-114">Note</span></span>**  
<span data-ttu-id="69c94-115">Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="69c94-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="69c94-116">Para implantar recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="69c94-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="69c94-117">Inicie o assistente de instalação do MBAM e clique em **instalar** na página de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="69c94-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="69c94-118">Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="69c94-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="69c94-119">Por padrão, todos os recursos do MBAM são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="69c94-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="69c94-120">Desmarque os recursos que você deseja instalar em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="69c94-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="69c94-121">Os recursos que você deseja instalar no mesmo computador devem ser instalados todos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="69c94-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="69c94-122">Os recursos do MBAM devem ser instalados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="69c94-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="69c94-123">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="69c94-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="69c94-124">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="69c94-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="69c94-125">Auditoria e relatórios de conformidade</span><span class="sxs-lookup"><span data-stu-id="69c94-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="69c94-126">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="69c94-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="69c94-127">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="69c94-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="69c94-128">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-128">Note</span></span>**  
    <span data-ttu-id="69c94-129">O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="69c94-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="69c94-130">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="69c94-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="69c94-131">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="69c94-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="69c94-132">Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="69c94-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="69c94-133">O assistente de configuração do MBAM exibirá as páginas de instalação dos recursos selecionados.</span><span class="sxs-lookup"><span data-stu-id="69c94-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="69c94-134">As seções a seguir descrevem os procedimentos de instalação para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="69c94-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="69c94-135">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-135">Note</span></span>**  
    <span data-ttu-id="69c94-136">Geralmente, cada recurso é instalado em um servidor separado.</span><span class="sxs-lookup"><span data-stu-id="69c94-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="69c94-137">Se você quiser instalar vários recursos em um único servidor, poderá alterar ou eliminar algumas das etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="69c94-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="69c94-138">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69c94-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="69c94-139">Quando as informações do recurso MBAM selecionado estiverem completas, você estará pronto para iniciar a instalação do MBAM usando o assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="69c94-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="69c94-140">Clique em **voltar** para mover-se pelo assistente se precisar revisar ou alterar as configurações de instalação.</span><span class="sxs-lookup"><span data-stu-id="69c94-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="69c94-141">Clique em **instalar** para começar a instalação.</span><span class="sxs-lookup"><span data-stu-id="69c94-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="69c94-142">Clique em **Cancelar** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="69c94-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="69c94-143">A instalação instala os recursos do MBAM que você selecionou e avisa que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="69c94-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="69c94-144">Clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="69c94-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="69c94-145">Adicione usuários às funções MBAM apropriadas, após a instalação dos recursos do servidor do MBAM..</span><span class="sxs-lookup"><span data-stu-id="69c94-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="69c94-146">Para obter mais informações, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="69c94-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="69c94-147">Configuração pós-instalação</span><span class="sxs-lookup"><span data-stu-id="69c94-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="69c94-148">Após a conclusão da instalação do MBAM, você deve adicionar funções de usuário para que os usuários possam acessar os recursos no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="69c94-149">No servidor de administração e monitoramento, adicione usuários aos grupos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="69c94-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="69c94-150">**Usuários de hardware do MBAM**: os membros desse grupo local podem acessar o recurso de hardware no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="69c94-151">**Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de módulos de plataforma confiáveis (TPM) no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="69c94-152">Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="69c94-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="69c94-153">**Usuários de helpdesk avançados do MBAM**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="69c94-154">Para os usuários avançados da assistência técnica, somente o campo ID da chave é necessário na recuperação de unidade.</span><span class="sxs-lookup"><span data-stu-id="69c94-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="69c94-155">Em gerenciar TPM, somente os campos domínio do computador e nome do computador são necessários.</span><span class="sxs-lookup"><span data-stu-id="69c94-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="69c94-156">No servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria, adicione usuários ao grupo local a seguir para dar a eles acesso ao recurso relatórios no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="69c94-157">**Usuários de relatório MBAM**: os membros desse grupo local podem acessar os relatórios no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="69c94-158">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-158">Note</span></span>**  
    <span data-ttu-id="69c94-159">Associações de usuário ou de grupo idênticas do grupo local **usuários do relatório MBAM** devem ser mantidas em todos os computadores nos quais os recursos de servidor administração e monitoramento do MBAM, banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estejam instalados.</span><span class="sxs-lookup"><span data-stu-id="69c94-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="69c94-160">Validar a instalação de recursos do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="69c94-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="69c94-161">Quando a instalação do recurso MBAM Server estiver concluída, você deve validar se a instalação configurou com êxito todos os recursos necessários para o MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c94-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="69c94-162">Use o procedimento a seguir para confirmar se o serviço MBAM está funcionando.</span><span class="sxs-lookup"><span data-stu-id="69c94-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="69c94-163">Para validar uma instalação do MBAM</span><span class="sxs-lookup"><span data-stu-id="69c94-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="69c94-164">Em cada servidor, onde um recurso do MBAM é implantado, abra o **painel de controle**, clique em **programas**e clique em **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="69c94-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="69c94-165">Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .</span><span class="sxs-lookup"><span data-stu-id="69c94-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="69c94-166">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-166">Note</span></span>**  
   <span data-ttu-id="69c94-167">Para validar a instalação do MBAM, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="69c94-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="69c94-168">No servidor em que o banco de dados de recuperação e de hardware está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="69c94-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="69c94-169">No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **status de conformidade do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="69c94-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="69c94-170">No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com privilégios administrativos e navegue até a "página inicial" do site do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="69c94-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="69c94-171">O local padrão Home de uma instância do site do SQL Server Reporting Services pode ser encontrado em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="69c94-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="69c94-172">Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias especificadas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="69c94-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="69c94-173">Confirme se uma pasta denominada **relatórios de conformidade de Malta** está listada e se contém cinco relatórios e uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="69c94-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="69c94-174">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-174">Note</span></span>**  
   <span data-ttu-id="69c94-175">Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="69c94-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="69c94-176">No servidor em que o recurso administração e monitoramento estiver instalado, execute **o Gerenciador de servidores** e navegue até **funções**, selecione **servidor Web (IIS)** e clique em **Gerenciador dos serviços de informações da Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="69c94-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="69c94-177">Em **conexões** , navegue até \* &lt; NomeDoComputador &gt; \*, clique em **sites**e clique em **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="69c94-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="69c94-178">Verifique se **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.</span><span class="sxs-lookup"><span data-stu-id="69c94-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="69c94-179">No servidor em que o recurso administração e monitoramento estiver instalado, abra um navegador da Web com privilégios administrativos e navegue até os seguintes locais no site da MBAM para verificar se eles são carregados com êxito:</span><span class="sxs-lookup"><span data-stu-id="69c94-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="69c94-180">*http:// &lt; NomeDoComputador &gt; /Default.aspx* e confirme cada um dos links para navegação e relatórios</span><span class="sxs-lookup"><span data-stu-id="69c94-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="69c94-181">http:// &lt; nome_do_computador &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="69c94-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="69c94-182">http:// &lt; nome_do_computador &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="69c94-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="69c94-183">http:// &lt; nome_do_computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="69c94-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="69c94-184">Observação</span><span class="sxs-lookup"><span data-stu-id="69c94-184">Note</span></span>**  
   <span data-ttu-id="69c94-185">Normalmente, os serviços são instalados na porta padrão 80 sem criptografia de rede.</span><span class="sxs-lookup"><span data-stu-id="69c94-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="69c94-186">Se os serviços estiverem instalados em uma porta diferente, altere as URLs para incluir a porta apropriada.</span><span class="sxs-lookup"><span data-stu-id="69c94-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="69c94-187">Por exemplo, http://\* &lt; ComputerName &gt; : &lt; Port &gt; \*/default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> Default. aspx</span><span class="sxs-lookup"><span data-stu-id="69c94-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="69c94-188">Se os serviços foram instalados com a criptografia de rede, altere http://para https://.</span><span class="sxs-lookup"><span data-stu-id="69c94-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="69c94-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69c94-189">Related topics</span></span>


[<span data-ttu-id="69c94-190">Implantando a infraestrutura do Servidor do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="69c94-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









