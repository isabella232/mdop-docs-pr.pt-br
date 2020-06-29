---
title: Solicitar a restauração de um GPO excluído
description: Solicitar a restauração de um GPO excluído
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797711"
---
# <span data-ttu-id="f539e-103">Solicitar a restauração de um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="f539e-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="f539e-104">A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar a restauração de um objeto de política de grupo (GPO) excluído da lixeira para devolvê-lo ao arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="f539e-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="f539e-105">Uma conta de usuário com a função de editor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="f539e-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f539e-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="f539e-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f539e-107">Para solicitar a restauração de um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="f539e-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="f539e-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="f539e-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f539e-109">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="f539e-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="f539e-110">Clique com o botão direito do mouse no GPO que você deseja restaurar e clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="f539e-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="f539e-111">A menos que você tenha permissão especial para restaurar GPOs, você deve enviar uma solicitação para restauração do GPO excluído.</span><span class="sxs-lookup"><span data-stu-id="f539e-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="f539e-112">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="f539e-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="f539e-113">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="f539e-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="f539e-114">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="f539e-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f539e-115">O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="f539e-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="f539e-116">**Observação**  Se um GPO foi excluído do ambiente de produção, restaurá-lo para o arquivo não o reimplantará automaticamente no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="f539e-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="f539e-117">Para retornar o GPO ao ambiente de produção, implante o GPO.</span><span class="sxs-lookup"><span data-stu-id="f539e-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="f539e-118">Para obter informações, consulte [implantar um GPO](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="f539e-118">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="f539e-119">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="f539e-119">Additional considerations</span></span>

-   <span data-ttu-id="f539e-120">Por padrão, você deve ser um editor para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="f539e-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="f539e-121">Especificamente, você deve ter a permissão **listar conteúdo** e **Editar configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="f539e-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="f539e-122">Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**.</span><span class="sxs-lookup"><span data-stu-id="f539e-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="f539e-123">O GPO será retornado para a guia da **Lixeira** .</span><span class="sxs-lookup"><span data-stu-id="f539e-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="f539e-124">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="f539e-124">Additional references</span></span>

-   [<span data-ttu-id="f539e-125">Excluir, restaurar ou destruir um GPO</span><span class="sxs-lookup"><span data-stu-id="f539e-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





