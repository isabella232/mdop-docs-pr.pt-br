---
title: Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos
description: Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos
author: dansimp
ms.assetid: 6320afc4-af81-47e8-9f4c-463ff99d5a53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fd7966c9c72b2f0d30595af55520940c779a409f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797789"
---
# <span data-ttu-id="c59ca-103">Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos</span><span class="sxs-lookup"><span data-stu-id="c59ca-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="c59ca-104">Você pode gerar relatórios de diferença baseados em HTML ou baseados em XML para analisar as diferenças entre objetos de política de grupo (GPOs), modelos ou versões diferentes de um GPO.</span><span class="sxs-lookup"><span data-stu-id="c59ca-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="c59ca-105">Uma conta de usuário com a função revisor, editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="c59ca-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="c59ca-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="c59ca-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="c59ca-107">Identificar diferenças entre GPOs, versões de GPO ou modelos</span><span class="sxs-lookup"><span data-stu-id="c59ca-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="c59ca-108">Entre dois GPOs ou modelos</span><span class="sxs-lookup"><span data-stu-id="c59ca-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="c59ca-109">Entre um GPO e um modelo</span><span class="sxs-lookup"><span data-stu-id="c59ca-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="c59ca-110">Entre duas versões de um GPO</span><span class="sxs-lookup"><span data-stu-id="c59ca-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="c59ca-111">Entre uma versão de GPO e um modelo</span><span class="sxs-lookup"><span data-stu-id="c59ca-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="c59ca-112">Para identificar as diferenças entre dois GPOs ou modelos</span><span class="sxs-lookup"><span data-stu-id="c59ca-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="c59ca-113">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="c59ca-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c59ca-114">Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).</span><span class="sxs-lookup"><span data-stu-id="c59ca-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="c59ca-115">Selecione os dois GPOs ou modelos.</span><span class="sxs-lookup"><span data-stu-id="c59ca-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="c59ca-116">Clique com o botão direito do mouse em um dos GPOs ou modelos, clique em **diferenças**e, em seguida, clique em **relatório HTML** ou **relatório XML** para exibir um relatório de diferença Resumindo as configurações dos GPOs ou modelos.</span><span class="sxs-lookup"><span data-stu-id="c59ca-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="c59ca-117">Para identificar as diferenças entre um GPO e um modelo</span><span class="sxs-lookup"><span data-stu-id="c59ca-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="c59ca-118">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="c59ca-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c59ca-119">Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).</span><span class="sxs-lookup"><span data-stu-id="c59ca-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="c59ca-120">Clique com o botão direito do mouse no GPO, clique em **diferenças**e, em seguida, clique em **modelo**.</span><span class="sxs-lookup"><span data-stu-id="c59ca-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="c59ca-121">Selecione o modelo e o tipo de relatório e, em seguida, clique em **OK** para exibir um relatório de diferença Resumindo as configurações do GPO e do modelo.</span><span class="sxs-lookup"><span data-stu-id="c59ca-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="c59ca-122">Para identificar as diferenças entre duas versões de um GPO</span><span class="sxs-lookup"><span data-stu-id="c59ca-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="c59ca-123">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="c59ca-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c59ca-124">Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).</span><span class="sxs-lookup"><span data-stu-id="c59ca-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="c59ca-125">Clique duas vezes no GPO para exibir o histórico e, em seguida, realce as versões a serem comparadas.</span><span class="sxs-lookup"><span data-stu-id="c59ca-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="c59ca-126">Clique com o botão direito do mouse em uma das versões, clique em **diferenças**e, em seguida, clique em **relatório HTML** ou **relatório XML** para exibir um relatório de diferença Resumindo as configurações dos GPOs.</span><span class="sxs-lookup"><span data-stu-id="c59ca-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="c59ca-127">Para identificar as diferenças entre uma versão de GPO e um modelo</span><span class="sxs-lookup"><span data-stu-id="c59ca-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="c59ca-128">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="c59ca-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c59ca-129">Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).</span><span class="sxs-lookup"><span data-stu-id="c59ca-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="c59ca-130">Clique duas vezes no GPO para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="c59ca-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="c59ca-131">Clique com o botão direito do mouse na versão do GPO do interesse, clique em **diferenças**e, em seguida, clique em **modelo**.</span><span class="sxs-lookup"><span data-stu-id="c59ca-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="c59ca-132">Selecione o modelo e o tipo de relatório e, em seguida, clique em **OK** para exibir um relatório de diferença Resumindo as configurações da versão e do modelo do GPO.</span><span class="sxs-lookup"><span data-stu-id="c59ca-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="c59ca-133">Chave para relatórios de diferença</span><span class="sxs-lookup"><span data-stu-id="c59ca-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c59ca-134">Símbolo</span><span class="sxs-lookup"><span data-stu-id="c59ca-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="c59ca-135">Significado</span><span class="sxs-lookup"><span data-stu-id="c59ca-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="c59ca-136">Cor</span><span class="sxs-lookup"><span data-stu-id="c59ca-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c59ca-137">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c59ca-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="c59ca-138">O item existe com configurações idênticas nos dois GPOs</span><span class="sxs-lookup"><span data-stu-id="c59ca-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="c59ca-139">Varia de acordo com o nível</span><span class="sxs-lookup"><span data-stu-id="c59ca-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c59ca-140">[#]</span><span class="sxs-lookup"><span data-stu-id="c59ca-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c59ca-141">O item existe nos dois GPOs, mas com configurações alteradas</span><span class="sxs-lookup"><span data-stu-id="c59ca-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="c59ca-142">Chuva</span><span class="sxs-lookup"><span data-stu-id="c59ca-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c59ca-143">[-]</span><span class="sxs-lookup"><span data-stu-id="c59ca-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c59ca-144">O item existe somente no primeiro GPO</span><span class="sxs-lookup"><span data-stu-id="c59ca-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="c59ca-145">Vermelho</span><span class="sxs-lookup"><span data-stu-id="c59ca-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c59ca-146">[+]</span><span class="sxs-lookup"><span data-stu-id="c59ca-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c59ca-147">O item existe somente no segundo GPO</span><span class="sxs-lookup"><span data-stu-id="c59ca-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="c59ca-148">Verde</span><span class="sxs-lookup"><span data-stu-id="c59ca-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="c59ca-149">Para itens com configurações alteradas, as configurações alteradas são identificadas quando o item é expandido.</span><span class="sxs-lookup"><span data-stu-id="c59ca-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="c59ca-150">O valor do atributo em cada GPO é exibido na mesma ordem em que os GPOs são exibidos no relatório.</span><span class="sxs-lookup"><span data-stu-id="c59ca-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="c59ca-151">Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens diferentes (um presente somente no primeiro GPO, um presente somente no segundo) em vez de um item alterado.</span><span class="sxs-lookup"><span data-stu-id="c59ca-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="c59ca-152">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="c59ca-152">Additional considerations</span></span>

-   <span data-ttu-id="c59ca-153">Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="c59ca-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c59ca-154">Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="c59ca-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="c59ca-155">Além disso, para exibir a lista de GPOs, você deve ter permissão de **lista de conteúdo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="c59ca-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="c59ca-156">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="c59ca-156">Additional references</span></span>

-   [<span data-ttu-id="c59ca-157">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="c59ca-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





