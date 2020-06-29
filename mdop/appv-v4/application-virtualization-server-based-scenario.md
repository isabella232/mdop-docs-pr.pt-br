---
title: Cenário baseado no Application Virtualization Server
description: Cenário baseado no Application Virtualization Server
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797543"
---
# <span data-ttu-id="69472-103">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="69472-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="69472-104">Se você pretende usar um cenário de implantação baseado em servidor para o seu ambiente do Microsoft Application Virtualization (App-V), deve entender as diferenças entre o servidor de gerenciamento do Application Virtualization e o servidor de streaming do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="69472-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="69472-105">Os tópicos desta seção descrevem essas diferenças e também fornecem informações sobre métodos de entrega de pacote, protocolos de transmissão e componentes externos que você precisa considerar enquanto continua com a implantação.</span><span class="sxs-lookup"><span data-stu-id="69472-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="69472-106">Esta seção também fornece procedimentos passo a passo para instalar e configurar o servidor de gerenciamento do App-V e os servidores de streaming do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="69472-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="69472-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="69472-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="69472-108">Visão geral do Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="69472-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="69472-109">Fornece informações de implantação importantes sobre o servidor de gerenciamento do Application Virtualization, o servidor de streaming do Application Virtualization e os métodos de entrega de pacote, os protocolos e os componentes externos relevantes para seu plano de implantação baseado em servidor.</span><span class="sxs-lookup"><span data-stu-id="69472-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="69472-110">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="69472-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="69472-111">Descreve como instalar os componentes da plataforma do Microsoft Application Virtualization necessários para a implantação baseada em servidor.</span><span class="sxs-lookup"><span data-stu-id="69472-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="69472-112">Como configurar os servidores para a implantação baseada em servidor</span><span class="sxs-lookup"><span data-stu-id="69472-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="69472-113">Descreve como configurar o servidor de gerenciamento do Application Virtualization, o servidor de streaming do Application Virtualization, o servidor de integração de informações da Internet (IIS) e o servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="69472-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="69472-114">Como configurar um cache somente leitura no cliente do App-V (VDI)</span><span class="sxs-lookup"><span data-stu-id="69472-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="69472-115">Descreve como configurar o cliente App-V para usar cache somente leitura.</span><span class="sxs-lookup"><span data-stu-id="69472-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="69472-116">Como configurar um cache somente leitura no cliente do App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="69472-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="69472-117">Descreve como configurar o cliente App-V para usar cache somente leitura.</span><span class="sxs-lookup"><span data-stu-id="69472-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="69472-118">Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V</span><span class="sxs-lookup"><span data-stu-id="69472-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="69472-119">Descreve como configurar o espelhamento de banco de dados usando o Microsoft SQL Server para seu sistema App-V.</span><span class="sxs-lookup"><span data-stu-id="69472-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="69472-120">Referência</span><span class="sxs-lookup"><span data-stu-id="69472-120">Reference</span></span>


[<span data-ttu-id="69472-121">Parâmetros de linha de comando do instalador do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="69472-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="69472-122">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="69472-122">Related Sections</span></span>


[<span data-ttu-id="69472-123">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="69472-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="69472-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69472-124">Related topics</span></span>


[<span data-ttu-id="69472-125">Considerações de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="69472-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="69472-126">Cenário de Entrega Autônoma Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="69472-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





