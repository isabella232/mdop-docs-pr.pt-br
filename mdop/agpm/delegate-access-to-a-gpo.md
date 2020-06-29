---
title: Delegar acesso a um GPO
description: Delegar acesso a um GPO
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797394"
---
# <span data-ttu-id="a245f-103">Delegar acesso a um GPO</span><span class="sxs-lookup"><span data-stu-id="a245f-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="a245f-104">Um Aprovador pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado **criado pelo aprovador**.</span><span class="sxs-lookup"><span data-stu-id="a245f-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="a245f-105">Como um administrador do AGPM (controle total), o aprovador pode delegar o acesso a tal GPO, para que os editores selecionados possam editá-lo, os Revisores possam examiná-lo e outros Aprovadores possam aprová-lo.</span><span class="sxs-lookup"><span data-stu-id="a245f-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="a245f-106">Por padrão, um aprovador não pode delegar o acesso a GPOs criados por outro administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a245f-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="a245f-107">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="a245f-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="a245f-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="a245f-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="a245f-109">Para delegar o gerenciamento de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="a245f-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="a245f-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="a245f-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="a245f-111">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado.</span><span class="sxs-lookup"><span data-stu-id="a245f-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="a245f-112">Clique no botão **Adicionar** , selecione os usuários ou grupos para os quais você tem permissão de acesso e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a245f-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="a245f-113">Para personalizar as permissões para cada um, clique no botão **avançado** na guia **conteúdo** e marque as permissões de função para permitir ou recusar.</span><span class="sxs-lookup"><span data-stu-id="a245f-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="a245f-114">(Para obter controle mais detalhado, clique em **avançado** na caixa de diálogo **permissões** .)</span><span class="sxs-lookup"><span data-stu-id="a245f-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="a245f-115">Clique em **aplicar**e, em seguida, clique em **OK** na caixa de diálogo **permissões** .</span><span class="sxs-lookup"><span data-stu-id="a245f-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="a245f-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="a245f-116">Additional considerations</span></span>

-   <span data-ttu-id="a245f-117">Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="a245f-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="a245f-118">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="a245f-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="a245f-119">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="a245f-119">Additional references</span></span>

-   [<span data-ttu-id="a245f-120">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="a245f-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





