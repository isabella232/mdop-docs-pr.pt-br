---
title: Comandos de GPO controlado
description: Comandos de GPO controlado
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797861"
---
# <span data-ttu-id="87bb5-103">Comandos de GPO controlado</span><span class="sxs-lookup"><span data-stu-id="87bb5-103">Controlled GPO Commands</span></span>


<span data-ttu-id="87bb5-104">A guia **controlado** :</span><span class="sxs-lookup"><span data-stu-id="87bb5-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="87bb5-105">Exibe uma lista de objetos de política de grupo (GPOs) gerenciados pelo gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="87bb5-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="87bb5-106">Fornece um menu de atalho com comandos para gerenciar GPOs e para exibir o histórico e relatórios de GPOs.</span><span class="sxs-lookup"><span data-stu-id="87bb5-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="87bb5-107">Exibe uma lista dos grupos e usuários que têm permissão para acessar um GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="87bb5-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="87bb5-108">Clicar com o botão direito do mouse na lista **objetos de política de grupo** nessa guia exibe um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="87bb5-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu.</span></span> <span data-ttu-id="87bb5-109">Esse menu inclui a opção que se aplica às seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="87bb5-109">This menu includes whichever of the following options are applicable.</span></span>

## <span data-ttu-id="87bb5-110">Controle e histórico</span><span class="sxs-lookup"><span data-stu-id="87bb5-110">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87bb5-111">Comando</span><span class="sxs-lookup"><span data-stu-id="87bb5-111">Command</span></span></th>
<th align="left"><span data-ttu-id="87bb5-112">Efeito</span><span class="sxs-lookup"><span data-stu-id="87bb5-112">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-113">Novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="87bb5-113">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-114">Crie um novo GPO com controle de alterações gerenciado por meio do AGPM e implante-o no ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="87bb5-114">Create a new GPO with change control managed through AGPM and deploy it to the production environment of the domain.</span></span> <span data-ttu-id="87bb5-115">Se você não tiver permissão para criar um GPO, será solicitado a enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="87bb5-115">If you do not have permission to create a GPO, you are prompted to submit a request.</span></span> <span data-ttu-id="87bb5-116">(Esta opção será exibida se nenhum GPO for selecionado ao clicar com o <strong> botão direito do mouse na Lista de objetos de política de grupo </strong> .)</span><span class="sxs-lookup"><span data-stu-id="87bb5-116">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-117">Histórico</span><span class="sxs-lookup"><span data-stu-id="87bb5-117">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-118">Abrir uma janela listando todas as versões do GPO selecionado salvas no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="87bb5-118">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="87bb5-119">No histórico, você pode obter um relatório das configurações dentro de um GPO, comparar duas versões de um GPO, comparar um GPO a um modelo ou retornar a uma versão anterior de um GPO.</span><span class="sxs-lookup"><span data-stu-id="87bb5-119">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87bb5-120">Relatórios</span><span class="sxs-lookup"><span data-stu-id="87bb5-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87bb5-121">Comando</span><span class="sxs-lookup"><span data-stu-id="87bb5-121">Command</span></span></th>
<th align="left"><span data-ttu-id="87bb5-122">Efeito</span><span class="sxs-lookup"><span data-stu-id="87bb5-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-123">Configurações</span><span class="sxs-lookup"><span data-stu-id="87bb5-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-124">Gerar um relatório baseado em HTML ou baseado em XML exibindo as configurações no GPO selecionado ou exibir links para o (s) GPO (s) selecionado (s) de unidades organizacionais a partir de quando o (s) GPO (s) foi (m) mais recentemente controlado, importado ou check-in.</span><span class="sxs-lookup"><span data-stu-id="87bb5-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-125">Existentes</span><span class="sxs-lookup"><span data-stu-id="87bb5-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-126">Gerar um relatório baseado em HTML ou baseado em XML para comparar as configurações dentro de dois GPOs selecionados ou no GPO selecionado e um modelo.</span><span class="sxs-lookup"><span data-stu-id="87bb5-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87bb5-127">Edição</span><span class="sxs-lookup"><span data-stu-id="87bb5-127">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87bb5-128">Comando</span><span class="sxs-lookup"><span data-stu-id="87bb5-128">Command</span></span></th>
<th align="left"><span data-ttu-id="87bb5-129">Efeito</span><span class="sxs-lookup"><span data-stu-id="87bb5-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-130">Editar</span><span class="sxs-lookup"><span data-stu-id="87bb5-130">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-131">Abrir a <strong> janela do editor de gerenciamento de política de grupo </strong> para alterar o GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="87bb5-131">Open the <strong>Group Policy Management Editor</strong> window to change the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-132">Fazer Check-out</span><span class="sxs-lookup"><span data-stu-id="87bb5-132">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-133">Obtenha uma cópia do GPO selecionado do arquivo para edição offline e proíba a qualquer pessoa de editar o GPO até que ele seja novamente verificado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="87bb5-133">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing the GPO until it is checked back into the archive.</span></span> <span data-ttu-id="87bb5-134">O check-out pode ser substituído por um administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="87bb5-134">Check Out can be overridden by an AGPM Administrator (Full Control).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-135">Fazer Check-in</span><span class="sxs-lookup"><span data-stu-id="87bb5-135">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-136">Verifique a versão editada do GPO selecionado no arquivo morto para que outros editores autorizados possam fazer alterações ou um Aprovador possa implantar o GPO no ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="87bb5-136">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy the GPO to the production environment of the domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-137">Desfazer check-out</span><span class="sxs-lookup"><span data-stu-id="87bb5-137">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-138">Retorne um GPO com check-out para o arquivo sem alterações.</span><span class="sxs-lookup"><span data-stu-id="87bb5-138">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87bb5-139">Gerenciamento de versão</span><span class="sxs-lookup"><span data-stu-id="87bb5-139">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87bb5-140">Comando</span><span class="sxs-lookup"><span data-stu-id="87bb5-140">Command</span></span></th>
<th align="left"><span data-ttu-id="87bb5-141">Efeito</span><span class="sxs-lookup"><span data-stu-id="87bb5-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-142">Importar da produção</span><span class="sxs-lookup"><span data-stu-id="87bb5-142">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-143">Para o GPO selecionado, copie a versão no ambiente de produção do domínio para o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="87bb5-143">For the selected GPO, copy the version in the production environment of the domain to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-144">Importar do arquivo</span><span class="sxs-lookup"><span data-stu-id="87bb5-144">Import from File</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-145">Substitua as configurações de política do GPO selecionado e com check-out por aquelas de um arquivo de backup de GPO.</span><span class="sxs-lookup"><span data-stu-id="87bb5-145">Replace the policy settings of the selected, checked-out GPO with those from a GPO backup file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-146">Excluir</span><span class="sxs-lookup"><span data-stu-id="87bb5-146">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-147">Mova o GPO selecionado para a lixeira e indique se deseja sair da versão implantada (se houver) em produção ou excluir a versão implantada, além da versão no arquivo.</span><span class="sxs-lookup"><span data-stu-id="87bb5-147">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete the deployed version in addition to the version in the archive.</span></span> <span data-ttu-id="87bb5-148">Se você não tiver permissão para excluir um GPO, será solicitado a enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="87bb5-148">If you do not have permission to delete a GPO, you are prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-149">Implantar</span><span class="sxs-lookup"><span data-stu-id="87bb5-149">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-150">Mova o GPO selecionado que está marcado para o arquivo no ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="87bb5-150">Move the selected GPO that is checked into the archive to the production environment of the domain.</span></span> <span data-ttu-id="87bb5-151">Essa ação faz com que ela seja ativada na rede e substitui a versão ativa anteriormente do GPO, se houver uma existente.</span><span class="sxs-lookup"><span data-stu-id="87bb5-151">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="87bb5-152">Se você não tiver permissão para implantar um GPO, será solicitado a enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="87bb5-152">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-153">Exportar para</span><span class="sxs-lookup"><span data-stu-id="87bb5-153">Export to</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-154">Salve o GPO selecionado em um arquivo de backup para que você possa copiá-lo para outro domínio.</span><span class="sxs-lookup"><span data-stu-id="87bb5-154">Save the selected GPO to a backup file so that you can copy it to another domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-155">Rótulo</span><span class="sxs-lookup"><span data-stu-id="87bb5-155">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-156">Marque o GPO selecionado com um rótulo descritivo (como &quot; conhecido como satisfatório &quot; ) e faça um comentário para a manutenção de registros.</span><span class="sxs-lookup"><span data-stu-id="87bb5-156">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="87bb5-157">Os rótulos são exibidos <strong> na </strong> coluna Estado e nos comentários <strong> na </strong> coluna comentário da <strong> janela do histórico </strong> .</span><span class="sxs-lookup"><span data-stu-id="87bb5-157">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window.</span></span> <span data-ttu-id="87bb5-158">Elas ajudam a identificar versões anteriores de um GPO para que você possa reverter se ocorrer um problema.</span><span class="sxs-lookup"><span data-stu-id="87bb5-158">They help you identify earlier versions of a GPO so that you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-159">Renomear</span><span class="sxs-lookup"><span data-stu-id="87bb5-159">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-160">Alterar o nome do GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="87bb5-160">Change the name of the selected GPO.</span></span> <span data-ttu-id="87bb5-161">Se o GPO já tiver sido implantado, o nome será atualizado no ambiente de produção do domínio quando o GPO for reimplantado.</span><span class="sxs-lookup"><span data-stu-id="87bb5-161">If the GPO has already been deployed, the name will be updated in the production environment of the domain when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-162">Salvar como modelo</span><span class="sxs-lookup"><span data-stu-id="87bb5-162">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-163">Criar um novo modelo com base nas configurações do GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="87bb5-163">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87bb5-164">Diversos</span><span class="sxs-lookup"><span data-stu-id="87bb5-164">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87bb5-165">Comando</span><span class="sxs-lookup"><span data-stu-id="87bb5-165">Command</span></span></th>
<th align="left"><span data-ttu-id="87bb5-166">Efeito</span><span class="sxs-lookup"><span data-stu-id="87bb5-166">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87bb5-167">Atualizar</span><span class="sxs-lookup"><span data-stu-id="87bb5-167">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-168">Atualize a exibição do GPMC (console de gerenciamento de política de grupo) para incorporar alterações.</span><span class="sxs-lookup"><span data-stu-id="87bb5-168">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="87bb5-169">Algumas alterações não ficam visíveis até que a exibição seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="87bb5-169">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="87bb5-170">Ajuda</span><span class="sxs-lookup"><span data-stu-id="87bb5-170">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87bb5-171">Exibir a ajuda do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87bb5-171">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="87bb5-172">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="87bb5-172">Additional references</span></span>

-   [<span data-ttu-id="87bb5-173">Guia Conteúdo</span><span class="sxs-lookup"><span data-stu-id="87bb5-173">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="87bb5-174">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="87bb5-174">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="87bb5-175">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="87bb5-175">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="87bb5-176">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="87bb5-176">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





