---
title: Lista de verificação criar, editar e implantar um GPO
description: Lista de verificação criar, editar e implantar um GPO
author: dansimp
ms.assetid: a7a17706-304a-4455-9ada-52508ec620f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35255926ba2384e2942900fc30eae06a30049a15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797459"
---
# <span data-ttu-id="27e4a-103">Lista de verificação: Criar, editar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="27e4a-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="27e4a-104">Em um ambiente onde várias pessoas fazem alterações nos objetos de política de grupo (GPOs) usando o gerenciamento avançado de política de grupo (AGPM), um administrador do AGPM (controle total) delega permissão para editores, Aprovadores e revisores, como grupos ou como indivíduos.</span><span class="sxs-lookup"><span data-stu-id="27e4a-104">In an environment where multiple people make changes to Group Policy Objects (GPOs) using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="27e4a-105">Veja a seguir um processo típico de desenvolvimento de GPOs para um editor e um Aprovador.</span><span class="sxs-lookup"><span data-stu-id="27e4a-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27e4a-106">Tarefa</span><span class="sxs-lookup"><span data-stu-id="27e4a-106">Task</span></span></th>
<th align="left"><span data-ttu-id="27e4a-107">Referência</span><span class="sxs-lookup"><span data-stu-id="27e4a-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27e4a-108">O editor solicita a criação de um novo GPO ou um Aprovador cria um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="27e4a-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm30ops.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)"><span data-ttu-id="27e4a-109">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="27e4a-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm30ops.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm30ops.md)"><span data-ttu-id="27e4a-110">Criar um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="27e4a-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27e4a-111">O aprovador aprova a criação do GPO se ele foi solicitado por um editor.</span><span class="sxs-lookup"><span data-stu-id="27e4a-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm30ops.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm30ops.md)"><span data-ttu-id="27e4a-112">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="27e4a-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27e4a-113">O editor faz check-out de uma cópia do GPO do arquivamento, para que ninguém mais possa modificar o GPO.</span><span class="sxs-lookup"><span data-stu-id="27e4a-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="27e4a-114">O editor faz alterações no GPO e, em seguida, verifica o GPO modificado no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="27e4a-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm30ops.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm30ops.md)"><span data-ttu-id="27e4a-115">Editar um GPO offline</span><span class="sxs-lookup"><span data-stu-id="27e4a-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27e4a-116">O editor solicita a implantação do GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="27e4a-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm30ops.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm30ops.md)"><span data-ttu-id="27e4a-117">Solicitar a implantação de um GPO</span><span class="sxs-lookup"><span data-stu-id="27e4a-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27e4a-118">Revisores, como aprovadores ou editores, analise o GPO.</span><span class="sxs-lookup"><span data-stu-id="27e4a-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm30ops.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md)"><span data-ttu-id="27e4a-119">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="27e4a-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27e4a-120">O aprovador aprova e implanta o GPO no ambiente de produção ou rejeita o GPO.</span><span class="sxs-lookup"><span data-stu-id="27e4a-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm30ops.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm30ops.md)"><span data-ttu-id="27e4a-121">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="27e4a-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="27e4a-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="27e4a-122">Additional references</span></span>

[<span data-ttu-id="27e4a-123">Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="27e4a-123">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





