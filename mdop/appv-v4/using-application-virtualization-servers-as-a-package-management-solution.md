---
title: Uso do Application Virtualization Servers como uma Solução de Gerenciamento de Pacotes
description: Uso do Application Virtualization Servers como uma Solução de Gerenciamento de Pacotes
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796662"
---
# <span data-ttu-id="0c8b5-103">Uso do Application Virtualization Servers como uma Solução de Gerenciamento de Pacotes</span><span class="sxs-lookup"><span data-stu-id="0c8b5-103">Using Application Virtualization Servers as a Package Management Solution</span></span>


<span data-ttu-id="0c8b5-104">Se você não tiver um sistema ESD existente para implantar sua solução de virtualização de aplicativo ou não quiser usar uma, será necessário instalar um ou mais servidores de gerenciamento do Application Virtualization como núcleo da arquitetura do seu sistema.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-104">If you do not have an existing ESD system to deploy your Application Virtualization solution or do not wish to use one, you will need to install one or more Application Virtualization Management Servers as the core of your system architecture.</span></span> <span data-ttu-id="0c8b5-105">O servidor de gerenciamento do Application Virtualization requer um computador servidor dedicado e precisa de um banco de dados do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-105">The Application Virtualization Management Server requires a dedicated server computer and needs a Microsoft SQL Server database.</span></span> <span data-ttu-id="0c8b5-106">O banco de dados pode estar no mesmo servidor ou pode ser configurado em um servidor de banco de dados corporativo que seja acessível ao servidor de gerenciamento do Application Virtualization em uma conexão LAN de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-106">The database can be on the same server, or it can be configured on a corporate database server that is accessible to the Application Virtualization Management Server over a high-speed LAN connection.</span></span> <span data-ttu-id="0c8b5-107">Além disso, você precisará instalar o console de gerenciamento do Microsoft Application Virtualization, no servidor de gerenciamento do Application Virtualization ou em uma estação de trabalho de gerenciamento designado, e será necessário instalar o serviço Web de gerenciamento do Microsoft Application Virtualization, que também pode ser instalado no servidor de gerenciamento do Application Virtualization ou em um servidor IIS separado.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-107">In addition, you will need to install the Microsoft Application Virtualization Management Console, on either the Application Virtualization Management Server or on a designated management workstation, and you will need to install the Microsoft Application Virtualization Management Web Service, which can also be installed on the Application Virtualization Management Server or on a separate IIS server.</span></span> <span data-ttu-id="0c8b5-108">O console de gerenciamento do Application Virtualization é usado para se conectar ao serviço Web de gerenciamento do Application Virtualization, permitindo que o administrador do sistema interaja com o servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-108">The Application Virtualization Management Console is used to connect to the Application Virtualization Management Web Service, enabling the system administrator to interact with the Application Virtualization Management Server.</span></span>

<span data-ttu-id="0c8b5-109">**Observação**  O acesso aos aplicativos é controlado por meio de grupos de segurança nos serviços de domínio Active Directory, portanto, você precisará planejar um processo para configurar um grupo de segurança para cada aplicativo virtualizado e para gerenciar quais usuários serão adicionados a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-109">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process to set up a security group for each virtualized application and for managing which users are added to each group.</span></span> <span data-ttu-id="0c8b5-110">O administrador do servidor de gerenciamento do Application Virtualization configura o servidor para usar esses grupos do Active Directory, e o servidor controla automaticamente o acesso aos pacotes com base em associações de grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-110">The Application Virtualization Management Server administrator configures the server to use these Active Directory groups, and the server then automatically controls access to the packages based on Active Directory group membership.</span></span>

 

## <span data-ttu-id="0c8b5-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0c8b5-111">In This Section</span></span>


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[<span data-ttu-id="0c8b5-112">Visão geral dos Componentes do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="0c8b5-112">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)  
<span data-ttu-id="0c8b5-113">Lista e descreve os componentes principais do sistema de gerenciamento do Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-113">Lists and describes the primary components of the Microsoft Application Virtualization Management System.</span></span>

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[<span data-ttu-id="0c8b5-114">Publicação de aplicativos virtuais usando os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="0c8b5-114">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
<span data-ttu-id="0c8b5-115">Fornece uma breve visão geral de como os aplicativos virtuais são publicados em um cenário de implantação baseado em servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-115">Provides a brief overview of how virtual applications are published in an Application Virtualization Server-based deployment scenario.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[<span data-ttu-id="0c8b5-116">Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="0c8b5-116">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
<span data-ttu-id="0c8b5-117">Descreve as opções disponíveis para usar os servidores de streaming do Application Virtualization em conjunto com a implementação baseada em servidor de gerenciamento de virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0c8b5-117">Describes available options for using Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation.</span></span>

## <span data-ttu-id="0c8b5-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c8b5-118">Related topics</span></span>


[<span data-ttu-id="0c8b5-119">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="0c8b5-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="0c8b5-120">Planejamento da implantação do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="0c8b5-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





