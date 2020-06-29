---
title: Visão geral de cenário de entrega autônoma
description: Visão geral de cenário de entrega autônoma
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796699"
---
# <span data-ttu-id="56b81-103">Visão geral de cenário de entrega autônoma</span><span class="sxs-lookup"><span data-stu-id="56b81-103">Stand-Alone Delivery Scenario Overview</span></span>


<span data-ttu-id="56b81-104">O cenário de entrega autônomo é uma solução de virtualização de aplicativos ideal para ambientes em que a conectividade de largura de banda baixa ou nenhuma conectividade limita a capacidade do cliente de desktop do Application Virtualization para transmitir aplicativos de servidores centralizados.</span><span class="sxs-lookup"><span data-stu-id="56b81-104">The stand-alone delivery scenario is an ideal application virtualization solution for environments where either low bandwidth connectivity or no connectivity limits the ability of the Application Virtualization Desktop Client to stream applications from centralized servers.</span></span> <span data-ttu-id="56b81-105">Nesses ambientes, os usuários geralmente trabalham remotamente e os proprietários de dispositivos instalam aplicativos usando arquivos do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="56b81-105">In these environments, users often work remotely and device owners install applications by using Windows Installer files.</span></span>

<span data-ttu-id="56b81-106">Você pode usar o sequenciador do Application Virtualization para criar aplicativos sequenciados que incluem arquivos do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="56b81-106">You can use the Application Virtualization Sequencer to create sequenced applications that include Windows Installer files.</span></span> <span data-ttu-id="56b81-107">Esses pacotes incluem os aplicativos virtualizados, as informações de publicação e as rotinas de instalação necessárias para instalar os pacotes nos sistemas do cliente.</span><span class="sxs-lookup"><span data-stu-id="56b81-107">These packages include the virtualized applications, publication information, and the necessary installer routines for installing the packages on the client systems.</span></span> <span data-ttu-id="56b81-108">O instalador adiciona o pacote de aplicativo virtual ao cliente da área de trabalho do Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="56b81-108">The installer adds the virtual application package to the Microsoft Application Virtualization Desktop Client.</span></span> <span data-ttu-id="56b81-109">As informações da publicação são configuradas para carregar aplicativos de um local local em vez de transmiti-los em uma WAN.</span><span class="sxs-lookup"><span data-stu-id="56b81-109">The publication information is configured to load applications from a local location rather than stream them across a WAN.</span></span> <span data-ttu-id="56b81-110">Os usuários podem se conectar temporariamente a uma rede para recuperar os arquivos do Windows Installer ou executá-los a partir de um DVD.</span><span class="sxs-lookup"><span data-stu-id="56b81-110">Users can temporarily connect to a network to retrieve the Windows Installer files or can run them from a DVD.</span></span>

<span data-ttu-id="56b81-111">O cenário de entrega autônomo oferece aos usuários os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="56b81-111">The stand-alone delivery scenario provides users the following benefits:</span></span>

-   <span data-ttu-id="56b81-112">Operação de implantação simples.</span><span class="sxs-lookup"><span data-stu-id="56b81-112">Simple deployment operation.</span></span>

-   <span data-ttu-id="56b81-113">Rede e servidores não necessários em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="56b81-113">Network and servers not needed at runtime.</span></span>

-   <span data-ttu-id="56b81-114">Aplicativos previamente armazenados em cache e disponíveis para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="56b81-114">Applications pre-cached and available to all users.</span></span>

<span data-ttu-id="56b81-115">O cenário de entrega autônomo tem as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="56b81-115">The stand-alone delivery scenario has the following limitations:</span></span>

-   <span data-ttu-id="56b81-116">Relatórios internos e automatizados não estão disponíveis; relatórios devem ser gerados com ferramentas de relatórios externos.</span><span class="sxs-lookup"><span data-stu-id="56b81-116">Built-in, automated reporting is unavailable; reports must be generated with external reporting tools.</span></span>

-   <span data-ttu-id="56b81-117">Os aplicativos devem ser entregues ao cliente manualmente, como os arquivos originais do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="56b81-117">Applications must be delivered to the client manually like the original Windows Installer files.</span></span>

## <span data-ttu-id="56b81-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56b81-118">Related topics</span></span>


[<span data-ttu-id="56b81-119">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="56b81-119">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="56b81-120">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="56b81-120">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





