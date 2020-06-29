---
title: Excluir um GPO controlado
description: Excluir um GPO controlado
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797380"
---
# <span data-ttu-id="03555-103">Excluir um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="03555-103">Delete a Controlled GPO</span></span>


<span data-ttu-id="03555-104">Os aprovadores podem excluir um objeto de política de grupo (GPO) controlado, movendo-o para a lixeira.</span><span class="sxs-lookup"><span data-stu-id="03555-104">Approvers can delete a controlled Group Policy Object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="03555-105">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="03555-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="03555-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="03555-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="03555-107">Para excluir um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="03555-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="03555-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="03555-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="03555-109">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="03555-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="03555-110">Clique com o botão direito do mouse no GPO que você deseja excluir e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="03555-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="03555-111">Para excluir o GPO do arquivo morto, deixando a versão implantada do GPO intocado no ambiente de produção, clique em **excluir GPO somente de arquivo morto**.</span><span class="sxs-lookup"><span data-stu-id="03555-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="03555-112">Para excluir o GPO do ambiente de arquivamento e de produção, clique em **excluir GPO do arquivamento e da produção**.</span><span class="sxs-lookup"><span data-stu-id="03555-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="03555-113">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="03555-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="03555-114">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="03555-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="03555-115">O GPO é removido da guia **controlado** e é exibido na guia **Lixeira** , onde ele pode ser restaurado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="03555-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="03555-116">Se o GPO tiver sido excluído somente do arquivo morto, ele também será exibido na guia não **controlado** .</span><span class="sxs-lookup"><span data-stu-id="03555-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="03555-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="03555-117">Additional considerations</span></span>

-   <span data-ttu-id="03555-118">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="03555-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="03555-119">Especificamente, você deve ter permissões **list Content** e **delete GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="03555-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="03555-120">Para excluir um GPO não controlado do ambiente de produção sem primeiro controlá-lo, no **console de gerenciamento de política de grupo**, clique em **floresta**, clique em **domínios**, clique em \*\* &lt; &gt; mydomain\*\*e, em seguida, clique em objetos de política de **grupo**.</span><span class="sxs-lookup"><span data-stu-id="03555-120">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="03555-121">Clique com o botão direito do mouse no GPO não controlado e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="03555-121">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="03555-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="03555-122">Additional references</span></span>

-   [<span data-ttu-id="03555-123">Excluir, restaurar ou destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="03555-123">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





