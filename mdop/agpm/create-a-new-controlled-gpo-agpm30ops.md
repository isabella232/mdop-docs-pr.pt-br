---
title: Criar um novo GPO controlado
description: Criar um novo GPO controlado
author: dansimp
ms.assetid: f89eaae8-7858-4222-ba3f-a93a9d7ea5a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d666edf97459a8499ee0f74155473c692d583ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797858"
---
# <span data-ttu-id="9582d-103">Criar um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="9582d-103">Create a New Controlled GPO</span></span>


<span data-ttu-id="9582d-104">Novos objetos de política de grupo (GPOs) criados por meio da pasta de **controle de alterações** serão automaticamente controlados, permitindo que você o gerencie.</span><span class="sxs-lookup"><span data-stu-id="9582d-104">New Group Policy Objects (GPOs) created through the **Change Control** folder will automatically be controlled, enabling you to manage them.</span></span>

<span data-ttu-id="9582d-105">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="9582d-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9582d-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9582d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9582d-107">Para criar um novo GPO com controle de alterações gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="9582d-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="9582d-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="9582d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9582d-109">Clique com o botão direito do mouse em **controle de alterações**e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="9582d-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="9582d-110">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="9582d-110">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="9582d-111">Digite um nome para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="9582d-111">Type a name for the new GPO.</span></span>

    2.  <span data-ttu-id="9582d-112">Opcional: digite um comentário para o novo GPO a ser exibido no **histórico** do GPO.</span><span class="sxs-lookup"><span data-stu-id="9582d-112">Optional: Type a comment for the new GPO to be displayed in the **History** for the GPO.</span></span>

    3.  <span data-ttu-id="9582d-113">Para implantar imediatamente o novo GPO no ambiente de produção, clique em **criar ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="9582d-113">To immediately deploy the new GPO to the production environment, click **Create live**.</span></span> <span data-ttu-id="9582d-114">Para criar o novo GPO offline sem implantá-lo imediatamente, clique em **criar offline**.</span><span class="sxs-lookup"><span data-stu-id="9582d-114">To create the new GPO offline without immediately deploying it, click **Create offline**.</span></span>

    4.  <span data-ttu-id="9582d-115">Selecione o modelo de GPO a ser usado como ponto de partida para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="9582d-115">Select the GPO template to use as a starting point for the new GPO.</span></span>

    5.  <span data-ttu-id="9582d-116">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9582d-116">Click **OK**.</span></span>

4.  <span data-ttu-id="9582d-117">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="9582d-117">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9582d-118">O novo GPO é exibido na lista de GPOs na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="9582d-118">The new GPO is displayed in the list of GPOs on the **Controlled** tab.</span></span>

### <span data-ttu-id="9582d-119">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="9582d-119">Additional considerations</span></span>

-   <span data-ttu-id="9582d-120">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="9582d-120">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9582d-121">Especificamente, você deve ter **conteúdo de lista** e criar permissões de **GPO** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="9582d-121">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="9582d-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="9582d-122">Additional references</span></span>

-   [<span data-ttu-id="9582d-123">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="9582d-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





