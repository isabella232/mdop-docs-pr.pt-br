---
title: Reverter para uma versão anterior de um GPO
description: Reverter para uma versão anterior de um GPO
author: dansimp
ms.assetid: 06ce9251-95e0-46d0-99c2-b9a0690e5891
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1146a8ecaf25796b9ac105ba46ea7f27b06fc8aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797692"
---
# <span data-ttu-id="b71fd-103">Reverter para uma versão anterior de um GPO</span><span class="sxs-lookup"><span data-stu-id="b71fd-103">Roll Back to an Earlier Version of a GPO</span></span>


<span data-ttu-id="b71fd-104">Um Aprovador pode reverter as alterações em um GPO (objeto de política de grupo), implantando novamente uma versão anterior do GPO em seu histórico.</span><span class="sxs-lookup"><span data-stu-id="b71fd-104">An Approver can roll back changes to a Group Policy Object (GPO) by redeploying an earlier version of the GPO from its history.</span></span> <span data-ttu-id="b71fd-105">Implantar uma versão anterior de um GPO substitui a versão do GPO atualmente em produção.</span><span class="sxs-lookup"><span data-stu-id="b71fd-105">Deploying an earlier version of a GPO overwrites the version of the GPO currently in production.</span></span>

<span data-ttu-id="b71fd-106">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="b71fd-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="b71fd-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b71fd-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b71fd-108">Para implantar uma versão anterior de um GPO no ambiente de produção do domínio</span><span class="sxs-lookup"><span data-stu-id="b71fd-108">To deploy an earlier version of a GPO to the production environment of the domain</span></span>**

1.  <span data-ttu-id="b71fd-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b71fd-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b71fd-110">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="b71fd-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="b71fd-111">Clique duas vezes no GPO a ser implantado para exibir seu **histórico**.</span><span class="sxs-lookup"><span data-stu-id="b71fd-111">Double-click the GPO to be deployed to display its **History**.</span></span>

4.  <span data-ttu-id="b71fd-112">Clique com o botão direito do mouse na versão a ser implantada, clique em **implantar**e, em seguida, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="b71fd-112">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

5.  <span data-ttu-id="b71fd-113">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b71fd-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b71fd-114">Na janela do **histórico** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b71fd-114">In the **History** window, click **Close**.</span></span>

<span data-ttu-id="b71fd-115">**Observação**  Para verificar se a versão que foi reimplementada corresponde à versão pretendida, examine um relatório de diferença para as duas versões.</span><span class="sxs-lookup"><span data-stu-id="b71fd-115">**Note** To verify that the version that has been redeployed matches the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="b71fd-116">Na janela do **histórico** do GPO, realce as duas versões e clique com o botão direito do mouse e selecione **diferença** e relatório **HTML** ou **relatório XML**.</span><span class="sxs-lookup"><span data-stu-id="b71fd-116">In the **History** window for the GPO, highlight the two versions, and then right-click and select **Difference** and either **HTML Report** or **XML Report**.</span></span>

 

### <span data-ttu-id="b71fd-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="b71fd-117">Additional considerations</span></span>

-   <span data-ttu-id="b71fd-118">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="b71fd-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b71fd-119">Especificamente, você deve ter a **lista de conteúdo** e as permissões de GPO de **implantação** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="b71fd-119">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="b71fd-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="b71fd-120">Additional references</span></span>

-   [<span data-ttu-id="b71fd-121">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="b71fd-121">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





