---
title: Configurações com suporte no MBAM 2.5
description: Configurações com suporte no MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182923"
---
# <span data-ttu-id="17e33-103">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="17e33-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="17e33-104">Você pode executar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 em uma topologia autônoma ou em uma topologia de integração do Configuration Manager que integre o MBAM com o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="17e33-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="17e33-105">Se você usar a configuração recomendada para a topologia em um ambiente de produção, o MBAM oferece suporte a até 500.000 clientes do MBAM.</span><span class="sxs-lookup"><span data-stu-id="17e33-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="17e33-106">Para obter informações sobre a arquitetura e os recursos recomendados que são configurados em cada servidor para cada topologia, consulte [arquitetura de alto nível para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="17e33-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="17e33-107">Para configurações adicionais específicas para a topologia de integração do Configuration Manager, confira [versões do Configuration Manager às quais o MBAM oferece suporte](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="17e33-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="17e33-108">Observação</span><span class="sxs-lookup"><span data-stu-id="17e33-108">Note</span></span>**  
<span data-ttu-id="17e33-109">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17e33-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17e33-110">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17e33-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17e33-111">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17e33-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="17e33-112">Idiomas com suporte do MBAM</span><span class="sxs-lookup"><span data-stu-id="17e33-112">MBAM Supported Languages</span></span>


