---
title: Controlar um GPO não controlado anteriormente
description: Controlar um GPO não controlado anteriormente
author: dansimp
ms.assetid: 452689a9-4e32-4e3b-8208-56353a82bf36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d7349b16b326a49b701efae5379c313bde0964f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797415"
---
# <span data-ttu-id="61849-103">Controlar um GPO não controlado anteriormente</span><span class="sxs-lookup"><span data-stu-id="61849-103">Control a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="61849-104">Para usar o gerenciamento avançado de política de grupo (AGPM) para fornecer controle de alterações para um objeto de política de grupo (GPO), você deve primeiro controlar o GPO com o AGPM.</span><span class="sxs-lookup"><span data-stu-id="61849-104">To use Advanced Group Policy Management (AGPM) to provide change control for a Group Policy object (GPO), you must first control the GPO with AGPM.</span></span>

<span data-ttu-id="61849-105">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="61849-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="61849-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="61849-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="61849-107">Para controlar um GPO previamente controlado</span><span class="sxs-lookup"><span data-stu-id="61849-107">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="61849-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="61849-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="61849-109">Na guia **conteúdo** do painel detalhes, clique na guia não **controlado** para exibir os GPOs não controlados.</span><span class="sxs-lookup"><span data-stu-id="61849-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="61849-110">Clique com o botão direito do mouse no GPO para ser controlado com o AGPM e, em seguida, clique em **controle**.</span><span class="sxs-lookup"><span data-stu-id="61849-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="61849-111">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="61849-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="61849-112">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="61849-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="61849-113">O GPO é removido da lista na guia não **controlado** e adicionado à guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="61849-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="61849-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="61849-114">Additional considerations</span></span>

-   <span data-ttu-id="61849-115">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="61849-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="61849-116">Especificamente, você deve ter **conteúdo de lista** e criar permissões de **GPO** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="61849-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="61849-117">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="61849-117">Additional references</span></span>

-   [<span data-ttu-id="61849-118">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="61849-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





