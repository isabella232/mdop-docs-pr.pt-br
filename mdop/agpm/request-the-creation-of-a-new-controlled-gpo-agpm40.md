---
title: Solicitar a criação de um novo GPO controlado
description: Solicitar a criação de um novo GPO controlado
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797701"
---
# <span data-ttu-id="caa70-103">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="caa70-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="caa70-104">A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar a criação de um novo objeto de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="caa70-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="caa70-105">Uma conta de usuário com a função de editor ou de revisor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="caa70-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="caa70-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="caa70-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="caa70-107">Para criar um novo GPO com controle de alterações gerenciado por meio do AGPM</span><span class="sxs-lookup"><span data-stu-id="caa70-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="caa70-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="caa70-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="caa70-109">Clique com o botão direito do mouse em **controle de alterações**e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="caa70-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="caa70-110">A menos que você tenha permissão especial para criar GPOs, você deve enviar uma solicitação de criação.</span><span class="sxs-lookup"><span data-stu-id="caa70-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="caa70-111">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="caa70-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="caa70-112">Para receber uma cópia da solicitação, insira seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="caa70-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="caa70-113">Digite um nome para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="caa70-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="caa70-114">Opcional: digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="caa70-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="caa70-115">Para implantar o novo GPO no ambiente de produção do domínio imediatamente após a aprovação, clique em **criar ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="caa70-115">To deploy the new GPO to the production environment of the domain immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="caa70-116">Para criar o novo GPO offline sem implantá-lo imediatamente após a aprovação, clique em **criar offline**.</span><span class="sxs-lookup"><span data-stu-id="caa70-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="caa70-117">Selecione o modelo de GPO a ser usado como ponto de partida para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="caa70-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="caa70-118">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="caa70-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="caa70-119">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="caa70-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="caa70-120">O novo GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="caa70-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="caa70-121">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="caa70-121">Additional considerations</span></span>

-   <span data-ttu-id="caa70-122">Por padrão, você deve ser um editor ou um revisor para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="caa70-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="caa70-123">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="caa70-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="caa70-124">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="caa70-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="caa70-125">O GPO será destruído.</span><span class="sxs-lookup"><span data-stu-id="caa70-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="caa70-126">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="caa70-126">Additional references</span></span>

-   [<span data-ttu-id="caa70-127">Criar ou controlar um GPO</span><span class="sxs-lookup"><span data-stu-id="caa70-127">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





