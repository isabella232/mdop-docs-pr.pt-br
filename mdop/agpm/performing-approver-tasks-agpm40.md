---
title: Execução de tarefas do aprovador
description: Execução de tarefas do aprovador
author: dansimp
ms.assetid: e0a4b7fe-ce69-4755-9104-c7f523ea6b62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a0815bdd6c34a7a23b27075b3b5367757c1f84e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797731"
---
# <span data-ttu-id="39f72-103">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="39f72-103">Performing Approver Tasks</span></span>


<span data-ttu-id="39f72-104">Um Aprovador é uma pessoa autorizada por um administrador do AGPM (controle total) para criar, implantar e excluir objetos de política de grupo (GPOs) e aprovar ou rejeitar solicitações (geralmente de editores) para criar, implantar ou excluir GPOs.</span><span class="sxs-lookup"><span data-stu-id="39f72-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="39f72-105">**Importante**  Certifique-se de que você esteja se conectando ao arquivo central para GPOs.</span><span class="sxs-lookup"><span data-stu-id="39f72-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="39f72-106">Para obter mais informações, consulte [Configurar uma conexão com o servidor do AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="39f72-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="39f72-107">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="39f72-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm40.md)

-   [<span data-ttu-id="39f72-108">Criar ou controlar um GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-108">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

-   [<span data-ttu-id="39f72-109">Fazer check-in de um GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-109">Check In a GPO</span></span>](check-in-a-gpo-agpm40.md)

-   [<span data-ttu-id="39f72-110">Implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="39f72-111">Reverter para uma versão anterior de um GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-111">Roll Back to an Earlier Version of a GPO</span></span>](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="39f72-112">Excluir, restaurar ou destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

<span data-ttu-id="39f72-113">**Observação**  Antes de aprovar um GPO, um Aprovador deve revisar as configurações de política que ele contém.</span><span class="sxs-lookup"><span data-stu-id="39f72-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="39f72-114">A função de aprovador inclui as permissões para a função de revisor, para que um Aprovador possa revisar as configurações de política e comparar GPOs.</span><span class="sxs-lookup"><span data-stu-id="39f72-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="39f72-115">Confira [executar tarefas do revisor](performing-reviewer-tasks-agpm40.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="39f72-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="39f72-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="39f72-116">Additional considerations</span></span>

<span data-ttu-id="39f72-117">Por padrão, as seguintes permissões são fornecidas para a função de aprovador:</span><span class="sxs-lookup"><span data-stu-id="39f72-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="39f72-118">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="39f72-118">List Contents</span></span>

-   <span data-ttu-id="39f72-119">Ler configurações</span><span class="sxs-lookup"><span data-stu-id="39f72-119">Read Settings</span></span>

-   <span data-ttu-id="39f72-120">Criar GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-120">Create GPO</span></span>

-   <span data-ttu-id="39f72-121">Implantar GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-121">Deploy GPO</span></span>

-   <span data-ttu-id="39f72-122">Excluir GPO</span><span class="sxs-lookup"><span data-stu-id="39f72-122">Delete GPO</span></span>

<span data-ttu-id="39f72-123">Além disso, um Aprovador tem controle total sobre os GPOs que ele criou ou controlado.</span><span class="sxs-lookup"><span data-stu-id="39f72-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





