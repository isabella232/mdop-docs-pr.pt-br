---
title: Aprovar ou rejeitar uma ação pendente
description: Aprovar ou rejeitar uma ação pendente
author: dansimp
ms.assetid: 078ea8b5-9ac5-45fc-9ac1-a1aa629c10b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61014ec46db2beb9a525abe8d9b2b0902b3aa78d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797482"
---
# <span data-ttu-id="58229-103">Aprovar ou rejeitar uma ação pendente</span><span class="sxs-lookup"><span data-stu-id="58229-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="58229-104">A principal responsabilidade de um Aprovador é avaliar e aprovar ou rejeitar solicitações de criação, implantação e exclusão de objetos de política de grupo (GPO) de editores ou revisores que não têm permissão para completar essas ações.</span><span class="sxs-lookup"><span data-stu-id="58229-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy Object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="58229-105">Os relatórios podem ajudar um Aprovador a avaliar uma nova versão de um GPO.</span><span class="sxs-lookup"><span data-stu-id="58229-105">Reports can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="58229-106">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="58229-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="58229-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="58229-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="58229-108">Para aprovar ou rejeitar uma solicitação pendente</span><span class="sxs-lookup"><span data-stu-id="58229-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="58229-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="58229-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="58229-110">Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.</span><span class="sxs-lookup"><span data-stu-id="58229-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="58229-111">Clique com o botão direito do mouse em um GPO pendente e, em seguida, clique em **aprovar** ou **rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="58229-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="58229-112">Se estiver aprovando a implantação, clique em **avançado** na caixa de diálogo **aprovar operação pendente** para revisar os links para o GPO.</span><span class="sxs-lookup"><span data-stu-id="58229-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="58229-113">Pause o ponteiro do mouse sobre um item na árvore para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="58229-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="58229-114">Por padrão, todos os links para o GPO serão restaurados.</span><span class="sxs-lookup"><span data-stu-id="58229-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="58229-115">Para impedir que um link seja restaurado, desmarque a caixa de seleção desse link.</span><span class="sxs-lookup"><span data-stu-id="58229-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="58229-116">Para impedir que todos os links sejam restaurados, desmarque a caixa de seleção **restaurar vínculos** na caixa de diálogo **implantar GPO** .</span><span class="sxs-lookup"><span data-stu-id="58229-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="58229-117">Clique em **Sim** ou **OK** para confirmar a aprovação ou rejeição da ação pendente.</span><span class="sxs-lookup"><span data-stu-id="58229-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="58229-118">Se você tiver aprovado a solicitação, o GPO será movido para a guia apropriada para a ação executada.</span><span class="sxs-lookup"><span data-stu-id="58229-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="58229-119">**Observação**  Se o endereço de email de um Aprovador estiver incluído no campo **endereço de email** na guia **delegação** de **domínio** , o aprovador receberá o email do alias do AGPM quando um editor ou revisor enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="58229-119">**Note** If an Approver's e-mail address is included in the **To e-mail address** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="58229-120">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="58229-120">Additional considerations</span></span>

-   <span data-ttu-id="58229-121">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="58229-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="58229-122">Especificamente, você deve ter as permissões necessárias para executar a solicitação que está aprovando.</span><span class="sxs-lookup"><span data-stu-id="58229-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="58229-123">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="58229-123">Additional references</span></span>

-   [<span data-ttu-id="58229-124">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="58229-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





