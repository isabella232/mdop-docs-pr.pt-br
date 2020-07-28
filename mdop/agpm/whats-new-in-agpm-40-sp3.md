---
title: Novidades do AGPM 4.0 SP3
description: Novidades do AGPM 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895761"
---
# <span data-ttu-id="2c2ca-103">Novidades do AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="2c2ca-103">What's New in AGPM 4.0 SP3</span></span>


<span data-ttu-id="2c2ca-104">Este conteúdo descreve melhorias e configurações com suporte para o serviço de gerenciamento de política de grupo avançado (AGPM) 4.0 da Microsoft Pack3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="2c2ca-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="2c2ca-105">Se houver uma diferença entre esse conteúdo e outra documentação do AGPM, considere esse conteúdo autoritativo e assuma que ele substitui a outra documentação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="2c2ca-106">O que há de novo</span><span class="sxs-lookup"><span data-stu-id="2c2ca-106">What’s new</span></span>


<span data-ttu-id="2c2ca-107">O AGPM 4.0 SP3 é compatível com os recursos e funcionalidades a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-107">AGPM4.0 SP3 supports the following features and functionality.</span></span>

### <span data-ttu-id="2c2ca-108">Suporte para Windows10</span><span class="sxs-lookup"><span data-stu-id="2c2ca-108">Support for Windows10</span></span>

<span data-ttu-id="2c2ca-109">O AGPM 4.0 SP3 adiciona suporte para os sistemas operacionais Windows10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-109">AGPM4.0 SP3 adds support for the Windows10 and Windows Server 2016 operating systems.</span></span>

### <span data-ttu-id="2c2ca-110">Suporte para o PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c2ca-110">Support for PowerShell</span></span>

<span data-ttu-id="2c2ca-111">O AGPM 4.0 SP3 adiciona suporte para cmdlets do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-111">AGPM4.0 SP3 adds support for PowerShell cmdlets.</span></span> <span data-ttu-id="2c2ca-112">Para obter uma lista dos cmdlets disponíveis no AGPM 4.0 SP3, incluindo descrições e sintaxe, consulte [automação do Microsoft Desktop Optimization Pack with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span><span class="sxs-lookup"><span data-stu-id="2c2ca-112">For a list of the cmdlets available in AGPM4.0 SP3, including descriptions and syntax, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span></span>

### <span data-ttu-id="2c2ca-113">Feedback do cliente e pacote cumulativo de hotfix</span><span class="sxs-lookup"><span data-stu-id="2c2ca-113">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="2c2ca-114">O AGPM 4,0 SP3 inclui um ROLLUP de todas as correções até e incluindo o gerenciamento avançado de política de grupo da Microsoft 4,0 SP2 e quaisquer correções para problemas encontrados desde o AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-114">AGPM 4.0 SP3 includes a rollup of all fixes up to and including Microsoft Advanced Group Policy Management 4.0 SP2 and any fixes for issues found since AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="2c2ca-115">Capacidade de atualizar para o AGPM 4.0 SP3 sem digitar novamente os parâmetros de configuração</span><span class="sxs-lookup"><span data-stu-id="2c2ca-115">Ability to upgrade to AGPM4.0 SP3 without re-entering configuration parameters</span></span>

<span data-ttu-id="2c2ca-116">Você pode atualizar o cliente do AGPM ou o servidor do AGPM para o AGPM 4.0 SP3 sem ser solicitado a digitar novamente os parâmetros de configuração (chamado de atualização inteligente) apenas do AGPM 4.0 e posterior, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-116">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP3 without being prompted to re-enter configuration parameters (called the Smart Upgrade) only from AGPM4.0 and later, as shown in the following table.</span></span> <span data-ttu-id="2c2ca-117">Se você estiver atualizando para o AGPM 4.0 SP3 de outras versões do AGPM, conforme mostrado na tabela, você deve usar a atualização clássica, que exige que você insira novamente os parâmetros de configuração.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-117">If you are upgrading to AGPM4.0 SP3 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="2c2ca-118">Como cada versão do AGPM está associada a um sistema operacional específico, consulte [escolhendo qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) e certifique-se de atualizar o sistema operacional conforme apropriado antes de atualizar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-118">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="2c2ca-119">Atualizações compatíveis com o AGPM 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="2c2ca-119">AGPM 4.0 SP3 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c2ca-120">Versão do AGPM a partir da qual você pode atualizar</span><span class="sxs-lookup"><span data-stu-id="2c2ca-120">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2c2ca-121">2,5</span><span class="sxs-lookup"><span data-stu-id="2c2ca-121">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2c2ca-122">3,0</span><span class="sxs-lookup"><span data-stu-id="2c2ca-122">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2c2ca-123">4,0</span><span class="sxs-lookup"><span data-stu-id="2c2ca-123">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2c2ca-124">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-124">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2c2ca-125">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="2c2ca-125">4.0 SP2</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2c2ca-126">4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="2c2ca-126">4.0 SP3</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c2ca-127">2,5</span><span class="sxs-lookup"><span data-stu-id="2c2ca-127">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-128">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-128">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-129">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="2c2ca-129">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-130">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="2c2ca-130">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-131">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-131">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-132">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-132">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-133">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-133">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-134">3,0</span><span class="sxs-lookup"><span data-stu-id="2c2ca-134">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-135">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-135">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-136">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-136">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-137">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="2c2ca-137">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-138">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-138">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-139">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-139">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-140">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-140">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c2ca-141">4,0</span><span class="sxs-lookup"><span data-stu-id="2c2ca-141">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-142">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-142">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-143">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-143">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-144">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-144">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-145">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="2c2ca-145">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-146">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="2c2ca-146">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-147">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="2c2ca-147">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-148">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-149">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-149">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-150">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-150">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-151">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-152">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-152">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-153">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="2c2ca-153">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-154">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="2c2ca-154">Smart Upgrade</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c2ca-155">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="2c2ca-155">4.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-156">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-156">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-157">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-158">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-159">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-159">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-160">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2c2ca-160">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-161">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="2c2ca-161">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2c2ca-162">Configurações compatíveis</span><span class="sxs-lookup"><span data-stu-id="2c2ca-162">Supported configurations</span></span>


