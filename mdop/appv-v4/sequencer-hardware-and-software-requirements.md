---
title: Requisitos de hardware e software do Sequencer
description: Requisitos de hardware e software do Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796744"
---
# <span data-ttu-id="b33ab-103">Requisitos de hardware e software do Sequencer</span><span class="sxs-lookup"><span data-stu-id="b33ab-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="b33ab-104">Este tópico descreve os requisitos mínimos de hardware e software para o computador que executa o sequenciador do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="b33ab-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="b33ab-105">Antes de instalar o sequenciador e depois de sequenciar cada aplicativo, você deve restaurar uma imagem limpa do sistema operacional para o computador de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="b33ab-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="b33ab-106">Você pode usar um dos seguintes métodos para restaurar o computador que executa o sequenciador:</span><span class="sxs-lookup"><span data-stu-id="b33ab-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="b33ab-107">Reformate o disco rígido e reinstale o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b33ab-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="b33ab-108">Restaure o disco rígido no computador que executa a imagem do sequenciador usando outro software de criação de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="b33ab-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="b33ab-109">A lista a seguir descreve os requisitos de hardware recomendados para executar o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="b33ab-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="b33ab-110">Requisitos de Hardware</span><span class="sxs-lookup"><span data-stu-id="b33ab-110">Hardware Requirements</span></span>

-   <span data-ttu-id="b33ab-111">Processador — Intel Pentium III, 1 GHz (32 bits ou 64 bits).</span><span class="sxs-lookup"><span data-stu-id="b33ab-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="b33ab-112">O processo de sequenciamento é um processo de thread único e não aproveita os dois processadores.</span><span class="sxs-lookup"><span data-stu-id="b33ab-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="b33ab-113">Memória: 1GB ou mais, 2 GB recomendado.</span><span class="sxs-lookup"><span data-stu-id="b33ab-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="b33ab-114">Disco rígido – 40 gigabytes (GB) de espaço em disco rígido com no mínimo 15 GB de espaço disponível no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="b33ab-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="b33ab-115">Recomendamos que você tenha pelo menos três vezes o espaço do disco rígido que o aplicativo que você está sequenciando requer.</span><span class="sxs-lookup"><span data-stu-id="b33ab-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="b33ab-116">**Observação**  O sequenciamento requer uso intenso do disco.</span><span class="sxs-lookup"><span data-stu-id="b33ab-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="b33ab-117">Uma velocidade de disco rápido pode diminuir o tempo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="b33ab-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="b33ab-118">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="b33ab-118">Software Requirements</span></span>

<span data-ttu-id="b33ab-119">A lista a seguir descreve os sistemas operacionais com suporte para executar o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="b33ab-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b33ab-120">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b33ab-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="b33ab-121">Edição</span><span class="sxs-lookup"><span data-stu-id="b33ab-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="b33ab-122">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b33ab-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b33ab-123">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="b33ab-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b33ab-124">Pacote</span><span class="sxs-lookup"><span data-stu-id="b33ab-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-125">Professional</span><span class="sxs-lookup"><span data-stu-id="b33ab-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-126">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="b33ab-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-127">x86</span><span class="sxs-lookup"><span data-stu-id="b33ab-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b33ab-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b33ab-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-129">Business, Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="b33ab-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-130">Sem Service Pack, SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="b33ab-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-131">x86</span><span class="sxs-lookup"><span data-stu-id="b33ab-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b33ab-132">¹ do Windows7</span><span class="sxs-lookup"><span data-stu-id="b33ab-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-133">Professional, Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="b33ab-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b33ab-134">x86</span><span class="sxs-lookup"><span data-stu-id="b33ab-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b33ab-135">¹ com suporte para App-V 4,5 com SP1 ou SP2 e App-V 4,6 somente</span><span class="sxs-lookup"><span data-stu-id="b33ab-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="b33ab-136">**Observação**  O sequenciador do Application Virtualization (App-V) 4,6 dá suporte a versões de 32 bits e 64 bits desses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="b33ab-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="b33ab-137">Você deve configurar os computadores que executam o sequenciador com os mesmos aplicativos instalados nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="b33ab-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="b33ab-138">Requisitos de software para serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="b33ab-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b33ab-139">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b33ab-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="b33ab-140">Edição</span><span class="sxs-lookup"><span data-stu-id="b33ab-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="b33ab-141">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b33ab-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b33ab-142">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="b33ab-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b33ab-143">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="b33ab-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-144">Edição Standard, Enterprise Edition ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b33ab-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-145">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="b33ab-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-146">x86</span><span class="sxs-lookup"><span data-stu-id="b33ab-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b33ab-147">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="b33ab-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-148">Edição Standard, Enterprise Edition ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b33ab-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b33ab-149">x86</span><span class="sxs-lookup"><span data-stu-id="b33ab-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b33ab-150">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="b33ab-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-151">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="b33ab-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-152">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="b33ab-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b33ab-153">x86</span><span class="sxs-lookup"><span data-stu-id="b33ab-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b33ab-154">**Observação**  O Application Virtualization (App-V) 4,6 para serviços de área de trabalho remota é compatível com as versões de 32 bits e de 64 bits desses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="b33ab-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="b33ab-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b33ab-155">Related topics</span></span>


[<span data-ttu-id="b33ab-156">Visão geral do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="b33ab-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





