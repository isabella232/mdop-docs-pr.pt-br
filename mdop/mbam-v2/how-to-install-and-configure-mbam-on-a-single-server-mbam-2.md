---
title: Como instalar e configurar o MBAM em um servidor único
description: Como instalar e configurar o MBAM em um servidor único
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799398"
---
# <span data-ttu-id="62c35-103">Como instalar e configurar o MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="62c35-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="62c35-104">Os procedimentos neste tópico descrevem como instalar o Microsoft BitLocker Administration and Monitoring (MBAM) na topologia autônoma em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="62c35-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="62c35-105">Use a configuração de servidor único em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="62c35-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="62c35-106">Para ambientes de produção, use dois ou mais servidores.</span><span class="sxs-lookup"><span data-stu-id="62c35-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="62c35-107">Se você estiver instalando a administração e o monitoramento do Microsoft BitLocker usando a topologia do Configuration Manager, consulte [implantando o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="62c35-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="62c35-108">O diagrama a seguir mostra um exemplo de uma arquitetura de servidor único.</span><span class="sxs-lookup"><span data-stu-id="62c35-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="62c35-109">Para obter uma descrição dos bancos de dados e recursos, consulte [arquitetura de alto nível para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="62c35-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![MBAM 2 topologia de implantação de servidor único](images/mbam2-1-server.gif)

