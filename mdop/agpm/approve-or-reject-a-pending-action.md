---
title: Aprovar ou rejeitar uma ação pendente
description: Aprovar ou rejeitar uma ação pendente
author: dansimp
ms.assetid: 22921a51-50fb-4a47-bec1-4f563f523675
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 508df2766b7d480f8ba4d6e13c97ed880ef6939e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797481"
---
# <span data-ttu-id="9e238-103">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="9e238-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="9e238-104">A principal responsabilidade de um Aprovador é avaliar e aprovar ou rejeitar solicitações de criação, implantação e exclusão de objetos de política de grupo (GPO) de editores ou revisores que não têm permissão para completar essas ações.</span><span class="sxs-lookup"><span data-stu-id="9e238-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="9e238-105">Os recursos de relatório do recurso gerenciamento avançado de política de grupo (AGPM) podem ajudar um Aprovador a avaliar uma nova versão de um GPO.</span><span class="sxs-lookup"><span data-stu-id="9e238-105">The report capabilities of Advanced Group Policy Management (AGPM) can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="9e238-106">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="9e238-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="9e238-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9e238-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9e238-108">Para aprovar ou rejeitar uma solicitação pendente</span><span class="sxs-lookup"><span data-stu-id="9e238-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="9e238-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="9e238-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9e238-110">Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.</span><span class="sxs-lookup"><span data-stu-id="9e238-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="9e238-111">Clique com o botão direito do mouse em um GPO pendente e, em seguida, clique em **aprovar** ou **rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="9e238-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="9e238-112">Se estiver aprovando a implantação, clique em **avançado** na caixa de diálogo **aprovar operação pendente** para revisar os links para o GPO.</span><span class="sxs-lookup"><span data-stu-id="9e238-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="9e238-113">Pause o ponteiro do mouse sobre um nó na árvore para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="9e238-113">Pause the mouse pointer on a node in the tree to display details.</span></span>

    -   <span data-ttu-id="9e238-114">Por padrão, todos os links para o GPO serão restaurados.</span><span class="sxs-lookup"><span data-stu-id="9e238-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="9e238-115">Para impedir que um link seja restaurado, desmarque a caixa de seleção desse link.</span><span class="sxs-lookup"><span data-stu-id="9e238-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="9e238-116">Para impedir que todos os links sejam restaurados, desmarque a caixa de seleção **restaurar vínculos** na caixa de diálogo **implantar GPO** .</span><span class="sxs-lookup"><span data-stu-id="9e238-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="9e238-117">Clique em **Sim** ou **OK** para confirmar a aprovação ou rejeição da ação pendente.</span><span class="sxs-lookup"><span data-stu-id="9e238-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="9e238-118">Se você tiver aprovado a solicitação, o GPO será movido para a guia apropriada para a ação executada.</span><span class="sxs-lookup"><span data-stu-id="9e238-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="9e238-119">**Observação**  Se o endereço de email de um Aprovador estiver incluído no campo **para** na guia de **delegação** de **domínio** , o aprovador receberá o email do alias do AGPM quando um editor ou revisor enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9e238-119">**Note** If an Approver's e-mail address is included in the **To** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="9e238-120">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="9e238-120">Additional considerations</span></span>

-   <span data-ttu-id="9e238-121">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="9e238-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9e238-122">Especificamente, você deve ter as permissões necessárias para executar a solicitação que está aprovando.</span><span class="sxs-lookup"><span data-stu-id="9e238-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="9e238-123">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="9e238-123">Additional references</span></span>

-   [<span data-ttu-id="9e238-124">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="9e238-124">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





