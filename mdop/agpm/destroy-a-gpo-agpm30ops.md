---
title: Destruir um GPO
description: Destruir um GPO
author: dansimp
ms.assetid: bfabd71a-47f3-462e-b86f-5f15762b9e28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 842a546c4db9cc6048908521baa05c6cc1a1a8a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797374"
---
# <span data-ttu-id="45a90-103">Destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="45a90-103">Destroy a GPO</span></span>


<span data-ttu-id="45a90-104">Os aprovadores podem destruir um objeto de política de grupo (GPO), removê-lo da lixeira e excluí-lo permanentemente para que ele não possa mais ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="45a90-104">Approvers can destroy a Group Policy Object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="45a90-105">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="45a90-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="45a90-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="45a90-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="45a90-107">Para excluir permanentemente um GPO para que ele não possa mais ser restaurado</span><span class="sxs-lookup"><span data-stu-id="45a90-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="45a90-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="45a90-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="45a90-109">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="45a90-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="45a90-110">Clique com o botão direito do mouse no GPO a ser destruído e, em seguida, clique em **destruir**.</span><span class="sxs-lookup"><span data-stu-id="45a90-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="45a90-111">Clique em **Sim** para confirmar que você deseja excluir permanentemente o GPO selecionado e todos os backups do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="45a90-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="45a90-112">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="45a90-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="45a90-113">O GPO é removido da guia **Lixeira** e é excluído permanentemente.</span><span class="sxs-lookup"><span data-stu-id="45a90-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="45a90-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="45a90-114">Additional considerations</span></span>

-   <span data-ttu-id="45a90-115">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="45a90-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="45a90-116">Especificamente, você deve ter permissões **list Content** e **delete GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="45a90-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="45a90-117">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="45a90-117">Additional references</span></span>

-   [<span data-ttu-id="45a90-118">Excluir, restaurar ou destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="45a90-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





