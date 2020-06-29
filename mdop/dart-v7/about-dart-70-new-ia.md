---
title: Sobre o DaRT 7.0
description: Sobre o DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799239"
---
# <span data-ttu-id="84652-103">Sobre o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="84652-103">About DaRT 7.0</span></span>


<span data-ttu-id="84652-104">O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 ajuda você a solucionar problemas e reparar desktops baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="84652-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 helps you troubleshoot and repair Windows-based desktops.</span></span> <span data-ttu-id="84652-105">Isso inclui as áreas de trabalho que não podem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="84652-105">This includes those desktops that cannot be started.</span></span> <span data-ttu-id="84652-106">O DaRT é um poderoso conjunto de ferramentas que ampliam o ambiente de recuperação do Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="84652-106">DaRT is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="84652-107">Ao usar o DaRT, você pode analisar um problema para determinar a causa, por exemplo, ao inspecionar o log de eventos do computador ou o registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="84652-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span>

<span data-ttu-id="84652-108">O DaRT também fornece ferramentas para ajudá-lo a corrigir um problema assim que você determinar a causa.</span><span class="sxs-lookup"><span data-stu-id="84652-108">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="84652-109">Por exemplo, você pode usar as ferramentas do DaRT para desabilitar um driver de dispositivo defeituoso, remover hotfixes, restaurar arquivos excluídos e verificar o computador em busca de malware, mesmo quando não for possível ou não deve iniciar o sistema operacional Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="84652-109">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="84652-110">O DaRT pode ajudá-lo a recuperar rapidamente computadores que executam versões de 32 bits ou 64 bits do Windows 7, geralmente em menos tempo do que era necessário para fazer a nova imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="84652-110">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 7, typically in less time than it would take to reimage the computer.</span></span>

## <span data-ttu-id="84652-111">Sobre a imagem de recuperação do DaRT 7</span><span class="sxs-lookup"><span data-stu-id="84652-111">About the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="84652-112">A funcionalidade no DaRT permite criar uma imagem de recuperação baseada no WinRE combinado com um conjunto de ferramentas fornecidas pelo DaRT.</span><span class="sxs-lookup"><span data-stu-id="84652-112">Functionality in DaRT lets you create a recovery image that is based on WinRE combined with a set of tools that DaRT provides.</span></span> <span data-ttu-id="84652-113">A imagem de recuperação do DaRT aproveita o WinRE, a partir da qual você pode acessar a janela **diagnóstico e conjunto de ferramentas de recuperação** .</span><span class="sxs-lookup"><span data-stu-id="84652-113">The DaRT recovery image takes advantage of WinRE, from which you can access the **Diagnostics and Recovery Toolset** window.</span></span>

<span data-ttu-id="84652-114">Use o **Assistente de imagem de recuperação DART** para criar a imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="84652-114">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="84652-115">Por padrão, o assistente cria um arquivo de imagem International Organization for Standardization (ISO) na sua área de trabalho chamado DaRT70. ISO, embora você possa especificar um local e um nome de arquivo diferentes.</span><span class="sxs-lookup"><span data-stu-id="84652-115">By default, the wizard creates an International Organization for Standardization (ISO) image file on your desktop that is named DaRT70.iso, although you can specify a different location and file name.</span></span> <span data-ttu-id="84652-116">O assistente também permite que você grave a imagem em um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="84652-116">The wizard also lets you burn the image to a CD or DVD.</span></span> <span data-ttu-id="84652-117">Depois de concluir o assistente, você pode salvar a imagem de recuperação em uma unidade flash USB ou salvá-la em um formato que possa ser usado para criar uma partição remota ou uma partição de recuperação.</span><span class="sxs-lookup"><span data-stu-id="84652-117">After you have finished the wizard, you can save the recovery image to a USB flash drive or save it in a format that you can use to create a remote partition or a recovery partition.</span></span>

