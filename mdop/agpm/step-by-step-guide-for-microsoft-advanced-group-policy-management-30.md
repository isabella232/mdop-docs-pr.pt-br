---
title: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft
description: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797303"
---
# <span data-ttu-id="b6f55-103">Guia passo a passo do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="b6f55-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="b6f55-104">Este guia passo a passo demonstra técnicas avançadas de gerenciamento de política de grupo usando o console de gerenciamento de política de grupo (GPMC) e o gerenciamento avançado de política de grupo (AGPM) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b6f55-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="b6f55-105">O AGPM aumenta a funcionalidade do GPMC, fornecendo:</span><span class="sxs-lookup"><span data-stu-id="b6f55-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="b6f55-106">Funções padrão para delegar permissões para gerenciar GPOs (objetos de política de grupo) para vários administradores de política de grupo, bem como a capacidade de delegar o acesso a GPOs no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="b6f55-107">Um arquivo morto para permitir que os administradores de política de grupo criem e modifiquem os GPOs offline antes de implantá-los em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="b6f55-108">A capacidade de reverter para qualquer versão anterior de um GPO no arquivo morto e limitar o número de versões armazenadas no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b6f55-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="b6f55-109">Funcionalidade de check-in/check-out para os GPOs para garantir que os administradores de política de grupo não substituam acidentalmente o trabalho uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="b6f55-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="b6f55-110">Visão geral do cenário do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-110">AGPM scenario overview</span></span>


<span data-ttu-id="b6f55-111">Para esse cenário, você usará uma conta de usuário separada para cada função no AGPM para demonstrar como a política de grupo pode ser gerenciada em um ambiente com vários administradores de política de grupo com diferentes níveis de permissões.</span><span class="sxs-lookup"><span data-stu-id="b6f55-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="b6f55-112">Especificamente, você vai executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b6f55-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="b6f55-113">Usando uma conta que seja membro do grupo Domain admins, instale o servidor do AGPM e atribua a função de administrador do AGPM a uma conta ou grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="b6f55-114">Usando contas às quais você atribuirá funções do AGPM, instale o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="b6f55-115">Usar uma conta com a função de administrador do AGPM, configurar o AGPM e o acesso de representante a GPOs atribuindo funções a outras contas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="b6f55-116">Usando uma conta com a função editor, solicite a criação de um GPO, que você Então aprova usando uma conta com a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="b6f55-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="b6f55-117">Com a conta editor, verifique o GPO do arquivo morto, edite o GPO, verifique o GPO no arquivo e solicite a implantação.</span><span class="sxs-lookup"><span data-stu-id="b6f55-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="b6f55-118">Usando uma conta com a função Aprovador, examine o GPO e implante-o em seu ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="b6f55-119">Usando uma conta com a função editor, crie um modelo de GPO e use-o como ponto de partida para criar um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="b6f55-120">Usar uma conta com a função Aprovador, excluir e restaurar um GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![processo de desenvolvimento de objetos de política de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="b6f55-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6f55-122">Requirements</span></span>


<span data-ttu-id="b6f55-123">Os computadores em que você deseja instalar o AGPM devem atender aos seguintes requisitos, e você deve criar contas para uso nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="b6f55-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="b6f55-124">**Observação**  Se você tiver o AGPM 2,5 instalado e estiver atualizando do Windows Server® 2003 para o Windows Server2008 ou WindowsVista® sem nenhum Service Pack instalado para o WindowsVista com o Service Pack1, você deve atualizar o sistema operacional antes de poder atualizar para o AGPM 3.0.</span><span class="sxs-lookup"><span data-stu-id="b6f55-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="b6f55-125">Requisitos do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-125">AGPM Server requirements</span></span>

<span data-ttu-id="b6f55-126">O servidor do AGPM 3.0 requer o Windows Server2008 ou o WindowsVista com Service Pack1 e o GPMC a partir de ferramentas de administração de servidor remoto (RSAT) instaladas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="b6f55-127">Há suporte para as duas versões de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b6f55-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="b6f55-128">Antes de instalar o servidor do AGPM, você deve ser membro do grupo Domain admins e os seguintes recursos do Windows devem estar presentes, a menos que indicado de outra forma:</span><span class="sxs-lookup"><span data-stu-id="b6f55-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="b6f55-129">GPMC</span><span class="sxs-lookup"><span data-stu-id="b6f55-129">GPMC</span></span>

    -   <span data-ttu-id="b6f55-130">Windows Server 2008: o GPMC será instalado automaticamente pelo AGPM, se não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="b6f55-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="b6f55-131">Windows Vista: você deve instalar o GPMC a partir do RSAT antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="b6f55-132">Para obter mais informações, consulte <https://go.microsoft.com/fwlink/?LinkID=116179> .</span><span class="sxs-lookup"><span data-stu-id="b6f55-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="b6f55-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="b6f55-133">.NET Framework 3.5</span></span>

