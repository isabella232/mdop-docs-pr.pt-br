---
title: Solicitar a exclusão de um GPO
description: Solicitar a exclusão de um GPO
author: dansimp
ms.assetid: 2410f7a1-ccca-44cf-ab26-76ad474409e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfdb50fba872b76c82152b469f787f2e1a6fb539
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797323"
---
# <span data-ttu-id="aa524-103">Solicitar a exclusão de um GPO</span><span class="sxs-lookup"><span data-stu-id="aa524-103">Request Deletion of a GPO</span></span>


<span data-ttu-id="aa524-104">A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar a exclusão de um objeto de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="aa524-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the deletion of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="aa524-105">Uma conta de usuário com a função de editor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="aa524-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="aa524-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="aa524-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="aa524-107">Para solicitar a exclusão de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="aa524-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="aa524-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="aa524-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="aa524-109">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="aa524-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="aa524-110">Clique com o botão direito do mouse no GPO que você deseja excluir e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="aa524-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="aa524-111">Para excluir o GPO do arquivo morto, deixando a versão implantada do GPO intocado no ambiente de produção, clique em **excluir GPO somente de arquivo morto**.</span><span class="sxs-lookup"><span data-stu-id="aa524-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="aa524-112">Para excluir o GPO do ambiente de arquivo morto e de produção do domínio, clique em **excluir GPO do arquivamento e da produção**.</span><span class="sxs-lookup"><span data-stu-id="aa524-112">To delete the GPO from both the archive and production environment of the domain, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="aa524-113">A menos que você tenha permissão especial para excluir GPOs, você deve enviar uma solicitação de exclusão do GPO implantado.</span><span class="sxs-lookup"><span data-stu-id="aa524-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="aa524-114">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="aa524-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="aa524-115">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="aa524-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="aa524-116">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="aa524-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="aa524-117">O GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado a sua solicitação, o GPO será movido da guia **pendente** para a guia **Lixeira** , onde poderá ser restaurado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="aa524-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="aa524-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="aa524-118">Additional considerations</span></span>

-   <span data-ttu-id="aa524-119">Por padrão, você deve ser um editor para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="aa524-119">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="aa524-120">Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="aa524-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="aa524-121">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="aa524-121">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="aa524-122">O GPO será retornado para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="aa524-122">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="aa524-123">Para excluir um GPO não controlado do ambiente de produção sem primeiro controlá-lo, no **console de gerenciamento de política de grupo**, clique em **floresta**, clique em **domínios**, clique em \*\* &lt; &gt; mydomain\*\*e, em seguida, clique em objetos de política de **grupo**.</span><span class="sxs-lookup"><span data-stu-id="aa524-123">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="aa524-124">Clique com o botão direito do mouse no GPO não controlado e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="aa524-124">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="aa524-125">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="aa524-125">Additional references</span></span>

-   [<span data-ttu-id="aa524-126">Excluir ou restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="aa524-126">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

 

 