<span data-ttu-id="62c35-111">Cada recurso do servidor tem determinados pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="62c35-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="62c35-112">Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="62c35-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="62c35-113">Além disso, alguns recursos também têm informações que devem ser fornecidas durante o processo de instalação para a implantação bem-sucedida do recurso.</span><span class="sxs-lookup"><span data-stu-id="62c35-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="62c35-114">Você também deve rever [a preparação do seu ambiente para o MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md) antes de iniciar a implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="62c35-115">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-115">Note</span></span>**  
<span data-ttu-id="62c35-116">Para obter os arquivos de log de instalação, use o pacote msiexec e a opção **/l** &lt; Location &gt; para instalar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="62c35-117">Os arquivos de log são criados no local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="62c35-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="62c35-118">Arquivos de log de instalação adicionais são criados na pasta% temp% no servidor do usuário que está instalando o MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="62c35-119">Para instalar os recursos do MBAM Server em um único servidor</span><span class="sxs-lookup"><span data-stu-id="62c35-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="62c35-120">As etapas a seguir descrevem como instalar os recursos gerais do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="62c35-121">Para iniciar a instalação dos recursos do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="62c35-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="62c35-122">No servidor em que você deseja instalar o MBAM, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="62c35-123">Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="62c35-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="62c35-124">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="62c35-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="62c35-125">Na página **seleção de topologia** , selecione a topologia **autônoma** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="62c35-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="62c35-126">Na página **selecionar recursos para instalar** , selecione os recursos que você deseja instalar.</span><span class="sxs-lookup"><span data-stu-id="62c35-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="62c35-127">Por padrão, todos os recursos do MBAM são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="62c35-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="62c35-128">Os recursos que devem ser instalados no mesmo computador devem ser instalados juntos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="62c35-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="62c35-129">Desmarque as caixas de seleção de todos os recursos que você deseja instalar em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="62c35-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="62c35-130">Você deve instalar os recursos do MBAM na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="62c35-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="62c35-131">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="62c35-131">Recovery Database</span></span>

    -   <span data-ttu-id="62c35-132">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="62c35-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="62c35-133">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="62c35-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="62c35-134">Servidor de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="62c35-134">Self-Service Server</span></span>

    -   <span data-ttu-id="62c35-135">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="62c35-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="62c35-136">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="62c35-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="62c35-137">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-137">Note</span></span>**  
    <span data-ttu-id="62c35-138">O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="62c35-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="62c35-139">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="62c35-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="62c35-140">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="62c35-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="62c35-141">Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="62c35-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="62c35-142">Na página **Configurar segurança de comunicação de rede** , escolha se deseja criptografar a comunicação entre os serviços Web no servidor de administração e monitoramento e nos clientes.</span><span class="sxs-lookup"><span data-stu-id="62c35-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="62c35-143">Se você decidir criptografar a comunicação, selecione a autoridade de certificação-certificado provisionado para usar para criptografia.</span><span class="sxs-lookup"><span data-stu-id="62c35-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="62c35-144">O certificado deve ser criado antes desta etapa para permitir que você o selecione nessa página.</span><span class="sxs-lookup"><span data-stu-id="62c35-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="62c35-145">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-145">Note</span></span>**  
    <span data-ttu-id="62c35-146">Esta página será exibida somente se você tiver selecionado o portal de autoatendimento ou o recurso de servidor de administração e monitoramento na página **selecionar recursos para instalar** .</span><span class="sxs-lookup"><span data-stu-id="62c35-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="62c35-147">Clique em **Avançar**e, em seguida, prossiga para o próximo conjunto de etapas para configurar os recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="62c35-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="62c35-148">Para configurar os recursos do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="62c35-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="62c35-149">Na página **Configurar o banco** de dados de recuperação, especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="62c35-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="62c35-150">Você também deve especificar onde os arquivos do banco de dados serão localizados e onde as informações do log serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="62c35-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="62c35-151">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="62c35-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="62c35-152">Na página **Configurar o banco de dados de conformidade e auditoria** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="62c35-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="62c35-153">Você também deve especificar onde os arquivos do banco de dados serão localizados e onde as informações do log serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="62c35-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="62c35-154">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="62c35-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="62c35-155">Na página **Configurar a conformidade e os relatórios de auditoria** , especifique a instância do SQL Server Reporting Services na qual os relatórios de conformidade e auditoria serão instalados e forneça uma conta de usuário de domínio e uma senha para acessar o banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="62c35-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="62c35-156">Configure a senha desta conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="62c35-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="62c35-157">A conta de usuário deve poder acessar todos os dados disponíveis para o grupo usuários do MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="62c35-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="62c35-158">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="62c35-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="62c35-159">Na página **Configurar o portal de autoatendimento** , insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="62c35-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="62c35-160">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-160">Note</span></span>**  
    <span data-ttu-id="62c35-161">O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo.</span><span class="sxs-lookup"><span data-stu-id="62c35-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="62c35-162">Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="62c35-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="62c35-163">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="62c35-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="62c35-164">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="62c35-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="62c35-165">Isso não ativa as atualizações automáticas no Windows.</span><span class="sxs-lookup"><span data-stu-id="62c35-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="62c35-166">Na página **Configurar o servidor de administração e monitoramento** , insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do site de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="62c35-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="62c35-167">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-167">Note</span></span>**  
    <span data-ttu-id="62c35-168">O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo.</span><span class="sxs-lookup"><span data-stu-id="62c35-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="62c35-169">Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="62c35-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="62c35-170">Na página **Resumo da instalação** , examine a lista de recursos que serão instalados e clique em **instalar** para começar a instalar os recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="62c35-171">Clique em **voltar** para voltar ao assistente se precisar revisar ou alterar as configurações de instalação ou clique em **Cancelar** para sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="62c35-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="62c35-172">A instalação instala os recursos do MBAM e avisa que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="62c35-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="62c35-173">Clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="62c35-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="62c35-174">Depois que os recursos do Microsoft BitLocker Administration and Monitoring Server tiverem sido instalados, prossiga para a próxima seção e conclua as etapas necessárias para adicionar usuários às funções de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="62c35-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="62c35-175">Para obter mais informações sobre as funções, consulte [planejando funções de administrador do MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="62c35-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="62c35-176">Para executar a configuração pós-instalação</span><span class="sxs-lookup"><span data-stu-id="62c35-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="62c35-177">No servidor de administração e monitoramento, adicione usuários aos grupos locais a seguir para dar a eles acesso aos recursos de site do suporte técnico do MBAM:</span><span class="sxs-lookup"><span data-stu-id="62c35-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="62c35-178">**Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="62c35-179">Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="62c35-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="62c35-180">**MBAM usuários avançados da assistência técnica**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="62c35-181">Para os usuários avançados da assistência técnica, somente o campo **ID da chave** é necessário na recuperação de unidade.</span><span class="sxs-lookup"><span data-stu-id="62c35-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="62c35-182">Em gerenciar TPM, somente os campos **domínio do computador** e nome do **computador** são necessários.</span><span class="sxs-lookup"><span data-stu-id="62c35-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="62c35-183">No servidor de administração e monitoramento, adicione usuários ao grupo local a seguir para habilitá-los a acessar o recurso relatórios no site Administração e monitoramento do MBAM:</span><span class="sxs-lookup"><span data-stu-id="62c35-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="62c35-184">**Usuários de relatório MBAM**: os membros desse grupo local podem acessar os recursos de relatórios no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62c35-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="62c35-185">Marca o portal de autoatendimento com o nome da sua empresa, o texto de aviso e outras informações específicas da empresa.</span><span class="sxs-lookup"><span data-stu-id="62c35-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="62c35-186">Para obter instruções, consulte [como marcar o portal de autoatendimento](how-to-brand-the-self-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="62c35-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="62c35-187">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-187">Note</span></span>**  
    <span data-ttu-id="62c35-188">Associações de usuário ou de grupo idênticas do grupo local **usuários do relatório do MBAM** devem ser mantidas em todos os computadores nos quais os recursos do servidor de administração e monitoramento do MBAM, banco de dados de conformidade e auditoria, e conformidade e relatórios de auditoria estejam instalados.</span><span class="sxs-lookup"><span data-stu-id="62c35-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="62c35-189">A maneira recomendada de fazer isso é criar um grupo de segurança de domínio e adicionar esse grupo de domínio a cada grupo de usuários de relatório MBAM local.</span><span class="sxs-lookup"><span data-stu-id="62c35-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="62c35-190">Ao usar esse processo, gerencie as associações de grupo por meio do grupo de domínio.</span><span class="sxs-lookup"><span data-stu-id="62c35-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="62c35-191">Validando a instalação de recursos do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="62c35-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="62c35-192">Quando a instalação do Microsoft BitLocker Administration and Monitoring for concluída, valide se a instalação configurou com êxito todos os recursos MBAM necessários para o gerenciamento do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="62c35-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="62c35-193">Use o procedimento a seguir para confirmar se o serviço MBAM está funcionando.</span><span class="sxs-lookup"><span data-stu-id="62c35-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="62c35-194">Para validar a instalação de recursos do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="62c35-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="62c35-195">Em cada servidor em que um recurso MBAM está implantado, abra o **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="62c35-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="62c35-196">Selecione **programas**e, em seguida, selecione **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="62c35-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="62c35-197">Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .</span><span class="sxs-lookup"><span data-stu-id="62c35-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="62c35-198">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-198">Note</span></span>**  
   <span data-ttu-id="62c35-199">Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="62c35-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="62c35-200">No servidor em que o banco de dados de recuperação está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="62c35-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="62c35-201">No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o **banco de dados de status de conformidade do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="62c35-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="62c35-202">No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com credenciais administrativas e navegue até a "página inicial" do site do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="62c35-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="62c35-203">O local padrão Home de uma instância do site do SQL Server Reporting Services está em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.</span><span class="sxs-lookup"><span data-stu-id="62c35-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="62c35-204">Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias especificadas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="62c35-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="62c35-205">Confirme se uma pasta de relatórios denominada administração e administração do Microsoft BitLocker contém uma fonte de dados chamada **MaltaDataSource** e se uma pasta **en-US** contém quatro relatórios.</span><span class="sxs-lookup"><span data-stu-id="62c35-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="62c35-206">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-206">Note</span></span>**  
   <span data-ttu-id="62c35-207">Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="62c35-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="62c35-208">No servidor em que o recurso administração e monitoramento estiver instalado, execute o **Gerenciador de servidores** e navegue até **funções**.</span><span class="sxs-lookup"><span data-stu-id="62c35-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="62c35-209">Selecione **servidor Web (IIS)** e, em seguida, clique em **Gerenciador dos serviços de informações da Internet (IIS).**</span><span class="sxs-lookup"><span data-stu-id="62c35-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="62c35-210">Em **conexões,** navegue até \* &lt; NomeDoComputador &gt; \*, selecione **sites**e, em seguida, selecione **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="62c35-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="62c35-211">Verifique se o **MBAMAdministrationService**, o **MBAMUserSupportService**, o **MBAMComplianceStatusService**e o **MBAMRecoveryAndHardwareService** estão listados.</span><span class="sxs-lookup"><span data-stu-id="62c35-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="62c35-212">No servidor em que os recursos de administração e monitoramento e o portal de autoatendimento estão instalados, abra um navegador da Web com credenciais administrativas e navegue até os seguintes locais para verificar se eles são carregados com êxito:</span><span class="sxs-lookup"><span data-stu-id="62c35-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="62c35-213">*http:// &lt; hostname &gt; /helpdesk/default.aspx* e confirme cada um dos links para navegação e relatórios</span><span class="sxs-lookup"><span data-stu-id="62c35-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="62c35-214">http:// &lt; hostname &gt; /SelfService&gt;/</span><span class="sxs-lookup"><span data-stu-id="62c35-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="62c35-215">http:// &lt; nome_do_computador &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="62c35-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="62c35-216">http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="62c35-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="62c35-217">http:// &lt; nome_do_computador &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="62c35-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="62c35-218">http:// &lt; nome_do_computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="62c35-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="62c35-219">Observação</span><span class="sxs-lookup"><span data-stu-id="62c35-219">Note</span></span>**  
   <span data-ttu-id="62c35-220">Presume-se que os recursos do servidor foram instalados na porta padrão sem criptografia de rede.</span><span class="sxs-lookup"><span data-stu-id="62c35-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="62c35-221">Se você instalou os recursos de servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada, por exemplo, *http:// &lt; hostname &gt; : &lt; Port &gt; /helpdesk/default.asp*x ou*http:// &lt; hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /Default.aspx*</span><span class="sxs-lookup"><span data-stu-id="62c35-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="62c35-222">Se os recursos do servidor foram instalados com a criptografia de rede, altere http://para https://.</span><span class="sxs-lookup"><span data-stu-id="62c35-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="62c35-223">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62c35-223">Related topics</span></span>


[<span data-ttu-id="62c35-224">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="62c35-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