<span data-ttu-id="b6f55-134">Os seguintes recursos do Windows são exigidos pelo servidor do AGPM e serão instalados automaticamente se não estiverem presentes:</span><span class="sxs-lookup"><span data-stu-id="b6f55-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="b6f55-135">Ativação do WCF; Ativação não HTTP</span><span class="sxs-lookup"><span data-stu-id="b6f55-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="b6f55-136">Serviço de Ativação de Processos do Windows</span><span class="sxs-lookup"><span data-stu-id="b6f55-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="b6f55-137">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="b6f55-137">Process Model</span></span>

    -   <span data-ttu-id="b6f55-138">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="b6f55-138">.NET Environment</span></span>

    -   <span data-ttu-id="b6f55-139">APIs de configuração</span><span class="sxs-lookup"><span data-stu-id="b6f55-139">Configuration APIs</span></span>

### <span data-ttu-id="b6f55-140">Requisitos do cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-140">AGPM Client requirements</span></span>

<span data-ttu-id="b6f55-141">O cliente do AGPM 3.0 requer o Windows Server2008 ou o WindowsVista com Service Pack 1 e o GPMC a partir de ferramentas de administração de servidor remoto (RSAT) instaladas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="b6f55-142">Há suporte para as duas versões de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b6f55-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="b6f55-143">O cliente do AGPM pode ser instalado em um computador que esteja executando o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="b6f55-144">Os seguintes recursos do Windows são necessários para o cliente do AGPM e serão instalados automaticamente se não forem apresentados, a menos que seja observado o contrário:</span><span class="sxs-lookup"><span data-stu-id="b6f55-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="b6f55-145">GPMC</span><span class="sxs-lookup"><span data-stu-id="b6f55-145">GPMC</span></span>

    -   <span data-ttu-id="b6f55-146">Windows Server 2008: o GPMC será instalado automaticamente pelo AGPM, se não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="b6f55-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="b6f55-147">Windows Vista: você deve instalar o GPMC a partir do RSAT antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="b6f55-148">Para obter mais informações, consulte <https://go.microsoft.com/fwlink/?LinkID=116179> .</span><span class="sxs-lookup"><span data-stu-id="b6f55-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="b6f55-149">.NET Framework 3,0</span><span class="sxs-lookup"><span data-stu-id="b6f55-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="b6f55-150">Requisitos do cenário</span><span class="sxs-lookup"><span data-stu-id="b6f55-150">Scenario requirements</span></span>

