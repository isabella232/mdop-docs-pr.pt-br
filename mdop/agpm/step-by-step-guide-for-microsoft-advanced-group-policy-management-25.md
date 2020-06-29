---
title: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft
description: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797676"
---
# <span data-ttu-id="7ac20-103">Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ac20-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="7ac20-104">Este guia passo a passo demonstra técnicas avançadas de gerenciamento de política de grupo usando o console de gerenciamento de política de grupo (GPMC) e o gerenciamento avançado de política de grupo (AGPM) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ac20-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="7ac20-105">O AGPM aumenta a funcionalidade do GPMC, fornecendo:</span><span class="sxs-lookup"><span data-stu-id="7ac20-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="7ac20-106">Funções padrão para delegar permissões para gerenciar GPOs (objetos de política de grupo) para vários administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="7ac20-107">Um arquivo morto para permitir que os administradores de política de grupo criem e modifiquem os GPOs offline antes de implantá-los em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="7ac20-108">A capacidade de reverter para qualquer versão anterior de um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="7ac20-109">Funcionalidade de check-in/check-out para os GPOs para garantir que os administradores de política de grupo não substituam acidentalmente o trabalho uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="7ac20-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="7ac20-110">Visão geral do cenário do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-110">AGPM scenario overview</span></span>


<span data-ttu-id="7ac20-111">Para esse cenário, você usará uma conta de usuário separada para cada função no AGPM para demonstrar como a política de grupo pode ser gerenciada em um ambiente com vários administradores de política de grupo com diferentes níveis de permissões.</span><span class="sxs-lookup"><span data-stu-id="7ac20-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="7ac20-112">Especificamente, você vai executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="7ac20-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="7ac20-113">Usando uma conta que seja membro do grupo Domain admins, instale o servidor do AGPM e atribua a função de administrador do AGPM a uma conta ou grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="7ac20-114">Usando contas às quais você atribuirá funções do AGPM, instale o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="7ac20-115">Usar uma conta com a função de administrador do AGPM, configurar o AGPM e o acesso de representante a GPOs atribuindo funções a outras contas.</span><span class="sxs-lookup"><span data-stu-id="7ac20-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="7ac20-116">Usando uma conta com a função editor, solicite a criação de um GPO, que você Então aprova usando uma conta com a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="7ac20-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="7ac20-117">Com a conta editor, verifique o GPO do arquivo morto, edite o GPO, verifique o GPO no arquivo e solicite a implantação.</span><span class="sxs-lookup"><span data-stu-id="7ac20-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="7ac20-118">Usando uma conta com a função Aprovador, examine o GPO e implante-o em seu ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="7ac20-119">Usando uma conta com a função editor, crie um modelo de GPO e use-o como ponto de partida para criar um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="7ac20-120">Usar uma conta com a função Aprovador, excluir e restaurar um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![processo de desenvolvimento de objetos de política de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="7ac20-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ac20-122">Requirements</span></span>


<span data-ttu-id="7ac20-123">Os computadores em que você deseja instalar o AGPM devem atender aos seguintes requisitos, e você deve criar contas para uso nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="7ac20-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="7ac20-124">Requisitos do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-124">AGPM Server requirements</span></span>

