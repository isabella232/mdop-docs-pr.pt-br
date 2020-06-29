---
title: Comandos de modelo
description: Comandos de modelo
author: dansimp
ms.assetid: 243a9b18-bf3f-44fa-94d7-5c793f7322da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2c540bf87462f501a4db5596faca43ef66ee8558
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797295"
---
# <span data-ttu-id="27cff-103">Comandos de modelo</span><span class="sxs-lookup"><span data-stu-id="27cff-103">Template Commands</span></span>


<span data-ttu-id="27cff-104">A guia **modelos** :</span><span class="sxs-lookup"><span data-stu-id="27cff-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="27cff-105">Exibe uma lista de modelos disponíveis que você pode usar para criar novos objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="27cff-105">Displays a list of available templates that you can use to create new Group Policy Objects (GPOs).</span></span>

-   <span data-ttu-id="27cff-106">Fornece um menu de atalho com comandos para criar um GPO com base em um modelo selecionado, gerenciar modelos e exibir relatórios para modelos.</span><span class="sxs-lookup"><span data-stu-id="27cff-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="27cff-107">Exibe uma lista dos grupos e usuários que têm permissão para acessar um modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="27cff-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="27cff-108">Como um modelo não pode ser alterado, os modelos não têm histórico.</span><span class="sxs-lookup"><span data-stu-id="27cff-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="27cff-109">No entanto, como qualquer versão do GPO, as configurações de um modelo podem ser exibidas com um relatório de configurações ou comparadas a outro GPO com um relatório de diferença.</span><span class="sxs-lookup"><span data-stu-id="27cff-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="27cff-110">**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.</span><span class="sxs-lookup"><span data-stu-id="27cff-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="27cff-111">Clicar com o botão direito do mouse na lista **objetos de política de grupo** nessa guia exibe um menu de atalho, incluindo qualquer uma das opções a seguir, que se aplicam.</span><span class="sxs-lookup"><span data-stu-id="27cff-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="27cff-112">Controle</span><span class="sxs-lookup"><span data-stu-id="27cff-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27cff-113">Comando</span><span class="sxs-lookup"><span data-stu-id="27cff-113">Command</span></span></th>
<th align="left"><span data-ttu-id="27cff-114">Efeito</span><span class="sxs-lookup"><span data-stu-id="27cff-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27cff-115">Novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="27cff-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-116">Criar um novo GPO com base no modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="27cff-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="27cff-117">É fornecida a opção para implantar o novo GPO no ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="27cff-117">The option to deploy the new GPO to the production environment of the domain is provided.</span></span> <span data-ttu-id="27cff-118">Se você não tiver permissão para criar um GPO, será solicitado a enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="27cff-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="27cff-119">(Esta opção será exibida se nenhum GPO for selecionado ao clicar com o <strong> botão direito do mouse na Lista de objetos de política de grupo </strong> .)</span><span class="sxs-lookup"><span data-stu-id="27cff-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="27cff-120">Relatórios</span><span class="sxs-lookup"><span data-stu-id="27cff-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27cff-121">Comando</span><span class="sxs-lookup"><span data-stu-id="27cff-121">Command</span></span></th>
<th align="left"><span data-ttu-id="27cff-122">Efeito</span><span class="sxs-lookup"><span data-stu-id="27cff-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27cff-123">Configurações</span><span class="sxs-lookup"><span data-stu-id="27cff-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-124">Gerar um relatório baseado em HTML ou baseado em XML exibindo as configurações dentro do GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="27cff-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27cff-125">Existentes</span><span class="sxs-lookup"><span data-stu-id="27cff-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-126">Gerar um relatório baseado em HTML ou baseado em XML para comparar as configurações dentro de dois modelos de GPO selecionados.</span><span class="sxs-lookup"><span data-stu-id="27cff-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="27cff-127">Gerenciamento de modelos</span><span class="sxs-lookup"><span data-stu-id="27cff-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27cff-128">Comando</span><span class="sxs-lookup"><span data-stu-id="27cff-128">Command</span></span></th>
<th align="left"><span data-ttu-id="27cff-129">Efeito</span><span class="sxs-lookup"><span data-stu-id="27cff-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27cff-130">Definir como padrão</span><span class="sxs-lookup"><span data-stu-id="27cff-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-131">Defina o modelo selecionado como o padrão a ser usado automaticamente ao criar um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="27cff-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27cff-132">Excluir</span><span class="sxs-lookup"><span data-stu-id="27cff-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-133">Mover o modelo selecionado para a <strong> Lixeira </strong> .</span><span class="sxs-lookup"><span data-stu-id="27cff-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="27cff-134">Se você não tiver permissão para excluir um GPO, será solicitado a enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="27cff-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27cff-135">Renomear</span><span class="sxs-lookup"><span data-stu-id="27cff-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-136">Alterar o nome do modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="27cff-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="27cff-137">Diversos</span><span class="sxs-lookup"><span data-stu-id="27cff-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27cff-138">Comando</span><span class="sxs-lookup"><span data-stu-id="27cff-138">Command</span></span></th>
<th align="left"><span data-ttu-id="27cff-139">Efeito</span><span class="sxs-lookup"><span data-stu-id="27cff-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27cff-140">Atualizar</span><span class="sxs-lookup"><span data-stu-id="27cff-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-141">Atualize a exibição do console de gerenciamento de política de grupo para incorporar alterações.</span><span class="sxs-lookup"><span data-stu-id="27cff-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="27cff-142">Algumas alterações não ficam visíveis até que a exibição seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="27cff-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27cff-143">Ajuda</span><span class="sxs-lookup"><span data-stu-id="27cff-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27cff-144">Exibir ajuda para o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="27cff-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="27cff-145">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="27cff-145">Additional references</span></span>

-   [<span data-ttu-id="27cff-146">Guia Conteúdo</span><span class="sxs-lookup"><span data-stu-id="27cff-146">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="27cff-147">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="27cff-147">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="27cff-148">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="27cff-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





