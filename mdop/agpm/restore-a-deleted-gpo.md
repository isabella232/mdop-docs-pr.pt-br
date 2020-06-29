---
title: Restaurar um GPO excluído
description: Restaurar um GPO excluído
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797320"
---
# <span data-ttu-id="30f4a-103">Restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="30f4a-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="30f4a-104">O gerenciamento avançado de política de grupo (AGPM) permite que os aprovadores restaurem um objeto de política de grupo (GPO) excluído da lixeira, retornando-o ao arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="30f4a-104">Advanced Group Policy Management (AGPM) enables Approvers to restore a deleted Group Policy object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="30f4a-105">Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="30f4a-105">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="30f4a-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="30f4a-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="30f4a-107">Para restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="30f4a-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="30f4a-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="30f4a-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="30f4a-109">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="30f4a-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="30f4a-110">Clique com o botão direito do mouse no GPO para restaurar e clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="30f4a-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="30f4a-111">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="30f4a-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="30f4a-112">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="30f4a-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="30f4a-113">O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="30f4a-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="30f4a-114">**Observação**  Se um GPO foi excluído do ambiente de produção, restaurá-lo para o arquivo não o reimplantará automaticamente no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="30f4a-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="30f4a-115">Para retornar o GPO ao ambiente de produção, implante o GPO.</span><span class="sxs-lookup"><span data-stu-id="30f4a-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="30f4a-116">Para obter informações, consulte [implantar um GPO](deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="30f4a-116">For information, see [Deploy a GPO](deploy-a-gpo.md).</span></span>

 

### <span data-ttu-id="30f4a-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="30f4a-117">Additional considerations</span></span>

-   <span data-ttu-id="30f4a-118">Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="30f4a-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="30f4a-119">Especificamente, você deve ter **conteúdo da lista** e **Editar as configurações**, **implantar o GPO**ou excluir permissões de **GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="30f4a-119">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="30f4a-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="30f4a-120">Additional references</span></span>

-   [<span data-ttu-id="30f4a-121">Excluir, restaurar ou destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="30f4a-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