<span data-ttu-id="b6f55-151">Antes de iniciar esse cenário, crie quatro contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="b6f55-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="b6f55-152">Durante o cenário, você atribuirá uma das seguintes funções do AGPM a cada uma dessas contas: administrador do AGPM (controle total), Aprovador, editor e revisor.</span><span class="sxs-lookup"><span data-stu-id="b6f55-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="b6f55-153">Essas contas devem ser capazes de enviar e receber mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="b6f55-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="b6f55-154">Atribua a permissão de **vincular GPOs** às contas com as funções do editor do administrador do AGPM, Aprovador e (opcionalmente).</span><span class="sxs-lookup"><span data-stu-id="b6f55-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="b6f55-155">**Observação** 
 A permissão **vincular GPOs** é atribuída a membros de administradores de domínio e administradores corporativos por padrão.</span><span class="sxs-lookup"><span data-stu-id="b6f55-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="b6f55-156">Para atribuir permissões de **GPOs de link** a usuários ou grupos adicionais (como contas com funções de administrador ou aprovador do AGPM), clique no nó do domínio e, em seguida, clique na guia **delegação** , selecione **vincular GPOs**, clique em **Adicionar**e selecione os usuários ou grupos aos quais atribuir a permissão.</span><span class="sxs-lookup"><span data-stu-id="b6f55-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="b6f55-157">Etapas para instalar e configurar o AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="b6f55-158">Você deve completar as etapas a seguir para instalar e configurar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="b6f55-159">Etapa 1: instalar o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="b6f55-160">Etapa 2: instalar o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="b6f55-161">Etapa 3: configurar uma conexão com o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="b6f55-162">Etapa 4: configurar a notificação por email</span><span class="sxs-lookup"><span data-stu-id="b6f55-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="b6f55-163">Etapa 5: delegar acesso</span><span class="sxs-lookup"><span data-stu-id="b6f55-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="b6f55-164">Etapa 1: instalar o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="b6f55-165">Nesta etapa, você instala o servidor do AGPM no servidor membro ou controlador de domínio que executará o serviço do AGPM e você poderá configurar o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b6f55-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="b6f55-166">Todas as operações do AGPM são gerenciadas por meio desse serviço do Windows e são executadas com as credenciais do serviço.</span><span class="sxs-lookup"><span data-stu-id="b6f55-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="b6f55-167">O arquivo gerenciado por um servidor do AGPM pode ser hospedado nesse servidor ou em outro servidor na mesma floresta.</span><span class="sxs-lookup"><span data-stu-id="b6f55-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="b6f55-168">Para instalar o servidor do AGPM no computador que irá hospedar o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="b6f55-169">Faça logon com uma conta que seja membro do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="b6f55-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="b6f55-170">Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **Advanced Group Policy Management-Server**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="b6f55-171">Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="b6f55-172">Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="b6f55-173">Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="b6f55-174">O computador no qual o servidor do AGPM está instalado hospedará o serviço do AGPM e gerenciará o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b6f55-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="b6f55-175">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-175">Click **Next**.</span></span>

6.  <span data-ttu-id="b6f55-176">Na caixa de diálogo **caminho do arquivo morto** , selecione um local para o arquivo morto relativo ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="b6f55-177">O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas você deve selecionar um local com espaço suficiente para armazenar todos os GPOs e dados do histórico gerenciados por esse servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="b6f55-178">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-178">Click **Next**.</span></span>

7.  <span data-ttu-id="b6f55-179">Na caixa de diálogo **conta de serviço do AGPM** , selecione uma conta de serviço na qual o serviço do AGPM será executado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="b6f55-180">Na caixa de diálogo **proprietário do arquivo** , selecione uma conta ou grupo à qual atribuir inicialmente a função de administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="b6f55-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="b6f55-181">Esse administrador do AGPM pode atribuir funções do AGPM e permissões a outros administradores de política de grupo (incluindo a função de administrador do AGPM).</span><span class="sxs-lookup"><span data-stu-id="b6f55-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="b6f55-182">Para esse cenário, selecione a conta a ser usada na função de administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="b6f55-183">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-183">Click **Next**.</span></span>

9.  <span data-ttu-id="b6f55-184">Na caixa de diálogo **configuração de portabilidade** , digite uma porta na qual o serviço do AGPM deve escutar.</span><span class="sxs-lookup"><span data-stu-id="b6f55-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="b6f55-185">Não desmarque a caixa de seleção **Adicionar exceção de porta ao firewall** , a menos que você configure manualmente exceções de porta ou use regras para configurar exceções de porta.</span><span class="sxs-lookup"><span data-stu-id="b6f55-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="b6f55-186">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-186">Click **Next**.</span></span>

10. <span data-ttu-id="b6f55-187">Na caixa de diálogo **idiomas** , selecione um ou mais idiomas de exibição para instalar no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="b6f55-188">Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="b6f55-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="b6f55-189">**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b6f55-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="b6f55-190">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="b6f55-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="b6f55-191">Para saber mais sobre como modificar as configurações do serviço, confira ajuda para gerenciamento avançado de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="b6f55-192">Etapa 2: instalar o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="b6f55-193">Cada administrador da política de grupo — qualquer pessoa que cria, edita, implanta, revisa ou exclui GPOs — deve ter o cliente do AGPM instalado em computadores que eles usam para gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="b6f55-194">Para esse cenário, instale o cliente do AGPM em pelo menos um computador.</span><span class="sxs-lookup"><span data-stu-id="b6f55-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="b6f55-195">Você não precisa instalar o cliente do AGPM nos computadores dos usuários finais que não executam a administração da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="b6f55-196">Para instalar o cliente do AGPM no computador de um administrador de política de grupo</span><span class="sxs-lookup"><span data-stu-id="b6f55-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="b6f55-197">Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **gerenciamento avançado de política de grupo-cliente**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="b6f55-198">Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="b6f55-199">Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="b6f55-200">Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="b6f55-201">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-201">Click **Next**.</span></span>

