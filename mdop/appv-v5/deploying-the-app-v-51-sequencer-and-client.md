---
title: Implantação do sequenciador e do cliente App-V 5.1
description: Implantação do sequenciador e do cliente App-V 5.1
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796532"
---
# <span data-ttu-id="c368a-103">Implantação do sequenciador e do cliente App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c368a-103">Deploying the App-V 5.1 Sequencer and Client</span></span>


<span data-ttu-id="c368a-104">O sequenciador do Microsoft Application Virtualization (App-V) 5,1 e o cliente permitem que os administradores virtualizam e executem aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="c368a-104">The Microsoft Application Virtualization (App-V) 5.1 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="c368a-105">Implantar o cliente</span><span class="sxs-lookup"><span data-stu-id="c368a-105">Deploy the client</span></span>


<span data-ttu-id="c368a-106">O cliente App-V 5,1 é o componente que executa um aplicativo virtualizado em um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="c368a-106">The App-V 5.1 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="c368a-107">O cliente permite que os usuários interajam com ícones e clique duas vezes em tipos de arquivo, para que eles possam iniciar um aplicativo virtualizado.</span><span class="sxs-lookup"><span data-stu-id="c368a-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="c368a-108">O cliente também pode obter o conteúdo do aplicativo virtual do servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c368a-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="c368a-109">Como implantar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="c368a-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-51gb18030.md)

