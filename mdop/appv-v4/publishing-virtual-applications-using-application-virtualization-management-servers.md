---
title: Publicação de aplicativos virtuais usando os Application Virtualization Management Servers
description: Publicação de aplicativos virtuais usando os Application Virtualization Management Servers
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796791"
---
# <span data-ttu-id="060f9-103">Publicação de aplicativos virtuais usando os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="060f9-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="060f9-104">Em uma implantação baseada em servidor do Application Virtualization, os pacotes de aplicativos virtuais que foram importados, testados e importados para implantação são copiados para o compartilhamento de conteúdo principal a ser usado pelo servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="060f9-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="060f9-105">Depois que os pacotes são importados no servidor de gerenciamento do Application Virtualization, eles podem ser publicados nos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="060f9-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="060f9-106">**Observação**  O compartilhamento de conteúdo deve estar localizado no armazenamento de disco anexado do servidor.</span><span class="sxs-lookup"><span data-stu-id="060f9-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="060f9-107">Usar um dispositivo de armazenamento de rede, como uma SAN ou um compartilhamento DFS, deve ser considerado cuidadosamente devido ao impacto na rede.</span><span class="sxs-lookup"><span data-stu-id="060f9-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="060f9-108">Os aplicativos são provisionados para grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="060f9-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="060f9-109">Normalmente, o administrador do Application Virtualization criará grupos do Active Directory para cada aplicativo virtual a ser publicado e adicionará os usuários apropriados a esses grupos.</span><span class="sxs-lookup"><span data-stu-id="060f9-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="060f9-110">Quando os usuários fazem logon em suas estações de trabalho, o cliente de virtualização de aplicativos, por padrão, executa uma atualização de publicação usando as credenciais do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="060f9-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="060f9-111">Em seguida, o usuário pode iniciar aplicativos em qualquer lugar que os atalhos foram colocados.</span><span class="sxs-lookup"><span data-stu-id="060f9-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="060f9-112">O administrador de virtualização de aplicativos determina onde e quantos atalhos estão localizados no sistema do cliente durante o sequenciamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="060f9-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="060f9-113">**Observação**  Uma *atualização de publicação* é uma chamada para o servidor do Application Virtualization definido no cliente do Application Virtualization, para determinar quais atalhos de aplicativo virtual são enviados ao cliente para serem usados pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="060f9-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="060f9-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="060f9-114">Related topics</span></span>


[<span data-ttu-id="060f9-115">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="060f9-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="060f9-116">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="060f9-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="060f9-117">Visão geral dos Componentes do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="060f9-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="060f9-118">Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="060f9-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