<span data-ttu-id="7ac20-125">O servidor do AGPM 2.5 requer o WindowsVista® (versão de 32 bits) sem Service Packs instalados ou Windows Server® 2003 (versão de 32 bits), bem como o GPMC.</span><span class="sxs-lookup"><span data-stu-id="7ac20-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="7ac20-126">Além disso, você deve ser membro do grupo Domain admins para instalar o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="7ac20-127">Você deve instalar o servidor do AGPM em um servidor membro ou controlador de domínio com a versão mais recente do GPMC que está disponível para você e com o suporte do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="7ac20-128">O AGPM usa o GPMC para fazer backup e restaurar GPOs, e as versões mais recentes do GPMC fornecem configurações de política adicionais não disponíveis nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7ac20-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="7ac20-129">Se a versão do GPMC em seu servidor do AGPM for mais antiga do que a versão nos computadores que os administradores usam para gerenciar a política de grupo, o servidor do AGPM não poderá armazenar essas configurações de política não estarão disponíveis na versão anterior do GPMC.</span><span class="sxs-lookup"><span data-stu-id="7ac20-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="7ac20-130">Especificamente, se o seu servidor do AGPM estiver executando o Windows Server2003 e a versão do GPMC que o acompanha, e os computadores dos administradores de política de grupo estiverem executando o WindowsVista e a versão do GPMC que o acompanha, você ainda poderá gerenciar a maioria das configurações de política.</span><span class="sxs-lookup"><span data-stu-id="7ac20-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="7ac20-131">No entanto, as configurações de política do GPMC no Windows Vista que não estão disponíveis no GPMC no Windows Server 2003, como aquelas relacionadas ao redirecionamento de pastas, à rede sem fio (IEEE 802,11) e às impressoras implantadas, não podem ser armazenadas pelo servidor do AGPM, mesmo que os administradores possam configurá-las usando o AGPM em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="7ac20-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="7ac20-132">Se você precisar instalar o servidor do AGPM em um computador com uma versão mais antiga do GPMC do que os administradores de política de grupo estão em execução, consulte a referência de configurações da política de grupo para obter detalhes sobre quais configurações de política estão disponíveis com quais sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="7ac20-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="7ac20-133">Para baixar a referência de configurações de política de grupo, consulte <https://go.microsoft.com/fwlink/?LinkID=106147> .</span><span class="sxs-lookup"><span data-stu-id="7ac20-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="7ac20-134">**Observação**  Não é possível migrar arquivos de um servidor do AGPM ou um servidor do GPOVault que executa o Windows Server2003 para um servidor do AGPM executando o WindowsVista.</span><span class="sxs-lookup"><span data-stu-id="7ac20-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="7ac20-135">Para o Windows Server2003, se o GPOVault Server estiver instalado no computador em que você deseja instalar o servidor do AGPM, é recomendável que você não desinstale o GPOVault Server antes de começar a instalação.</span><span class="sxs-lookup"><span data-stu-id="7ac20-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="7ac20-136">A instalação do servidor do AGPM desinstalará o GPOVault Server e transferirá automaticamente os dados de arquivo morto existentes do GPOVault para um arquivo do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="7ac20-137">Requisitos do cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-137">AGPM Client requirements</span></span>

<span data-ttu-id="7ac20-138">O cliente do AGPM 2.5 requer o WindowsVista (versão de 32 bits) sem Service Packs instalados ou Windows Server2003 (versão de 32 bits), bem como o GPMC.</span><span class="sxs-lookup"><span data-stu-id="7ac20-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="7ac20-139">O cliente do AGPM pode ser instalado em um computador que esteja executando o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="7ac20-140">Requisitos do cenário</span><span class="sxs-lookup"><span data-stu-id="7ac20-140">Scenario requirements</span></span>

