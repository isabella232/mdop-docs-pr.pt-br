---
title: Recursos comuns da guia secundária
description: Recursos comuns da guia secundária
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797455"
---
# <span data-ttu-id="0eba4-103">Recursos comuns da guia secundária</span><span class="sxs-lookup"><span data-stu-id="0eba4-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="0eba4-104">Cada guia secundária tem duas seções:**objetos** e **grupos e usuários**da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="0eba4-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="0eba4-105">Seção objetos de política de grupo</span><span class="sxs-lookup"><span data-stu-id="0eba4-105">Group Policy objects section</span></span>


<span data-ttu-id="0eba4-106">A seção **objetos de política de grupo** exibe uma lista filtrada dos objetos de política de grupo (GPOs) e identifica as características a seguir para cada GPO:</span><span class="sxs-lookup"><span data-stu-id="0eba4-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0eba4-107">Característica do GPO</span><span class="sxs-lookup"><span data-stu-id="0eba4-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="0eba4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0eba4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0eba4-109">Name</span><span class="sxs-lookup"><span data-stu-id="0eba4-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-110">Nome do objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="0eba4-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0eba4-111">Computador (comp.)</span><span class="sxs-lookup"><span data-stu-id="0eba4-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-112">Versão gerada automaticamente da parte de configuração do computador do GPO.</span><span class="sxs-lookup"><span data-stu-id="0eba4-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0eba4-113">Usuário</span><span class="sxs-lookup"><span data-stu-id="0eba4-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-114">Versão gerada automaticamente da parte de configuração do usuário do GPO.</span><span class="sxs-lookup"><span data-stu-id="0eba4-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0eba4-115">Estado</span><span class="sxs-lookup"><span data-stu-id="0eba4-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-116">O estado do GPO selecionado:</span><span class="sxs-lookup"><span data-stu-id="0eba4-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="0eba4-117">Não controlado: </strong> não gerenciado pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="0eba4-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="0eba4-118">Check-in: </strong> disponível para editores autorizados para fazer check-out para edição ou para a implantação de um administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="0eba4-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="0eba4-119">Check-out: </strong> atualmente sendo editado.</span><span class="sxs-lookup"><span data-stu-id="0eba4-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="0eba4-120">Não disponível para outros editores fazer check-out até o editor que o fez check-out ou um administrador do AGPM fazer o check-in.</span><span class="sxs-lookup"><span data-stu-id="0eba4-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="0eba4-121">Pendente: </strong> aguardando aprovação de um administrador de política de grupo antes de ser criado, controlado, implantado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="0eba4-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="0eba4-122">Excluído: </strong> excluído do arquivo morto, mas ainda pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="0eba4-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="0eba4-123">Modelo: </strong> uma versão estática de um GPO para ser usada como ponto de partida ao criar novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="0eba4-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="0eba4-124">Modelo (padrão): </strong> por padrão, esse modelo é o ponto de partida usado durante a criação de um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="0eba4-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0eba4-125">Status do GPO</span><span class="sxs-lookup"><span data-stu-id="0eba4-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-126">A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente.</span><span class="sxs-lookup"><span data-stu-id="0eba4-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="0eba4-127">O status do GPO indica quais partes do GPO estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="0eba4-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0eba4-128">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="0eba4-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-129">Exiba os filtros WMI aplicados a esse GPO.</span><span class="sxs-lookup"><span data-stu-id="0eba4-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="0eba4-130">Os filtros WMI são gerenciados no <strong> nó filtros WMI </strong> do domínio na árvore de console do GPMC.</span><span class="sxs-lookup"><span data-stu-id="0eba4-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0eba4-131">Modificação em</span><span class="sxs-lookup"><span data-stu-id="0eba4-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-132">Para um GPO controlado, a data mais recente em que foi feito o check-in após a modificação ou check-out para ser modificado.</span><span class="sxs-lookup"><span data-stu-id="0eba4-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="0eba4-133">Para um GPO não controlado, a data em que ele foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0eba4-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0eba4-134">Proprietário</span><span class="sxs-lookup"><span data-stu-id="0eba4-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-135">O editor que fez check-in ou o aprovador que implantou o GPO selecionado.</span><span class="sxs-lookup"><span data-stu-id="0eba4-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0eba4-136">Seção grupos e usuários</span><span class="sxs-lookup"><span data-stu-id="0eba4-136">Groups and Users section</span></span>


<span data-ttu-id="0eba4-137">Quando um GPO é selecionado, a seção **grupos e usuários** exibe uma lista dos grupos e usuários com acesso a esse GPO.</span><span class="sxs-lookup"><span data-stu-id="0eba4-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="0eba4-138">As permissões e herança permitidas são exibidas para cada grupo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="0eba4-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="0eba4-139">Um administrador do AGPM pode configurar permissões usando as funções padrão do AGPM (editor, Aprovador e revisor) ou uma combinação personalizada de permissões.</span><span class="sxs-lookup"><span data-stu-id="0eba4-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0eba4-140">Botão</span><span class="sxs-lookup"><span data-stu-id="0eba4-140">Button</span></span></th>
<th align="left"><span data-ttu-id="0eba4-141">Efeito</span><span class="sxs-lookup"><span data-stu-id="0eba4-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0eba4-142">Adicionar</span><span class="sxs-lookup"><span data-stu-id="0eba4-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-143">Adicione uma nova entrada ao descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0eba4-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="0eba4-144">Qualquer usuário ou grupo no Active Directory pode ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0eba4-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0eba4-145">Remover</span><span class="sxs-lookup"><span data-stu-id="0eba4-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-146">Remover a entrada selecionada da lista de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="0eba4-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0eba4-147">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0eba4-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-148">Exibir as propriedades do objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="0eba4-148">Display the properties for the selected object.</span></span> <span data-ttu-id="0eba4-149">A página Propriedades é a mesma exibida para um objeto em <strong> usuários e computadores do Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="0eba4-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0eba4-150">Avançado</span><span class="sxs-lookup"><span data-stu-id="0eba4-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0eba4-151">Abrir o <strong> Editor de lista de controle de acesso </strong> .</span><span class="sxs-lookup"><span data-stu-id="0eba4-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0eba4-152">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="0eba4-152">Additional considerations</span></span>

-   <span data-ttu-id="0eba4-153">Para obter informações sobre funções e permissões relacionadas a tarefas específicas, consulte as tarefas em [executando tarefas do administrador do AGPM](performing-agpm-administrator-tasks.md), [executando tarefas do editor](performing-editor-tasks.md), [executando tarefas do aprovador](performing-approver-tasks.md)e [executando tarefas do revisor](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="0eba4-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="0eba4-154">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="0eba4-154">Additional references</span></span>

-   [<span data-ttu-id="0eba4-155">Guia Conteúdo</span><span class="sxs-lookup"><span data-stu-id="0eba4-155">Contents Tab</span></span>](contents-tab.md)

 

 





