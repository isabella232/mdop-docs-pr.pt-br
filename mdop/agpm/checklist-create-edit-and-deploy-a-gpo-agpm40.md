---
title: Lista de verificação criar, editar e implantar um GPO
description: Lista de verificação criar, editar e implantar um GPO
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797458"
---
# <span data-ttu-id="5cba7-103">Lista de verificação: Criar, editar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="5cba7-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="5cba7-104">Em um ambiente em que várias pessoas alteram objetos de política de grupo (GPOs) usando o gerenciamento avançado de política de grupo (AGPM), um administrador do AGPM (controle total) delega permissão para editores, Aprovadores e revisores como grupos ou como indivíduos.</span><span class="sxs-lookup"><span data-stu-id="5cba7-104">In an environment where multiple people change Group Policy Objects (GPOs) by using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers either as groups or as individuals.</span></span> <span data-ttu-id="5cba7-105">Veja a seguir um processo típico de desenvolvimento de GPOs para um editor e um Aprovador.</span><span class="sxs-lookup"><span data-stu-id="5cba7-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5cba7-106">Tarefa</span><span class="sxs-lookup"><span data-stu-id="5cba7-106">Task</span></span></th>
<th align="left"><span data-ttu-id="5cba7-107">Referência</span><span class="sxs-lookup"><span data-stu-id="5cba7-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cba7-108">O editor solicita que um novo GPO seja criado ou um Aprovador cria um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="5cba7-108">Editor requests that a new GPO be created or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="5cba7-109">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="5cba7-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="5cba7-110">Criar um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="5cba7-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cba7-111">O aprovador aprova a criação do GPO se ele foi solicitado por um editor.</span><span class="sxs-lookup"><span data-stu-id="5cba7-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="5cba7-112">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="5cba7-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cba7-113">O editor verifica uma cópia do GPO do arquivo morto para que ninguém mais possa modificar o GPO.</span><span class="sxs-lookup"><span data-stu-id="5cba7-113">Editor checks out a copy of the GPO from the archive so that no one else can modify the GPO.</span></span> <span data-ttu-id="5cba7-114">O editor faz alterações no GPO e, em seguida, verifica o GPO modificado no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="5cba7-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)"><span data-ttu-id="5cba7-115">Editar um GPO offline</span><span class="sxs-lookup"><span data-stu-id="5cba7-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cba7-116">Se estiver desenvolvendo em uma floresta de teste, o editor exportará o GPO para um arquivo, transferirá o arquivo para a floresta de produção e importará o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cba7-116">If developing in a test forest, Editor exports the GPO to a file, transfers the file to the production forest, and imports the file.</span></span> <span data-ttu-id="5cba7-117">Além disso, um editor pode vincular o GPO a uma unidade organizacional que contém computadores de teste e usuários.</span><span class="sxs-lookup"><span data-stu-id="5cba7-117">Additionally, an Editor can link the GPO to an organizational unit that contains test computers and users.</span></span></p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)"><span data-ttu-id="5cba7-118">Como usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="5cba7-118">Using a Test Environment</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cba7-119">O editor solicita a implantação do GPO no ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="5cba7-119">Editor requests deployment of the GPO to the production environment of the domain.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)"><span data-ttu-id="5cba7-120">Solicitar a implantação de um GPO</span><span class="sxs-lookup"><span data-stu-id="5cba7-120">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cba7-121">Revisores, como aprovadores ou editores, analise o GPO.</span><span class="sxs-lookup"><span data-stu-id="5cba7-121">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)"><span data-ttu-id="5cba7-122">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="5cba7-122">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cba7-123">O aprovador aprova e implanta o GPO no ambiente de produção do domínio ou rejeita o GPO.</span><span class="sxs-lookup"><span data-stu-id="5cba7-123">Approver approves and deploys the GPO to the production environment of the domain or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="5cba7-124">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="5cba7-124">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5cba7-125">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="5cba7-125">Additional references</span></span>

[<span data-ttu-id="5cba7-126">Gerenciamento Avançado de Política de Grupo 4.0</span><span class="sxs-lookup"><span data-stu-id="5cba7-126">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