<span data-ttu-id="7ac20-141">Antes de iniciar esse cenário, crie quatro contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="7ac20-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="7ac20-142">Durante o cenário, você atribuirá uma das seguintes funções do AGPM a cada uma dessas contas: administrador do AGPM (controle total), Aprovador, editor e revisor.</span><span class="sxs-lookup"><span data-stu-id="7ac20-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="7ac20-143">Essas contas devem ser capazes de enviar e receber mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="7ac20-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="7ac20-144">Atribua a permissão de **vincular GPOs** às contas com as funções do editor do administrador do AGPM, Aprovador e (opcionalmente).</span><span class="sxs-lookup"><span data-stu-id="7ac20-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="7ac20-145">**Observação** 
 A permissão **vincular GPOs** é atribuída a membros de administradores de domínio e administradores corporativos por padrão.</span><span class="sxs-lookup"><span data-stu-id="7ac20-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="7ac20-146">Para atribuir permissões de **GPOs de link** a usuários ou grupos adicionais (como contas com funções de administrador ou aprovador do AGPM), clique no nó do domínio e, em seguida, clique na guia **delegação** , selecione **vincular GPOs**, clique em **Adicionar**e selecione os usuários ou grupos aos quais atribuir a permissão.</span><span class="sxs-lookup"><span data-stu-id="7ac20-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="7ac20-147">Para esse cenário, você executa ações com contas diferentes.</span><span class="sxs-lookup"><span data-stu-id="7ac20-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="7ac20-148">Você pode fazer logon com cada conta conforme indicado ou pode usar o comando **Executar como** para iniciar o GPMC com a conta indicada.</span><span class="sxs-lookup"><span data-stu-id="7ac20-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="7ac20-149">**Observação**  Para usar o comando **Executar como** com o GPMC no Windows Server2003, clique em **Iniciar**, aponte para **Ferramentas administrativas**, clique com o botão direito do mouse em **Gerenciamento de política de grupo**e clique em **Executar como**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="7ac20-150">Clique **no seguinte usuário** e insira as credenciais de uma conta.</span><span class="sxs-lookup"><span data-stu-id="7ac20-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="7ac20-151">Para usar o comando **Executar como** com o GPMC no Windows Vista, clique no botão **Iniciar** , aponte para **executar**e digite **runas/User:** <em> DomainName\\UserName </em> **"mmc%windir%\\system32\\gpmc.msc"** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="7ac20-152">Digite a senha da conta quando for solicitado.</span><span class="sxs-lookup"><span data-stu-id="7ac20-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="7ac20-153">Etapas para instalar e configurar o AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="7ac20-154">Você deve completar as etapas a seguir para instalar e configurar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="7ac20-155">Etapa 1: instalar o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="7ac20-156">Etapa 2: instalar o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="7ac20-157">Etapa 3: configurar uma conexão com o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="7ac20-158">Etapa 4: configurar a notificação por email</span><span class="sxs-lookup"><span data-stu-id="7ac20-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="7ac20-159">Etapa 5: delegar acesso</span><span class="sxs-lookup"><span data-stu-id="7ac20-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="7ac20-160">Etapa 1: instalar o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="7ac20-161">Nesta etapa, você instala o servidor do AGPM no servidor membro ou controlador de domínio que executará o serviço do AGPM e você poderá configurar o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="7ac20-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="7ac20-162">Todas as operações do AGPM são gerenciadas por meio desse serviço do Windows e são executadas com as credenciais do serviço.</span><span class="sxs-lookup"><span data-stu-id="7ac20-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="7ac20-163">O arquivo gerenciado por um servidor do AGPM pode ser hospedado nesse servidor ou em outro servidor na mesma floresta.</span><span class="sxs-lookup"><span data-stu-id="7ac20-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="7ac20-164">Para instalar o servidor do AGPM no computador que irá hospedar o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="7ac20-165">Faça logon com uma conta que seja membro do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="7ac20-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="7ac20-166">Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **Advanced Group Policy Management-Server**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="7ac20-167">Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="7ac20-168">Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="7ac20-169">Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="7ac20-170">O computador no qual o servidor do AGPM está instalado hospedará o serviço do AGPM e gerenciará o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="7ac20-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="7ac20-171">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-171">Click **Next**.</span></span>

6.  <span data-ttu-id="7ac20-172">Na caixa de diálogo **caminho do arquivo morto** , selecione um local para o arquivo morto relativo ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="7ac20-173">O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas você deve selecionar um local com espaço suficiente para armazenar todos os GPOs e dados do histórico gerenciados por esse servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="7ac20-174">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-174">Click **Next**.</span></span>

7.  <span data-ttu-id="7ac20-175">Na caixa de diálogo **conta de serviço do AGPM** , selecione uma conta de serviço na qual o serviço do AGPM será executado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="7ac20-176">Na caixa de diálogo **proprietário do arquivo** , selecione uma conta ou grupo à qual atribuir inicialmente a função de administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="7ac20-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="7ac20-177">Esse administrador do AGPM pode atribuir funções do AGPM e permissões a outros administradores de política de grupo (incluindo a função de administrador do AGPM).</span><span class="sxs-lookup"><span data-stu-id="7ac20-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="7ac20-178">Para esse cenário, selecione a conta a ser usada na função de administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="7ac20-179">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-179">Click **Next**.</span></span>

9.  <span data-ttu-id="7ac20-180">Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="7ac20-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="7ac20-181">**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7ac20-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="7ac20-182">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="7ac20-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="7ac20-183">Para saber mais sobre como modificar as configurações do serviço, confira ajuda para gerenciamento avançado de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="7ac20-184">Etapa 2: instalar o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="7ac20-185">Cada administrador da política de grupo — qualquer pessoa que cria, edita, implanta, revisa ou exclui GPOs — deve ter o cliente do AGPM instalado em computadores que eles usam para gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="7ac20-186">Para esse cenário, instale o cliente do AGPM em pelo menos um computador.</span><span class="sxs-lookup"><span data-stu-id="7ac20-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="7ac20-187">Você não precisa instalar o cliente do AGPM nos computadores dos usuários finais que não executam a administração da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="7ac20-188">Para instalar o cliente do AGPM no computador de um administrador de política de grupo</span><span class="sxs-lookup"><span data-stu-id="7ac20-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="7ac20-189">Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **gerenciamento avançado de política de grupo-cliente**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="7ac20-190">Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="7ac20-191">Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="7ac20-192">Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="7ac20-193">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-193">Click **Next**.</span></span>

