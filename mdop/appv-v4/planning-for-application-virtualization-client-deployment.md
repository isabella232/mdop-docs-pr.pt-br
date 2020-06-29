---
title: Planejamento da implantação do Application Virtualization Client
description: Planejamento da implantação do Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796828"
---
# <span data-ttu-id="a2bdb-103">Planejamento da implantação do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="a2bdb-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="a2bdb-104">Depois de decidir como publicar e implantar pacotes de aplicativos virtuais em seus computadores de usuário final, você deve planejar a implantação do software cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="a2bdb-105">O cliente Application Virtualization é o componente que realmente executa os aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="a2bdb-106">O cliente de virtualização de aplicativos permite que os usuários interajam com ícones e clique duas vezes em tipos de arquivo para iniciar um aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="a2bdb-107">Ele também manipula o streaming do conteúdo do aplicativo a partir de um servidor de streaming e o armazena em cache antes de iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="a2bdb-108">O conteúdo do aplicativo é estruturado de forma que todo o conteúdo necessário para iniciar o aplicativo e manipular a interação inicial do usuário é transmitido primeiro para o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="a2bdb-109">Há dois tipos diferentes de software cliente de virtualização de aplicativo: o cliente de virtualização de aplicativos para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal), que é usado em sistemas de servidor host de sessão de área de trabalho remota (host RDSession) e no cliente da área de trabalho de virtualização, que é usado para todos os outros computadores.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="a2bdb-110">O cliente do Application Virtualization deve ser configurado no momento da instalação, seja no console de gerenciamento do Application Virtualization ou por meio da linha de comando do instalador, com várias configurações importantes, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a2bdb-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="a2bdb-111">Locais dos ícones de todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="a2bdb-112">O local do arquivo OSD que contém as informações de definição do pacote.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="a2bdb-113">A fonte de conteúdo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-113">The application content source.</span></span>

-   <span data-ttu-id="a2bdb-114">O protocolo de comunicação a ser usado durante a recuperação dos itens anteriores.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="a2bdb-115">O tamanho do cache e o método de gerenciamento do tamanho do cache a serem usados.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="a2bdb-116">Para agilizar a implantação do software cliente do Application Virtualization ao usar uma solução ESD (distribuição de software eletrônico), as configurações anteriores devem ser definidas cuidadosamente com antecedência.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="a2bdb-117">Isso é especialmente importante quando você tem computadores em escritórios diferentes, em que seus clientes precisam ser configurados para usar locais de origem diferentes.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="a2bdb-118">Observação</span><span class="sxs-lookup"><span data-stu-id="a2bdb-118">Note</span></span>**  
-   <span data-ttu-id="a2bdb-119">O local do ícone e os valores do arquivo OSD são um fator importante a ser considerado ao escolher o método de publicação, seja usando o Windows Installer ou o SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="a2bdb-120">A configuração da fonte de conteúdo do aplicativo é definida pela sua escolha de método de streaming.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="a2bdb-121">Para garantir que o cache tem espaço suficiente alocado para todos os pacotes que podem ser implantados, use a configuração **usar o limite de espaço em disco livre** ao configurar o cliente para que o cache possa crescer conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="a2bdb-122">Ou, se preferir, determine com antecedência quanto espaço em disco será necessário para o cache do App-V e, no momento da instalação, defina o tamanho do cache de acordo.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="a2bdb-123">Para obter mais informações sobre o recurso de gerenciamento de espaço de cache, consulte **como usar o recurso de gerenciamento de espaço em cache** no guia de operações do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a2bdb-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="a2bdb-124">Durante as operações de streaming e de transmissão HTTP (S), os clientes do App-V 4,5 SP1 usam as configurações de servidor proxy configuradas no Internet Explorer no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="a2bdb-125">Para obter mais informações sobre como configurar os parâmetros de instalação do cliente, consulte [parâmetros da linha de comando do instalador do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a2bdb-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="a2bdb-126">Por fim, você precisa determinar como implantar o software cliente da área de trabalho do Application Virtualization para os clientes da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="a2bdb-127">Embora seja possível implantar o cliente da área de trabalho do Application Virtualization manualmente em cada computador, a maioria das organizações precisaria fazer isso por meio de um processo automatizado.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="a2bdb-128">Uma organização média ou grande pode ter um sistema ESD em operação, e essa seria uma maneira ideal de implantar o cliente.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="a2bdb-129">Se não houver um sistema ESD, você pode usar o método padrão de instalação do software em sua organização.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="a2bdb-130">As opções incluem política de grupo ou várias técnicas de script.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="a2bdb-131">Dependendo do número e do tamanho dos escritórios que você tem, esse processo de implantação pode ser complexo, e é essencial que você tenha uma abordagem estruturada para garantir que todos os computadores tenham um cliente instalado com a configuração correta.</span><span class="sxs-lookup"><span data-stu-id="a2bdb-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="a2bdb-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2bdb-132">Related topics</span></span>


[<span data-ttu-id="a2bdb-133">Planejamento da implantação do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="a2bdb-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="a2bdb-134">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="a2bdb-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="a2bdb-135">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="a2bdb-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="a2bdb-136">Como fazer upgrade do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="a2bdb-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="a2bdb-137">Como desinstalar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="a2bdb-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





