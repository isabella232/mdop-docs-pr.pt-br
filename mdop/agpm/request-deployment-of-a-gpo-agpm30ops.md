---
title: Solicitar a implantação de um GPO
description: Solicitar a implantação de um GPO
author: dansimp
ms.assetid: f44ae0fb-bcf7-477b-b99e-9dd6a55ee597
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c8d1ac1ab157f744a6d5f2ede9bb281b553f718
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797325"
---
# <span data-ttu-id="f1632-103">Solicitar a implantação de um GPO</span><span class="sxs-lookup"><span data-stu-id="f1632-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="f1632-104">Depois de modificar e verificar um GPO (objeto de política de grupo), implante o GPO para que ele entre em vigor no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="f1632-104">After you have modified and checked in a Group Policy Object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="f1632-105">Uma conta de usuário com a função de editor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="f1632-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f1632-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="f1632-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f1632-107">Para solicitar a implantação de um GPO para o ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="f1632-107">To request the deployment of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="f1632-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="f1632-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f1632-109">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="f1632-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f1632-110">Clique com o botão direito do mouse no GPO a ser implantado e, em seguida, clique em **implantar**.</span><span class="sxs-lookup"><span data-stu-id="f1632-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="f1632-111">A menos que você seja um Aprovador ou administrador do AGPM ou tenha permissão especial para implantar GPOs, você deve enviar uma solicitação de implantação.</span><span class="sxs-lookup"><span data-stu-id="f1632-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="f1632-112">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="f1632-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="f1632-113">Digite um comentário a ser exibido no **histórico** do GPO e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="f1632-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="f1632-114">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="f1632-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f1632-115">O GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido da guia **pendente** para a guia **controlado** e será implantado.</span><span class="sxs-lookup"><span data-stu-id="f1632-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="f1632-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="f1632-116">Additional considerations</span></span>

-   <span data-ttu-id="f1632-117">Por padrão, você deve ser um editor para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="f1632-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="f1632-118">Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="f1632-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="f1632-119">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="f1632-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="f1632-120">O GPO será retornado para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="f1632-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="f1632-121">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="f1632-121">Additional references</span></span>

-   [<span data-ttu-id="f1632-122">Editando um GPO</span><span class="sxs-lookup"><span data-stu-id="f1632-122">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