5.  <span data-ttu-id="7ac20-194">Na caixa de diálogo **servidor do AGPM** , digite o nome do computador totalmente qualificado e a porta do servidor do AGPM ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="7ac20-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="7ac20-195">A porta padrão do serviço do AGPM é 4600.</span><span class="sxs-lookup"><span data-stu-id="7ac20-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="7ac20-196">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-196">Click **Next**.</span></span>

6.  <span data-ttu-id="7ac20-197">Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="7ac20-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="7ac20-198">Etapa 3: configurar uma conexão com o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="7ac20-199">O AGPM armazena todas as versões de cada objeto de política de grupo (GPO) controlado — um GPO para o qual o AGPM fornece controle de alterações — em um arquivo central, para que os administradores de política de grupo possam exibir e modificar os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="7ac20-200">Nesta etapa, você configura uma conexão do servidor do AGPM e garante que todos os administradores de política de grupo se conectam ao mesmo servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="7ac20-201">(Para obter informações sobre como configurar vários servidores de AGPM, consulte a ajuda para gerenciamento avançado de política de grupo.)</span><span class="sxs-lookup"><span data-stu-id="7ac20-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="7ac20-202">Para configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="7ac20-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="7ac20-203">Em um computador no qual você instalou o cliente do AGPM, faça logon com a conta de usuário selecionada como o proprietário do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="7ac20-204">Esse usuário tem a função de administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="7ac20-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="7ac20-205">Clique em **Iniciar**, aponte para **Ferramentas administrativas**e clique em **Gerenciamento de política de grupo** para abrir o **GPMC (console de gerenciamento de política de grupo)**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="7ac20-206">Na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="7ac20-207">Na janela **Editor de objeto de política de grupo** , clique em **configuração do usuário**, **modelos administrativos**e **componentes do Windows**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="7ac20-208">Se o **AGPM** não estiver listado em **componentes do Windows**:</span><span class="sxs-lookup"><span data-stu-id="7ac20-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="7ac20-209">Clique com o botão direito do mouse em **modelos administrativos** e selecione **Adicionar/remover modelos**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="7ac20-210">Clique **em Adicionar**, selecione **AGPM. admx** ou **AGPM. adm**, clique em **abrir**e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="7ac20-211">Em **componentes do Windows**, clique duas vezes em **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="7ac20-212">No painel de detalhes, clique duas vezes em **servidor do AGPM (todos os domínios)**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="7ac20-213">Na janela de **Propriedades do servidor do AGPM (todos os domínios)** , selecione **habilitado** e digite o nome do computador e a porta totalmente qualificados (por exemplo, Server.contoso.com:4600) para o servidor que hospeda o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="7ac20-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="7ac20-214">A porta usada pelo serviço do AGPM é a porta 4600.</span><span class="sxs-lookup"><span data-stu-id="7ac20-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="7ac20-215">Clique em **OK**e feche a janela do **Editor de objeto de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="7ac20-216">Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="7ac20-217">Etapa 4: configurar a notificação por email</span><span class="sxs-lookup"><span data-stu-id="7ac20-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="7ac20-218">Como administrador do AGPM (controle total), você designa os endereços de email de aprovadores e administradores do AGPM para quem uma mensagem de email contendo uma solicitação é enviada quando um editor tenta criar, implantar ou excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="7ac20-219">Você também pode determinar o alias do qual essas mensagens são enviadas.</span><span class="sxs-lookup"><span data-stu-id="7ac20-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="7ac20-220">Para configurar a notificação por email para o AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="7ac20-221">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="7ac20-222">No painel de detalhes, clique na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="7ac20-223">No campo **de** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="7ac20-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="7ac20-224">No campo **para** , digite o endereço de email da conta de usuário à qual você pretende atribuir a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="7ac20-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="7ac20-225">No campo **servidor SMTP** , digite um servidor de email SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="7ac20-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="7ac20-226">Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário com acesso ao serviço SMTP.</span><span class="sxs-lookup"><span data-stu-id="7ac20-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="7ac20-227">Clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="7ac20-228">Etapa 5: delegar acesso</span><span class="sxs-lookup"><span data-stu-id="7ac20-228">Step 5: Delegate access</span></span>