[<span data-ttu-id="c368a-110">Como desinstalar o cliente do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c368a-110">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)

[<span data-ttu-id="c368a-111">Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="c368a-111">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## <span data-ttu-id="c368a-112">Definições de configuração do cliente</span><span class="sxs-lookup"><span data-stu-id="c368a-112">Client Configuration Settings</span></span>


<span data-ttu-id="c368a-113">O cliente App-V 5,1 armazena sua configuração no registro.</span><span class="sxs-lookup"><span data-stu-id="c368a-113">The App-V 5.1 client stores its configuration in the registry.</span></span> <span data-ttu-id="c368a-114">Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro.</span><span class="sxs-lookup"><span data-stu-id="c368a-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="c368a-115">Você também pode configurar várias ações do cliente alterando as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="c368a-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="c368a-116">Sobre as configurações do cliente</span><span class="sxs-lookup"><span data-stu-id="c368a-116">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

## <span data-ttu-id="c368a-117">Configurar o cliente usando o modelo ADMX e a política de grupo</span><span class="sxs-lookup"><span data-stu-id="c368a-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="c368a-118">Você pode usar o modelo ADMX da Microsoft para definir as configurações do cliente para o cliente do App-V 5,1 e o cliente de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="c368a-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.1 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="c368a-119">O modelo ADMX gerencia configurações comuns do cliente usando uma infraestrutura de política de grupo existente e inclui configurações para a configuração do cliente do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="c368a-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.1 client configuration.</span></span>

<span data-ttu-id="c368a-120">**Importante**  Você pode obter o modelo ADMX do App-V 5,1 a partir do centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c368a-120">**Important** You can obtain the App-V 5.1 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="c368a-121">Depois de baixar e instalar o modelo ADMX, execute as seguintes etapas no computador que você usará para gerenciar a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c368a-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="c368a-122">Geralmente, esse é o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c368a-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="c368a-123">Salve o arquivo **. admx** no seguinte diretório: **Windows \ \ policyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="c368a-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="c368a-124">Salve o arquivo **. adml** no seguinte diretório: **Windows \ \ policyDefinitions \ \ &lt; diretório &gt; de idioma**</span><span class="sxs-lookup"><span data-stu-id="c368a-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="c368a-125">Depois de concluir as etapas anteriores, você pode gerenciar as configurações de cliente do App-V 5,1 com o console de **Gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="c368a-125">After you have completed the preceding steps, you can manage the App-V 5.1 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="c368a-126">O cliente App-V 5,1 também armazena sua configuração no registro.</span><span class="sxs-lookup"><span data-stu-id="c368a-126">The App-V 5.1 client also stores its configuration in the registry.</span></span> <span data-ttu-id="c368a-127">Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro.</span><span class="sxs-lookup"><span data-stu-id="c368a-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="c368a-128">Você também pode configurar várias ações do cliente alterando as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="c368a-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="c368a-129">Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c368a-129">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="c368a-130">Implantar o cliente usando o modo de repositório de conteúdo compartilhado</span><span class="sxs-lookup"><span data-stu-id="c368a-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="c368a-131">O modo SCS (Shared Content Store) do App-V 5,1 permite que os clientes do SCS App-V 5,1 executem aplicativos virtualizados sem salvar qualquer um dos dados de pacote associados localmente.</span><span class="sxs-lookup"><span data-stu-id="c368a-131">The App-V 5.1 Shared Content Store (SCS) mode enables the SCS App-V 5.1 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="c368a-132">Todos os dados obrigatórios de pacotes virtualizados são transmitidos na rede; Portanto, você deve usar somente o modo SCS em ambientes com conexão rápida.</span><span class="sxs-lookup"><span data-stu-id="c368a-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="c368a-133">Os serviços de área de trabalho remota (RDS) e a versão padrão do cliente App-V 5,1 são compatíveis com o modo SCS.</span><span class="sxs-lookup"><span data-stu-id="c368a-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.1 client are supported with SCS mode.</span></span>

<span data-ttu-id="c368a-134">**Importante**  Se o cliente do App-V 5,1 estiver configurado para ser executado no modo SCS, o local em que os pacotes do App-V 5,1 são transmitidos deve estar disponível, caso contrário, o pacote virtualizado falhará.</span><span class="sxs-lookup"><span data-stu-id="c368a-134">**Important** If the App-V 5.1 client is configured to run in the SCS mode, the location where the App-V 5.1 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="c368a-135">Além disso, não recomendamos a implantação de aplicativos virtualizados em computadores que executam o cliente App-V 5,1 no modo SCS na Internet.</span><span class="sxs-lookup"><span data-stu-id="c368a-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.1 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="c368a-136">Além disso, o SCS não é um local físico que contém pacotes virtualizados.</span><span class="sxs-lookup"><span data-stu-id="c368a-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="c368a-137">É um modo que permite que o cliente App-V 5,1 transmita os dados de pacote virtualizados necessários na rede.</span><span class="sxs-lookup"><span data-stu-id="c368a-137">It is a mode that allows the App-V 5.1 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="c368a-138">O modo SCS é útil nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="c368a-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="c368a-139">Implantações de infraestrutura de área de trabalho virtual (VDI)</span><span class="sxs-lookup"><span data-stu-id="c368a-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="c368a-140">Implantações de serviços de área de trabalho remota (RDS)</span><span class="sxs-lookup"><span data-stu-id="c368a-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="c368a-141">Para usar o SCS em seu ambiente, você deve habilitar o cliente App-V 5,1 para ser executado no modo SCS.</span><span class="sxs-lookup"><span data-stu-id="c368a-141">To use SCS in your environment, you must enable the App-V 5.1 client to run in SCS mode.</span></span> <span data-ttu-id="c368a-142">Essa configuração deve ser especificada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c368a-142">This setting should be specified during installation.</span></span> <span data-ttu-id="c368a-143">Por padrão, o cliente não está configurado para usar o modo SCS.</span><span class="sxs-lookup"><span data-stu-id="c368a-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="c368a-144">Você deve instalar o cliente usando o procedimento sugerido se planeja usar o SCS.</span><span class="sxs-lookup"><span data-stu-id="c368a-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="c368a-145">No entanto, você pode configurar um cliente App-V 5,1 existente para ser executado no modo SCS inserindo o seguinte comando do PowerShell no computador que executa o cliente App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="c368a-145">However, you can configure an existing App-V 5.1 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.1 client:</span></span>

**<span data-ttu-id="c368a-146">Set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="c368a-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="c368a-147">Pode haver casos em que o administrador pré-carrega alguns aplicativos virtuais no computador que executa o cliente App-V 5,1 no modo SCS.</span><span class="sxs-lookup"><span data-stu-id="c368a-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.1 client in SCS mode.</span></span> <span data-ttu-id="c368a-148">Isso pode ser feito com comandos do PowerShell para adicionar, publicar e montar o pacote.</span><span class="sxs-lookup"><span data-stu-id="c368a-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="c368a-149">Por exemplo, se um pacote é pré-carregado em todos os computadores, o administrador pode adicionar, publicar e montar o pacote usando comandos do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c368a-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="c368a-150">O pacote não transmitiria pela rede porque seria armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="c368a-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="c368a-151">Como instalar o cliente App-V 5.1 para o modo de repositório de conteúdo compartilhado</span><span class="sxs-lookup"><span data-stu-id="c368a-151">How to Install the App-V 5.1 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## <span data-ttu-id="c368a-152">Implantar o sequenciador</span><span class="sxs-lookup"><span data-stu-id="c368a-152">Deploy the Sequencer</span></span>


<span data-ttu-id="c368a-153">O sequenciador é uma ferramenta usada para converter aplicativos padrão em pacotes virtuais para implantação em computadores que executam o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="c368a-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="c368a-154">O sequenciador ajuda a fornecer um processo de conversão simples e previsível com alterações mínimas nos fluxos de trabalho de sequenciamento anteriores.</span><span class="sxs-lookup"><span data-stu-id="c368a-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="c368a-155">Além disso, o sequenciador permite aos usuários configurar aplicativos com mais facilidade para permitir conexões de aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="c368a-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="c368a-156">Para obter uma lista de alterações no sequenciador do App-V 5,1, consulte [sobre o app-v 5,1](about-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="c368a-156">For a list of changes in the App-V 5.1 Sequencer, see [About App-V 5.1](about-app-v-51.md).</span></span>

[<span data-ttu-id="c368a-157">Como instalar o sequenciador</span><span class="sxs-lookup"><span data-stu-id="c368a-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> <span data-ttu-id="c368a-158">Logs do cliente e do sequenciador do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="c368a-158">App-V 5.1 Client and Sequencer logs</span></span>


<span data-ttu-id="c368a-159">Você pode usar as informações do log do sequenciador do App-V 5,1 para ajudar a solucionar problemas de instalação e eventos operacionais do sequenciador ao usar o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="c368a-159">You can use the App-V 5.1 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.1.</span></span> <span data-ttu-id="c368a-160">As informações do log relacionadas ao sequenciador podem ser analisadas com o **Visualizador de eventos**.</span><span class="sxs-lookup"><span data-stu-id="c368a-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="c368a-161">A linha a seguir exibe o caminho específico para eventos relacionados ao sequenciador:</span><span class="sxs-lookup"><span data-stu-id="c368a-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="c368a-162">**Visualizador de eventos \ \ aplicativos e logs de serviços \ \ Microsoft \ \ App V**. Os eventos relacionados ao sequenciador são anexados ao **AppV \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="c368a-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="c368a-163">Os eventos relacionados ao cliente são anexados ao **AppV \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="c368a-163">Client-related events are prepended with **AppV\_Client**.</span></span>

## <span data-ttu-id="c368a-164">Outros recursos para a implantação do sequenciador e do cliente</span><span class="sxs-lookup"><span data-stu-id="c368a-164">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="c368a-165">Implantação do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c368a-165">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="c368a-166">Planejamento para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c368a-166">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)






 

 





