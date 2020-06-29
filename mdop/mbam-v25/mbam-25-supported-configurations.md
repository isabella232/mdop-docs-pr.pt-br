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
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799363"
---
# <span data-ttu-id="84f21-103">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="84f21-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="84f21-104">Você pode executar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 em uma topologia autônoma ou em uma topologia de integração do Configuration Manager que integre o MBAM com o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84f21-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="84f21-105">Se você usar a configuração recomendada para a topologia em um ambiente de produção, o MBAM oferece suporte a até 500.000 clientes do MBAM.</span><span class="sxs-lookup"><span data-stu-id="84f21-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="84f21-106">Para obter informações sobre a arquitetura e os recursos recomendados que são configurados em cada servidor para cada topologia, consulte [arquitetura de alto nível para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="84f21-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="84f21-107">Para configurações adicionais específicas para a topologia de integração do Configuration Manager, confira [versões do Configuration Manager às quais o MBAM oferece suporte](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="84f21-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="84f21-108">Observação</span><span class="sxs-lookup"><span data-stu-id="84f21-108">Note</span></span>**  
<span data-ttu-id="84f21-109">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="84f21-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="84f21-110">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="84f21-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="84f21-111">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="84f21-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="84f21-112">Idiomas com suporte do MBAM</span><span class="sxs-lookup"><span data-stu-id="84f21-112">MBAM Supported Languages</span></span>