<span data-ttu-id="7ac20-229">Como administrador do AGPM (controle total), você delega o acesso no nível do domínio aos GPOs, atribuindo funções à conta de cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="7ac20-230">**Observação**  Você também pode delegar o acesso no nível do GPO em vez do nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="7ac20-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="7ac20-231">Para obter detalhes, consulte ajuda para gerenciamento avançado de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="7ac20-232">**Importante**  Você deve restringir a participação no grupo proprietários criadores de política de grupo, portanto, não pode ser usado para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="7ac20-233">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="7ac20-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="7ac20-234">Para delegar o acesso a todos os GPOs em um domínio</span><span class="sxs-lookup"><span data-stu-id="7ac20-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="7ac20-235">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="7ac20-236">Na guia **delegação de domínio** , clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="7ac20-237">Na caixa de diálogo **permissões** :</span><span class="sxs-lookup"><span data-stu-id="7ac20-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="7ac20-238">Clique na conta de usuário de um administrador de política de grupo e marque a caixa de seleção **Aprovador** para atribuir essa função à conta.</span><span class="sxs-lookup"><span data-stu-id="7ac20-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="7ac20-239">Desmarque a caixa de seleção **Editor** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="7ac20-240">(Essa função inclui a função de revisor.)</span><span class="sxs-lookup"><span data-stu-id="7ac20-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="7ac20-241">Clique na conta de usuário de outro administrador de política de grupo e, em seguida, marque a caixa de seleção **Editor** para atribuir essa função à conta.</span><span class="sxs-lookup"><span data-stu-id="7ac20-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="7ac20-242">(Essa função inclui a função de revisor.)</span><span class="sxs-lookup"><span data-stu-id="7ac20-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="7ac20-243">Clique em uma terceira conta e marque a caixa **de seleção revisor para** atribuir apenas a função de revisor à conta desse administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="7ac20-244">Desmarque a caixa de seleção **Editor** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="7ac20-245">Clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="7ac20-246">Na caixa de diálogo **configurações de segurança avançadas** :</span><span class="sxs-lookup"><span data-stu-id="7ac20-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="7ac20-247">Selecione um administrador de política de grupo e, em seguida, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="7ac20-248">Em **aplicar**em, selecione **este objeto e objetos aninhados**e, em seguida, clique em **OK** na caixa de diálogo **entrada** de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="7ac20-249">Repita para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="7ac20-250">Na caixa de diálogo **configurações de segurança avançadas** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="7ac20-251">Na caixa de diálogo **permissões** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="7ac20-252">Etapas para gerenciar GPOs</span><span class="sxs-lookup"><span data-stu-id="7ac20-252">Steps for managing GPOs</span></span>


