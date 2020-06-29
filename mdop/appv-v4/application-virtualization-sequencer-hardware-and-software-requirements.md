---
title: Requisitos de Hardware e Software do Application Virtualization Sequencer
description: Requisitos de Hardware e Software do Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797562"
---
# <span data-ttu-id="14542-103">Requisitos de Hardware e Software do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="14542-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="14542-104">Este tópico descreve os requisitos mínimos de hardware e software para o computador que executa o sequenciador do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="14542-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="14542-105">**Importante**  Você deve executar o sequenciador do App-V (**SFTSequencer.exe**) usando uma conta com privilégios de administrador, devido às alterações que o sequenciador faz ao sistema local.</span><span class="sxs-lookup"><span data-stu-id="14542-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="14542-106">Essas alterações podem incluir a gravação de arquivos no diretório de **arquivos de c:\\Arquivos** , o que torna o registro alterado, o início e a interrupção de serviços, a atualização dos descritores de segurança para arquivos e a alteração de permissões.</span><span class="sxs-lookup"><span data-stu-id="14542-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="14542-107">Antes de instalar o sequenciador e depois de sequenciar cada aplicativo, você deve restaurar uma imagem limpa do sistema operacional para o computador de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="14542-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="14542-108">Você pode usar um dos seguintes métodos para restaurar o computador que executa o sequenciador:</span><span class="sxs-lookup"><span data-stu-id="14542-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="14542-109">Reformate o disco rígido e reinstale o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="14542-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="14542-110">Restaure o disco rígido no computador que executa a imagem do sequenciador usando outro software de criação de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="14542-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="14542-111">Reverter uma imagem do sistema operacional virtual, como uma imagem do Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="14542-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="14542-112">Usar uma máquina virtual permite que ambientes de sequenciamento limpos sejam facilmente reutilizados com administração mínima.</span><span class="sxs-lookup"><span data-stu-id="14542-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="14542-113">A lista a seguir descreve os requisitos de hardware recomendados para executar o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="14542-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="14542-114">Os requisitos são listados primeiro para Microsoft Application Virtualization (App-V) 4.6 SP2, seguido pelos requisitos para versões que precedem o App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="14542-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="14542-115">Requisitos de Hardware</span><span class="sxs-lookup"><span data-stu-id="14542-115">Hardware Requirements</span></span>

