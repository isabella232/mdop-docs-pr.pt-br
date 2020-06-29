---
title: Janela Histórico
description: Janela Histórico
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797797"
---
# <span data-ttu-id="00b96-103">Janela Histórico</span><span class="sxs-lookup"><span data-stu-id="00b96-103">History Window</span></span>


<span data-ttu-id="00b96-104">O histórico de um objeto de política de grupo (GPO) pode ser exibido clicando duas vezes em um GPO ou clicando com o botão direito do mouse em um GPO e, em seguida, clicando em **histórico**.</span><span class="sxs-lookup"><span data-stu-id="00b96-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="00b96-105">Ele também é exibido no GPMC ( **console de gerenciamento de política de grupo** ) como uma guia para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="00b96-106">O histórico fornece um registro de eventos durante o tempo de vida do GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="00b96-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="00b96-107">Na janela do **histórico** , você pode obter um relatório das configurações dentro de uma versão do GPO, comparar várias versões de um GPO ou retornar a uma versão anterior de um GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="00b96-108">Filtrar eventos na janela de histórico</span><span class="sxs-lookup"><span data-stu-id="00b96-108">Filtering events in the History window</span></span>


<span data-ttu-id="00b96-109">As guias dentro da janela do **histórico** filtram os Estados no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="00b96-110">Guias</span><span class="sxs-lookup"><span data-stu-id="00b96-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="00b96-111">Filtre</span><span class="sxs-lookup"><span data-stu-id="00b96-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-112">Todos os Estados</span><span class="sxs-lookup"><span data-stu-id="00b96-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-113">Exibir todos os Estados no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-114">Versões exclusivas</span><span class="sxs-lookup"><span data-stu-id="00b96-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-115">Exiba somente as versões exclusivas do GPO verificado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="00b96-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="00b96-116">A versão implantada no ambiente de produção, atalhos para versões exclusivas e Estados informativos são omitidos nesta lista.</span><span class="sxs-lookup"><span data-stu-id="00b96-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="00b96-117">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="00b96-117">Event information</span></span>


<span data-ttu-id="00b96-118">As informações são fornecidas para cada Estado no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="00b96-119">Atributo GPO</span><span class="sxs-lookup"><span data-stu-id="00b96-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="00b96-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="00b96-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-121">Alterar Data</span><span class="sxs-lookup"><span data-stu-id="00b96-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-122">Carimbo de data/hora em que a ação da <strong> </strong> coluna Estado foi realizada.</span><span class="sxs-lookup"><span data-stu-id="00b96-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-123">Estado</span><span class="sxs-lookup"><span data-stu-id="00b96-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-124">Um estado no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-125">Alterado por</span><span class="sxs-lookup"><span data-stu-id="00b96-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-126">A pessoa que fez check-in ou implantou o GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-127">Comentário</span><span class="sxs-lookup"><span data-stu-id="00b96-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-128">Um comentário inserido pela pessoa que fez check-in ou implantou um GPO no momento em que essa versão foi modificada.</span><span class="sxs-lookup"><span data-stu-id="00b96-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="00b96-129">Útil para identificar as especificidades da versão em caso de necessidade de reverter para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="00b96-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-130">Excluídos</span><span class="sxs-lookup"><span data-stu-id="00b96-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-131">Se essa versão do GPO pode ser excluída se o número de versões exclusivas de cada GPO retido no arquivo for limitado.</span><span class="sxs-lookup"><span data-stu-id="00b96-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="00b96-132">Observação</span><span class="sxs-lookup"><span data-stu-id="00b96-132">Note</span></span></strong><br/><p><span data-ttu-id="00b96-133">Você pode modificar se uma versão de um GPO pode ser excluída clicando com o botão direito do mouse e, em seguida, clicando em não <strong> Permitir exclusão </strong> ou <strong> Permitir exclusão </strong> .</span><span class="sxs-lookup"><span data-stu-id="00b96-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-134">Versão do computador</span><span class="sxs-lookup"><span data-stu-id="00b96-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-135">Versão gerada automaticamente da parte de configuração do computador do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-136">Versão do usuário</span><span class="sxs-lookup"><span data-stu-id="00b96-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-137">Versão gerada automaticamente da parte de configuração do usuário do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-138">Status do GPO</span><span class="sxs-lookup"><span data-stu-id="00b96-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-139">A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente umas das outras.</span><span class="sxs-lookup"><span data-stu-id="00b96-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="00b96-140">Esse status mostra quais partes do GPO estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="00b96-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-141">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="00b96-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-142">Exiba os filtros WMI aplicados a esse GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="00b96-143">Os filtros WMI são gerenciados na <strong> pasta filtros WMI </strong> do domínio na árvore de console do GPMC.</span><span class="sxs-lookup"><span data-stu-id="00b96-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="00b96-144">Relatórios</span><span class="sxs-lookup"><span data-stu-id="00b96-144">Reports</span></span>