<span data-ttu-id="7ac20-253">Você deve completar as etapas a seguir para criar, editar, revisar e implantar GPOs usando o AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="7ac20-254">Além disso, você criará um modelo, excluirá um GPO e restaurará um GPO excluído.</span><span class="sxs-lookup"><span data-stu-id="7ac20-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="7ac20-255">Etapa 1: criar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="7ac20-256">Etapa 2: editar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="7ac20-257">Etapa 3: revisar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="7ac20-258">Etapa 4: usar um modelo para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="7ac20-259">Etapa 5: excluir e restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="7ac20-260">Etapa 1: criar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="7ac20-261">Em um ambiente com vários administradores de política de grupo, aqueles com a função editor têm a capacidade de solicitar a criação de novos GPOs, mas essa solicitação deve ser aprovada por alguém com a função de aprovador porque a criação de um novo GPO impacta o ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="7ac20-262">Nesta etapa, você usa uma conta com a função de editor para solicitar a criação de um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="7ac20-263">Usando uma conta com a função Aprovador, você aprova essa solicitação e conclui a criação de um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="7ac20-264">Para solicitar a criação de um novo GPO gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="7ac20-265">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="7ac20-266">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="7ac20-267">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="7ac20-268">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="7ac20-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="7ac20-269">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="7ac20-270">Digite **MyGPO** como o nome do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="7ac20-271">Digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="7ac20-272">Clique em **criar ao vivo** para que o novo GPO seja implantado para o ambiente de produção imediatamente após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="7ac20-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="7ac20-273">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="7ac20-274">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-275">O novo GPO será exibido na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="7ac20-276">Para aprovar a solicitação pendente para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="7ac20-277">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de aprovador no AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="7ac20-278">Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com a solicitação do editor para criar um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="7ac20-279">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="7ac20-280">Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.</span><span class="sxs-lookup"><span data-stu-id="7ac20-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="7ac20-281">Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="7ac20-282">Clique em **Sim** para confirmar a aprovação da criação do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="7ac20-283">O GPO será movido para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="7ac20-284">Etapa 2: editar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="7ac20-285">Você pode usar GPOs para configurar o computador ou o usuário e implantá-los em muitos computadores ou usuários.</span><span class="sxs-lookup"><span data-stu-id="7ac20-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="7ac20-286">Nesta etapa, você usa uma conta com a função de editor para fazer check-out de um GPO do arquivo, editar o GPO offline, verificar o GPO editado no arquivo morto e solicitar a implantação do GPO ao ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="7ac20-287">Nesse cenário, você define uma configuração no GPO para exigir que a senha tenha pelo menos oito caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="7ac20-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="7ac20-288">Para fazer check-out do GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="7ac20-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="7ac20-289">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="7ac20-290">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="7ac20-291">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="7ac20-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="7ac20-292">Clique com o botão direito do mouse em **MyGPO**e clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="7ac20-293">Digite um comentário a ser exibido no **histórico** do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="7ac20-294">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-295">Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="7ac20-296">Para editar o GPO offline e configurar o tamanho mínimo da senha</span><span class="sxs-lookup"><span data-stu-id="7ac20-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="7ac20-297">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de objeto de política de grupo** e fazer alterações em uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="7ac20-298">Para esse cenário, configure o tamanho mínimo da senha:</span><span class="sxs-lookup"><span data-stu-id="7ac20-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="7ac20-299">Em **configuração do computador**, clique duas vezes em **configurações do Windows**, clique duas vezes em **configurações de segurança**, clique duas vezes em políticas de **conta**e clique duas vezes em **política de senha**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="7ac20-300">No painel de detalhes, clique duas vezes em **tamanho mínimo da senha**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="7ac20-301">Na janela Propriedades, marque a caixa de seleção **definir esta configuração de política** , defina o número de caracteres para **8**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="7ac20-302">Feche a janela do **Editor de objeto de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="7ac20-303">Para verificar o GPO no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="7ac20-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="7ac20-304">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **check-in**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="7ac20-305">Digite um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="7ac20-306">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-307">Na guia **controlado** , o estado do GPO é identificado como **checked-in**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="7ac20-308">Para solicitar a implantação do GPO ao ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="7ac20-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="7ac20-309">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **implantar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="7ac20-310">Como essa conta não é um Aprovador ou administrador do AGPM, você deve enviar uma solicitação de implantação.</span><span class="sxs-lookup"><span data-stu-id="7ac20-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="7ac20-311">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="7ac20-312">Digite um comentário a ser exibido no **histórico** do GPO e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="7ac20-313">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-314">**MyGPO** é exibido na lista de GPOs na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="7ac20-315">Etapa 3: revisar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="7ac20-316">Nesta etapa, você atua como Aprovador, criando relatórios e analisando as configurações e alterando as configurações no GPO para determinar se devem ser aprovadas.</span><span class="sxs-lookup"><span data-stu-id="7ac20-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="7ac20-317">Depois de avaliar o GPO, implante-o no ambiente de produção e vincule-o a um domínio ou a uma UO (unidade organizacional) para que ele tenha efeito quando a política de grupo for atualizada para computadores nesse domínio ou unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="7ac20-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="7ac20-318">Para revisar as configurações no GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="7ac20-319">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de aprovador no AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="7ac20-320">(Qualquer administrador de política de grupo com a função revisor, que está incluído em todas as outras funções, pode revisar as configurações em um GPO.)</span><span class="sxs-lookup"><span data-stu-id="7ac20-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="7ac20-321">Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com uma solicitação de editor para implantar um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="7ac20-322">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="7ac20-323">Na guia **conteúdo** do painel detalhes, clique na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="7ac20-324">Clique duas vezes em **MyGPO** para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="7ac20-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="7ac20-325">Examine as configurações na versão mais recente do MyGPO:</span><span class="sxs-lookup"><span data-stu-id="7ac20-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="7ac20-326">Na janela do **histórico** , clique com o botão direito do mouse na versão do GPO com o carimbo de data e hora mais recente, clique em **configurações**e, em seguida, clique em **relatório HTML** para exibir um resumo das configurações do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="7ac20-327">No navegador da Web, clique em **Mostrar tudo** para exibir todas as configurações no GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="7ac20-328">Feche a janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="7ac20-328">Close the browser.</span></span>

