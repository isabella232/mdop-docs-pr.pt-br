---
title: Controlar um GPO não controlado
description: Controlar um GPO não controlado
author: dansimp
ms.assetid: 603f00f9-1e65-4b2f-902a-e53dafedbd8d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 904c3f76ce89f3814b739ee958fc14198899fb14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797414"
---
# <span data-ttu-id="8ebbe-103">Controlar um GPO não controlado</span><span class="sxs-lookup"><span data-stu-id="8ebbe-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="8ebbe-104">Para fornecer controle de alterações para um objeto de política de grupo (GPO), você deve primeiro controlar o GPO.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="8ebbe-105">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="8ebbe-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8ebbe-107">Para controlar um GPO não controlado</span><span class="sxs-lookup"><span data-stu-id="8ebbe-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="8ebbe-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8ebbe-109">Na guia **conteúdo** do painel detalhes, clique na guia não **controlado** para exibir os GPOs não controlados.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="8ebbe-110">Clique com o botão direito do mouse no GPO para ser controlado com o AGPM e, em seguida, clique em **controle**.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="8ebbe-111">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="8ebbe-112">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8ebbe-113">O GPO é removido da lista na guia não **controlado** e adicionado à guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="8ebbe-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="8ebbe-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="8ebbe-114">Additional considerations</span></span>

-   <span data-ttu-id="8ebbe-115">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8ebbe-116">Especificamente, você deve ter **conteúdo de lista** e criar permissões de **GPO** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="8ebbe-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="8ebbe-117">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="8ebbe-117">Additional references</span></span>

-   [<span data-ttu-id="8ebbe-118">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="8ebbe-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





