---
title: Janela Histórico
description: Janela Histórico
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797796"
---
# <span data-ttu-id="900ea-103">Janela Histórico</span><span class="sxs-lookup"><span data-stu-id="900ea-103">History Window</span></span>


<span data-ttu-id="900ea-104">O histórico de um objeto de política de grupo (GPO) pode ser exibido clicando duas vezes em um GPO ou clicando com o botão direito do mouse em um GPO e, em seguida, clicando em **histórico**.</span><span class="sxs-lookup"><span data-stu-id="900ea-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="900ea-105">Ele também é exibido no GPMC (console de gerenciamento de política de grupo) como uma guia para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="900ea-106">O histórico fornece um registro de eventos durante o tempo de vida do GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="900ea-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="900ea-107">Na janela do **histórico** , você pode obter um relatório das configurações em uma versão do GPO, comparar várias versões de um GPO ou retornar a uma versão anterior de um GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="900ea-108">Filtrar eventos na janela de histórico</span><span class="sxs-lookup"><span data-stu-id="900ea-108">Filtering events in the History window</span></span>


<span data-ttu-id="900ea-109">As guias dentro da janela do **histórico** filtram os Estados no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="900ea-110">Guias</span><span class="sxs-lookup"><span data-stu-id="900ea-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="900ea-111">Filtre</span><span class="sxs-lookup"><span data-stu-id="900ea-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-112">Todos os Estados</span><span class="sxs-lookup"><span data-stu-id="900ea-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-113">Exibir todos os Estados no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-114">Versões exclusivas</span><span class="sxs-lookup"><span data-stu-id="900ea-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-115">Exiba somente as versões exclusivas do GPO verificado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="900ea-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="900ea-116">A versão implantada no ambiente de produção, atalhos para versões exclusivas e Estados informativos são omitidos nesta lista.</span><span class="sxs-lookup"><span data-stu-id="900ea-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="900ea-117">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="900ea-117">Event information</span></span>


<span data-ttu-id="900ea-118">As informações são fornecidas para cada Estado no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="900ea-119">Atributo GPO</span><span class="sxs-lookup"><span data-stu-id="900ea-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="900ea-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="900ea-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-121">Alterar Data</span><span class="sxs-lookup"><span data-stu-id="900ea-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-122">Carimbo de data/hora em que a ação da <strong> </strong> coluna Estado foi realizada.</span><span class="sxs-lookup"><span data-stu-id="900ea-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-123">Estado</span><span class="sxs-lookup"><span data-stu-id="900ea-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-124">Um estado no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-125">Alterado por</span><span class="sxs-lookup"><span data-stu-id="900ea-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-126">A pessoa que fez check-in ou implantou o GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-127">Comentário</span><span class="sxs-lookup"><span data-stu-id="900ea-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-128">Um comentário inserido pela pessoa que fez check-in ou implantou um GPO no momento em que essa versão foi alterada, útil para identificar as especificidades da versão em caso de necessidade de reverter para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="900ea-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-129">Excluídos</span><span class="sxs-lookup"><span data-stu-id="900ea-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-130">Se essa versão do GPO pode ser excluída se o número de versões exclusivas de cada GPO retido no arquivo for limitado.</span><span class="sxs-lookup"><span data-stu-id="900ea-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="900ea-131">Observação</span><span class="sxs-lookup"><span data-stu-id="900ea-131">Note</span></span></strong><br/><p><span data-ttu-id="900ea-132">Você pode alterar se uma versão de um GPO pode ser excluída clicando com o botão direito do mouse no GPO e clicando em não <strong> Permitir exclusão </strong> ou <strong> Permitir exclusão </strong> .</span><span class="sxs-lookup"><span data-stu-id="900ea-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-133">Versão do computador</span><span class="sxs-lookup"><span data-stu-id="900ea-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-134">Versão gerada automaticamente da parte de configuração do computador do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-135">Versão do usuário</span><span class="sxs-lookup"><span data-stu-id="900ea-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-136">Versão gerada automaticamente da parte de configuração do usuário do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-137">Status do GPO</span><span class="sxs-lookup"><span data-stu-id="900ea-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-138">A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente umas das outras.</span><span class="sxs-lookup"><span data-stu-id="900ea-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="900ea-139">Esse status mostra quais partes do GPO estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="900ea-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-140">Informações do GPO de origem</span><span class="sxs-lookup"><span data-stu-id="900ea-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-141">Para um GPO que tenha sido importado de outra floresta, o nome do GPO original, o domínio e o usuário e a data associados à última alteração.</span><span class="sxs-lookup"><span data-stu-id="900ea-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="900ea-142">Relatórios</span><span class="sxs-lookup"><span data-stu-id="900ea-142">Reports</span></span>