<span data-ttu-id="84f21-113">As tabelas a seguir mostram os idiomas com suporte para o cliente MBAM (incluindo o portal de autoatendimento) e o servidor MBAM no MBAM 2,5 e MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="84f21-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="84f21-114">Idiomas com suporte no MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="84f21-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-115">Idiomas do cliente</span><span class="sxs-lookup"><span data-stu-id="84f21-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="84f21-116">Idiomas do servidor</span><span class="sxs-lookup"><span data-stu-id="84f21-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-117">Tcheco (República Tcheca) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="84f21-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="84f21-118">Dinamarquês (Dinamarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="84f21-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="84f21-119">Holandês (Holanda) nl-NL</span><span class="sxs-lookup"><span data-stu-id="84f21-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="84f21-120">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="84f21-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="84f21-121">Finlandês (Finlândia) fi-FI</span><span class="sxs-lookup"><span data-stu-id="84f21-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="84f21-122">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="84f21-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="84f21-123">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="84f21-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="84f21-124">Grego (Grécia) El-GA</span><span class="sxs-lookup"><span data-stu-id="84f21-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="84f21-125">Húngaro (Hungria) hu-HU</span><span class="sxs-lookup"><span data-stu-id="84f21-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="84f21-126">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="84f21-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="84f21-127">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="84f21-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="84f21-128">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="84f21-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="84f21-129">Norueguês, Bokmål (Noruega) NB-não</span><span class="sxs-lookup"><span data-stu-id="84f21-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="84f21-130">Polonês (Polônia) pl-PL</span><span class="sxs-lookup"><span data-stu-id="84f21-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="84f21-131">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="84f21-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="84f21-132">Português (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="84f21-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="84f21-133">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="84f21-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="84f21-134">Eslovaco (Eslováquia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="84f21-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="84f21-135">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="84f21-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="84f21-136">Sueco (Suécia) VA-SE</span><span class="sxs-lookup"><span data-stu-id="84f21-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="84f21-137">Turco (Turquia) TR-TR</span><span class="sxs-lookup"><span data-stu-id="84f21-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="84f21-138">Esloveno (Eslovênia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="84f21-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="84f21-139">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="84f21-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="84f21-140">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="84f21-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="84f21-141">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="84f21-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="84f21-142">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="84f21-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="84f21-143">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="84f21-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="84f21-144">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="84f21-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="84f21-145">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="84f21-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="84f21-146">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="84f21-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="84f21-147">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="84f21-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="84f21-148">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="84f21-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="84f21-149">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="84f21-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="84f21-150">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="84f21-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="84f21-151">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="84f21-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="84f21-152">Idiomas com suporte no MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="84f21-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-153">Idiomas do cliente</span><span class="sxs-lookup"><span data-stu-id="84f21-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="84f21-154">Idiomas do servidor</span><span class="sxs-lookup"><span data-stu-id="84f21-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="84f21-155">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="84f21-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="84f21-156">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="84f21-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="84f21-157">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="84f21-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="84f21-158">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="84f21-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="84f21-159">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="84f21-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="84f21-160">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="84f21-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="84f21-161">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="84f21-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="84f21-162">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="84f21-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="84f21-163">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="84f21-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="84f21-164">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="84f21-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="84f21-165">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="84f21-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="84f21-166">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="84f21-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="84f21-167">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="84f21-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="84f21-168">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="84f21-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="84f21-169">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="84f21-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="84f21-170">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="84f21-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="84f21-171">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="84f21-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="84f21-172">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="84f21-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="84f21-173">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="84f21-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="84f21-174">Espanhol (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="84f21-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="84f21-175">Chinês simplificado (República Popular da China) zh-CN</span><span class="sxs-lookup"><span data-stu-id="84f21-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="84f21-176">Chinês tradicional (Taiwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="84f21-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="84f21-177">Requisitos do sistema do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="84f21-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="84f21-178">Requisitos do sistema operacional do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="84f21-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="84f21-179">É altamente recomendável que você execute o cliente MBAM e o MBAM Server na mesma linha de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="84f21-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="84f21-180">Por exemplo, Windows 10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84f21-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="84f21-181">A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="84f21-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-182">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="84f21-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="84f21-183">Edição</span><span class="sxs-lookup"><span data-stu-id="84f21-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="84f21-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84f21-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84f21-185">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="84f21-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-186">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84f21-186">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-187">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="84f21-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-188">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-189">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84f21-189">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-190">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-190">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-191">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-192">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84f21-192">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-193">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-193">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="84f21-194">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-195">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f21-195">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-196">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-196">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-197">SP1</span><span class="sxs-lookup"><span data-stu-id="84f21-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-198">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-198">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="84f21-199">O domínio da empresa deve conter pelo menos um controlador de domínio do Windows Server 2008 (ou posterior).</span><span class="sxs-lookup"><span data-stu-id="84f21-199">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="84f21-200">MBAM do processador do servidor, RAM e requisitos de espaço em disco – topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="84f21-200">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="84f21-201">Esses requisitos são para a topologia autônoma do MBAM.</span><span class="sxs-lookup"><span data-stu-id="84f21-201">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="84f21-202">Para obter os requisitos para a topologia de integração do Configuration Manager, consulte [topologia do processador do servidor MBAM, RAM e requisitos de espaço em disco – topologia de integração do Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="84f21-202">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-203">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="84f21-203">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="84f21-204">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="84f21-204">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="84f21-205">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="84f21-205">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-206">Processador</span><span class="sxs-lookup"><span data-stu-id="84f21-206">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-207">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="84f21-207">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-208">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="84f21-208">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-209">RAM</span><span class="sxs-lookup"><span data-stu-id="84f21-209">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-210">8 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-210">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-211">12 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-211">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-212">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="84f21-212">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-213">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-214">2 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-214">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="84f21-215">Processador de servidor MBAM, RAM e requisitos de espaço em disco – topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="84f21-215">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="84f21-216">A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para servidores MBAM quando você estiver usando a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84f21-216">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="84f21-217">Para obter os requisitos para a topologia autônoma, consulte [processador do MBAM Server, RAM e requisitos de espaço em disco – topologia](#bkmk-stand-alone-ramreqs)autônoma.</span><span class="sxs-lookup"><span data-stu-id="84f21-217">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-218">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="84f21-218">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="84f21-219">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="84f21-219">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="84f21-220">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="84f21-220">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-221">Processador</span><span class="sxs-lookup"><span data-stu-id="84f21-221">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-222">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="84f21-222">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-223">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="84f21-223">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-224">RAM</span><span class="sxs-lookup"><span data-stu-id="84f21-224">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-225">4 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-225">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-226">8 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-226">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-227">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="84f21-227">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-228">1 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-228">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-229">2 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-229">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="84f21-230">Versões do Configuration Manager com suporte no MBAM</span><span class="sxs-lookup"><span data-stu-id="84f21-230">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="84f21-231">O MBAM dá suporte para as seguintes versões do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84f21-231">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-232">Versão com suporte</span><span class="sxs-lookup"><span data-stu-id="84f21-232">Supported version</span></span></th>
<th align="left"><span data-ttu-id="84f21-233">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84f21-233">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84f21-234">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="84f21-234">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-235">Microsoft System Center Configuration Manager (ramificação atual), versões de até 1902</span><span class="sxs-lookup"><span data-stu-id="84f21-235">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-236">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-236">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-237">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="84f21-237">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-238">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-238">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-239">Microsoft System Center Configuration Manager (corporativo-versão 1606)</span><span class="sxs-lookup"><span data-stu-id="84f21-239">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-240">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-240">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-241">Gerenciador de configuração do Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="84f21-241">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-242">SP1</span><span class="sxs-lookup"><span data-stu-id="84f21-242">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-244">Microsoft System Center Configuration Manager 2007 R2 ou posterior</span><span class="sxs-lookup"><span data-stu-id="84f21-244">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-245">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-245">64-bit</span></span></p>

<span data-ttu-id="84f21-246">&gt;<strong>Observação </strong> embora o Configuration Manager 2007 R2 seja 32 bits, você deve instalá-lo e SQL Server em um sistema operacional de 64 bits para corresponder ao software MBAM de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="84f21-246">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="84f21-247">Para obter uma lista de configurações compatíveis com o Configuration Manager Server, consulte a documentação apropriada do TechNet para a versão do Configuration Manager que você está usando.</span><span class="sxs-lookup"><span data-stu-id="84f21-247">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="84f21-248">O MBAM não tem requisitos de sistema adicionais para o servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84f21-248">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="84f21-249">Requisitos de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="84f21-249">SQL Server database requirements</span></span>

<span data-ttu-id="84f21-250">A tabela a seguir lista as versões do Microsoft SQL Server com suporte para os recursos do servidor do MBAM, que incluem o banco de dados de recuperação, o banco de dados de auditoria e a conformidade e o recurso relatórios.</span><span class="sxs-lookup"><span data-stu-id="84f21-250">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="84f21-251">As versões necessárias se aplicam às topologias autônomas ou de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84f21-251">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="84f21-252">Você deve instalar o SQL Server com o agrupamento do **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** .</span><span class="sxs-lookup"><span data-stu-id="84f21-252">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-253">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="84f21-253">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="84f21-254">Edição</span><span class="sxs-lookup"><span data-stu-id="84f21-254">Edition</span></span></th>
<th align="left"><span data-ttu-id="84f21-255">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84f21-255">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84f21-256">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="84f21-256">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-257">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="84f21-257">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-258">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-258">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-259">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="84f21-260">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="84f21-260">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-261">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-262">SP1</span><span class="sxs-lookup"><span data-stu-id="84f21-262">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="84f21-263">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-263">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-264">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="84f21-264">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-265">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-265">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-266">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="84f21-266">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-267">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-267">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-268">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="84f21-268">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-269">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-269">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-270">SP3</span><span class="sxs-lookup"><span data-stu-id="84f21-270">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-271">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-271">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-272">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f21-272">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-273">Standard ou Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-273">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-274">SP3</span><span class="sxs-lookup"><span data-stu-id="84f21-274">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-275">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-275">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="84f21-276">Observação</span><span class="sxs-lookup"><span data-stu-id="84f21-276">Note</span></span>**  
<span data-ttu-id="84f21-277">Para dar suporte ao SQL 2016, você deve instalar a versão de manutenção do 2017 de março do MDOP https://www.microsoft.com/download/details.aspx?id=54967 e para dar suporte ao sql 2017, instale o lançamento de serviços de julho de 2018 para o MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="84f21-277">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="84f21-278">Em geral, mantenha-se atualizado sempre usando a atualização de manutenção mais recente, pois também inclui todos os recursos correções e novos.</span><span class="sxs-lookup"><span data-stu-id="84f21-278">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="84f21-279">Requisitos de processador, RAM e espaço em disco do SQL Server – topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="84f21-279">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="84f21-280">A tabela a seguir lista os requisitos de processador do servidor, RAM e espaço em disco recomendados para o computador SQL Server quando você estiver usando a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="84f21-280">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="84f21-281">Use estes requisitos como guia.</span><span class="sxs-lookup"><span data-stu-id="84f21-281">Use these requirements as a guide.</span></span> <span data-ttu-id="84f21-282">Seus requisitos específicos variam de acordo com o número de computadores cliente que você tem suporte na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="84f21-282">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="84f21-283">Para ver os requisitos da topologia de integração do Configuration Manager, consulte [topologia do processador do SQL Server, da RAM e dos requisitos de espaço em disco – topologia de integração do Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="84f21-283">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-284">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="84f21-284">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="84f21-285">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="84f21-285">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="84f21-286">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="84f21-286">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-287">Processador</span><span class="sxs-lookup"><span data-stu-id="84f21-287">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-288">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="84f21-288">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-289">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="84f21-289">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-290">RAM</span><span class="sxs-lookup"><span data-stu-id="84f21-290">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-291">8 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-291">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-292">12 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-292">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-293">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="84f21-293">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-294">5 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-294">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-295">5 GB ou mais</span><span class="sxs-lookup"><span data-stu-id="84f21-295">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="84f21-296">Requisitos de processador, RAM e espaço em disco do SQL Server-topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="84f21-296">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="84f21-297">A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para o computador Microsoft SQL Server quando você estiver usando a topologia de integração do Configuration Manager, consulte o [processador do SQL Server, a RAM e requisitos de espaço em disco – topologia autônoma](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="84f21-297">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-298">Item de hardware</span><span class="sxs-lookup"><span data-stu-id="84f21-298">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="84f21-299">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="84f21-299">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="84f21-300">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="84f21-300">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-301">Processador</span><span class="sxs-lookup"><span data-stu-id="84f21-301">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-302">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="84f21-302">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-303">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="84f21-303">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-304">RAM</span><span class="sxs-lookup"><span data-stu-id="84f21-304">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-305">4 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-305">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-306">8 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-306">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-307">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="84f21-307">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-308">5 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-308">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-309">5 GB</span><span class="sxs-lookup"><span data-stu-id="84f21-309">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="84f21-310">Requisitos do sistema do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="84f21-310">MBAM Client system requirements</span></span>


### <span data-ttu-id="84f21-311">Requisitos do sistema operacional do cliente</span><span class="sxs-lookup"><span data-stu-id="84f21-311">Client operating system requirements</span></span>

<span data-ttu-id="84f21-312">É altamente recomendável que você execute o cliente MBAM e o MBAM Server na mesma linha de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="84f21-312">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="84f21-313">Por exemplo, Windows 10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84f21-313">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="84f21-314">A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="84f21-314">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="84f21-315">Os mesmos requisitos se aplicam às topologias autônomas e de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84f21-315">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-316">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="84f21-316">Operating system</span></span></th>
<th align="left"><span data-ttu-id="84f21-317">Edição</span><span class="sxs-lookup"><span data-stu-id="84f21-317">Edition</span></span></th>
<th align="left"><span data-ttu-id="84f21-318">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84f21-318">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84f21-319">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="84f21-319">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="84f21-320">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="84f21-320">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="84f21-321">Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-321">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="84f21-322">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-322">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-323">Windows 10</span><span class="sxs-lookup"><span data-stu-id="84f21-323">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-324">Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-324">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-325">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-325">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-326">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="84f21-326">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-327">Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-327">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-328">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-328">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-329">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84f21-329">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-330">Empresa ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="84f21-330">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-331">SP1</span><span class="sxs-lookup"><span data-stu-id="84f21-331">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-332">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-332">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-333">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="84f21-333">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-334">Windows 8,1 e Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-334">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-335">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-335">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="84f21-336">Requisitos de RAM do cliente</span><span class="sxs-lookup"><span data-stu-id="84f21-336">Client RAM requirements</span></span>

<span data-ttu-id="84f21-337">Não há requisitos de RAM específicos para a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="84f21-337">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="84f21-338">Requisitos do sistema da política de grupo do MBAM</span><span class="sxs-lookup"><span data-stu-id="84f21-338">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="84f21-339">A tabela a seguir lista os sistemas operacionais suportados para a instalação de modelos de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="84f21-339">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84f21-340">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="84f21-340">Operating system</span></span></th>
<th align="left"><span data-ttu-id="84f21-341">Edição</span><span class="sxs-lookup"><span data-stu-id="84f21-341">Edition</span></span></th>
<th align="left"><span data-ttu-id="84f21-342">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84f21-342">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84f21-343">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="84f21-343">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="84f21-344">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="84f21-344">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="84f21-345">Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-345">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="84f21-346">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-346">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-347">Windows 10</span><span class="sxs-lookup"><span data-stu-id="84f21-347">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-348">Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-348">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-349">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-349">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-350">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="84f21-350">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-351">Enterprise</span><span class="sxs-lookup"><span data-stu-id="84f21-351">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-352">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-352">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-353">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84f21-353">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-354">Enterprise ou Ultimate</span><span class="sxs-lookup"><span data-stu-id="84f21-354">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-355">SP1</span><span class="sxs-lookup"><span data-stu-id="84f21-355">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-356">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-356">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-357">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84f21-357">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-358">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-358">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-359">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-359">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84f21-360">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84f21-360">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-361">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-361">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84f21-362">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-362">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84f21-363">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f21-363">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-364">Standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="84f21-364">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-365">SP1</span><span class="sxs-lookup"><span data-stu-id="84f21-365">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84f21-366">64 bits</span><span class="sxs-lookup"><span data-stu-id="84f21-366">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="84f21-367">MBAM no Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="84f21-367">MBAM In Azure IaaS</span></span>

<span data-ttu-id="84f21-368">O servidor MBAM pode ser implantado no Azure infraestrutura como serviço (IaaS) em qualquer uma das versões de sistema operacional compatíveis listadas acima, conectando-se a um Active Directory hospedado em um local ou a um Active Directory também hospedado no Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="84f21-368">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="84f21-369">A documentação para configurar e configurar o Active Directory no Azure IaaS está [aqui](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="84f21-369">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="84f21-370">O cliente MBAM não tem suporte em máquinas virtuais e também não é compatível com o Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="84f21-370">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="84f21-371">Lançamentos de serviço</span><span class="sxs-lookup"><span data-stu-id="84f21-371">Service releases</span></span> 

- [<span data-ttu-id="84f21-372">Hotfix de abril de 2016</span><span class="sxs-lookup"><span data-stu-id="84f21-372">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="84f21-373">Setembro de 2016</span><span class="sxs-lookup"><span data-stu-id="84f21-373">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="84f21-374">Dezembro de 2016</span><span class="sxs-lookup"><span data-stu-id="84f21-374">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="84f21-375">Março de 2017</span><span class="sxs-lookup"><span data-stu-id="84f21-375">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="84f21-376">Junho de 2017</span><span class="sxs-lookup"><span data-stu-id="84f21-376">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="84f21-377">Setembro de 2017</span><span class="sxs-lookup"><span data-stu-id="84f21-377">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="84f21-378">Março de 2018</span><span class="sxs-lookup"><span data-stu-id="84f21-378">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="84f21-379">De julho de 2018</span><span class="sxs-lookup"><span data-stu-id="84f21-379">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="84f21-380">Maio de 2019</span><span class="sxs-lookup"><span data-stu-id="84f21-380">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="84f21-381">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84f21-381">Related topics</span></span>


[<span data-ttu-id="84f21-382">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="84f21-382">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="84f21-383">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="84f21-383">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="84f21-384">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="84f21-384">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="84f21-385">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="84f21-385">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="84f21-386">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="84f21-386">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




