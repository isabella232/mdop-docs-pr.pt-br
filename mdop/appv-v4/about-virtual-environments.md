---
title: Sobre ambientes virtuais
description: Sobre ambientes virtuais
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799063"
---
# <span data-ttu-id="aed2f-103">Sobre ambientes virtuais</span><span class="sxs-lookup"><span data-stu-id="aed2f-103">About Virtual Environments</span></span>


<span data-ttu-id="aed2f-104">Os aplicativos virtuais são executados em ambientes virtuais.</span><span class="sxs-lookup"><span data-stu-id="aed2f-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="aed2f-105">Os ambientes virtuais permitem que cada aplicativo seja executado em um servidor de desktop, laptop ou host de sessão de área de trabalho remota (host RDSession) sem instalação e alteração do sistema operacional do host.</span><span class="sxs-lookup"><span data-stu-id="aed2f-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="aed2f-106">Cada aplicativo transporta suas próprias informações de configuração no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="aed2f-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="aed2f-107">Como resultado, muitos aplicativos são executados lado a lado com outros aplicativos no mesmo computador sem conflitos.</span><span class="sxs-lookup"><span data-stu-id="aed2f-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="aed2f-108">Os aplicativos virtuais são executados localmente, portanto, eles são executados com o desempenho completo, a funcionalidade e o acesso aos serviços locais que você esperaria de qualquer aplicativo instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="aed2f-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="aed2f-109">Como cada aplicativo é executado em um ambiente virtual, os seguintes problemas são reduzidos:</span><span class="sxs-lookup"><span data-stu-id="aed2f-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="aed2f-110">Conflitos de aplicativos — em ambientes que não usam a virtualização de aplicativos, você deve testar exaustivamente cada aplicativo para garantir que ele não interfira em outros aplicativos instalados.</span><span class="sxs-lookup"><span data-stu-id="aed2f-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="aed2f-111">Teste de regressão — como o aplicativo não altera o sistema operacional subjacente, o teste de regressão extensa é eliminado.</span><span class="sxs-lookup"><span data-stu-id="aed2f-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="aed2f-112">Incompatibilidades de versão: versões diferentes do mesmo aplicativo podem ser executadas simultaneamente no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="aed2f-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="aed2f-113">Acesso multiusuário – aplicativos que não são executados no modo multiusuário e, portanto, não podem ser executados dentro de um host RDSession, agora podem fazê-lo e funcionar corretamente para vários usuários em um único host de RDSession.</span><span class="sxs-lookup"><span data-stu-id="aed2f-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="aed2f-114">Problemas de multilocação – duas instâncias do mesmo aplicativo que usam configurações diferentes podem ser executadas no mesmo computador ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="aed2f-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="aed2f-115">Siloing de servidor — a necessidade de muitos farms de servidores separados é eliminada.</span><span class="sxs-lookup"><span data-stu-id="aed2f-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="aed2f-116">Os ambientes virtuais incluem um registro virtual para cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aed2f-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="aed2f-117">As configurações de registro criadas por um aplicativo não podem ser vistas por outros aplicativos ou utilitários como o regedit.</span><span class="sxs-lookup"><span data-stu-id="aed2f-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="aed2f-118">Em vez de copiar todo o registro, o registro virtual usa um método de *sobreposição* .</span><span class="sxs-lookup"><span data-stu-id="aed2f-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="aed2f-119">Itens no registro do cliente podem ser lidos pelo aplicativo desde que uma cópia virtual desse item do registro não seja incluída no registro virtual.</span><span class="sxs-lookup"><span data-stu-id="aed2f-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="aed2f-120">Todas as gravações de aplicativo no registro estão contidas no registro virtual.</span><span class="sxs-lookup"><span data-stu-id="aed2f-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="aed2f-121">Os ambientes virtuais também incluem um sistema de arquivos virtual e outros componentes virtuais, incluindo serviços virtuais e COM virtual.</span><span class="sxs-lookup"><span data-stu-id="aed2f-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="aed2f-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aed2f-122">Related topics</span></span>


[<span data-ttu-id="aed2f-123">Visão geral do Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="aed2f-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