5.  <span data-ttu-id="b6f55-202">Na caixa de diálogo **servidor do AGPM** , digite o nome do computador totalmente qualificado para o servidor do AGPM e a porta à qual deseja se conectar.</span><span class="sxs-lookup"><span data-stu-id="b6f55-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="b6f55-203">A porta padrão do serviço do AGPM é 4600.</span><span class="sxs-lookup"><span data-stu-id="b6f55-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="b6f55-204">Não desmarque a caixa de seleção **permitir o console de gerenciamento da Microsoft por meio do firewall** , a menos que você configure manualmente exceções de porta ou use regras para configurar exceções de porta.</span><span class="sxs-lookup"><span data-stu-id="b6f55-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="b6f55-205">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-205">Click **Next**.</span></span>

6.  <span data-ttu-id="b6f55-206">Na caixa de diálogo **idiomas** , selecione um ou mais idiomas de exibição para instalar para o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="b6f55-207">Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="b6f55-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="b6f55-208">Etapa 3: configurar uma conexão com o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="b6f55-209">O AGPM armazena todas as versões de cada objeto de política de grupo (GPO) controlado — um GPO para o qual o AGPM fornece controle de alterações — em um arquivo central, para que os administradores de política de grupo possam exibir e modificar os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="b6f55-210">Nesta etapa, você configura uma conexão do servidor do AGPM e garante que todos os administradores de política de grupo se conectam ao mesmo servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="b6f55-211">(Para obter informações sobre como configurar vários servidores de AGPM, consulte a ajuda para gerenciamento avançado de política de grupo.)</span><span class="sxs-lookup"><span data-stu-id="b6f55-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="b6f55-212">Para configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="b6f55-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="b6f55-213">Em um computador no qual você instalou o cliente do AGPM, faça logon com a conta de usuário selecionada como o proprietário do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="b6f55-214">Esse usuário tem a função de administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="b6f55-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="b6f55-215">Clique em **Iniciar**, aponte para **Ferramentas administrativas**e clique em **Gerenciamento de política de grupo** para abrir o GPMC.</span><span class="sxs-lookup"><span data-stu-id="b6f55-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="b6f55-216">Editar um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="b6f55-217">Na janela **Editor de gerenciamento de política de grupo** , clique duas vezes em **configuração do usuário**, **políticas**, **modelos administrativos**, **componentes do Windows**e **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="b6f55-218">No painel detalhes, clique duas vezes em **AGPM: especifique o servidor do AGPM padrão (todos os domínios)**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="b6f55-219">Na janela **Propriedades** , selecione **habilitado** e digite o nome do computador e a porta totalmente qualificados (por exemplo, **Server.contoso.com:4600**) para o servidor que hospeda o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b6f55-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="b6f55-220">Por padrão, o serviço do AGPM usa a porta 4600.</span><span class="sxs-lookup"><span data-stu-id="b6f55-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="b6f55-221">Clique em **OK**e feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="b6f55-222">Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="b6f55-223">Etapa 4: configurar a notificação por email</span><span class="sxs-lookup"><span data-stu-id="b6f55-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="b6f55-224">Como administrador do AGPM (controle total), você designa os endereços de email de aprovadores e administradores do AGPM para quem uma mensagem de email contendo uma solicitação é enviada quando um editor tenta criar, implantar ou excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="b6f55-225">Você também pode determinar o alias do qual essas mensagens são enviadas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="b6f55-226">Para configurar a notificação por email para o AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="b6f55-227">No painel de detalhes, clique na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="b6f55-228">No campo **do endereço de email** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="b6f55-229">No campo **endereço de email para** , digite o endereço de email da conta de usuário à qual você pretende atribuir a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="b6f55-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="b6f55-230">No campo **servidor SMTP** , digite um servidor de email SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="b6f55-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="b6f55-231">Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário com acesso ao serviço SMTP.</span><span class="sxs-lookup"><span data-stu-id="b6f55-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="b6f55-232">Clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="b6f55-233">Etapa 5: delegar acesso</span><span class="sxs-lookup"><span data-stu-id="b6f55-233">Step 5: Delegate access</span></span>