<span data-ttu-id="2c2ca-163">O AGPM 4.0 SP3 dá suporte às configurações da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-163">AGPM4.0 SP3 supports the configurations in the following table.</span></span> <span data-ttu-id="2c2ca-164">Embora o AGPM dê suporte a configurações mistas, recomendamos que você execute o cliente do AGPM e o servidor do AGPM na mesma linha do sistema operacional, por exemplo, Windows10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-164">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

**<span data-ttu-id="2c2ca-165">Configurações de política e sistemas operacionais compatíveis com o AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="2c2ca-165">AGPM4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="2c2ca-166">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="2c2ca-166">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="2c2ca-167">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="2c2ca-167">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="2c2ca-168">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="2c2ca-168">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-169">Windows Server 2019 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2ca-169">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-170">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2ca-170">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-171">Suportado</span><span class="sxs-lookup"><span data-stu-id="2c2ca-171">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-172">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2ca-172">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-173">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2ca-173">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-174">Suportado</span><span class="sxs-lookup"><span data-stu-id="2c2ca-174">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c2ca-175">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-175">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-176">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-176">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-177">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2c2ca-177">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-178">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-178">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c2ca-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-180">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-180">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c2ca-181">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="2c2ca-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-182">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="2c2ca-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-183">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-183">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-184">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c2ca-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-185">Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="2c2ca-185">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-186">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="2c2ca-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c2ca-187">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-188">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c2ca-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-189">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="2c2ca-189">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c2ca-190">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-191">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c2ca-192">Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2c2ca-193">Pré-requisitos para a instalação do AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="2c2ca-193">Prerequisites for installing AGPM4.0 SP3</span></span>

<span data-ttu-id="2c2ca-194">A tabela a seguir descreve o comportamento dos instaladores do cliente e do servidor do AGPM 4.0 SP3 quando o .NET Framework 4.5.1, o PowerShell 3,0 ou o GPMC nas ferramentas de administração do servidor remoto estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-194">The following table describes the behavior of AGPM4.0 SP3 Client and Server installers when the .NET Framework4.5.1, PowerShell 3.0, or the GPMC in the Remote Server Administration Tools is missing.</span></span>

| <span data-ttu-id="2c2ca-195">Cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="2c2ca-195">AGPM Client</span></span>            |                                                                                                 |                                                                            | <span data-ttu-id="2c2ca-196">Servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="2c2ca-196">AGPM Server</span></span>                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2c2ca-197">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="2c2ca-197">Operating system</span></span>       | <span data-ttu-id="2c2ca-198">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="2c2ca-198">.NET Framework</span></span>                                                                                  | <span data-ttu-id="2c2ca-199">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c2ca-199">PowerShell</span></span>                                                                 | <span data-ttu-id="2c2ca-200">Ferramentas de Administração de Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="2c2ca-200">Remote Server Administration Tools</span></span>                                              | <span data-ttu-id="2c2ca-201">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="2c2ca-201">.NET Framework</span></span>                                                                                  | <span data-ttu-id="2c2ca-202">Ferramentas de Administração de Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="2c2ca-202">Remote Server Administration Tools</span></span>                                              |
| <span data-ttu-id="2c2ca-203">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2ca-203">Windows 10</span></span>             | <span data-ttu-id="2c2ca-204">Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-204">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-205">Se o PowerShell 3,0 não estiver instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-205">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-206">Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-206">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-207">Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-207">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-208">Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-208">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="2c2ca-209">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c2ca-209">Windows 8.1</span></span>            | <span data-ttu-id="2c2ca-210">Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-210">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-211">Se o PowerShell 3,0 não estiver instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-211">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-212">Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-213">Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-213">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-214">Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-214">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="2c2ca-215">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2c2ca-215">Windows Server 2012 R2</span></span> | <span data-ttu-id="2c2ca-216">Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-216">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-217">Se o PowerShell 3,0 não estiver instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-217">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-218">Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-218">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   | <span data-ttu-id="2c2ca-219">Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-219">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="2c2ca-220">Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-220">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   |

 

## <span data-ttu-id="2c2ca-221">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="2c2ca-221">How to Get MDOP Technologies</span></span>


<span data-ttu-id="2c2ca-222">O AGPM 4,0 SP3 faz parte do Microsoft Desktop Optimization Pack (MDOP) desde o MDOP 2015.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-222">AGPM 4.0 SP3 is a part of the Microsoft Desktop Optimization Pack (MDOP) since MDOP 2015.</span></span> <span data-ttu-id="2c2ca-223">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="2c2ca-223">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="2c2ca-224">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="2c2ca-224">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="2c2ca-225">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c2ca-225">Related topics</span></span>


[<span data-ttu-id="2c2ca-226">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="2c2ca-226">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="2c2ca-227">Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="2c2ca-227">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[<span data-ttu-id="2c2ca-228">Como escolher qual versão do AGPM a ser instalada</span><span class="sxs-lookup"><span data-stu-id="2c2ca-228">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