<span data-ttu-id="84652-118">Quando você precisa usar o DaRT para inicializar um computador de usuário final que não inicia, você pode seguir as instruções sobre [como recuperar computadores locais usando a imagem de recuperação do DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="84652-118">When you have to use DaRT to startup an end-user computer that will not start, you can follow the instructions at [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="84652-119">Para obter informações detalhadas sobre as ferramentas no DaRT, consulte [visão geral das ferramentas do dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="84652-119">For detailed information about the tools in DaRT, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

## <a href="" id="what-s-new-in-dart-7"></a><span data-ttu-id="84652-120">O que há de novo no DaRT 7</span><span class="sxs-lookup"><span data-stu-id="84652-120">What’s New in DaRT 7</span></span>


<span data-ttu-id="84652-121">O DaRT7 continua a dar suporte a todos os cenários incluídos nas versões anteriores e ele adiciona um novo recurso de conexão remota, além de três novas opções de implantação.</span><span class="sxs-lookup"><span data-stu-id="84652-121">DaRT7 continues to support all the scenarios included in previous versions and it adds a new Remote Connection feature in addition to three new deployment options.</span></span>

### <span data-ttu-id="84652-122">Criação de imagens do DaRT 7</span><span class="sxs-lookup"><span data-stu-id="84652-122">DaRT 7 Image Creation</span></span>

<span data-ttu-id="84652-123">O assistente que você usa para criar imagens ISO do DaRT agora é chamado de **imagem de recuperação DART** e agora oferece suporte a uma opção para habilitar ou desabilitar o novo recurso de conexão remota.</span><span class="sxs-lookup"><span data-stu-id="84652-123">The wizard that you use to create DaRT ISO images is now called **DaRT Recovery Image** and it now supports an option to enable or disable the new Remote Connection feature.</span></span> <span data-ttu-id="84652-124">A conexão remota permite que um agente de helpdesk execute as ferramentas DaRT a partir de um local remoto.</span><span class="sxs-lookup"><span data-stu-id="84652-124">Remote Connection lets a helpdesk agent run the DaRT tools from a remote location.</span></span> <span data-ttu-id="84652-125">Em versões anteriores, o agente de helpdesk precisa estar fisicamente presente no computador do usuário final para executar as ferramentas do DaRT.</span><span class="sxs-lookup"><span data-stu-id="84652-125">In previous releases, the helpdesk agent had to be physically present at the end-user computer to run the DaRT tools.</span></span>

<span data-ttu-id="84652-126">O assistente também permite que você personalize a mensagem de boas-vindas do recurso conexão remota (a mensagem é exibida quando os usuários finais executam a ferramenta conexão remota).</span><span class="sxs-lookup"><span data-stu-id="84652-126">The wizard also lets you customize the Welcome message for the Remote Connection feature (the message is shown when end users run the Remote Connection tool).</span></span> <span data-ttu-id="84652-127">Os administradores de ti também podem configurar qual número de porta deve ser usado pela conexão remota.</span><span class="sxs-lookup"><span data-stu-id="84652-127">IT Admins can also configure which Port Number should be used by Remote Connection.</span></span>

<span data-ttu-id="84652-128">Para obter mais informações sobre o **Assistente de imagem de recuperação do DART** ou conexão remota, consulte [criando a imagem de recuperação do DART 7,0](creating-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="84652-128">For more information about the **DaRT Recovery Image Wizard** or Remote Connection, see [Creating the DaRT 7.0 Recovery Image](creating-the-dart-70-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="84652-129">Implantação ISO do DaRT 7</span><span class="sxs-lookup"><span data-stu-id="84652-129">DaRT 7 ISO Deployment</span></span>

<span data-ttu-id="84652-130">Além de gravar em um CD ou DVD, o DaRT7 adiciona três novas opções ao implantar o ISO que contém a imagem de recuperação do DaRT:</span><span class="sxs-lookup"><span data-stu-id="84652-130">In addition to burning to a CD or DVD, DaRT7 adds three new options when you deploy the ISO that contains the DaRT recovery image:</span></span>

-   <span data-ttu-id="84652-131">Implantação de unidade flash USB</span><span class="sxs-lookup"><span data-stu-id="84652-131">USB flash drive deployment</span></span>

-   <span data-ttu-id="84652-132">Implantação de partição remota</span><span class="sxs-lookup"><span data-stu-id="84652-132">Remote partition deployment</span></span>

-   <span data-ttu-id="84652-133">Implantação de partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="84652-133">Recovery partition deployment</span></span>

<span data-ttu-id="84652-134">A opção de implantação de unidade flash USB permite que uma empresa use o DaRT em computadores que não tenham unidades de CD ou DVD disponíveis.</span><span class="sxs-lookup"><span data-stu-id="84652-134">The USB flash drive deployment option lets a company use DaRT on computers that do not have CD or DVD drives available.</span></span> <span data-ttu-id="84652-135">As opções de recuperação e partição remota permitem que os usuários finais tenham acesso fácil à imagem do DaRT e habilitar a funcionalidade de conexão remota.</span><span class="sxs-lookup"><span data-stu-id="84652-135">The recovery and remote partition options let end users have easy access to the DaRT image and to enable the Remote Connection functionality.</span></span>

<span data-ttu-id="84652-136">Para obter mais informações sobre como implantar imagens de recuperação do DaRT, consulte [implantando a imagem de recuperação do dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="84652-136">For more information about how to deploy DaRT recovery images, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="84652-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84652-137">Related topics</span></span>


[<span data-ttu-id="84652-138">Introdução ao DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="84652-138">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

[<span data-ttu-id="84652-139">Notas de versão do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="84652-139">Release Notes for DaRT 7.0</span></span>](release-notes-for-dart-70-new-ia.md)

 

 