<span data-ttu-id="b6f55-234">Como administrador do AGPM (controle total), você delega o acesso no nível do domínio aos GPOs, atribuindo funções à conta de cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="b6f55-235">**Observação**  Você também pode delegar o acesso no nível do GPO em vez do nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="b6f55-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="b6f55-236">Para obter detalhes, consulte ajuda para gerenciamento avançado de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="b6f55-237">**Importante**  Você deve restringir a participação no grupo proprietários criadores de política de grupo, portanto, não pode ser usado para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="b6f55-238">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="b6f55-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="b6f55-239">Para delegar o acesso a todos os GPOs em um domínio</span><span class="sxs-lookup"><span data-stu-id="b6f55-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="b6f55-240">Na guia **delegação de domínio** , clique no botão **Adicionar** , selecione a conta de usuário do administrador de política de grupo para atuar como Aprovador e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="b6f55-241">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione a função **Aprovador** para atribuir a função à conta e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="b6f55-242">(Essa função inclui a função de revisor.)</span><span class="sxs-lookup"><span data-stu-id="b6f55-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="b6f55-243">Clique no botão **Adicionar** , selecione a conta de usuário do administrador de política de grupo para atuar como editor e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="b6f55-244">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione a função de **Editor** para atribuir a função à conta e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="b6f55-245">(Essa função inclui a função de revisor.)</span><span class="sxs-lookup"><span data-stu-id="b6f55-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="b6f55-246">Clique no botão **Adicionar** , selecione a conta de usuário do administrador de política de grupo para atuar como revisor e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="b6f55-247">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione a função **revisor** para atribuir apenas essa função à conta.</span><span class="sxs-lookup"><span data-stu-id="b6f55-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="b6f55-248">Etapas para gerenciar GPOs</span><span class="sxs-lookup"><span data-stu-id="b6f55-248">Steps for managing GPOs</span></span>


