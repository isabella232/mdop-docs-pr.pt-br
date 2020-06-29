---
title: Implantar um GPO
description: Implantar um GPO
author: dansimp
ms.assetid: 3767b722-db43-40f1-a714-bb8e38bcaa10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71c08a3b2d4f5af5bc7f1b69f964e9bb707d889c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797820"
---
# <span data-ttu-id="a68ae-103">Implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="a68ae-103">Deploy a GPO</span></span>


<span data-ttu-id="a68ae-104">Um Aprovador pode implantar um objeto de política de grupo (GPO) novo ou editado no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="a68ae-104">An Approver can deploy a new or edited Group Policy Object (GPO) to the production environment.</span></span> <span data-ttu-id="a68ae-105">Para obter informações sobre como reimplantar uma versão anterior de um GPO, consulte [reverter para uma versão anterior de um GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="a68ae-105">For information about redeploying a previous version of a GPO, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span></span>

<span data-ttu-id="a68ae-106">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="a68ae-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="a68ae-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="a68ae-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="a68ae-108">Para implantar um GPO no ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="a68ae-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="a68ae-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="a68ae-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="a68ae-110">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="a68ae-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="a68ae-111">Clique com o botão direito do mouse no GPO a ser implantado e clique em **implantar**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="a68ae-112">Para revisar os links para o GPO, clique em **avançado**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="a68ae-113">Pause o ponteiro do mouse sobre um item na árvore para exibir detalhes.</span><span class="sxs-lookup"><span data-stu-id="a68ae-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="a68ae-114">Por padrão, todos os links para o GPO serão restaurados.</span><span class="sxs-lookup"><span data-stu-id="a68ae-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="a68ae-115">Para impedir que um link seja restaurado, desmarque a caixa de seleção desse link.</span><span class="sxs-lookup"><span data-stu-id="a68ae-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="a68ae-116">Para impedir que todos os links sejam restaurados, desmarque a caixa de seleção **restaurar vínculos** na caixa de diálogo **implantar GPO** .</span><span class="sxs-lookup"><span data-stu-id="a68ae-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="a68ae-117">Clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-117">Click **Yes**.</span></span> <span data-ttu-id="a68ae-118">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="a68ae-119">**Observação**  Para verificar se a versão mais recente de um GPO foi implantada, na guia **controlado** , clique duas vezes no GPO para exibir seu **histórico**.</span><span class="sxs-lookup"><span data-stu-id="a68ae-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="a68ae-120">No **histórico** do GPO, a coluna **estado** indica se um GPO foi implantado.</span><span class="sxs-lookup"><span data-stu-id="a68ae-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="a68ae-121">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="a68ae-121">Additional considerations</span></span>

-   <span data-ttu-id="a68ae-122">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="a68ae-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="a68ae-123">Especificamente, você deve ter a **lista de conteúdo** e as permissões de GPO de **implantação** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="a68ae-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="a68ae-124">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="a68ae-124">Additional references</span></span>

-   [<span data-ttu-id="a68ae-125">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="a68ae-125">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

 

 





