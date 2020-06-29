---
title: Solicitar o controle de um GPO não controlado anteriormente
description: Solicitar o controle de um GPO não controlado anteriormente
author: dansimp
ms.assetid: 00e8725d-5d7f-4eed-a5e6-c3631632cfbd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a92db48d87398568900fc0031e688c862a69b417
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797330"
---
# <span data-ttu-id="aed3e-103">Solicitar o controle de um GPO não controlado anteriormente</span><span class="sxs-lookup"><span data-stu-id="aed3e-103">Request Control of a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="aed3e-104">Para usar o gerenciamento avançado de política de grupo (AGPM) para fornecer controle de alterações para um objeto de política de grupo (GPO) existente, o GPO deve ser controlado com o AGPM.</span><span class="sxs-lookup"><span data-stu-id="aed3e-104">To use Advanced Group Policy Management (AGPM) to provide change control for an existing Group Policy object (GPO), the GPO must be controlled with AGPM.</span></span> <span data-ttu-id="aed3e-105">A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar que o GPO seja controlado.</span><span class="sxs-lookup"><span data-stu-id="aed3e-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="aed3e-106">Uma conta de usuário com a função de editor ou revisor ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="aed3e-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="aed3e-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="aed3e-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="aed3e-108">Para controlar um GPO previamente controlado</span><span class="sxs-lookup"><span data-stu-id="aed3e-108">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="aed3e-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="aed3e-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="aed3e-110">Na guia **conteúdo** do painel detalhes, clique na guia não **controlado** para exibir os GPOs não controlados.</span><span class="sxs-lookup"><span data-stu-id="aed3e-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="aed3e-111">Clique com o botão direito do mouse no GPO para ser controlado com o AGPM e, em seguida, clique em **controle**.</span><span class="sxs-lookup"><span data-stu-id="aed3e-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="aed3e-112">A menos que você tenha permissão especial para controlar os GPOs, você deve enviar uma solicitação de controle.</span><span class="sxs-lookup"><span data-stu-id="aed3e-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="aed3e-113">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="aed3e-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="aed3e-114">Digite um comentário a ser exibido no **histórico** do GPO e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="aed3e-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="aed3e-115">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="aed3e-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aed3e-116">O GPO é removido da lista na guia não **controlado** e adicionado à guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="aed3e-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="aed3e-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="aed3e-117">Additional considerations</span></span>

-   <span data-ttu-id="aed3e-118">Por padrão, você deve ser um editor ou um revisor para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="aed3e-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="aed3e-119">Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="aed3e-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="aed3e-120">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="aed3e-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="aed3e-121">O GPO será retornado para a guia não **controlado** .</span><span class="sxs-lookup"><span data-stu-id="aed3e-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="aed3e-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="aed3e-122">Additional references</span></span>

-   [<span data-ttu-id="aed3e-123">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="aed3e-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





