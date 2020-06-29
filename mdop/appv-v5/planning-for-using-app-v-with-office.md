---
title: Planejando o uso do App-V com o Office
description: Planejando o uso do App-V com o Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796246"
---
# <span data-ttu-id="1dc95-103">Planejando o uso do App-V com o Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="1dc95-104">Use as informações a seguir para planejar a implantação do Office usando o App-V.</span><span class="sxs-lookup"><span data-stu-id="1dc95-104">Use the following information to plan how to deploy Office by using App-V.</span></span> <span data-ttu-id="1dc95-105">Este artigo inclui:</span><span class="sxs-lookup"><span data-stu-id="1dc95-105">This article includes:</span></span>

-   [<span data-ttu-id="1dc95-106">Suporte do App-V para pacotes de idiomas</span><span class="sxs-lookup"><span data-stu-id="1dc95-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="1dc95-107">Versões com suporte do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="1dc95-108">Planejando o uso do App-V com versões coexistentes do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="1dc95-109">Como o Office se integra ao Windows ao implantar usar o App-V para implantar o Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="1dc95-110">Suporte do App-V para pacotes de idiomas</span><span class="sxs-lookup"><span data-stu-id="1dc95-110">App-V support for Language Packs</span></span>


<span data-ttu-id="1dc95-111">Você pode usar o sequenciador do App-V 5,0 para criar pacotes de plug-in para pacotes de idiomas, pacotes de interface de idioma, revisores de ferramenta e idiomas de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="1dc95-111">You can use the App-V 5.0 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="1dc95-112">Em seguida, você pode incluir os pacotes de plug-in em um grupo de conexão, juntamente com o pacote do Office 2013 que você cria usando o kit de ferramentas de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="1dc95-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="1dc95-113">Os pacotes de idiomas do plug-in e os aplicativos do Office interagem perfeitamente no mesmo grupo de conexão, assim como qualquer outro pacote agrupado em um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="1dc95-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

<span data-ttu-id="1dc95-114">**Observação**  O Microsoft Visio e o Microsoft Project não oferecem suporte para o pacote de idiomas do tailandês.</span><span class="sxs-lookup"><span data-stu-id="1dc95-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="1dc95-115">Versões com suporte do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-115">Supported versions of Microsoft Office</span></span>


<span data-ttu-id="1dc95-116">A tabela a seguir lista as versões do Microsoft Office que o App-V suporta, métodos de criação de pacotes do Office, licenciamento com suporte e implantações com suporte.</span><span class="sxs-lookup"><span data-stu-id="1dc95-116">The following table lists the versions of Microsoft Office that App-V supports, methods of Office package creation, supported licensing, and supported deployments.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dc95-117">Versão do Office compatível</span><span class="sxs-lookup"><span data-stu-id="1dc95-117">Supported Office Version</span></span></th>
<th align="left"><span data-ttu-id="1dc95-118">Versões do App-V com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc95-118">Supported App-V Versions</span></span></th>
<th align="left"><span data-ttu-id="1dc95-119">Criação de pacote</span><span class="sxs-lookup"><span data-stu-id="1dc95-119">Package Creation</span></span></th>
<th align="left"><span data-ttu-id="1dc95-120">Licenciamento compatível</span><span class="sxs-lookup"><span data-stu-id="1dc95-120">Supported Licensing</span></span></th>
<th align="left"><span data-ttu-id="1dc95-121">Implantações com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc95-121">Supported Deployments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-122">Aplicativos do Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="1dc95-122">Microsoft 365 Apps for enterprise</span></span></p>
<p><span data-ttu-id="1dc95-123">Também com suporte:</span><span class="sxs-lookup"><span data-stu-id="1dc95-123">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="1dc95-124">Visio pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="1dc95-124">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="1dc95-125">Project pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="1dc95-125">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1dc95-126">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1dc95-126">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="1dc95-127">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="1dc95-127">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="1dc95-128">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="1dc95-128">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1dc95-129">Ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-129">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-130">Assinatura</span><span class="sxs-lookup"><span data-stu-id="1dc95-130">Subscription</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1dc95-131">Desktop</span><span class="sxs-lookup"><span data-stu-id="1dc95-131">Desktop</span></span></p></li>
<li><p><span data-ttu-id="1dc95-132">VDI pessoal</span><span class="sxs-lookup"><span data-stu-id="1dc95-132">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="1dc95-133">VDI em pool</span><span class="sxs-lookup"><span data-stu-id="1dc95-133">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="1dc95-134">AOS</span><span class="sxs-lookup"><span data-stu-id="1dc95-134">RDS</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-135">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="1dc95-135">Office Professional Plus 2013</span></span></p>
<p><span data-ttu-id="1dc95-136">Também com suporte:</span><span class="sxs-lookup"><span data-stu-id="1dc95-136">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="1dc95-137">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="1dc95-137">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="1dc95-138">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="1dc95-138">Project Professional 2013</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1dc95-139">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1dc95-139">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="1dc95-140">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="1dc95-140">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="1dc95-141">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="1dc95-141">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1dc95-142">Ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-142">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-143">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="1dc95-143">Volume Licensing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1dc95-144">Desktop</span><span class="sxs-lookup"><span data-stu-id="1dc95-144">Desktop</span></span></p></li>
<li><p><span data-ttu-id="1dc95-145">VDI pessoal</span><span class="sxs-lookup"><span data-stu-id="1dc95-145">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="1dc95-146">VDI em pool</span><span class="sxs-lookup"><span data-stu-id="1dc95-146">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="1dc95-147">AOS</span><span class="sxs-lookup"><span data-stu-id="1dc95-147">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="1dc95-148">Planejando o uso do App-V com versões coexistentes do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-148">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="1dc95-149">Você pode instalar mais de uma versão do Microsoft Office lado a lado no mesmo computador usando a "coexistência do Microsoft Office".</span><span class="sxs-lookup"><span data-stu-id="1dc95-149">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="1dc95-150">Você pode implementar a coexistência do Office com combinações de todas as versões principais do Office e com métodos de instalação, conforme aplicável, usando a versão do Office com base no Windows Installer (MSi) do Office, clique para executar e App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="1dc95-150">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.0 SP2.</span></span> <span data-ttu-id="1dc95-151">No entanto, o uso de coexistência do Office não é recomendado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1dc95-151">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="1dc95-152">A prática recomendada pela Microsoft é evitar a coexistência do Office completamente para evitar problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="1dc95-152">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="1dc95-153">No entanto, ao migrar para uma versão mais recente do Office, os problemas surgem ocasionalmente que não podem ser resolvidos imediatamente, portanto, você pode implementar a coexistência temporariamente para facilitar uma migração mais recente para a versão mais recente do produto.</span><span class="sxs-lookup"><span data-stu-id="1dc95-153">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="1dc95-154">Usar a coexistência do Office em uma base de longo prazo nunca é recomendado, e sua organização deve ter um plano para fazer toda a transição no futuro imediato.</span><span class="sxs-lookup"><span data-stu-id="1dc95-154">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="1dc95-155">Antes de implementar a coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-155">Before you implement Office coexistence</span></span>

<span data-ttu-id="1dc95-156">Antes de implementar a coexistência do Office, examine a seguinte documentação do Office.</span><span class="sxs-lookup"><span data-stu-id="1dc95-156">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="1dc95-157">Escolha o artigo que corresponde à versão mais recente do Office para a qual você planeja implementar a coexistência.</span><span class="sxs-lookup"><span data-stu-id="1dc95-157">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dc95-158">Versão do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-158">Office version</span></span></th>
<th align="left"><span data-ttu-id="1dc95-159">Link para diretrizes</span><span class="sxs-lookup"><span data-stu-id="1dc95-159">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-160">Office 2013</span><span class="sxs-lookup"><span data-stu-id="1dc95-160">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="1dc95-161">Informações sobre como usar os pacotes e programas do Office 2013 (implantação do MSI) em um computador que esteja executando outra versão do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-161">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-162">Office 2010</span><span class="sxs-lookup"><span data-stu-id="1dc95-162">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="1dc95-163">Informações sobre como usar os pacotes e programas do Office 2010 em um computador que esteja executando outra versão do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-163">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1dc95-164">A documentação do Office fornece diretrizes abrangentes sobre a coexistência para instalações do Windows Installer (MSi) e com Clique para executar do Office.</span><span class="sxs-lookup"><span data-stu-id="1dc95-164">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="1dc95-165">Este tópico do App-V na coexistência suplementa a orientação do Office com informações que são mais específicas para implantações do App-V.</span><span class="sxs-lookup"><span data-stu-id="1dc95-165">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="1dc95-166">Cenários de coexistência do Office com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc95-166">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="1dc95-167">As tabelas a seguir resumem os cenários de coexistência com suporte.</span><span class="sxs-lookup"><span data-stu-id="1dc95-167">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="1dc95-168">Elas são organizadas de acordo com a versão e o método de implantação com o qual você está começando e o método de versão e implantação para o qual você está migrando.</span><span class="sxs-lookup"><span data-stu-id="1dc95-168">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="1dc95-169">Certifique-se de testar completamente todas as soluções de coexistência antes de implantá-las em um público de produção.</span><span class="sxs-lookup"><span data-stu-id="1dc95-169">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

<span data-ttu-id="1dc95-170">**Observação**  A Microsoft não oferece suporte ao uso de várias versões do Office em ambientes Windows Server com o serviço de função de host da sessão da área de trabalho remota habilitado.</span><span class="sxs-lookup"><span data-stu-id="1dc95-170">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="1dc95-171">Para executar cenários de coexistência do Office, você deve desabilitar esse serviço de função.</span><span class="sxs-lookup"><span data-stu-id="1dc95-171">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="1dc95-172">Integrações do Windows & a coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-172">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="1dc95-173">Os métodos de instalação do Office para Windows Installer e com Clique para executar integram-se com determinados pontos do sistema operacional Windows subjacente.</span><span class="sxs-lookup"><span data-stu-id="1dc95-173">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="1dc95-174">Quando você usa a coexistência, as integrações comuns do sistema operacional entre duas versões do Office podem entrar em conflito, causando problemas de compatibilidade e experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dc95-174">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="1dc95-175">Com o App-V, você pode sequenciar determinadas versões do Office para excluir as integrações, portanto "isolando"-as do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1dc95-175">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="1dc95-176">Modo em que o App-V pode sequenciar esta versão do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-176">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-177">Office 2007</span><span class="sxs-lookup"><span data-stu-id="1dc95-177">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-178">Sempre não integrado.</span><span class="sxs-lookup"><span data-stu-id="1dc95-178">Always non-integrated.</span></span> <span data-ttu-id="1dc95-179">O App-V não oferece integrações de sistema operacional com uma versão virtualizada do Office 2007.</span><span class="sxs-lookup"><span data-stu-id="1dc95-179">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-180">Office 2010</span><span class="sxs-lookup"><span data-stu-id="1dc95-180">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-181">Modo integrado e não integrado.</span><span class="sxs-lookup"><span data-stu-id="1dc95-181">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-182">Office 2013</span><span class="sxs-lookup"><span data-stu-id="1dc95-182">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-183">Sempre integrado.</span><span class="sxs-lookup"><span data-stu-id="1dc95-183">Always integrated.</span></span> <span data-ttu-id="1dc95-184">Não é possível desabilitar as integrações do sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="1dc95-184">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1dc95-185">A Microsoft recomenda que você implante a coexistência do Office com apenas uma instância integrada do Office.</span><span class="sxs-lookup"><span data-stu-id="1dc95-185">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="1dc95-186">Por exemplo, se você estiver usando o App-V para implantar o Office 2010 e o Office 2013, você deve sequenciar o Office 2010 no modo não integrado.</span><span class="sxs-lookup"><span data-stu-id="1dc95-186">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="1dc95-187">Para obter mais informações sobre o sequenciamento do Office no modo não integração (isolado), consulte [como sequenciar o Microsoft office 2010 no Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="1dc95-187">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="1dc95-188">Limitações conhecidas dos cenários de coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-188">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="1dc95-189">As seções a seguir descrevem alguns problemas que você pode encontrar ao usar o App-V para implementar a coexistência com o Office.</span><span class="sxs-lookup"><span data-stu-id="1dc95-189">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="1dc95-190">Limitações comuns em cenários de coexistência do Office com base no Windows Installer/com Clique para executar e App-V</span><span class="sxs-lookup"><span data-stu-id="1dc95-190">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="1dc95-191">As seguintes limitações podem ocorrer quando você instala as seguintes versões do Office no mesmo computador:</span><span class="sxs-lookup"><span data-stu-id="1dc95-191">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="1dc95-192">O Office 2010 usando a versão baseada no Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1dc95-192">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="1dc95-193">Office 2013 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="1dc95-193">Office 2013 by using App-V</span></span>

<span data-ttu-id="1dc95-194">Após a publicação do Office 2013 usando o App-V lado a lado com uma versão anterior do Office 2010 baseado no Windows Installer também pode fazer com que o Windows Installer seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="1dc95-194">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="1dc95-195">Isso ocorre porque a versão baseada no Windows Installer ou clique para executar do Office 2010 está tentando registrar-se automaticamente no computador.</span><span class="sxs-lookup"><span data-stu-id="1dc95-195">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="1dc95-196">Para ignorar a operação de registro automático do Word nativo do Word 2010, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="1dc95-196">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="1dc95-197">Saia do Word 2010.</span><span class="sxs-lookup"><span data-stu-id="1dc95-197">Exit Word 2010.</span></span>

2.  <span data-ttu-id="1dc95-198">Inicie o editor do registro fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1dc95-198">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="1dc95-199">No Windows 7: clique em **Iniciar**, digite **regedit** na caixa Iniciar pesquisa e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="1dc95-199">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="1dc95-200">No Windows 8, digite **regedit** e pressione Enter na página inicial e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="1dc95-200">In Windows 8, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="1dc95-201">Se for solicitada uma senha de administrador ou uma confirmação, digite a senha ou clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="1dc95-201">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="1dc95-202">Localize e selecione a seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="1dc95-202">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="1dc95-203">No menu **Editar** , clique em **novo**e, em seguida, clique em **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1dc95-203">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="1dc95-204">Digite **NoReReg**e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="1dc95-204">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="1dc95-205">Clique com o botão direito do mouse em **NoReReg** e clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="1dc95-205">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="1dc95-206">Na caixa **ValueData** , digite **1**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1dc95-206">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="1dc95-207">No menu arquivo, clique em **sair** para fechar o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="1dc95-207">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="1dc95-208">Como o Office se integra ao Windows quando você usa o App-V para implantar o Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-208">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="1dc95-209">Ao implantar o Office 2013 usando o App-V, o Office é totalmente integrado ao sistema operacional, que fornece aos usuários finais os mesmos recursos e funcionalidades que o Office tem quando ele é implantado sem App-V.</span><span class="sxs-lookup"><span data-stu-id="1dc95-209">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="1dc95-210">O pacote do Office 2013 App-V é compatível com os seguintes pontos de integração com o sistema operacional Windows:</span><span class="sxs-lookup"><span data-stu-id="1dc95-210">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dc95-211">Ponto de extensão</span><span class="sxs-lookup"><span data-stu-id="1dc95-211">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="1dc95-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="1dc95-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-213">Plug-in de junção de reunião do Lync para Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="1dc95-213">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-214">O usuário pode ingressar em reuniões do Lync a partir do Firefox e do Chrome</span><span class="sxs-lookup"><span data-stu-id="1dc95-214">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-215">Enviado para o driver de impressão do OneNote</span><span class="sxs-lookup"><span data-stu-id="1dc95-215">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-216">O usuário pode imprimir no OneNote</span><span class="sxs-lookup"><span data-stu-id="1dc95-216">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-217">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="1dc95-217">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-218">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="1dc95-218">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-219">Enviar para o suplemento do OneNote para Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="1dc95-219">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-220">O usuário pode enviar para o OneNote do IE</span><span class="sxs-lookup"><span data-stu-id="1dc95-220">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-221">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="1dc95-221">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-222">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="1dc95-222">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-223">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="1dc95-223">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-224">Os aplicativos e suplementos nativos podem interagir com o Outlook virtual por MAPI</span><span class="sxs-lookup"><span data-stu-id="1dc95-224">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-225">Plug-in do SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="1dc95-225">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-226">O usuário pode usar os recursos do SharePoint no Firefox</span><span class="sxs-lookup"><span data-stu-id="1dc95-226">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-227">Applet do painel de controle de email</span><span class="sxs-lookup"><span data-stu-id="1dc95-227">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-228">O usuário Obtém o applet do painel de controle de email no Outlook</span><span class="sxs-lookup"><span data-stu-id="1dc95-228">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-229">Assemblies de interoperabilidade primária</span><span class="sxs-lookup"><span data-stu-id="1dc95-229">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-230">Suporte a suplementos gerenciados</span><span class="sxs-lookup"><span data-stu-id="1dc95-230">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-231">Manipulador do cache de documentos do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-231">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-232">Permite o cache de documentos para aplicativos do Office</span><span class="sxs-lookup"><span data-stu-id="1dc95-232">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-233">Manipulador de pesquisa de protocolo do Outlook</span><span class="sxs-lookup"><span data-stu-id="1dc95-233">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-234">O usuário pode pesquisar no Outlook</span><span class="sxs-lookup"><span data-stu-id="1dc95-234">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-235">Controles ActiveX:</span><span class="sxs-lookup"><span data-stu-id="1dc95-235">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-236">Para obter mais informações sobre controles ActiveX, consulte <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> referência da API do controle ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="1dc95-236">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-237">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="1dc95-237">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-238">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-239">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="1dc95-239">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-240">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-240">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-241">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="1dc95-241">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-242">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-242">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-243">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="1dc95-243">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-244">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-244">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-245">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="1dc95-245">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-246">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-246">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-247">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="1dc95-247">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-248">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-248">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-249">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="1dc95-249">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-250">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-250">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-251">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="1dc95-251">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-252">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-252">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-253">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="1dc95-253">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-254">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-254">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-255">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="1dc95-255">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-256">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-256">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-257">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="1dc95-257">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-258">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-258">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-259">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="1dc95-259">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-260">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-260">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-261">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="1dc95-261">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-262">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-262">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-263">CommunicatorMeetingJoinAx. Joinmanager</span><span class="sxs-lookup"><span data-stu-id="1dc95-263">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-264">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-264">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1dc95-265">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="1dc95-265">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-266">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1dc95-266">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1dc95-267">Auxiliar do navegador do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="1dc95-267">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-268">Controle ActiveX]</span><span class="sxs-lookup"><span data-stu-id="1dc95-268">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-269">Sobreposições de ícones do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="1dc95-269">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc95-270">O ícone do shell do Windows Explorer se sobrepõe quando os usuários confiram pastas pastas do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="1dc95-270">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-271">Extensões de shell</span><span class="sxs-lookup"><span data-stu-id="1dc95-271">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc95-272">Teclado</span><span class="sxs-lookup"><span data-stu-id="1dc95-272">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc95-273">Windows Search</span><span class="sxs-lookup"><span data-stu-id="1dc95-273">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





