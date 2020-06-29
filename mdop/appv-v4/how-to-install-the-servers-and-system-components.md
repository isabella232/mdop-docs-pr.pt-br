---
title: Como instalar os componentes de servidores e do sistema
description: Como instalar os componentes de servidores e do sistema
author: dansimp
ms.assetid: c6f5fef0-522a-4ef1-8585-05b292d0289b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ceb5b8376189aee7631229dca912140e454536b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797086"
---
# <span data-ttu-id="3d4b8-103">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="3d4b8-103">How to Install the Servers and System Components</span></span>


<span data-ttu-id="3d4b8-104">Antes de poder entregar aplicativos aos usuários, você deve instalar os componentes da plataforma Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-104">Before you can deliver applications to users, you must install the Microsoft Application Virtualization Platform components.</span></span> <span data-ttu-id="3d4b8-105">Os tópicos desta seção fornecem as informações necessárias para instalar os servidores do Application Virtualization e os outros componentes do sistema do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-105">The topics in this section provide the information required to install the Application Virtualization Servers and the other Application Virtualization System components.</span></span>

<span data-ttu-id="3d4b8-106">**Observação**  Os procedimentos desta seção levam você por meio de uma instalação personalizada, onde você escolhe e escolhe os componentes para instalar em computadores separados, conforme recomendado em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-106">**Note** The procedures in this section take you through a customized installation, where you pick and choose components to install on separate computers, as recommended in a production environment.</span></span> <span data-ttu-id="3d4b8-107">No entanto, os procedimentos operacionais podem ditar uma abordagem diferente e, durante o processo de instalação, você pode querer agrupar componentes juntos.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-107">However, your operating procedures might dictate a different approach, and during the installation process you might want to group components together.</span></span> <span data-ttu-id="3d4b8-108">Não importa onde você instale os componentes, você pode instalá-los em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-108">Regardless of where you install the components, you can install them in any order.</span></span>

 

## <span data-ttu-id="3d4b8-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3d4b8-109">In This Section</span></span>


<a href="" id="how-to-install-application-virtualization-management-server"></a>[<span data-ttu-id="3d4b8-110">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="3d4b8-110">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)  
<span data-ttu-id="3d4b8-111">Fornece um procedimento passo a passo para instalar o servidor de gerenciamento do Application Virtualization e atribuí-lo ao grupo de servidores apropriado.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-111">Provides a step-by-step procedure for installing the Application Virtualization Management Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-application-virtualization-streaming-server"></a>[<span data-ttu-id="3d4b8-112">Como instalar o Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="3d4b8-112">How to Install the Application Virtualization Streaming Server</span></span>](how-to-install-the-application-virtualization-streaming-server.md)  
<span data-ttu-id="3d4b8-113">Fornece um procedimento passo a passo para instalar o servidor de streaming do Application Virtualization e atribuí-lo ao grupo de servidores apropriado.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-113">Provides a step-by-step procedure for installing the Application Virtualization Streaming Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-management-web-service"></a>[<span data-ttu-id="3d4b8-114">Como instalar o Management Web Service</span><span class="sxs-lookup"><span data-stu-id="3d4b8-114">How to Install the Management Web Service</span></span>](how-to-install-the-management-web-service.md)  
<span data-ttu-id="3d4b8-115">Fornece um procedimento passo a passo para instalar o serviço Web de gerenciamento do Application Virtualization em um computador de destino na sua rede.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-115">Provides a step-by-step procedure for installing the Application Virtualization Management Web Service on a target computer on your network.</span></span>

<a href="" id="how-to-install-the-management-console"></a>[<span data-ttu-id="3d4b8-116">Como instalar o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3d4b8-116">How to Install the Management Console</span></span>](how-to-install-the-management-console.md)  
<span data-ttu-id="3d4b8-117">Fornece um procedimento passo a passo para instalar o console de gerenciamento do Application Virtualization em um computador de destino na sua rede.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-117">Provides a step-by-step procedure for installing the Application Virtualization Management Console on a target computer on your network.</span></span>

<a href="" id="how-to-install-a-database"></a>[<span data-ttu-id="3d4b8-118">Como instalar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="3d4b8-118">How to Install a Database</span></span>](how-to-install-a-database.md)  
<span data-ttu-id="3d4b8-119">Fornece um procedimento passo a passo para instalar um banco de dados para a implantação baseada em servidor da virtualização de aplicativos, se um banco de dados ainda não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-119">Provides a step-by-step procedure for installing a database for your server-based deployment of Application Virtualization, if a database is not already available.</span></span>

<a href="" id="how-to-remove-the-application-virtualization-system-components"></a>[<span data-ttu-id="3d4b8-120">Como remover os componentes do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="3d4b8-120">How to Remove the Application Virtualization System Components</span></span>](how-to-remove-the-application-virtualization-system-components.md)  
<span data-ttu-id="3d4b8-121">Fornece procedimentos passo a passo para remover todos os componentes do software de virtualização de aplicativos ou do aplicativo selecionado de um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-121">Provides step-by-step procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

## <span data-ttu-id="3d4b8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d4b8-122">Related topics</span></span>


[<span data-ttu-id="3d4b8-123">Visão geral do Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="3d4b8-123">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="3d4b8-124">Como configurar os servidores para a implantação baseada em servidor</span><span class="sxs-lookup"><span data-stu-id="3d4b8-124">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="3d4b8-125">Como fazer upgrade dos componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="3d4b8-125">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)

 

 





