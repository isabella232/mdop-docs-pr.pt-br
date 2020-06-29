---
title: Renomear um GPO ou modelo
description: Renomear um GPO ou modelo
author: dansimp
ms.assetid: 84293f7a-4ff7-497e-bdbc-cabb70189a03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 642622ae0242e614733e8f33ea5840c8b6758db8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797340"
---
# <span data-ttu-id="1440f-103">Renomear um GPO ou modelo</span><span class="sxs-lookup"><span data-stu-id="1440f-103">Rename a GPO or Template</span></span>


<span data-ttu-id="1440f-104">Você pode renomear um objeto de política de grupo (GPO) controlado ou um modelo.</span><span class="sxs-lookup"><span data-stu-id="1440f-104">You can rename a controlled Group Policy Object (GPO) or a template.</span></span>

<span data-ttu-id="1440f-105">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo (AGPM) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="1440f-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="1440f-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1440f-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1440f-107">Para renomear um GPO ou um modelo</span><span class="sxs-lookup"><span data-stu-id="1440f-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="1440f-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="1440f-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1440f-109">Na guia **conteúdo** , clique na guia **controlado** ou **modelos** para exibir o item a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="1440f-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="1440f-110">Clique com o botão direito no GPO ou no modelo para renomear e clique em **renomear**.</span><span class="sxs-lookup"><span data-stu-id="1440f-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="1440f-111">Digite o novo nome para o GPO ou modelo e um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1440f-111">Type the new name for the GPO or template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="1440f-112">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="1440f-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="1440f-113">O GPO ou modelo aparece sob o novo nome na guia **conteúdo** .</span><span class="sxs-lookup"><span data-stu-id="1440f-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="1440f-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="1440f-114">Additional considerations</span></span>

-   <span data-ttu-id="1440f-115">Por padrão, você deve ser o aprovador que criou ou controlado o GPO, um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="1440f-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1440f-116">Especificamente, você deve ter a permissão **listar conteúdo** e **Editar configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="1440f-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="1440f-117">Quando você renomeia um GPO que foi implantado, o nome é alterado imediatamente no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="1440f-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="1440f-118">O nome é alterado no ambiente de produção apenas quando o GPO é reimplantado.</span><span class="sxs-lookup"><span data-stu-id="1440f-118">The name is changed in the production environment only when the GPO is redeployed.</span></span> <span data-ttu-id="1440f-119">Até que o GPO seja reimplantado (ou que a cópia de produção seja excluída), o nome antigo ainda está em uso no ambiente de produção e, portanto, não pode ser usado para outro GPO.</span><span class="sxs-lookup"><span data-stu-id="1440f-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="1440f-120">Da mesma forma, o GPO no arquivo não pode ser renomeado para seu nome original até que o GPO tenha sido implantado (alterando o nome da cópia de produção) ou que a cópia de produção tenha sido excluída.</span><span class="sxs-lookup"><span data-stu-id="1440f-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="1440f-121">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="1440f-121">Additional references</span></span>

-   [<span data-ttu-id="1440f-122">Editando um GPO</span><span class="sxs-lookup"><span data-stu-id="1440f-122">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

 

 