-   <span data-ttu-id="14542-116">Processador — Intel Pentium III, 1 GHz (32 bits ou 64 bits).</span><span class="sxs-lookup"><span data-stu-id="14542-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="14542-117">O processo de sequenciamento é um processo de thread único e não aproveita os dois processadores.</span><span class="sxs-lookup"><span data-stu-id="14542-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="14542-118">Memória: 1GB ou superior, 2 GB recomendado.</span><span class="sxs-lookup"><span data-stu-id="14542-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="14542-119">Disco rígido – 40 gigabytes (GB) de espaço em disco rígido com no mínimo 15 GB de espaço disponível no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="14542-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="14542-120">Recomendamos que você tenha pelo menos três vezes o espaço do disco rígido que o aplicativo que você está sequenciando requer.</span><span class="sxs-lookup"><span data-stu-id="14542-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="14542-121">**Observação**  O sequenciamento requer uso intenso do disco.</span><span class="sxs-lookup"><span data-stu-id="14542-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="14542-122">Uma velocidade de disco rápido pode diminuir o tempo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="14542-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="14542-123">Requisitos de software para o App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="14542-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="14542-124">A lista a seguir descreve os sistemas operacionais suportados para executar o App-V 4,6 SP2 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="14542-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14542-125">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="14542-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="14542-126">Edição</span><span class="sxs-lookup"><span data-stu-id="14542-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="14542-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="14542-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="14542-128">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="14542-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-129">Pacote</span><span class="sxs-lookup"><span data-stu-id="14542-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-130">Professional</span><span class="sxs-lookup"><span data-stu-id="14542-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-131">SP3</span><span class="sxs-lookup"><span data-stu-id="14542-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-132">x86</span><span class="sxs-lookup"><span data-stu-id="14542-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14542-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-134">Business, Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="14542-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-135">SP2</span><span class="sxs-lookup"><span data-stu-id="14542-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-136">x86</span><span class="sxs-lookup"><span data-stu-id="14542-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-137">7</span><span class="sxs-lookup"><span data-stu-id="14542-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-138">Professional, Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="14542-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-139">Sem Service Pack ou SP1</span><span class="sxs-lookup"><span data-stu-id="14542-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-140">x86 e x64</span><span class="sxs-lookup"><span data-stu-id="14542-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14542-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-142">Edição pro ou Enterprise</span><span class="sxs-lookup"><span data-stu-id="14542-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="14542-143">x86 e x64</span><span class="sxs-lookup"><span data-stu-id="14542-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14542-144">**Observação**  O sequenciador do Application Virtualization (App-V) 4,6 é compatível com as versões de 32 bits e 64 bits desses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="14542-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="14542-145">Você deve configurar os computadores que executam o sequenciador com os mesmos aplicativos instalados nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="14542-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="14542-146">Requisitos de software para versões que precedem o App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="14542-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="14542-147">A lista a seguir descreve os sistemas operacionais com suporte para executar o sequenciador para versões que precedem o App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="14542-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14542-148">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="14542-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="14542-149">Edição</span><span class="sxs-lookup"><span data-stu-id="14542-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="14542-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="14542-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="14542-151">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="14542-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-152">Pacote</span><span class="sxs-lookup"><span data-stu-id="14542-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-153">Professional</span><span class="sxs-lookup"><span data-stu-id="14542-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-154">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="14542-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-155">x86</span><span class="sxs-lookup"><span data-stu-id="14542-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14542-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-157">Business, Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="14542-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-158">Sem Service Pack, SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="14542-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-159">x86</span><span class="sxs-lookup"><span data-stu-id="14542-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-160">¹ do Windows7</span><span class="sxs-lookup"><span data-stu-id="14542-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-161">Professional, Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="14542-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="14542-162">x86</span><span class="sxs-lookup"><span data-stu-id="14542-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14542-163">¹ com suporte para App-V 4,5 com SP1 ou SP2 e App-V 4,6 somente</span><span class="sxs-lookup"><span data-stu-id="14542-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="14542-164">**Observação**  O sequenciador do Application Virtualization (App-V) 4,6 dá suporte a versões de 32 bits e 64 bits desses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="14542-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="14542-165">Você deve configurar os computadores que executam o sequenciador com os mesmos aplicativos instalados nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="14542-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="14542-166">Requisitos de software para serviços de área de trabalho remota do App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="14542-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14542-167">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="14542-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="14542-168">Edição</span><span class="sxs-lookup"><span data-stu-id="14542-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="14542-169">Service Pack</span><span class="sxs-lookup"><span data-stu-id="14542-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="14542-170">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="14542-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-171">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="14542-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-172">Edição Standard, Enterprise Edition ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-173">SP2</span><span class="sxs-lookup"><span data-stu-id="14542-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-174">x86</span><span class="sxs-lookup"><span data-stu-id="14542-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-175">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="14542-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-176">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-177">SP2</span><span class="sxs-lookup"><span data-stu-id="14542-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-178">x86</span><span class="sxs-lookup"><span data-stu-id="14542-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-179">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="14542-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-180">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-181">Sem Service Pack ou SP1</span><span class="sxs-lookup"><span data-stu-id="14542-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-182">x64</span><span class="sxs-lookup"><span data-stu-id="14542-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14542-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-184">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="14542-185">x86 ou x64</span><span class="sxs-lookup"><span data-stu-id="14542-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14542-186">**Observação**  O Application Virtualization (App-V) 4,6 SP2 para serviços de área de trabalho remota é compatível com as versões de 32 bits e 64 bits desses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="14542-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="14542-187">Requisitos de software para serviços de área de trabalho remota para versões que precedem App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="14542-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14542-188">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="14542-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="14542-189">Edição</span><span class="sxs-lookup"><span data-stu-id="14542-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="14542-190">Service Pack</span><span class="sxs-lookup"><span data-stu-id="14542-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="14542-191">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="14542-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-192">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="14542-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-193">Edição Standard, Enterprise Edition ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-194">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="14542-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-195">x86</span><span class="sxs-lookup"><span data-stu-id="14542-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-196">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="14542-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-197">Edição Standard, Enterprise Edition ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-198">Sem Service Pack ou SP2</span><span class="sxs-lookup"><span data-stu-id="14542-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-199">x86</span><span class="sxs-lookup"><span data-stu-id="14542-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14542-200">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="14542-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-201">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-202">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="14542-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-203">x86</span><span class="sxs-lookup"><span data-stu-id="14542-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14542-204">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="14542-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-205">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="14542-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-206">Sem Service Pack ou SP1</span><span class="sxs-lookup"><span data-stu-id="14542-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="14542-207">x64</span><span class="sxs-lookup"><span data-stu-id="14542-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14542-208">**Observação**  O Application Virtualization (App-V) 4,6 SP2 para serviços de área de trabalho remota é compatível com as versões de 32 bits e 64 bits desses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="14542-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="14542-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14542-209">Related topics</span></span>


[<span data-ttu-id="14542-210">Requisitos de Hardware e Software do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="14542-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="14542-211">Requisitos de Sistema do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="14542-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="14542-212">Como instalar o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="14542-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="14542-213">Como fazer upgrade do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="14542-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





