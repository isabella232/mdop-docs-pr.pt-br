---
title: Excluir um GPO
description: Excluir um GPO
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797832"
---
# <span data-ttu-id="d1b4c-103">Excluir um GPO</span><span class="sxs-lookup"><span data-stu-id="d1b4c-103">Delete a GPO</span></span>


<span data-ttu-id="d1b4c-104">Como um editor, talvez você não tenha permissão para concluir a exclusão de um objeto de política de grupo (GPO), mas tem a permissão necessária para iniciar o processo e enviar sua solicitação a um Aprovador.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-104">As an Editor, you may not have permission to complete the deletion of a Group Policy object (GPO), but you do have the permission necessary to begin the process and submit your request to an Approver.</span></span>

<span data-ttu-id="d1b4c-105">Uma conta de usuário com a função de editor ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="d1b4c-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d1b4c-107">Para solicitar a exclusão de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="d1b4c-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="d1b4c-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d1b4c-109">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="d1b4c-110">Clique com o botão direito do mouse no GPO a ser excluído e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="d1b4c-111">Para excluir o GPO do arquivo morto, deixando a versão implantada do GPO intocado no ambiente de produção, clique em **excluir GPO de somente arquivo morto (não controlar)**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="d1b4c-112">Para excluir o GPO do ambiente de arquivamento e de produção, clique em **excluir GPO do arquivamento e da produção**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

        <span data-ttu-id="d1b4c-113">A menos que você tenha permissão especial para excluir GPOs, você deve enviar uma solicitação de exclusão do GPO implantado.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="d1b4c-114">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="d1b4c-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="d1b4c-115">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

4.  <span data-ttu-id="d1b4c-116">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d1b4c-117">O GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado a sua solicitação, o GPO será movido da guia **pendente** para a guia **Lixeira** , onde poderá ser restaurado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="d1b4c-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="d1b4c-118">Additional considerations</span></span>

-   <span data-ttu-id="d1b4c-119">Por padrão, você deve ser um editor para solicitar a exclusão de um GPO implantado.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-119">By default, you must be an Editor to request the deletion of a deployed GPO.</span></span> <span data-ttu-id="d1b4c-120">Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="d1b4c-121">Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para excluir um GPO do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-121">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="d1b4c-122">Especificamente, você deve ter **conteúdo da lista** e **Editar as** permissões do **GPO ou excluir** as permissões do GPO.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-122">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="d1b4c-123">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-123">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="d1b4c-124">O GPO será retornado para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="d1b4c-124">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="d1b4c-125">Para excluir um GPO não controlado do ambiente de produção sem primeiro controlá-lo, no **console de gerenciamento de política de grupo**, clique em **floresta**, clique em **domínios**, clique em \*\* &lt; &gt; mydomain\*\*e, em seguida, clique em objetos de política de **grupo**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-125">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="d1b4c-126">Clique com o botão direito do mouse no GPO não controlado e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="d1b4c-126">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="d1b4c-127">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="d1b4c-127">Additional references</span></span>

-   [<span data-ttu-id="d1b4c-128">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="d1b4c-128">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

 

 





