---
title: Sobre o DaRT 8.0
description: Sobre o DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797894"
---
# <span data-ttu-id="2038d-103">Sobre o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="2038d-103">About DaRT 8.0</span></span>


<span data-ttu-id="2038d-104">O conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft 8,0 ajuda você a solucionar problemas e reparar computadores baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="2038d-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 helps you troubleshoot and repair Windows-based computers.</span></span> <span data-ttu-id="2038d-105">Isso inclui os computadores que não podem ser iniciados.</span><span class="sxs-lookup"><span data-stu-id="2038d-105">This includes those computers that cannot be started.</span></span> <span data-ttu-id="2038d-106">O DaRT 8,0 é um poderoso conjunto de ferramentas que ampliam o ambiente de recuperação do Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="2038d-106">DaRT 8.0 is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="2038d-107">Ao usar o DaRT, você pode analisar um problema para determinar a causa, por exemplo, ao inspecionar o log de eventos do computador ou o registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="2038d-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span> <span data-ttu-id="2038d-108">O DaRT é compatível com a recuperação de discos rígidos básicos que contêm partições, por exemplo, partições primárias e unidades lógicas, além de oferecer suporte à recuperação de volumes.</span><span class="sxs-lookup"><span data-stu-id="2038d-108">DaRT supports the recovery of basic hard disks that contain partitions, for example, primary partitions and logical drives, and supports the recovery of volumes.</span></span>

<span data-ttu-id="2038d-109">**Observação**  O DaRT não é compatível com a recuperação de discos dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="2038d-109">**Note** DaRT does not support the recovery of dynamic disks.</span></span>

 

<span data-ttu-id="2038d-110">O DaRT também fornece ferramentas para ajudá-lo a corrigir um problema assim que você determinar a causa.</span><span class="sxs-lookup"><span data-stu-id="2038d-110">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="2038d-111">Por exemplo, você pode usar as ferramentas do DaRT para desabilitar um driver de dispositivo defeituoso, remover hotfixes, restaurar arquivos excluídos e verificar o computador em busca de malware, mesmo quando não for possível ou não deve iniciar o sistema operacional Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="2038d-111">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="2038d-112">O DaRT pode ajudá-lo a recuperar rapidamente computadores que executam versões de 32 bits ou 64 bits do Windows 8, geralmente em menos tempo do que era necessário para fazer a nova imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="2038d-112">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span>

<span data-ttu-id="2038d-113">A funcionalidade no DaRT permite criar uma imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2038d-113">Functionality in DaRT lets you create a recovery image.</span></span> <span data-ttu-id="2038d-114">A imagem de recuperação inicia o ambiente de recuperação do Windows (Windows RE), a partir da qual você pode iniciar a janela **diagnóstico e do conjunto de ferramentas de recuperação** e acessar as ferramentas do DART.</span><span class="sxs-lookup"><span data-stu-id="2038d-114">The recovery image starts Windows Recovery Environment (Windows RE), from which you can start the **Diagnostics and Recovery Toolset** window and access the DaRT tools.</span></span>

<span data-ttu-id="2038d-115">Use o **Assistente de imagem de recuperação DART** para criar a imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="2038d-115">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="2038d-116">Por padrão, o assistente cria um arquivo de imagem ISO (International Organization for Standardization) e um arquivo Windows Imaging Format (WIM) e permite que você grave a imagem em um CD, DVD ou USB.</span><span class="sxs-lookup"><span data-stu-id="2038d-116">By default, the wizard creates an International Organization for Standardization (ISO) image file and a Windows Imaging Format (WIM) file and let you burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="2038d-117">Você pode implantar a imagem localmente nos computadores dos usuários finais ou pode implantá-la a partir de uma partição de rede remota ou de uma partição de recuperação no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="2038d-117">You can deploy the image locally at end user’s computers, or you can deploy it from a remote network partition or a recovery partition on the local hard drive.</span></span>

## <a href="" id="what-s-new-in-dart-8-0"></a><span data-ttu-id="2038d-118">O que há de novo no DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="2038d-118">What’s new in DaRT 8.0</span></span>


<span data-ttu-id="2038d-119">O DaRT 8,0 pode ajudá-lo a recuperar rapidamente computadores que executam versões de 32 bits ou 64 bits do Windows 8, geralmente em menos tempo do que seria necessário para fazer a nova imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="2038d-119">DaRT 8.0 can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span> <span data-ttu-id="2038d-120">O DaRT 8,0 tem os novos recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2038d-120">DaRT 8.0 has the following new features.</span></span>

### <span data-ttu-id="2038d-121">Criar imagens DaRT usando o Windows 8 ou o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2038d-121">Create DaRT images by using Windows 8 or Windows Server 2012</span></span>

