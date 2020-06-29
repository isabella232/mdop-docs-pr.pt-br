---
title: Fazer check-in de um GPO
description: Fazer check-in de um GPO
author: dansimp
ms.assetid: b838c8a2-eb9e-4e5b-8740-d7701a4294ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 27924e57e7430cdf992a7730e5cd141ed4fb52ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797474"
---
# <span data-ttu-id="c4c46-103">Fazer check-in de um GPO</span><span class="sxs-lookup"><span data-stu-id="c4c46-103">Check In a GPO</span></span>


<span data-ttu-id="c4c46-104">Normalmente, os editores devem verificar objetos de política de grupo (GPOs) que foram editados quando suas modificações são concluídas.</span><span class="sxs-lookup"><span data-stu-id="c4c46-104">Ordinarily, Editors should check in Group Policy Objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="c4c46-105">(Para obter detalhes, consulte [Editar um GPO offline](edit-a-gpo-offline-agpm40.md).) No entanto, se o editor estiver indisponível, um Aprovador também pode fazer check-in de um GPO.</span><span class="sxs-lookup"><span data-stu-id="c4c46-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline-agpm40.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="c4c46-106">Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="c4c46-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="c4c46-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="c4c46-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c4c46-108">Para fazer check-in de um GPO que foi verificado por um editor</span><span class="sxs-lookup"><span data-stu-id="c4c46-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="c4c46-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="c4c46-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c4c46-110">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="c4c46-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="c4c46-111">Para descartar alterações feitas pelo editor, clique com o botão direito do mouse no GPO, clique em **desfazer check-out**e, em seguida, clique em **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="c4c46-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="c4c46-112">Para reter as alterações feitas pelo editor, clique com o botão direito do mouse no GPO e, em seguida, clique em **check-in**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="c4c46-113">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="c4c46-114">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c4c46-115">Na guia **controlado** , o estado do GPO é identificado como **checked-in**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="c4c46-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="c4c46-116">Additional considerations</span></span>

-   <span data-ttu-id="c4c46-117">Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="c4c46-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c4c46-118">Especificamente, você deve ter o **conteúdo da lista** e **Editar as** permissões do **GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="c4c46-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="c4c46-119">Se você não for um Aprovador ou administrador do AGPM (ou outro administrador da política de grupo com a permissão **implantar GPO** ), você deve ser o editor que fez check-out do GPO.</span><span class="sxs-lookup"><span data-stu-id="c4c46-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="c4c46-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="c4c46-120">Additional references</span></span>

-   [<span data-ttu-id="c4c46-121">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="c4c46-121">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="c4c46-122">Editar um GPO offline</span><span class="sxs-lookup"><span data-stu-id="c4c46-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline-agpm40.md)

 

 





