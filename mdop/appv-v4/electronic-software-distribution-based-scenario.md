---
title: Cenário baseado em Distribuição Eletrônica de Software
description: Cenário baseado em Distribuição Eletrônica de Software
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797956"
---
# <span data-ttu-id="943bb-103">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="943bb-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="943bb-104">Se você pretende usar um cenário de implantação ESD (Electronic Software Distribution) para o seu ambiente do Microsoft Application Virtualization, é importante entender os fatores que entram e são afetados por essa decisão.</span><span class="sxs-lookup"><span data-stu-id="943bb-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="943bb-105">Os tópicos desta seção descrevem o cenário ESD e fornecem informações sobre métodos de entrega de pacote, protocolos de transmissão e componentes externos que você precisará considerar na estratégia de implantação.</span><span class="sxs-lookup"><span data-stu-id="943bb-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="943bb-106">Você também pode usar os procedimentos desta seção para concluir a implantação, a partir da fase de configuração do servidor por meio da fase de verificação de implantação.</span><span class="sxs-lookup"><span data-stu-id="943bb-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="943bb-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="943bb-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="943bb-108">Visão geral de cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="943bb-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="943bb-109">Fornece informações importantes sobre os métodos de publicação e streaming que você pode usar para uma implantação baseada em ESD.</span><span class="sxs-lookup"><span data-stu-id="943bb-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="943bb-110">Como configurar servidores para a implantação baseada em ESD</span><span class="sxs-lookup"><span data-stu-id="943bb-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="943bb-111">Esta seção fornece procedimentos que você pode usar para configurar os servidores de streaming do Application Virtualization, o servidor IIS e o servidor de arquivos para a estratégia de implantação baseada em distribuição de software eletrônico.</span><span class="sxs-lookup"><span data-stu-id="943bb-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="943bb-112">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="943bb-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="943bb-113">Fornece procedimentos de linha de comando para instalar o cliente do Application Virtualization usando o setup.exe ou o arquivo setup.msi.</span><span class="sxs-lookup"><span data-stu-id="943bb-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="943bb-114">Como desinstalar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="943bb-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="943bb-115">Fornece um procedimento passo a passo que você pode usar para confirmar que o cliente do Application Virtualization foi instalado e está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="943bb-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="943bb-116">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="943bb-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="943bb-117">Fornece procedimentos de linha de comando para publicar um pacote de aplicativo usando o Windows Installer ou o SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="943bb-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="943bb-118">Referência</span><span class="sxs-lookup"><span data-stu-id="943bb-118">Reference</span></span>


[<span data-ttu-id="943bb-119">Parâmetros de linha de comando do instalador do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="943bb-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="943bb-120">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="943bb-120">Related Sections</span></span>


[<span data-ttu-id="943bb-121">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="943bb-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="943bb-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="943bb-122">Related topics</span></span>


[<span data-ttu-id="943bb-123">Considerações de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="943bb-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="943bb-124">Cenário de Entrega Autônoma Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="943bb-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





