---
title: Rotular a versão atual de um GPO
description: Rotular a versão atual de um GPO
author: dansimp
ms.assetid: 3845211a-0bc9-4875-9906-cb758c443825
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f9e656258591a56397c5a8053b2e98772f57949a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797771"
---
# <span data-ttu-id="1775c-103">Rotular a versão atual de um GPO</span><span class="sxs-lookup"><span data-stu-id="1775c-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="1775c-104">Você pode rotular a versão atual de um objeto de política de grupo (GPO) para facilitar a identificação em seu histórico.</span><span class="sxs-lookup"><span data-stu-id="1775c-104">You can label the current version of a Group Policy Object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="1775c-105">Você pode usar um rótulo para identificar uma versão válida conhecida para a qual você pode reverter se ocorrer um problema.</span><span class="sxs-lookup"><span data-stu-id="1775c-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="1775c-106">Além disso, ao rotular vários GPOs com o mesmo rótulo ao mesmo tempo, você pode marcar os GPOs relacionados que devem ser revertidos para o mesmo ponto se a reversão posteriormente for necessária.</span><span class="sxs-lookup"><span data-stu-id="1775c-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="1775c-107">Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="1775c-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="1775c-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1775c-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1775c-109">Para rotular a versão atual dos GPOs em seus históricos</span><span class="sxs-lookup"><span data-stu-id="1775c-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="1775c-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="1775c-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1775c-111">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="1775c-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="1775c-112">Clique em um GPO para o qual você deseja rotular a versão atual.</span><span class="sxs-lookup"><span data-stu-id="1775c-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="1775c-113">Para selecionar vários GPOs, pressione SHIFT e clique no último GPO em um grupo contíguo de GPOs ou pressione CTRL e clique em GPOs individuais.</span><span class="sxs-lookup"><span data-stu-id="1775c-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="1775c-114">Clique com o botão direito do mouse em um GPO selecionado e, em seguida, clique em **rótulo**.</span><span class="sxs-lookup"><span data-stu-id="1775c-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="1775c-115">Digite um rótulo e um comentário a ser exibido no histórico de cada GPO selecionado e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1775c-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="1775c-116">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="1775c-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="1775c-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="1775c-117">Additional considerations</span></span>

-   <span data-ttu-id="1775c-118">Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="1775c-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1775c-119">Especificamente, você deve ter o **conteúdo da lista** e **Editar as** permissões do **GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="1775c-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="1775c-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="1775c-120">Additional references</span></span>

-   [<span data-ttu-id="1775c-121">Editando um GPO</span><span class="sxs-lookup"><span data-stu-id="1775c-121">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