<span data-ttu-id="b6f55-249">Você deve completar as etapas a seguir para criar, editar, revisar e implantar GPOs usando o AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="b6f55-250">Além disso, você criará um modelo, excluirá um GPO e restaurará um GPO excluído.</span><span class="sxs-lookup"><span data-stu-id="b6f55-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="b6f55-251">Etapa 1: criar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="b6f55-252">Etapa 2: editar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="b6f55-253">Etapa 3: revisar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="b6f55-254">Etapa 4: usar um modelo para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="b6f55-255">Etapa 5: excluir e restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="b6f55-256">Etapa 1: criar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="b6f55-257">Em um ambiente com vários administradores de política de grupo, aqueles com a função editor têm a capacidade de solicitar a criação de novos GPOs, mas essa solicitação deve ser aprovada por alguém com a função de aprovador porque a criação de um novo GPO impacta o ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="b6f55-258">Nesta etapa, você usa uma conta com a função de editor para solicitar a criação de um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="b6f55-259">Usando uma conta com a função Aprovador, você aprova essa solicitação e conclui a criação de um GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="b6f55-260">Para solicitar a criação de um novo GPO gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="b6f55-261">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="b6f55-262">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b6f55-263">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="b6f55-264">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="b6f55-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="b6f55-265">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="b6f55-266">Digite **MyGPO** como o nome do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="b6f55-267">Digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="b6f55-268">Clique em **criar ao vivo** para que o novo GPO seja implantado para o ambiente de produção imediatamente após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="b6f55-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="b6f55-269">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="b6f55-270">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-271">O novo GPO será exibido na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="b6f55-272">Para aprovar a solicitação pendente para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="b6f55-273">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de aprovador no AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="b6f55-274">Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com a solicitação do editor para criar um GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="b6f55-275">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="b6f55-276">Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.</span><span class="sxs-lookup"><span data-stu-id="b6f55-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="b6f55-277">Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="b6f55-278">Clique em **Sim** para confirmar a aprovação da criação do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="b6f55-279">O GPO será movido para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="b6f55-280">Etapa 2: editar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="b6f55-281">Você pode usar GPOs para configurar o computador ou o usuário e implantá-los em muitos computadores ou usuários.</span><span class="sxs-lookup"><span data-stu-id="b6f55-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="b6f55-282">Nesta etapa, você usa uma conta com a função de editor para fazer check-out de um GPO do arquivo, editar o GPO offline, verificar o GPO editado no arquivo morto e solicitar a implantação do GPO ao ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="b6f55-283">Nesse cenário, você define uma configuração no GPO para exigir que a senha tenha pelo menos oito caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="b6f55-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="b6f55-284">Para fazer check-out do GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="b6f55-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="b6f55-285">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="b6f55-286">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b6f55-287">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="b6f55-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="b6f55-288">Clique com o botão direito do mouse em **MyGPO**e clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="b6f55-289">Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="b6f55-290">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-291">Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="b6f55-292">Para editar o GPO offline e configurar o tamanho mínimo da senha</span><span class="sxs-lookup"><span data-stu-id="b6f55-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="b6f55-293">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de gerenciamento de política de grupo** e fazer alterações em uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="b6f55-294">Para esse cenário, configure o tamanho mínimo da senha:</span><span class="sxs-lookup"><span data-stu-id="b6f55-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="b6f55-295">Em **configuração do computador**, clique duas vezes em **políticas**, **configurações do Windows**, configurações de **segurança**, **políticas de conta**e **política de senha**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="b6f55-296">No painel de detalhes, clique duas vezes em **tamanho mínimo da senha**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="b6f55-297">Na janela Propriedades, marque a caixa de seleção **definir esta configuração de política** , defina o número de caracteres para **8**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="b6f55-298">Feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="b6f55-299">Para verificar o GPO no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="b6f55-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="b6f55-300">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **check-in**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="b6f55-301">Digite um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="b6f55-302">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-303">Na guia **controlado** , o estado do GPO é identificado como **checked-in**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="b6f55-304">Para solicitar a implantação do GPO ao ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="b6f55-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="b6f55-305">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **implantar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="b6f55-306">Como essa conta não é um Aprovador ou administrador do AGPM, você deve enviar uma solicitação de implantação.</span><span class="sxs-lookup"><span data-stu-id="b6f55-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="b6f55-307">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="b6f55-308">Digite um comentário a ser exibido no histórico do GPO e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="b6f55-309">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-310">**MyGPO** é exibido na lista de GPOs na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="b6f55-311">Etapa 3: revisar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="b6f55-312">Nesta etapa, você atua como Aprovador, criando relatórios e analisando as configurações e alterando as configurações no GPO para determinar se devem ser aprovadas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="b6f55-313">Depois de avaliar o GPO, implante-o no ambiente de produção e vincule-o a um domínio ou a uma UO (unidade organizacional) para que ele tenha efeito quando a política de grupo for atualizada para computadores nesse domínio ou unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="b6f55-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="b6f55-314">Para revisar as configurações no GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="b6f55-315">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de aprovador no AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="b6f55-316">(Qualquer administrador de política de grupo com a função revisor, que está incluído em todas as outras funções, pode revisar as configurações em um GPO.)</span><span class="sxs-lookup"><span data-stu-id="b6f55-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="b6f55-317">Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com uma solicitação de editor para implantar um GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="b6f55-318">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="b6f55-319">Na guia **conteúdo** do painel detalhes, clique na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="b6f55-320">Clique duas vezes em **MyGPO** para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="b6f55-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="b6f55-321">Examine as configurações na versão mais recente do MyGPO:</span><span class="sxs-lookup"><span data-stu-id="b6f55-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="b6f55-322">Na janela do **histórico** , clique com o botão direito do mouse na versão do GPO com o carimbo de data e hora mais recente, clique em **configurações**e, em seguida, clique em **relatório HTML** para exibir um resumo das configurações do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="b6f55-323">No navegador da Web, clique em **Mostrar tudo** para exibir todas as configurações no GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="b6f55-324">Feche a janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="b6f55-324">Close the browser.</span></span>

7. <span data-ttu-id="b6f55-325">Compare a versão mais recente do MyGPO com a primeira versão verificada no arquivo morto:</span><span class="sxs-lookup"><span data-stu-id="b6f55-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="b6f55-326">Na janela do **histórico** , clique na versão do GPO com o carimbo de data/hora mais recente.</span><span class="sxs-lookup"><span data-stu-id="b6f55-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="b6f55-327">Pressione CTRL e clique na versão mais antiga do GPO para a qual a **versão do computador** não é \* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="b6f55-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="b6f55-328">Clique no botão **diferenças** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-328">Click the **Differences** button.</span></span> <span data-ttu-id="b6f55-329">A seção **políticas de conta/política de senha** é realçada em verde e precedida por **\ [+ \]**, indicando que essa configuração é definida somente na versão mais recente do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="b6f55-330">Clique em **políticas de conta/política de senha**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="b6f55-331">A configuração **comprimento mínimo da senha** também é realçada em verde e precedida por **\ [+ \]**, indicando que ela está configurada somente na última versão do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="b6f55-332">Fechar o navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="b6f55-332">Close the Web browser.</span></span>