<span data-ttu-id="2038d-122">O DaRT 8,0 permite que você crie imagens DaRT usando o Windows® 8 ou o Windows Server® 2012.</span><span class="sxs-lookup"><span data-stu-id="2038d-122">DaRT 8.0 enables you to create DaRT images using either Windows® 8 or Windows Server® 2012.</span></span> <span data-ttu-id="2038d-123">Para versões do Windows anteriores ao Windows 8 e Windows Server 2012, os clientes devem continuar a usar versões anteriores do DaRT.</span><span class="sxs-lookup"><span data-stu-id="2038d-123">For versions of Windows earlier than Windows 8 and Windows Server 2012, customers should continue to use earlier versions of DaRT.</span></span>

### <span data-ttu-id="2038d-124">Gerar imagens de 32 e de 64 bits a partir de um computador</span><span class="sxs-lookup"><span data-stu-id="2038d-124">Generate both 32- and 64-bit images from one computer</span></span>

<span data-ttu-id="2038d-125">O DaRT 8,0 permite que você gere imagens de 32 bits e de 64 bits a partir de um único computador que esteja executando o DaRT, independentemente de o computador ser um computador de 32 ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2038d-125">DaRT 8.0 enables you to generate both 32-bit and 64-bit images from a single computer that is running DaRT, regardless of whether the computer is a 32-bit or 64-bit computer.</span></span> <span data-ttu-id="2038d-126">No DaRT7, a imagem que foi criada precisa ser igual, bit a bit, como o computador que estava executando o DaRT.</span><span class="sxs-lookup"><span data-stu-id="2038d-126">In DaRT7, the image that was created had to be the same, bit-wise, as the computer that was running DaRT.</span></span>

### <span data-ttu-id="2038d-127">Crie uma imagem compatível com computadores que tenham uma interface BIOS ou UEFI</span><span class="sxs-lookup"><span data-stu-id="2038d-127">Create one image that supports computers that have either a BIOS or UEFI interface</span></span>

<span data-ttu-id="2038d-128">O suporte do DaRT 8.0 para a interface de firmware unificada (UEFI) e interfaces do BIOS permite que você crie apenas uma imagem que funcione com computadores que tenham uma interface.</span><span class="sxs-lookup"><span data-stu-id="2038d-128">DaRT 8.0’s support for both the Unified Extensible Firmware Interface (UEFI) and BIOS interfaces enables you to create just one image that works with computers that have either interface.</span></span>

### <span data-ttu-id="2038d-129">Usar uma GPT (tabela de partição GUID) para particionamento</span><span class="sxs-lookup"><span data-stu-id="2038d-129">Use a GUID partition table (GPT) for partitioning</span></span>

<span data-ttu-id="2038d-130">Agora, as ferramentas do DaRT 8,0 dão suporte a discos GPT do Windows 8, que fornecem um mecanismo mais flexível para particionar discos do que o esquema de particionamento MBR (MBR) mais antigo.</span><span class="sxs-lookup"><span data-stu-id="2038d-130">DaRT 8.0 tools now support Windows 8 GPT disks, which provide a more flexible mechanism for partitioning disks than the older master boot record (MBR) partitioning scheme.</span></span> <span data-ttu-id="2038d-131">As ferramentas do DaRT 8,0 continuam a dar suporte ao particionamento MBR.</span><span class="sxs-lookup"><span data-stu-id="2038d-131">DaRT 8.0 tools continue to support MBR partitioning.</span></span>

### <span data-ttu-id="2038d-132">Instalar o Windows 8 e o Windows Server 2012 no disco rígido local</span><span class="sxs-lookup"><span data-stu-id="2038d-132">Install Windows 8 and Windows Server 2012 on the local hard disk</span></span>

<span data-ttu-id="2038d-133">As ferramentas do DaRT 8,0 podem ser usadas apenas quando o Windows 8 e o Windows Server 2012 são instalados no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="2038d-133">DaRT 8.0 tools can be used only when Windows 8 and Windows Server 2012 are installed on the local hard disk.</span></span> <span data-ttu-id="2038d-134">No momento, não há suporte para o Windows to go.</span><span class="sxs-lookup"><span data-stu-id="2038d-134">Currently, there is no support for Windows To Go.</span></span>

### <a href="" id="-------------dart-8-0-release-notes"></a> <span data-ttu-id="2038d-135">Notas de versão do DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="2038d-135">DaRT 8.0 release notes</span></span>

<span data-ttu-id="2038d-136">Para saber mais e saber mais sobre as últimas notícias que não o fizeram na documentação, consulte as notas de [versão do DaRT 8,0](release-notes-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="2038d-136">For more information, and for late-breaking news that did not make it into the documentation, see the [Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="2038d-137">Como obter o DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="2038d-137">How to Get DaRT 8.0</span></span>


<span data-ttu-id="2038d-138">Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="2038d-138">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="2038d-139">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="2038d-139">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="2038d-140">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="2038d-140">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="2038d-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2038d-141">Related topics</span></span>


[<span data-ttu-id="2038d-142">Introdução ao DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="2038d-142">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="2038d-143">Notas de versão do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="2038d-143">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)

 

 