<span data-ttu-id="17e33-113">As tabelas a seguir mostram os idiomas com suporte para o cliente MBAM (incluindo o portal Self-Service) e o servidor MBAM no MBAM 2,5 e MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e33-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="17e33-114">Idiomas com suporte no MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="17e33-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-115">Idiomas do cliente</span><span class="sxs-lookup"><span data-stu-id="17e33-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="17e33-116">Idiomas do servidor</span><span class="sxs-lookup"><span data-stu-id="17e33-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-117">Tcheco (República Tcheca) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="17e33-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="17e33-118">Dinamarquês (Dinamarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="17e33-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="17e33-119">Holandês (Holanda) nl-NL</span><span class="sxs-lookup"><span data-stu-id="17e33-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="17e33-120">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="17e33-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="17e33-121">Finlandês (Finlândia) fi-FI</span><span class="sxs-lookup"><span data-stu-id="17e33-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="17e33-122">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="17e33-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="17e33-123">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="17e33-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="17e33-124">Grego (Grécia) El-GA</span><span class="sxs-lookup"><span data-stu-id="17e33-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="17e33-125">Húngaro (Hungria) hu-HU</span><span class="sxs-lookup"><span data-stu-id="17e33-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="17e33-126">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="17e33-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="17e33-127">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="17e33-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="17e33-128">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="17e33-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="17e33-129">Norueguês, Bokmål (Noruega) NB-não</span><span class="sxs-lookup"><span data-stu-id="17e33-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="17e33-130">Polonês (Polônia) pl-PL</span><span class="sxs-lookup"><span data-stu-id="17e33-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="17e33-131">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="17e33-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="17e33-132">Português (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="17e33-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="17e33-133">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="17e33-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="17e33-134">Eslovaco (Eslováquia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="17e33-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="17e33-135">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="17e33-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="17e33-136">Sueco (Suécia) VA-SE</span><span class="sxs-lookup"><span data-stu-id="17e33-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="17e33-137">Turco (Turquia) TR-TR</span><span class="sxs-lookup"><span data-stu-id="17e33-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="17e33-138">Esloveno (Eslovênia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="17e33-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="17e33-139">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="17e33-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="17e33-140">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="17e33-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="17e33-141">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="17e33-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="17e33-142">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="17e33-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="17e33-143">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="17e33-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="17e33-144">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="17e33-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="17e33-145">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="17e33-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="17e33-146">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="17e33-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="17e33-147">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="17e33-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="17e33-148">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="17e33-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="17e33-149">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="17e33-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="17e33-150">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="17e33-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="17e33-151">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="17e33-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="17e33-152">Idiomas com suporte no MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="17e33-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-153">Idiomas do cliente</span><span class="sxs-lookup"><span data-stu-id="17e33-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="17e33-154">Idiomas do servidor</span><span class="sxs-lookup"><span data-stu-id="17e33-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="17e33-155">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="17e33-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="17e33-156">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="17e33-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="17e33-157">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="17e33-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="17e33-158">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="17e33-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="17e33-159">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="17e33-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="17e33-160">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="17e33-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="17e33-161">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="17e33-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="17e33-162">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="17e33-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="17e33-163">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="17e33-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="17e33-164">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="17e33-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="17e33-165">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="17e33-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="17e33-166">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="17e33-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="17e33-167">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="17e33-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="17e33-168">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="17e33-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="17e33-169">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="17e33-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="17e33-170">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="17e33-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="17e33-171">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="17e33-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="17e33-172">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="17e33-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="17e33-173">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="17e33-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="17e33-174">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="17e33-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="17e33-175">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="17e33-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="17e33-176">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="17e33-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="17e33-177">Requisitos do sistema do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="17e33-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="17e33-178">Requisitos do sistema operacional do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="17e33-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="17e33-179">É altamente recomendável que você execute o cliente MBAM e o MBAM Server na mesma linha de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="17e33-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="17e33-180">Por exemplo, Windows 10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="17e33-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="17e33-181">A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="17e33-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-182">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17e33-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17e33-183">Edição</span><span class="sxs-lookup"><span data-stu-id="17e33-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="17e33-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17e33-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17e33-185">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17e33-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-186">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="17e33-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-187">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17e33-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-189">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="17e33-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-190">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17e33-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-192">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="17e33-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-193">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-194">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17e33-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-196">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17e33-197">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17e33-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-199">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-200">SP1</span><span class="sxs-lookup"><span data-stu-id="17e33-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-201">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="17e33-202">O domínio da empresa deve conter pelo menos um controlador de domínio do Windows Server 2008 (ou posterior).</span><span class="sxs-lookup"><span data-stu-id="17e33-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="17e33-203">MBAM do processador do servidor, RAM e requisitos de espaço em disco – topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="17e33-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="17e33-204">Esses requisitos são para a topologia autônoma do MBAM.</span><span class="sxs-lookup"><span data-stu-id="17e33-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="17e33-205">Para obter os requisitos para a topologia de integração do Configuration Manager, consulte [topologia do processador do servidor MBAM, RAM e requisitos de espaço em disco – topologia de integração do Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="17e33-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-206">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="17e33-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="17e33-207">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="17e33-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="17e33-208">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="17e33-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-209">Processor</span><span class="sxs-lookup"><span data-stu-id="17e33-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-210">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="17e33-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-211">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="17e33-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-212">RAM</span><span class="sxs-lookup"><span data-stu-id="17e33-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-213">8 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-214">12 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-215">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="17e33-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-216">1 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-217">2 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="17e33-218">Processador de servidor MBAM, RAM e requisitos de espaço em disco – topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="17e33-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="17e33-219">A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para servidores MBAM quando você estiver usando a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="17e33-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="17e33-220">Para obter os requisitos para a topologia autônoma, consulte [processador do MBAM Server, RAM e requisitos de espaço em disco – topologia](#bkmk-stand-alone-ramreqs)autônoma.</span><span class="sxs-lookup"><span data-stu-id="17e33-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-221">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="17e33-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="17e33-222">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="17e33-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="17e33-223">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="17e33-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-224">Processor</span><span class="sxs-lookup"><span data-stu-id="17e33-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-225">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="17e33-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-226">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="17e33-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-227">RAM</span><span class="sxs-lookup"><span data-stu-id="17e33-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-228">4 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-229">8 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-230">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="17e33-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-231">1 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="17e33-233">Versões do Configuration Manager com suporte no MBAM</span><span class="sxs-lookup"><span data-stu-id="17e33-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="17e33-234">O MBAM dá suporte para as seguintes versões do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="17e33-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-235">Versão com suporte</span><span class="sxs-lookup"><span data-stu-id="17e33-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="17e33-236">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17e33-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17e33-237">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17e33-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-238">Microsoft System Center Configuration Manager (ramificação atual), versões de até 1902</span><span class="sxs-lookup"><span data-stu-id="17e33-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-239">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="17e33-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-241">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-242">Microsoft System Center Configuration Manager (corporativo-versão 1606)</span><span class="sxs-lookup"><span data-stu-id="17e33-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-244">Gerenciador de configuração do Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="17e33-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-245">SP1</span><span class="sxs-lookup"><span data-stu-id="17e33-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-246">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-247">Microsoft System Center Configuration Manager 2007 R2 ou posterior</span><span class="sxs-lookup"><span data-stu-id="17e33-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-248">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-248">64-bit</span></span></p>

<span data-ttu-id="17e33-249">&gt;<strong>Observação </strong> embora o Configuration Manager 2007 R2 seja 32 bits, você deve instalá-lo e SQL Server em um sistema operacional de 64 bits para corresponder ao software MBAM de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="17e33-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="17e33-250">Para obter uma lista de configurações compatíveis com o Configuration Manager Server, consulte a documentação apropriada do TechNet para a versão do Configuration Manager que você está usando.</span><span class="sxs-lookup"><span data-stu-id="17e33-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="17e33-251">O MBAM não tem requisitos de sistema adicionais para o servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="17e33-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="17e33-252">Requisitos de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="17e33-252">SQL Server database requirements</span></span>

<span data-ttu-id="17e33-253">A tabela a seguir lista as versões do Microsoft SQL Server com suporte para os recursos do servidor do MBAM, que incluem o banco de dados de recuperação, o banco de dados de auditoria e a conformidade e o recurso relatórios.</span><span class="sxs-lookup"><span data-stu-id="17e33-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="17e33-254">As versões necessárias se aplicam às topologias autônomas ou de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="17e33-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="17e33-255">Você deve instalar o SQL Server com o agrupamento do **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** .</span><span class="sxs-lookup"><span data-stu-id="17e33-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-256">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="17e33-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="17e33-257">Edição</span><span class="sxs-lookup"><span data-stu-id="17e33-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="17e33-258">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17e33-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17e33-259">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17e33-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="17e33-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-261">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-262">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="17e33-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="17e33-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-264">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-265">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="17e33-266">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="17e33-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-267">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-268">SP1</span><span class="sxs-lookup"><span data-stu-id="17e33-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="17e33-269">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-270">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="17e33-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-271">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-272">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="17e33-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-273">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-274">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="17e33-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-275">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-276">SP3</span><span class="sxs-lookup"><span data-stu-id="17e33-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-277">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17e33-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-279">Standard ou Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-280">SP3</span><span class="sxs-lookup"><span data-stu-id="17e33-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-281">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="17e33-282">Observação</span><span class="sxs-lookup"><span data-stu-id="17e33-282">Note</span></span>**  
<span data-ttu-id="17e33-283">O MBAM tem um nível de compatibilidade máximo com suporte de 140.</span><span class="sxs-lookup"><span data-stu-id="17e33-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="17e33-284">O nível de compatibilidade padrão para novos bancos de dados criados no SQL Server 2019 é 150 que precisará ser alterado para 140 ou inferior, usando o comando ALTER DATABASE, após a criação do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17e33-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="17e33-285">Bancos de dados existentes migrados do SQL Server 2017 ou inferior permanecerão em seu nível de compatibilidade anterior e não precisarão ser alterados.</span><span class="sxs-lookup"><span data-stu-id="17e33-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="17e33-286">Para dar suporte ao SQL 2016, você deve instalar a versão de manutenção do 2017 de março do MDOP https://www.microsoft.com/download/details.aspx?id=54967  e para dar suporte ao sql 2017, instale o lançamento de serviços de julho de 2018 para o MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="17e33-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="17e33-287">Em geral, mantenha-se atualizado sempre usando a atualização de manutenção mais recente, pois também inclui todos os recursos correções e novos.</span><span class="sxs-lookup"><span data-stu-id="17e33-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="17e33-288">Requisitos de processador, RAM e espaço em disco do SQL Server – topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="17e33-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="17e33-289">A tabela a seguir lista os requisitos de processador do servidor, RAM e espaço em disco recomendados para o computador SQL Server quando você estiver usando a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="17e33-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="17e33-290">Use estes requisitos como guia.</span><span class="sxs-lookup"><span data-stu-id="17e33-290">Use these requirements as a guide.</span></span> <span data-ttu-id="17e33-291">Seus requisitos específicos variam de acordo com o número de computadores cliente que você tem suporte na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="17e33-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="17e33-292">Para ver os requisitos da topologia de integração do Configuration Manager, consulte [topologia do processador do SQL Server, da RAM e dos requisitos de espaço em disco – topologia de integração do Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="17e33-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-293">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="17e33-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="17e33-294">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="17e33-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="17e33-295">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="17e33-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-296">Processor</span><span class="sxs-lookup"><span data-stu-id="17e33-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-297">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="17e33-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-298">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="17e33-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-299">RAM</span><span class="sxs-lookup"><span data-stu-id="17e33-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-300">8 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-301">12 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-302">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="17e33-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-303">5 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-304">5 GB ou mais</span><span class="sxs-lookup"><span data-stu-id="17e33-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="17e33-305">Requisitos de processador, RAM e espaço em disco do SQL Server-topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="17e33-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="17e33-306">A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para o computador Microsoft SQL Server quando você estiver usando a topologia de integração do Configuration Manager, consulte o [processador do SQL Server, a RAM e requisitos de espaço em disco – topologia autônoma](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="17e33-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-307">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="17e33-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="17e33-308">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="17e33-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="17e33-309">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="17e33-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-310">Processor</span><span class="sxs-lookup"><span data-stu-id="17e33-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-311">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="17e33-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-312">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="17e33-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-313">RAM</span><span class="sxs-lookup"><span data-stu-id="17e33-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-314">4 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-315">8 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-316">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="17e33-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-317">5 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-318">5 GB</span><span class="sxs-lookup"><span data-stu-id="17e33-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="17e33-319">Requisitos do sistema do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="17e33-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="17e33-320">Requisitos do sistema operacional do cliente</span><span class="sxs-lookup"><span data-stu-id="17e33-320">Client operating system requirements</span></span>

<span data-ttu-id="17e33-321">É altamente recomendável que você execute o cliente MBAM e o MBAM Server na mesma linha de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="17e33-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="17e33-322">Por exemplo, Windows 10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="17e33-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="17e33-323">A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="17e33-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="17e33-324">Os mesmos requisitos se aplicam às topologias autônomas e de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="17e33-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-325">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17e33-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17e33-326">Edição</span><span class="sxs-lookup"><span data-stu-id="17e33-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="17e33-327">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17e33-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17e33-328">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17e33-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="17e33-329">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="17e33-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17e33-330">Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="17e33-331">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-332">Windows 10</span><span class="sxs-lookup"><span data-stu-id="17e33-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-333">Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-334">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="17e33-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-336">Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-337">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-338">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17e33-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-339">Empresa ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="17e33-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-340">SP1</span><span class="sxs-lookup"><span data-stu-id="17e33-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-341">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-342">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="17e33-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-343">Windows 8,1 e Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-344">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="17e33-345">Requisitos de RAM do cliente</span><span class="sxs-lookup"><span data-stu-id="17e33-345">Client RAM requirements</span></span>

<span data-ttu-id="17e33-346">Não há requisitos de RAM específicos para a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="17e33-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="17e33-347">Requisitos do sistema da política de grupo do MBAM</span><span class="sxs-lookup"><span data-stu-id="17e33-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="17e33-348">A tabela a seguir lista os sistemas operacionais suportados para a instalação de modelos de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="17e33-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17e33-349">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17e33-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17e33-350">Edição</span><span class="sxs-lookup"><span data-stu-id="17e33-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="17e33-351">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17e33-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17e33-352">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17e33-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="17e33-353">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="17e33-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="17e33-354">Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="17e33-355">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-356">Windows 10</span><span class="sxs-lookup"><span data-stu-id="17e33-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-357">Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-358">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-359">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="17e33-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-360">Enterprise</span><span class="sxs-lookup"><span data-stu-id="17e33-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-361">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-362">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17e33-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-363">Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="17e33-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-364">SP1</span><span class="sxs-lookup"><span data-stu-id="17e33-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-365">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-366">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="17e33-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-367">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-368">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17e33-369">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17e33-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-370">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17e33-371">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17e33-372">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17e33-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-373">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="17e33-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-374">SP1</span><span class="sxs-lookup"><span data-stu-id="17e33-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17e33-375">64 bits</span><span class="sxs-lookup"><span data-stu-id="17e33-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="17e33-376">MBAM no Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="17e33-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="17e33-377">O servidor MBAM pode ser implantado no Azure infraestrutura como serviço (IaaS) em qualquer uma das versões de sistema operacional compatíveis listadas acima, conectando-se a um Active Directory hospedado em um local ou a um Active Directory também hospedado no Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="17e33-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="17e33-378">A documentação para configurar e configurar o Active Directory no Azure IaaS está [aqui](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="17e33-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="17e33-379">O cliente MBAM não tem suporte em máquinas virtuais e também não é compatível com o Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="17e33-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="17e33-380">Lançamentos de serviço</span><span class="sxs-lookup"><span data-stu-id="17e33-380">Service releases</span></span> 

- [<span data-ttu-id="17e33-381">Hotfix de abril de 2016</span><span class="sxs-lookup"><span data-stu-id="17e33-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="17e33-382">Setembro de 2016</span><span class="sxs-lookup"><span data-stu-id="17e33-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="17e33-383">Dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="17e33-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="17e33-384">Março de 2017</span><span class="sxs-lookup"><span data-stu-id="17e33-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="17e33-385">Junho de 2017</span><span class="sxs-lookup"><span data-stu-id="17e33-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="17e33-386">Setembro de 2017</span><span class="sxs-lookup"><span data-stu-id="17e33-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="17e33-387">Março de 2018</span><span class="sxs-lookup"><span data-stu-id="17e33-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="17e33-388">De julho de 2018</span><span class="sxs-lookup"><span data-stu-id="17e33-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="17e33-389">Maio de 2019</span><span class="sxs-lookup"><span data-stu-id="17e33-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="17e33-390">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17e33-390">Related topics</span></span>


[<span data-ttu-id="17e33-391">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="17e33-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="17e33-392">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="17e33-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="17e33-393">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="17e33-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="17e33-394">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="17e33-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="17e33-395">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="17e33-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




