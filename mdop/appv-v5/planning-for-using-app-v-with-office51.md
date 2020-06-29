---
title: Planejando o uso do App-V com o Office
description: Planejando o uso do App-V com o Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796243"
---
# <span data-ttu-id="b7cb0-103">Planejando o uso do App-V com o Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="b7cb0-104">Use as informações a seguir para planejar como implantar o Office usando o Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-104">Use the following information to plan how to deploy Office by using Microsoft Application Virtualization (App-V) 5.1.</span></span> <span data-ttu-id="b7cb0-105">Este artigo inclui:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-105">This article includes:</span></span>

-   [<span data-ttu-id="b7cb0-106">Suporte do App-V para pacotes de idiomas</span><span class="sxs-lookup"><span data-stu-id="b7cb0-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="b7cb0-107">Versões com suporte do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="b7cb0-108">Planejando o uso do App-V com versões coexistentes do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="b7cb0-109">Como o Office se integra ao Windows ao implantar usar o App-V para implantar o Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="b7cb0-110">Suporte do App-V para pacotes de idiomas</span><span class="sxs-lookup"><span data-stu-id="b7cb0-110">App-V support for Language Packs</span></span>


<span data-ttu-id="b7cb0-111">Você pode usar o sequenciador do App-V 5,1 para criar pacotes de plug-in para pacotes de idiomas, pacotes de interface de idioma, revisores de ferramenta e idiomas de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-111">You can use the App-V 5.1 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="b7cb0-112">Em seguida, você pode incluir os pacotes de plug-in em um grupo de conexão, juntamente com o pacote do Office 2013 que você cria usando o kit de ferramentas de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="b7cb0-113">Os pacotes de idiomas do plug-in e os aplicativos do Office interagem perfeitamente no mesmo grupo de conexão, assim como qualquer outro pacote agrupado em um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

><span data-ttu-id="b7cb0-114">**Observação**  O Microsoft Visio e o Microsoft Project não oferecem suporte para o pacote de idiomas do tailandês.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="b7cb0-115">Versões com suporte do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-115">Supported versions of Microsoft Office</span></span>

<span data-ttu-id="b7cb0-116">Consulte as [IDs de produto do Microsoft Office que o App-V suporta](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) para uma lista de produtos do Office com suporte.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-116">See [Microsoft Office Product IDs that App-V supports](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) for a list of supported Office products.</span></span>
><span data-ttu-id="b7cb0-117">**Note** &nbsp; Observação &nbsp; Você deve usar a ferramenta de implantação do Office para criar pacotes do App-V para aplicativos do Microsoft 365 para empresas.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-117">**Note**&nbsp;&nbsp;You must use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="b7cb0-118">Não há suporte para a criação de pacotes para versões de licença de volume do Office Professional Plus ou do Office Standard.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-118">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span> <span data-ttu-id="b7cb0-119">Não é possível usar o sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-119">You cannot use the App-V Sequencer.</span></span>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="b7cb0-120">Planejando o uso do App-V com versões coexistentes do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-120">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="b7cb0-121">Você pode instalar mais de uma versão do Microsoft Office lado a lado no mesmo computador usando a "coexistência do Microsoft Office".</span><span class="sxs-lookup"><span data-stu-id="b7cb0-121">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="b7cb0-122">Você pode implementar a coexistência do Office com as combinações de todas as versões principais do Office e com métodos de instalação, conforme aplicável, usando a versão do Office com base no Windows Installer (MSi) do Office, clique para executar e App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-122">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.1.</span></span> <span data-ttu-id="b7cb0-123">No entanto, o uso de coexistência do Office não é recomendado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-123">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="b7cb0-124">A prática recomendada pela Microsoft é evitar a coexistência do Office completamente para evitar problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-124">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="b7cb0-125">No entanto, ao migrar para uma versão mais recente do Office, os problemas surgem ocasionalmente que não podem ser resolvidos imediatamente, portanto, você pode implementar a coexistência temporariamente para facilitar uma migração mais recente para a versão mais recente do produto.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-125">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="b7cb0-126">Usar a coexistência do Office em uma base de longo prazo nunca é recomendado, e sua organização deve ter um plano para fazer toda a transição no futuro imediato.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-126">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="b7cb0-127">Antes de implementar a coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-127">Before you implement Office coexistence</span></span>

<span data-ttu-id="b7cb0-128">Antes de implementar a coexistência do Office, examine a seguinte documentação do Office.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-128">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="b7cb0-129">Escolha o artigo que corresponde à versão mais recente do Office para a qual você planeja implementar a coexistência.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-129">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b7cb0-130">Versão do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-130">Office version</span></span></th>
<th align="left"><span data-ttu-id="b7cb0-131">Link para diretrizes</span><span class="sxs-lookup"><span data-stu-id="b7cb0-131">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-132">Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7cb0-132">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="b7cb0-133">Informações sobre como usar os pacotes e programas do Office 2013 (implantação do MSI) em um computador que esteja executando outra versão do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-133">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-134">Office 2010</span><span class="sxs-lookup"><span data-stu-id="b7cb0-134">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="b7cb0-135">Informações sobre como usar os pacotes e programas do Office 2010 em um computador que esteja executando outra versão do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-135">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b7cb0-136">A documentação do Office fornece diretrizes abrangentes sobre a coexistência para instalações do Windows Installer (MSi) e com Clique para executar do Office.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-136">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="b7cb0-137">Este tópico do App-V na coexistência suplementa a orientação do Office com informações que são mais específicas para implantações do App-V.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-137">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="b7cb0-138">Cenários de coexistência do Office com suporte</span><span class="sxs-lookup"><span data-stu-id="b7cb0-138">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="b7cb0-139">As tabelas a seguir resumem os cenários de coexistência com suporte.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-139">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="b7cb0-140">Elas são organizadas de acordo com a versão e o método de implantação com o qual você está começando e o método de versão e implantação para o qual você está migrando.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-140">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="b7cb0-141">Certifique-se de testar completamente todas as soluções de coexistência antes de implantá-las em um público de produção.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-141">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

><span data-ttu-id="b7cb0-142">**Observação**  A Microsoft não oferece suporte ao uso de várias versões do Office em ambientes Windows Server com o serviço de função de host da sessão da área de trabalho remota habilitado.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-142">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="b7cb0-143">Para executar cenários de coexistência do Office, você deve desabilitar esse serviço de função.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-143">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="b7cb0-144">Integrações do Windows & a coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-144">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="b7cb0-145">Os métodos de instalação do Office para Windows Installer e com Clique para executar integram-se com determinados pontos do sistema operacional Windows subjacente.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-145">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="b7cb0-146">Quando você usa a coexistência, as integrações comuns do sistema operacional entre duas versões do Office podem entrar em conflito, causando problemas de compatibilidade e experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-146">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="b7cb0-147">Com o App-V, você pode sequenciar determinadas versões do Office para excluir as integrações, portanto "isolando"-as do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-147">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="b7cb0-148">Modo em que o App-V pode sequenciar esta versão do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-148">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-149">Office 2007</span><span class="sxs-lookup"><span data-stu-id="b7cb0-149">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-150">Sempre não integrado.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-150">Always non-integrated.</span></span> <span data-ttu-id="b7cb0-151">O App-V não oferece integrações de sistema operacional com uma versão virtualizada do Office 2007.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-151">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-152">Office 2010</span><span class="sxs-lookup"><span data-stu-id="b7cb0-152">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-153">Modo integrado e não integrado.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-153">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-154">Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7cb0-154">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-155">Sempre integrado.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-155">Always integrated.</span></span> <span data-ttu-id="b7cb0-156">Não é possível desabilitar as integrações do sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-156">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b7cb0-157">A Microsoft recomenda que você implante a coexistência do Office com apenas uma instância integrada do Office.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-157">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="b7cb0-158">Por exemplo, se você estiver usando o App-V para implantar o Office 2010 e o Office 2013, você deve sequenciar o Office 2010 no modo não integrado.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-158">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="b7cb0-159">Para obter mais informações sobre o sequenciamento do Office no modo não integração (isolado), consulte [como sequenciar o Microsoft office 2010 no Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="b7cb0-159">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="b7cb0-160">Limitações conhecidas dos cenários de coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-160">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="b7cb0-161">As seções a seguir descrevem alguns problemas que você pode encontrar ao usar o App-V para implementar a coexistência com o Office.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-161">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="b7cb0-162">Limitações comuns em cenários de coexistência do Office com base no Windows Installer/com Clique para executar e App-V</span><span class="sxs-lookup"><span data-stu-id="b7cb0-162">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="b7cb0-163">As seguintes limitações podem ocorrer quando você instala as seguintes versões do Office no mesmo computador:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-163">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="b7cb0-164">O Office 2010 usando a versão baseada no Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b7cb0-164">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="b7cb0-165">Office 2013 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="b7cb0-165">Office 2013 by using App-V</span></span>

<span data-ttu-id="b7cb0-166">Após a publicação do Office 2013 usando o App-V lado a lado com uma versão anterior do Office 2010 baseado no Windows Installer também pode fazer com que o Windows Installer seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-166">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="b7cb0-167">Isso ocorre porque a versão baseada no Windows Installer ou clique para executar do Office 2010 está tentando registrar-se automaticamente no computador.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-167">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="b7cb0-168">Para ignorar a operação de registro automático do Word nativo do Word 2010, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-168">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="b7cb0-169">Saia do Word 2010.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-169">Exit Word 2010.</span></span>

2.  <span data-ttu-id="b7cb0-170">Inicie o editor do registro fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-170">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="b7cb0-171">No Windows 7: clique em **Iniciar**, digite **regedit** na caixa Iniciar pesquisa e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-171">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="b7cb0-172">No Windows 8,1 ou no Windows 10, digite **regedit** e pressione Enter na página inicial e, em seguida, pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-172">In Windows 8.1 or Windows 10, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="b7cb0-173">Se for solicitada uma senha de administrador ou uma confirmação, digite a senha ou clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-173">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="b7cb0-174">Localize e selecione a seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-174">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="b7cb0-175">No menu **Editar** , clique em **novo**e, em seguida, clique em **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-175">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="b7cb0-176">Digite **NoReReg**e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-176">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="b7cb0-177">Clique com o botão direito do mouse em **NoReReg** e clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-177">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="b7cb0-178">Na caixa **ValueData** , digite **1**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-178">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="b7cb0-179">No menu arquivo, clique em **sair** para fechar o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-179">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="b7cb0-180">Como o Office se integra ao Windows quando você usa o App-V para implantar o Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-180">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="b7cb0-181">Ao implantar o Office 2013 usando o App-V, o Office é totalmente integrado ao sistema operacional, que fornece aos usuários finais os mesmos recursos e funcionalidades que o Office tem quando ele é implantado sem App-V.</span><span class="sxs-lookup"><span data-stu-id="b7cb0-181">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="b7cb0-182">O pacote do Office 2013 App-V é compatível com os seguintes pontos de integração com o sistema operacional Windows:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-182">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b7cb0-183">Ponto de extensão</span><span class="sxs-lookup"><span data-stu-id="b7cb0-183">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="b7cb0-184">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7cb0-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-185">Plug-in de junção de reunião do Lync para Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="b7cb0-185">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-186">O usuário pode ingressar em reuniões do Lync a partir do Firefox e do Chrome</span><span class="sxs-lookup"><span data-stu-id="b7cb0-186">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-187">Enviado para o driver de impressão do OneNote</span><span class="sxs-lookup"><span data-stu-id="b7cb0-187">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-188">O usuário pode imprimir no OneNote</span><span class="sxs-lookup"><span data-stu-id="b7cb0-188">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-189">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="b7cb0-189">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-190">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="b7cb0-190">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-191">Enviar para o suplemento do OneNote para Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b7cb0-191">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-192">O usuário pode enviar para o OneNote do IE</span><span class="sxs-lookup"><span data-stu-id="b7cb0-192">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-193">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="b7cb0-193">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-194">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="b7cb0-194">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-195">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="b7cb0-195">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-196">Os aplicativos e suplementos nativos podem interagir com o Outlook virtual por MAPI</span><span class="sxs-lookup"><span data-stu-id="b7cb0-196">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-197">Plug-in do SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="b7cb0-197">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-198">O usuário pode usar os recursos do SharePoint no Firefox</span><span class="sxs-lookup"><span data-stu-id="b7cb0-198">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-199">Applet do painel de controle de email</span><span class="sxs-lookup"><span data-stu-id="b7cb0-199">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-200">O usuário Obtém o applet do painel de controle de email no Outlook</span><span class="sxs-lookup"><span data-stu-id="b7cb0-200">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-201">Assemblies de interoperabilidade primária</span><span class="sxs-lookup"><span data-stu-id="b7cb0-201">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-202">Suporte a suplementos gerenciados</span><span class="sxs-lookup"><span data-stu-id="b7cb0-202">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-203">Manipulador do cache de documentos do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-203">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-204">Permite o cache de documentos para aplicativos do Office</span><span class="sxs-lookup"><span data-stu-id="b7cb0-204">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-205">Manipulador de pesquisa de protocolo do Outlook</span><span class="sxs-lookup"><span data-stu-id="b7cb0-205">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-206">O usuário pode pesquisar no Outlook</span><span class="sxs-lookup"><span data-stu-id="b7cb0-206">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-207">Controles ActiveX:</span><span class="sxs-lookup"><span data-stu-id="b7cb0-207">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-208">Para obter mais informações sobre controles ActiveX, consulte <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> referência da API do controle ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="b7cb0-208">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-209">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="b7cb0-209">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-210">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-210">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-211">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="b7cb0-211">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-212">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-212">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-213">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="b7cb0-213">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-214">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-214">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-215">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="b7cb0-215">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-216">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-216">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-217">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="b7cb0-217">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-218">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-218">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-219">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="b7cb0-219">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-220">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-220">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-221">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="b7cb0-221">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-222">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-222">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-223">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="b7cb0-223">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-224">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-224">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-225">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="b7cb0-225">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-226">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-226">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-227">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="b7cb0-227">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-228">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-228">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-229">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="b7cb0-229">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-230">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-230">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-231">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="b7cb0-231">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-232">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-232">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-233">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="b7cb0-233">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-234">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-234">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-235">CommunicatorMeetingJoinAx. Joinmanager</span><span class="sxs-lookup"><span data-stu-id="b7cb0-235">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-236">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-236">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b7cb0-237">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="b7cb0-237">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-238">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="b7cb0-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b7cb0-239">Auxiliar do navegador do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="b7cb0-239">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-240">Controle ActiveX]</span><span class="sxs-lookup"><span data-stu-id="b7cb0-240">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-241">Sobreposições de ícones do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="b7cb0-241">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="b7cb0-242">O ícone do shell do Windows Explorer se sobrepõe quando os usuários confiram pastas pastas do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="b7cb0-242">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-243">Extensões de shell</span><span class="sxs-lookup"><span data-stu-id="b7cb0-243">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b7cb0-244">Teclado</span><span class="sxs-lookup"><span data-stu-id="b7cb0-244">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b7cb0-245">Windows Search</span><span class="sxs-lookup"><span data-stu-id="b7cb0-245">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