<span data-ttu-id="00b96-145">Os botões **configurações** e **diferenças** exibem relatórios sobre as configurações do GPO para a versão do GPO ou versões selecionadas.</span><span class="sxs-lookup"><span data-stu-id="00b96-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="00b96-146">Clicar com o botão direito do mouse em versões do GPO fornece a opção de exibir relatórios baseados em XML também.</span><span class="sxs-lookup"><span data-stu-id="00b96-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="00b96-147">Botão</span><span class="sxs-lookup"><span data-stu-id="00b96-147">Button</span></span></th>
<th align="left"><span data-ttu-id="00b96-148">Efeito</span><span class="sxs-lookup"><span data-stu-id="00b96-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-149">Configurações</span><span class="sxs-lookup"><span data-stu-id="00b96-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-150">Gerar um relatório baseado em HTML exibindo as configurações dentro da versão selecionada do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-151">Existentes</span><span class="sxs-lookup"><span data-stu-id="00b96-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-152">Gerar um relatório baseado em HTML que compara as configurações dentro de várias versões selecionadas do GPO.</span><span class="sxs-lookup"><span data-stu-id="00b96-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="00b96-153">Chave para relatórios de diferença</span><span class="sxs-lookup"><span data-stu-id="00b96-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="00b96-154">Símbolo</span><span class="sxs-lookup"><span data-stu-id="00b96-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="00b96-155">Significado</span><span class="sxs-lookup"><span data-stu-id="00b96-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="00b96-156">Cor</span><span class="sxs-lookup"><span data-stu-id="00b96-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="00b96-157">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="00b96-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="00b96-158">O item existe com configurações idênticas nos dois GPOs</span><span class="sxs-lookup"><span data-stu-id="00b96-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="00b96-159">Varia de acordo com o nível</span><span class="sxs-lookup"><span data-stu-id="00b96-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-160">[#]</span><span class="sxs-lookup"><span data-stu-id="00b96-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-161">O item existe nos dois GPOs, mas com configurações alteradas</span><span class="sxs-lookup"><span data-stu-id="00b96-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="00b96-162">Chuva</span><span class="sxs-lookup"><span data-stu-id="00b96-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="00b96-163">[-]</span><span class="sxs-lookup"><span data-stu-id="00b96-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-164">O item existe somente no primeiro GPO</span><span class="sxs-lookup"><span data-stu-id="00b96-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="00b96-165">Vermelho</span><span class="sxs-lookup"><span data-stu-id="00b96-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="00b96-166">[+]</span><span class="sxs-lookup"><span data-stu-id="00b96-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="00b96-167">O item existe somente no segundo GPO</span><span class="sxs-lookup"><span data-stu-id="00b96-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="00b96-168">Verde</span><span class="sxs-lookup"><span data-stu-id="00b96-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="00b96-169">Para itens com configurações alteradas, as configurações alteradas são identificadas quando o item é expandido.</span><span class="sxs-lookup"><span data-stu-id="00b96-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="00b96-170">O valor do atributo em cada GPO é exibido na mesma ordem em que os GPOs são exibidos no relatório.</span><span class="sxs-lookup"><span data-stu-id="00b96-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="00b96-171">Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens diferentes (um presente somente no primeiro GPO, um presente somente no segundo), em vez de um item alterado.</span><span class="sxs-lookup"><span data-stu-id="00b96-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="00b96-172">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="00b96-172">Additional references</span></span>

-   [<span data-ttu-id="00b96-173">Guia Conteúdo</span><span class="sxs-lookup"><span data-stu-id="00b96-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









