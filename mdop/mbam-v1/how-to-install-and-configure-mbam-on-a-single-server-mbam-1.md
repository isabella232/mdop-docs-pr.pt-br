---
title: Como instalar e configurar o MBAM em um servidor único
description: Como instalar e configurar o MBAM em um servidor único
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799404"
---
# <span data-ttu-id="7d91c-103">Como instalar e configurar o MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="7d91c-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="7d91c-104">Os procedimentos neste tópico descrevem a instalação completa dos recursos do Microsoft BitLocker Administration and Monitoring (MBAM) em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="7d91c-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="7d91c-105">Cada recurso do servidor tem determinados pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="7d91c-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="7d91c-106">Para verificar se você cumpriu os pré-requisitos e os requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7d91c-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="7d91c-107">Além disso, alguns recursos também têm informações que devem ser fornecidas durante o processo de instalação para a implantação bem-sucedida do recurso.</span><span class="sxs-lookup"><span data-stu-id="7d91c-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="7d91c-108">Você também deve rever [a preparação do seu ambiente para o MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de começar a implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="7d91c-109">**Observação**  Para obter os arquivos de log de instalação, você deve instalar o MBAM usando o pacote **msiexec** e a opção **/l** &lt; Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="7d91c-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="7d91c-110">Os arquivos de log são criados no local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="7d91c-111">Arquivos de log de instalação adicionais são criados na pasta% Temp% do usuário que está instalando o MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="7d91c-112">Para instalar os recursos do MBAM Server em um único servidor</span><span class="sxs-lookup"><span data-stu-id="7d91c-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="7d91c-113">As etapas a seguir descrevem como instalar os recursos gerais do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="7d91c-114">**Observação**  Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7d91c-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="7d91c-115">Para iniciar a instalação dos recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="7d91c-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="7d91c-116">Inicie o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="7d91c-117">Clique em **instalar** na página de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="7d91c-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="7d91c-118">Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="7d91c-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="7d91c-119">Por padrão, todos os recursos do MBAM são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="7d91c-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="7d91c-120">Os recursos que serão instalados no mesmo computador deverão ser instalados juntos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="7d91c-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="7d91c-121">Desmarque os recursos que você deseja instalar em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="7d91c-122">Você deve instalar os recursos do MBAM na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="7d91c-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="7d91c-123">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="7d91c-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="7d91c-124">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="7d91c-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="7d91c-125">Auditoria e relatórios de conformidade</span><span class="sxs-lookup"><span data-stu-id="7d91c-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="7d91c-126">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="7d91c-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="7d91c-127">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="7d91c-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="7d91c-128">**Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="7d91c-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="7d91c-129">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="7d91c-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="7d91c-130">Se um pré-requisito ausente for detectado, você deve resolver os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="7d91c-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="7d91c-131">Depois que todos os pré-requisitos forem atendidos, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="7d91c-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="7d91c-132">Você será solicitado a configurar a segurança de comunicação de rede.</span><span class="sxs-lookup"><span data-stu-id="7d91c-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="7d91c-133">O MBAM pode criptografar a comunicação entre o banco de dados de recuperação e do hardware, o servidor de administração e monitoramento e os clientes.</span><span class="sxs-lookup"><span data-stu-id="7d91c-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="7d91c-134">Se você decidir criptografar a comunicação, será solicitado a selecionar o certificado provisionado pela autoridade que será usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="7d91c-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="7d91c-135">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="7d91c-136">O assistente de configuração do MBAM exibirá as páginas de instalação dos recursos selecionados.</span><span class="sxs-lookup"><span data-stu-id="7d91c-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="7d91c-137">Para implantar recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="7d91c-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="7d91c-138">Na janela **Configurar o banco de dados de recuperação e de hardware** , especifique a instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação e hardware.</span><span class="sxs-lookup"><span data-stu-id="7d91c-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="7d91c-139">Você também deve especificar o local dos arquivos de banco de dados e o local das informações de log.</span><span class="sxs-lookup"><span data-stu-id="7d91c-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="7d91c-140">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="7d91c-141">Na janela **Configurar o banco de dados de conformidade e auditoria** , especifique a instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="7d91c-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="7d91c-142">Em seguida, especifique o local dos arquivos de banco de dados e o local das informações de log.</span><span class="sxs-lookup"><span data-stu-id="7d91c-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="7d91c-143">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="7d91c-144">Na janela **relatórios de conformidade e auditoria** , especifique a instância do serviço de relatório que será usada e forneça uma conta de usuário de domínio para acessar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7d91c-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="7d91c-145">Deve ser uma conta de usuário que seja provisionada especificamente para esse uso.</span><span class="sxs-lookup"><span data-stu-id="7d91c-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="7d91c-146">A conta de usuário deve poder acessar todos os dados disponíveis para o grupo usuários do MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="7d91c-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="7d91c-147">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="7d91c-148">Na janela **Configurar o servidor de administração e monitoração** , insira a **Associação de porta**, o nome do **host** (opcional) e o **caminho de instalação** do servidor de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="7d91c-149">**Aviso**  O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que um nome de cabeçalho de host exclusivo seja especificado.</span><span class="sxs-lookup"><span data-stu-id="7d91c-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="7d91c-150">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="7d91c-151">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7d91c-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="7d91c-152">A opção atualizações da Microsoft não ativa as atualizações automáticas no Windows.</span><span class="sxs-lookup"><span data-stu-id="7d91c-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="7d91c-153">Quando o assistente de configuração coletou as informações de recurso necessárias, a instalação do MBAM está pronta para começar.</span><span class="sxs-lookup"><span data-stu-id="7d91c-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="7d91c-154">Clique em **voltar** para voltar ao assistente se desejar revisar ou alterar as configurações de instalação.</span><span class="sxs-lookup"><span data-stu-id="7d91c-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="7d91c-155">Clique em **instalar** para começar a instalação.</span><span class="sxs-lookup"><span data-stu-id="7d91c-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="7d91c-156">Clique em **Cancelar** para sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="7d91c-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="7d91c-157">A instalação instala os recursos do MBAM e avisa que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7d91c-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="7d91c-158">Clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="7d91c-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="7d91c-159">Depois de instalar os recursos do MBAM Server, você deve adicionar usuários às funções MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="7d91c-160">Para obter mais informações, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7d91c-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="7d91c-161">Para executar a configuração pós-instalação</span><span class="sxs-lookup"><span data-stu-id="7d91c-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="7d91c-162">Após a conclusão da instalação, você deve adicionar funções de usuário para que você possa conceder aos usuários acesso aos recursos do site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="7d91c-163">No servidor de administração e monitoramento, adicione usuários aos seguintes grupos locais:</span><span class="sxs-lookup"><span data-stu-id="7d91c-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="7d91c-164">**Usuários de hardware do MBAM**: os membros desse grupo local podem acessar o recurso de hardware no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="7d91c-165">**Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de TPM no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="7d91c-166">Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="7d91c-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="7d91c-167">**Usuários de helpdesk avançados do MBAM**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="7d91c-168">Para os usuários avançados da assistência técnica, somente o campo ID da chave é necessário na recuperação de unidade.</span><span class="sxs-lookup"><span data-stu-id="7d91c-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="7d91c-169">Para gerenciar usuários do TPM, somente os campos domínio do computador e nome do computador são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7d91c-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="7d91c-170">No servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no computador que hospeda os relatórios de conformidade e auditoria, adicione usuários ao grupo local a seguir para permitir que eles acessem o recurso relatórios no site de administração do MBAM:</span><span class="sxs-lookup"><span data-stu-id="7d91c-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="7d91c-171">**Usuários de relatório MBAM**: os membros desse grupo local podem acessar os recursos de relatórios no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d91c-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="7d91c-172">**Observação**  Associação de usuários idênticas ou associação de grupo do grupo local **usuários de relatórios MBAM** devem ser mantidas em todos os computadores nos quais os recursos de servidor de administração e monitoramento, o banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estão instalados.</span><span class="sxs-lookup"><span data-stu-id="7d91c-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="7d91c-173">Para manter associações idênticas em todos os computadores, você deve criar um grupo de segurança de domínio e adicionar esse grupo de domínio a cada grupo de usuários MBAM de relatório local.</span><span class="sxs-lookup"><span data-stu-id="7d91c-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="7d91c-174">Ao fazer isso, você pode gerenciar as associações de grupo usando o grupo de domínio.</span><span class="sxs-lookup"><span data-stu-id="7d91c-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="7d91c-175">Validando a instalação de recursos do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="7d91c-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="7d91c-176">Quando a instalação do MBAM estiver concluída, valide se a instalação configurou com êxito todos os recursos de MBAM necessários para o gerenciamento do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7d91c-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="7d91c-177">Use o procedimento a seguir para confirmar se o serviço MBAM está funcionando:</span><span class="sxs-lookup"><span data-stu-id="7d91c-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="7d91c-178">Para validar a instalação de recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="7d91c-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="7d91c-179">Em cada servidor em que um recurso MBAM está implantado, abra o **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="7d91c-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="7d91c-180">Clique em **programas**e, em seguida, clique em **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="7d91c-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="7d91c-181">Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .</span><span class="sxs-lookup"><span data-stu-id="7d91c-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="7d91c-182">Observação</span><span class="sxs-lookup"><span data-stu-id="7d91c-182">Note</span></span>**  
   <span data-ttu-id="7d91c-183">Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="7d91c-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="7d91c-184">No servidor em que o banco de dados de recuperação e de hardware está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="7d91c-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="7d91c-185">No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o **banco de dados de auditoria e conformidade** com o MBAM está instalado.</span><span class="sxs-lookup"><span data-stu-id="7d91c-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="7d91c-186">No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com privilégios administrativos e navegue até a "página inicial" do site do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="7d91c-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="7d91c-187">O local padrão Home de uma instância do site do SQL Server Reporting Services está em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.</span><span class="sxs-lookup"><span data-stu-id="7d91c-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="7d91c-188">Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias especificadas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="7d91c-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="7d91c-189">Confirme se uma pasta denominada **relatórios de conformidade de Malta** está listada e se contém cinco relatórios e uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7d91c-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="7d91c-190">Observação</span><span class="sxs-lookup"><span data-stu-id="7d91c-190">Note</span></span>**  
   <span data-ttu-id="7d91c-191">Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="7d91c-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="7d91c-192">No servidor em que o recurso administração e monitoramento estiver instalado, execute **o Gerenciador de servidores** e navegue até **funções**, selecione **servidor Web (IIS)** e clique em **Gerenciador dos serviços de informações da Internet (IIS)**</span><span class="sxs-lookup"><span data-stu-id="7d91c-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="7d91c-193">Em **conexões**, navegue até \* &lt; NomeDoComputador &gt; \*, selecione **sites**e selecione **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="7d91c-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="7d91c-194">Verifique se **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.</span><span class="sxs-lookup"><span data-stu-id="7d91c-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="7d91c-195">No servidor em que o recurso administração e monitoramento estiver instalado, abra um navegador da Web com privilégios administrativos e navegue até os seguintes locais no site do MBAM para verificar se eles são carregados com êxito:</span><span class="sxs-lookup"><span data-stu-id="7d91c-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="7d91c-196">*http:// &lt; NomeDoComputador &gt; /Default.aspx* e confirme cada um dos links para navegação e relatórios</span><span class="sxs-lookup"><span data-stu-id="7d91c-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="7d91c-197">http:// &lt; nome_do_computador &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="7d91c-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="7d91c-198">http:// &lt; nome_do_computador &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="7d91c-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="7d91c-199">http:// &lt; nome_do_computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="7d91c-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="7d91c-200">Observação</span><span class="sxs-lookup"><span data-stu-id="7d91c-200">Note</span></span>**  
   <span data-ttu-id="7d91c-201">Normalmente, os serviços são instalados na porta padrão 80 sem criptografia de rede.</span><span class="sxs-lookup"><span data-stu-id="7d91c-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="7d91c-202">Se os serviços estiverem instalados em uma porta diferente, altere as URLs para incluir a porta apropriada.</span><span class="sxs-lookup"><span data-stu-id="7d91c-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="7d91c-203">Por exemplo, http://\* &lt; ComputerName &gt; : &lt; Port &gt; \*/default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> Default. aspx.</span><span class="sxs-lookup"><span data-stu-id="7d91c-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="7d91c-204">Se os serviços estiverem instalados com a criptografia de rede, altere http://para https://.</span><span class="sxs-lookup"><span data-stu-id="7d91c-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="7d91c-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d91c-205">Related topics</span></span>


[<span data-ttu-id="7d91c-206">Implantando a infraestrutura do Servidor do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7d91c-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





