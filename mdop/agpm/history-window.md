---
title: Janela Histórico
description: Janela Histórico
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797795"
---
# <span data-ttu-id="fb793-103">Janela Histórico</span><span class="sxs-lookup"><span data-stu-id="fb793-103">History Window</span></span>


<span data-ttu-id="fb793-104">O histórico de um objeto de política de grupo (GPO) pode ser exibido clicando duas vezes em um GPO ou clicando com o botão direito do mouse em um GPO e, em seguida, clicando em **histórico**.</span><span class="sxs-lookup"><span data-stu-id="fb793-104">The history of a Group Policy object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="fb793-105">Ele também é exibido no GPMC ( **console de gerenciamento de política de grupo** ) como uma guia para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="fb793-106">O histórico fornece uma lista de todas as versões do GPO selecionado salvas no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="fb793-106">The history provides a list of all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="fb793-107">Na janela do **histórico** , você pode obter um relatório das configurações dentro de um GPO, comparar várias versões de um GPO ou retornar a uma versão anterior de um GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-107">From the **History** window, you can obtain a report of the settings within a GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="fb793-108">Filtrar eventos na janela de histórico</span><span class="sxs-lookup"><span data-stu-id="fb793-108">Filtering events in the History window</span></span>


<span data-ttu-id="fb793-109">As guias dentro da janela do **histórico** filtram os eventos exibidos.</span><span class="sxs-lookup"><span data-stu-id="fb793-109">The tabs within the **History** window filter the events displayed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb793-110">Guias</span><span class="sxs-lookup"><span data-stu-id="fb793-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="fb793-111">Filtre</span><span class="sxs-lookup"><span data-stu-id="fb793-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-112">Mostrar tudo</span><span class="sxs-lookup"><span data-stu-id="fb793-112">Show All</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-113">Exibir todas as versões do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-113">Display all versions of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-114">Check-in</span><span class="sxs-lookup"><span data-stu-id="fb793-114">Checked In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-115">Exiba somente as versões com check-in do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-115">Display only checked-in versions of the GPO.</span></span> <span data-ttu-id="fb793-116">A versão implantada é omitida nesta lista.</span><span class="sxs-lookup"><span data-stu-id="fb793-116">The deployed version is omitted from this list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-117">Somente rótulos</span><span class="sxs-lookup"><span data-stu-id="fb793-117">Labels Only</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-118">Exiba somente os GPOs que têm rótulos associados a eles.</span><span class="sxs-lookup"><span data-stu-id="fb793-118">Display only GPOs that have labels associated with them.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fb793-119">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="fb793-119">Event information</span></span>


<span data-ttu-id="fb793-120">As informações são fornecidas para cada evento no histórico do GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="fb793-120">Information is provided for each event in the history of the selected GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb793-121">Característica do GPO</span><span class="sxs-lookup"><span data-stu-id="fb793-121">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="fb793-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb793-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-123">Computador</span><span class="sxs-lookup"><span data-stu-id="fb793-123">Computer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-124">Versão gerada automaticamente da parte de configuração do computador do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-124">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-125">Usuário</span><span class="sxs-lookup"><span data-stu-id="fb793-125">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-126">Versão gerada automaticamente da parte de configuração do usuário do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-126">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-127">Hora</span><span class="sxs-lookup"><span data-stu-id="fb793-127">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-128">Carimbo de data/hora da versão do GPO quando a ação no campo status foi executada.</span><span class="sxs-lookup"><span data-stu-id="fb793-128">Timestamp of the version of the GPO when the action in the status field was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-129">Estado</span><span class="sxs-lookup"><span data-stu-id="fb793-129">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-130">O estado da versão selecionada do GPO:</span><span class="sxs-lookup"><span data-stu-id="fb793-130">The state of the selected version of the GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="fb793-131">Implantada </strong> : esta versão do GPO está atualmente em tempo real no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="fb793-131">Deployed</strong>: This version of the GPO is currently live in the production environment.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="fb793-132">Check-in </strong> : esta versão do GPO está disponível para editores autorizados a fazer check-out para edição ou para a implantação de um administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="fb793-132">Checked In</strong>: This version of the GPO is available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="fb793-133">Check-out </strong> : esta versão do GPO atualmente está com check-out por um editor e não está disponível para outros editores.</span><span class="sxs-lookup"><span data-stu-id="fb793-133">Checked Out</strong>: This version of the GPO is currently checked out by an Editor and is unavailable for other Editors.</span></span> <span data-ttu-id="fb793-134">(O estado checked out não é registrado no <strong> Histórico </strong> , exceto para indicar se um GPO está em check-out no momento.)</span><span class="sxs-lookup"><span data-stu-id="fb793-134">(The checked out state is not recorded in the <strong>History</strong> except to indicate if a GPO is currently checked out.)</span></span></p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong><span data-ttu-id="fb793-135">Criado </strong> : identifica a data e a hora da criação inicial do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-135">Created</strong>: Identifies the date and time of the initial creation of the GPO.</span></span></p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong><span data-ttu-id="fb793-136">Rotulado </strong> : identifica uma versão rotulada do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-136">Labeled</strong>: Identifies a labeled version of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-137">Status do GPO</span><span class="sxs-lookup"><span data-stu-id="fb793-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-138">A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente umas das outras.</span><span class="sxs-lookup"><span data-stu-id="fb793-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="fb793-139">Esse status mostra quais partes do GPO estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="fb793-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-140">Proprietário</span><span class="sxs-lookup"><span data-stu-id="fb793-140">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-141">A pessoa que fez check-in ou implantou o GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-141">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-142">Comentário</span><span class="sxs-lookup"><span data-stu-id="fb793-142">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-143">Um comentário inserido pelo proprietário de um GPO no momento em que essa versão foi modificada.</span><span class="sxs-lookup"><span data-stu-id="fb793-143">A comment entered by the owner of a GPO at the time that this version was modified.</span></span> <span data-ttu-id="fb793-144">Útil para identificar as especificidades da versão em caso de necessidade de reverter para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="fb793-144">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fb793-145">Relatórios</span><span class="sxs-lookup"><span data-stu-id="fb793-145">Reports</span></span>