7.  <span data-ttu-id="7ac20-329">Compare a versão mais recente do MyGPO com a primeira versão verificada no arquivo morto:</span><span class="sxs-lookup"><span data-stu-id="7ac20-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="7ac20-330">Na janela do **histórico** , clique na versão do GPO com o carimbo de data e hora mais recente.</span><span class="sxs-lookup"><span data-stu-id="7ac20-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="7ac20-331">Pressione **Ctrl** e clique na versão mais antiga do GPO que tem o estado **check-in**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="7ac20-332">Clique no botão **diferenças** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-332">Click the **Differences** button.</span></span> <span data-ttu-id="7ac20-333">A seção **políticas de conta/política de senha** é realçada em verde e precedida por **\ [+ \]**, indicando que essa configuração é definida somente na versão mais recente do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="7ac20-334">Clique em **políticas de conta/política de senha**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="7ac20-335">A configuração **comprimento mínimo da senha** também é realçada em verde e precedida por **\ [+ \]**, indicando que ela está configurada somente na última versão do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="7ac20-336">Fechar o navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="7ac20-336">Close the Web browser.</span></span>

**<span data-ttu-id="7ac20-337">Para implantar o GPO no ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="7ac20-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="7ac20-338">Na guia **pendente** , clique com o botão direito do mouse em **MyGPO** e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="7ac20-339">Digite um comentário para incluir no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="7ac20-340">Clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-340">Click **Yes**.</span></span> <span data-ttu-id="7ac20-341">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-342">O GPO é implantado no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="7ac20-343">Para vincular o GPO a um domínio ou unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="7ac20-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="7ac20-344">No GPMC, clique com o botão direito do mouse no domínio ou em uma UO à qual deseja aplicar o GPO que você configurou e clique em **vincular um GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="7ac20-345">Na caixa de diálogo **selecionar GPO** , clique em **MyGPO**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="7ac20-346">Etapa 4: usar um modelo para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="7ac20-347">Nesta etapa, você usa uma conta com a função de editor para criar um modelo, uma versão estática e não editável de um GPO para uso como ponto de partida para a criação de novos GPOs e, em seguida, cria um novo GPO com base nesse modelo.</span><span class="sxs-lookup"><span data-stu-id="7ac20-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="7ac20-348">Os modelos são úteis para criar rapidamente vários GPOs que incluam muitas das mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="7ac20-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="7ac20-349">Para criar um modelo com base em um GPO existente</span><span class="sxs-lookup"><span data-stu-id="7ac20-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="7ac20-350">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="7ac20-351">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="7ac20-352">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="7ac20-353">Clique com o botão direito do mouse em **MyGPO**e clique em **salvar como modelo** para criar um modelo que incorpora todas as configurações no MyGPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="7ac20-354">Digite **MyTemplate** como o nome do modelo e um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="7ac20-355">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-356">O novo modelo aparece na guia **modelos** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="7ac20-357">Para solicitar a criação de um novo GPO gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="7ac20-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="7ac20-358">Clique na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="7ac20-359">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="7ac20-360">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="7ac20-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="7ac20-361">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="7ac20-362">Digite **MyOtherGPO** como o nome do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="7ac20-363">Digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="7ac20-364">Clique em **criar ao vivo**, portanto, o novo GPO será implantado para o ambiente de produção imediatamente após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="7ac20-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="7ac20-365">Em **modelo de GPO**, selecione **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="7ac20-366">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="7ac20-367">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-368">O novo GPO será exibido na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="7ac20-369">Use uma conta que tenha sido atribuída à função de aprovador para aprovar a solicitação pendente para criar o GPO da mesma forma que você fez na [etapa 1: criar um GPO](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="7ac20-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="7ac20-370">MyTemplate incorpora todas as configurações que você configurou no MyGPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="7ac20-371">Como o MyOtherGPO foi criado usando MyTemplate, inicialmente ele contém todas as configurações que MyGPO contidas no momento em que MyTemplate foi criado.</span><span class="sxs-lookup"><span data-stu-id="7ac20-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="7ac20-372">Você pode confirmar isso gerando um relatório de diferença para comparar MyOtherGPO ao MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="7ac20-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="7ac20-373">Para fazer check-out do GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="7ac20-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="7ac20-374">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="7ac20-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="7ac20-375">Clique com o botão direito do mouse em **MyOtherGPO**e clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="7ac20-376">Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="7ac20-377">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-378">Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="7ac20-379">Para editar o GPO offline e configurar a duração do bloqueio de conta</span><span class="sxs-lookup"><span data-stu-id="7ac20-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="7ac20-380">Na guia **controlado** , clique com o botão direito do mouse em **MyOtherGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de objeto de política de grupo** e fazer alterações em uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="7ac20-381">Para esse cenário, configure o tamanho mínimo da senha:</span><span class="sxs-lookup"><span data-stu-id="7ac20-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="7ac20-382">Em **configuração do computador**, clique duas vezes em **configurações do Windows**, clique duas vezes em **configurações de segurança**, clique duas vezes em políticas de **conta**e clique duas vezes em política de **bloqueio de conta**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="7ac20-383">No painel de detalhes, clique duas vezes em **duração do bloqueio de conta**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="7ac20-384">Na janela Propriedades, marque **definir esta configuração de política**, defina a duração como **30** minutos e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="7ac20-385">Feche a janela do **Editor de objeto de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="7ac20-386">Verifique MyOtherGPO no arquivo morto e solicite a implantação como você fez para o MyGPO na [etapa 2: editar um GPO](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="7ac20-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="7ac20-387">Você pode comparar o MyOtherGPO ao MyGPO ou ao MyTemplate usando relatórios de diferença.</span><span class="sxs-lookup"><span data-stu-id="7ac20-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="7ac20-388">Qualquer conta que inclua a função de Revisor (administrador do AGPM \ [controle total \], Aprovador, editor ou revisor) pode gerar relatórios.</span><span class="sxs-lookup"><span data-stu-id="7ac20-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="7ac20-389">Para comparar um GPO a outro GPO e a um modelo</span><span class="sxs-lookup"><span data-stu-id="7ac20-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="7ac20-390">Para comparar o MyGPO e o MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="7ac20-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="7ac20-391">Na guia **controlado** , clique em **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="7ac20-392">Pressione **Ctrl** e clique em **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="7ac20-393">Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **relatório HTML**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="7ac20-394">Para comparar MyOtherGPO e MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="7ac20-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="7ac20-395">Na guia **controlado** , clique em **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="7ac20-396">Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **modelo**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="7ac20-397">Selecione meu **modelo** e **relatório HTML**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="7ac20-398">Etapa 5: excluir e restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="7ac20-399">Nesta etapa, você atua como um Aprovador para excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="7ac20-400">Para excluir um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="7ac20-401">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha atribuído a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="7ac20-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="7ac20-402">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="7ac20-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="7ac20-403">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="7ac20-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="7ac20-404">Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="7ac20-405">Clique em **excluir GPO do arquivo e da produção** para excluir a versão no arquivo e a versão implantada do GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="7ac20-406">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="7ac20-407">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-408">O GPO é removido da guia **controlado** e é exibido na guia **Lixeira** , onde ele pode ser restaurado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="7ac20-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="7ac20-409">Às vezes, você pode descobrir depois de excluir um GPO que ainda é necessário.</span><span class="sxs-lookup"><span data-stu-id="7ac20-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="7ac20-410">Nesta etapa, você atua como um Aprovador para restaurar um GPO que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="7ac20-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="7ac20-411">Para restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="7ac20-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="7ac20-412">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="7ac20-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="7ac20-413">Clique com o botão direito do mouse em **MyGPO**e clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="7ac20-414">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="7ac20-415">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-416">O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="7ac20-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="7ac20-417">**Observação**  Restaurar um GPO para o arquivo não o reimplanta automaticamente no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="7ac20-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="7ac20-418">Para retornar o GPO ao ambiente de produção, implante o GPO da [etapa 3: revise e implante um GPO](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="7ac20-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="7ac20-419">Depois de editar e implantar um GPO, você pode descobrir que alterações recentes no GPO estão causando um problema.</span><span class="sxs-lookup"><span data-stu-id="7ac20-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="7ac20-420">Nesta etapa, você atua como um Aprovador para reverter para uma versão anterior do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="7ac20-421">Você pode reverter para qualquer versão do histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="7ac20-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="7ac20-422">Você pode usar comentários e rótulos para identificar versões válidas conhecidas e quando foram feitas alterações específicas.</span><span class="sxs-lookup"><span data-stu-id="7ac20-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="7ac20-423">Para reverter para uma versão anterior de um GPO</span><span class="sxs-lookup"><span data-stu-id="7ac20-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="7ac20-424">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="7ac20-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="7ac20-425">Clique duas vezes em **MyGPO** para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="7ac20-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="7ac20-426">Clique com o botão direito do mouse na versão a ser implantada, clique em **implantar**e, em seguida, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="7ac20-427">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7ac20-428">Na janela do **histórico** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="7ac20-429">**Observação**  Para verificar se a versão que foi reimplementada é a versão pretendida, examine um relatório de diferença para as duas versões.</span><span class="sxs-lookup"><span data-stu-id="7ac20-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="7ac20-430">Na janela do **histórico** do GPO, selecione as duas versões, clique com o botão direito do mouse nelas, aponte para **diferença**e clique em **relatório HTML** ou **relatório XML**.</span><span class="sxs-lookup"><span data-stu-id="7ac20-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