<span data-ttu-id="900ea-143">Os botões **configurações** e **diferenças** exibem relatórios sobre as configurações do GPO para a versão do GPO ou versões selecionadas.</span><span class="sxs-lookup"><span data-stu-id="900ea-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="900ea-144">Além disso, clicar com o botão direito do mouse em uma versão de GPO ou em versões fornece a opção para exibir relatórios baseados em XML.</span><span class="sxs-lookup"><span data-stu-id="900ea-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="900ea-145">Botão</span><span class="sxs-lookup"><span data-stu-id="900ea-145">Button</span></span></th>
<th align="left"><span data-ttu-id="900ea-146">Efeito</span><span class="sxs-lookup"><span data-stu-id="900ea-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-147">Configurações</span><span class="sxs-lookup"><span data-stu-id="900ea-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-148">Gerar um relatório baseado em HTML exibindo as configurações dentro da versão selecionada do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-149">Existentes</span><span class="sxs-lookup"><span data-stu-id="900ea-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-150">Gerar um relatório baseado em HTML que compara as configurações dentro de várias versões selecionadas do GPO.</span><span class="sxs-lookup"><span data-stu-id="900ea-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="900ea-151">Chave para relatórios de diferença</span><span class="sxs-lookup"><span data-stu-id="900ea-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="900ea-152">Símbolo</span><span class="sxs-lookup"><span data-stu-id="900ea-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="900ea-153">Significado</span><span class="sxs-lookup"><span data-stu-id="900ea-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="900ea-154">Cor</span><span class="sxs-lookup"><span data-stu-id="900ea-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="900ea-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="900ea-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="900ea-156">O item existe com configurações idênticas nos dois GPOs</span><span class="sxs-lookup"><span data-stu-id="900ea-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="900ea-157">Varia de acordo com o nível</span><span class="sxs-lookup"><span data-stu-id="900ea-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-158">[#]</span><span class="sxs-lookup"><span data-stu-id="900ea-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-159">O item existe nos dois GPOs, mas com configurações alteradas</span><span class="sxs-lookup"><span data-stu-id="900ea-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="900ea-160">Chuva</span><span class="sxs-lookup"><span data-stu-id="900ea-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="900ea-161">[-]</span><span class="sxs-lookup"><span data-stu-id="900ea-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-162">O item existe somente no primeiro GPO</span><span class="sxs-lookup"><span data-stu-id="900ea-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="900ea-163">Vermelho</span><span class="sxs-lookup"><span data-stu-id="900ea-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="900ea-164">[+]</span><span class="sxs-lookup"><span data-stu-id="900ea-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="900ea-165">O item existe somente no segundo GPO</span><span class="sxs-lookup"><span data-stu-id="900ea-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="900ea-166">Verde</span><span class="sxs-lookup"><span data-stu-id="900ea-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="900ea-167">Para itens com configurações alteradas, as configurações alteradas são identificadas quando o item é expandido.</span><span class="sxs-lookup"><span data-stu-id="900ea-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="900ea-168">O valor do atributo em cada GPO é exibido na mesma ordem em que os GPOs são exibidos no relatório.</span><span class="sxs-lookup"><span data-stu-id="900ea-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="900ea-169">Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens (um presente somente no primeiro GPO, um presente somente no segundo), em vez de um item alterado.</span><span class="sxs-lookup"><span data-stu-id="900ea-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="900ea-170">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="900ea-170">Additional references</span></span>

-   [<span data-ttu-id="900ea-171">Guia Conteúdo</span><span class="sxs-lookup"><span data-stu-id="900ea-171">Contents Tab</span></span>](contents-tab-agpm40.md)









