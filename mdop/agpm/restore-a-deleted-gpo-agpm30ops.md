---
title: Restaurar um GPO excluído
description: Restaurar um GPO excluído
author: dansimp
ms.assetid: 853feb0a-d2d9-4be9-a07e-e113a56a9968
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aae55a654cad44130816af3acc6aad03e96c9959
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797324"
---
# <span data-ttu-id="b16b7-103">Restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="b16b7-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="b16b7-104">Os aprovadores podem restaurar um objeto de política de grupo (GPO) excluído da lixeira, retornando-o ao arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b16b7-104">Approvers can restore a deleted Group Policy Object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="b16b7-105">Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="b16b7-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="b16b7-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b16b7-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b16b7-107">Para restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="b16b7-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="b16b7-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="b16b7-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b16b7-109">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="b16b7-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="b16b7-110">Clique com o botão direito do mouse no GPO para restaurar e clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="b16b7-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="b16b7-111">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b16b7-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="b16b7-112">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="b16b7-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b16b7-113">O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="b16b7-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="b16b7-114">**Observação**  Se um GPO foi excluído do ambiente de produção, restaurá-lo para o arquivo não o reimplantará automaticamente no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b16b7-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="b16b7-115">Para retornar o GPO ao ambiente de produção, implante o GPO.</span><span class="sxs-lookup"><span data-stu-id="b16b7-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="b16b7-116">Para obter informações, consulte [implantar um GPO](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="b16b7-116">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="b16b7-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="b16b7-117">Additional considerations</span></span>

-   <span data-ttu-id="b16b7-118">Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="b16b7-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b16b7-119">Especificamente, você deve ter **conteúdo da lista** e **implantar** permissões de GPO ou **excluir** GPO para o GPO.</span><span class="sxs-lookup"><span data-stu-id="b16b7-119">Specifically, you must have **List Contents** and either **Deploy GPO** or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="b16b7-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="b16b7-120">Additional references</span></span>

-   [<span data-ttu-id="b16b7-121">Excluir, restaurar ou destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="b16b7-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