<span data-ttu-id="fb793-146">Dependendo se uma única versão do GPO ou várias versões do GPO estiverem selecionadas, os botões **configurações** e **diferenças** exibirão relatórios sobre as configurações do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-146">Depending on whether a single GPO version or multiple GPO versions are selected, the **Settings** and **Differences** buttons display reports on GPO settings.</span></span> <span data-ttu-id="fb793-147">Clicar com o botão direito do mouse em versões do GPO fornece a opção de exibir relatórios baseados em XML também.</span><span class="sxs-lookup"><span data-stu-id="fb793-147">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb793-148">Botão</span><span class="sxs-lookup"><span data-stu-id="fb793-148">Button</span></span></th>
<th align="left"><span data-ttu-id="fb793-149">Efeito</span><span class="sxs-lookup"><span data-stu-id="fb793-149">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-150">Configurações</span><span class="sxs-lookup"><span data-stu-id="fb793-150">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-151">Gerar um relatório baseado em HTML exibindo as configurações dentro da versão selecionada do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-151">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-152">Existentes</span><span class="sxs-lookup"><span data-stu-id="fb793-152">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-153">Gerar um relatório baseado em HTML que compara as configurações dentro de várias versões selecionadas do GPO.</span><span class="sxs-lookup"><span data-stu-id="fb793-153">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fb793-154">Chave para relatórios de diferença</span><span class="sxs-lookup"><span data-stu-id="fb793-154">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb793-155">Símbolo</span><span class="sxs-lookup"><span data-stu-id="fb793-155">Symbol</span></span></th>
<th align="left"><span data-ttu-id="fb793-156">Significado</span><span class="sxs-lookup"><span data-stu-id="fb793-156">Meaning</span></span></th>
<th align="left"><span data-ttu-id="fb793-157">Cor</span><span class="sxs-lookup"><span data-stu-id="fb793-157">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb793-158">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="fb793-158">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb793-159">O item existe com configurações idênticas nos dois GPOs</span><span class="sxs-lookup"><span data-stu-id="fb793-159">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb793-160">Varia de acordo com o nível</span><span class="sxs-lookup"><span data-stu-id="fb793-160">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-161">[#]</span><span class="sxs-lookup"><span data-stu-id="fb793-161">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-162">O item existe nos dois GPOs, mas com configurações alteradas</span><span class="sxs-lookup"><span data-stu-id="fb793-162">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb793-163">Chuva</span><span class="sxs-lookup"><span data-stu-id="fb793-163">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb793-164">[-]</span><span class="sxs-lookup"><span data-stu-id="fb793-164">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-165">O item existe somente no primeiro GPO</span><span class="sxs-lookup"><span data-stu-id="fb793-165">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb793-166">Vermelho</span><span class="sxs-lookup"><span data-stu-id="fb793-166">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb793-167">[+]</span><span class="sxs-lookup"><span data-stu-id="fb793-167">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb793-168">O item existe somente no segundo GPO</span><span class="sxs-lookup"><span data-stu-id="fb793-168">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb793-169">Verde</span><span class="sxs-lookup"><span data-stu-id="fb793-169">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="fb793-170">Para itens com configurações alteradas, as configurações alteradas são identificadas quando o item é expandido.</span><span class="sxs-lookup"><span data-stu-id="fb793-170">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="fb793-171">O valor do atributo em cada GPO é exibido na mesma ordem em que os GPOs são exibidos no relatório.</span><span class="sxs-lookup"><span data-stu-id="fb793-171">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="fb793-172">Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens diferentes (um presente somente no primeiro GPO, um presente somente no segundo), em vez de um item alterado.</span><span class="sxs-lookup"><span data-stu-id="fb793-172">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="fb793-173">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="fb793-173">Additional references</span></span>

-   [<span data-ttu-id="fb793-174">Guia Conteúdo</span><span class="sxs-lookup"><span data-stu-id="fb793-174">Contents Tab</span></span>](contents-tab.md)

 

 