**<span data-ttu-id="b6f55-333">Para implantar o GPO no ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="b6f55-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="b6f55-334">Na guia **pendente** , clique com o botão direito do mouse em **MyGPO** e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="b6f55-335">Digite um comentário para incluir no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="b6f55-336">Clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-336">Click **Yes**.</span></span> <span data-ttu-id="b6f55-337">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-338">O GPO é implantado no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="b6f55-339">Para vincular o GPO a um domínio ou unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="b6f55-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="b6f55-340">No GPMC, clique com o botão direito do mouse no domínio ou em uma UO à qual deseja aplicar o GPO que você configurou e clique em **vincular um GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="b6f55-341">Na caixa de diálogo **selecionar GPO** , clique em **MyGPO**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="b6f55-342">Etapa 4: usar um modelo para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="b6f55-343">Nesta etapa, você usa uma conta com a função de editor para criar um modelo, uma versão estática e não editável de um GPO para uso como ponto de partida para a criação de novos GPOs e, em seguida, cria um novo GPO com base nesse modelo.</span><span class="sxs-lookup"><span data-stu-id="b6f55-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="b6f55-344">Os modelos são úteis para criar rapidamente vários GPOs que incluam muitas das mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="b6f55-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="b6f55-345">Para criar um modelo com base em um GPO existente</span><span class="sxs-lookup"><span data-stu-id="b6f55-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="b6f55-346">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="b6f55-347">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b6f55-348">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="b6f55-349">Clique com o botão direito do mouse em **MyGPO**e clique em **salvar como modelo** para criar um modelo que incorpora todas as configurações no MyGPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="b6f55-350">Digite **MyTemplate** como o nome do modelo e um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="b6f55-351">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-352">O novo modelo aparece na guia **modelos** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="b6f55-353">Para solicitar a criação de um novo GPO gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="b6f55-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="b6f55-354">Clique na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="b6f55-355">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="b6f55-356">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="b6f55-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="b6f55-357">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="b6f55-358">Digite **MyOtherGPO** como o nome do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="b6f55-359">Digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="b6f55-360">Clique em **criar ao vivo**, portanto, o novo GPO será implantado para o ambiente de produção imediatamente após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="b6f55-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="b6f55-361">Em **modelo de GPO**, selecione **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="b6f55-362">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="b6f55-363">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-364">O novo GPO será exibido na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="b6f55-365">Use uma conta que tenha sido atribuída à função de aprovador para aprovar a solicitação pendente para criar o GPO da mesma forma que você fez na [etapa 1: criar um GPO](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="b6f55-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="b6f55-366">MyTemplate incorpora todas as configurações que você configurou no MyGPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="b6f55-367">Como o MyOtherGPO foi criado usando MyTemplate, inicialmente ele contém todas as configurações que MyGPO contidas no momento em que MyTemplate foi criado.</span><span class="sxs-lookup"><span data-stu-id="b6f55-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="b6f55-368">Você pode confirmar isso gerando um relatório de diferença para comparar MyOtherGPO ao MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="b6f55-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="b6f55-369">Para fazer check-out do GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="b6f55-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="b6f55-370">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="b6f55-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="b6f55-371">Clique com o botão direito do mouse em **MyOtherGPO**e clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="b6f55-372">Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="b6f55-373">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-374">Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="b6f55-375">Para editar o GPO offline e configurar a duração do bloqueio de conta</span><span class="sxs-lookup"><span data-stu-id="b6f55-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="b6f55-376">Na guia **controlado** , clique com o botão direito do mouse em **MyOtherGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de gerenciamento de política de grupo** e fazer alterações em uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="b6f55-377">Para esse cenário, configure o tamanho mínimo da senha:</span><span class="sxs-lookup"><span data-stu-id="b6f55-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="b6f55-378">Em **configuração do computador**, clique duas vezes em **políticas**, **configurações do Windows**, **configurações de segurança**, políticas de **conta**e política de **bloqueio de conta**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="b6f55-379">No painel de detalhes, clique duas vezes em **duração do bloqueio de conta**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="b6f55-380">Na janela Propriedades, marque **definir esta configuração de política**, defina a duração como **30** minutos e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="b6f55-381">Feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="b6f55-382">Verifique MyOtherGPO no arquivo morto e solicite a implantação como você fez para o MyGPO na [etapa 2: editar um GPO](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="b6f55-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="b6f55-383">Você pode comparar o MyOtherGPO ao MyGPO ou ao MyTemplate usando relatórios de diferença.</span><span class="sxs-lookup"><span data-stu-id="b6f55-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="b6f55-384">Qualquer conta que inclua a função de Revisor (administrador do AGPM \ [controle total \], Aprovador, editor ou revisor) pode gerar relatórios.</span><span class="sxs-lookup"><span data-stu-id="b6f55-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="b6f55-385">Para comparar um GPO a outro GPO e a um modelo</span><span class="sxs-lookup"><span data-stu-id="b6f55-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="b6f55-386">Para comparar o MyGPO e o MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="b6f55-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="b6f55-387">Na guia **controlado** , clique em **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="b6f55-388">Pressione CTRL e clique em **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="b6f55-389">Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **relatório HTML**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="b6f55-390">Para comparar MyOtherGPO e MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="b6f55-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="b6f55-391">Na guia **controlado** , clique em **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="b6f55-392">Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **modelo**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="b6f55-393">Selecione meu **modelo** e **relatório HTML**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="b6f55-394">Etapa 5: excluir e restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="b6f55-395">Nesta etapa, você atua como um Aprovador para excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="b6f55-396">Para excluir um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="b6f55-397">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha atribuído a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="b6f55-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="b6f55-398">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b6f55-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b6f55-399">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="b6f55-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="b6f55-400">Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="b6f55-401">Clique em **excluir GPO do arquivo e da produção** para excluir a versão no arquivo e a versão implantada do GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="b6f55-402">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="b6f55-403">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-404">O GPO é removido da guia **controlado** e é exibido na guia **Lixeira** , onde ele pode ser restaurado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="b6f55-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="b6f55-405">Às vezes, você pode descobrir depois de excluir um GPO que ainda é necessário.</span><span class="sxs-lookup"><span data-stu-id="b6f55-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="b6f55-406">Nesta etapa, você atua como um Aprovador para restaurar um GPO que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="b6f55-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="b6f55-407">Para restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="b6f55-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="b6f55-408">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="b6f55-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="b6f55-409">Clique com o botão direito do mouse em **MyGPO**e clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="b6f55-410">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="b6f55-411">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-412">O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="b6f55-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="b6f55-413">**Observação**  Restaurar um GPO para o arquivo não o reimplanta automaticamente no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b6f55-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="b6f55-414">Para retornar o GPO ao ambiente de produção, implante o GPO da [etapa 3: revise e implante um GPO](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="b6f55-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="b6f55-415">Depois de editar e implantar um GPO, você pode descobrir que alterações recentes no GPO estão causando um problema.</span><span class="sxs-lookup"><span data-stu-id="b6f55-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="b6f55-416">Nesta etapa, você atua como um Aprovador para reverter para uma versão anterior do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="b6f55-417">Você pode reverter para qualquer versão do histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="b6f55-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="b6f55-418">Você pode usar comentários e rótulos para identificar versões válidas conhecidas e quando foram feitas alterações específicas.</span><span class="sxs-lookup"><span data-stu-id="b6f55-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="b6f55-419">Para reverter para uma versão anterior de um GPO</span><span class="sxs-lookup"><span data-stu-id="b6f55-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="b6f55-420">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="b6f55-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="b6f55-421">Clique duas vezes em **MyGPO** para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="b6f55-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="b6f55-422">Clique com o botão direito do mouse na versão a ser implantada, clique em **implantar**e, em seguida, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="b6f55-423">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b6f55-424">Na janela do **histórico** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="b6f55-425">**Observação**  Para verificar se a versão que foi reimplementada é a versão pretendida, examine um relatório de diferença para as duas versões.</span><span class="sxs-lookup"><span data-stu-id="b6f55-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="b6f55-426">Na janela do **histórico** do GPO, selecione as duas versões, clique com o botão direito do mouse nelas, aponte para **diferença**e clique em **relatório HTML** ou **relatório XML**.</span><span class="sxs-lookup"><span data-stu-id="b6f55-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





