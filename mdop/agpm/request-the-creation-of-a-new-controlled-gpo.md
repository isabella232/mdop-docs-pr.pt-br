---
title: Solicitar a criação de um novo GPO controlado
description: Solicitar a criação de um novo GPO controlado
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797700"
---
# <span data-ttu-id="3aa05-103">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="3aa05-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="3aa05-104">A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar a criação de um novo objeto de política de grupo (GPO) se ele for gerenciado usando o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="3aa05-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy object (GPO) if it is to be managed using Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="3aa05-105">Uma conta de usuário com a função de editor ou revisor ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="3aa05-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="3aa05-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="3aa05-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3aa05-107">Para criar um novo GPO com controle de alterações gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="3aa05-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="3aa05-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="3aa05-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3aa05-109">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="3aa05-109">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="3aa05-110">A menos que você tenha permissão especial para criar GPOs, você deve enviar uma solicitação de criação.</span><span class="sxs-lookup"><span data-stu-id="3aa05-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="3aa05-111">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="3aa05-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="3aa05-112">Para receber uma cópia da solicitação, insira seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="3aa05-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="3aa05-113">Digite um nome para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="3aa05-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="3aa05-114">Opcional: digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="3aa05-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="3aa05-115">Para implantar o novo GPO para o ambiente de produção imediatamente após a aprovação, clique em **criar ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="3aa05-115">To deploy the new GPO to the production environment immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="3aa05-116">Para criar o novo GPO offline sem implantá-lo imediatamente após a aprovação, clique em **criar offline**.</span><span class="sxs-lookup"><span data-stu-id="3aa05-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="3aa05-117">Selecione o modelo de GPO a ser usado como ponto de partida para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="3aa05-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="3aa05-118">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="3aa05-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="3aa05-119">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="3aa05-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="3aa05-120">O novo GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="3aa05-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="3aa05-121">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="3aa05-121">Additional considerations</span></span>

-   <span data-ttu-id="3aa05-122">Por padrão, você deve ser um editor ou um revisor para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="3aa05-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="3aa05-123">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="3aa05-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="3aa05-124">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="3aa05-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="3aa05-125">O GPO será destruído.</span><span class="sxs-lookup"><span data-stu-id="3aa05-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="3aa05-126">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="3aa05-126">Additional references</span></span>

-   [<span data-ttu-id="3aa05-127">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="3aa05-127">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





