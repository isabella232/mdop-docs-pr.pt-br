---
title: Delegar acesso a um GPO individual
description: Delegar acesso a um GPO individual
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797384"
---
# <span data-ttu-id="79f70-103">Delegar acesso a um GPO individual</span><span class="sxs-lookup"><span data-stu-id="79f70-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="79f70-104">Como administrador do AGPM (controle total), você pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado, para que os grupos selecionados e editores possam editá-lo, os revisores podem revisá-lo e os aprovadores podem aprová-lo.</span><span class="sxs-lookup"><span data-stu-id="79f70-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="79f70-105">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="79f70-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="79f70-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="79f70-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="79f70-107">Para delegar o gerenciamento de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="79f70-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="79f70-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="79f70-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="79f70-109">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado.</span><span class="sxs-lookup"><span data-stu-id="79f70-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="79f70-110">Clique no botão **Adicionar** , selecione os usuários ou grupos para os quais você tem permissão de acesso e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="79f70-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="79f70-111">Para personalizar as permissões para cada usuário ou grupo, clique no botão **avançado** na guia **conteúdo** e marque permissões de função para permitir ou recusar.</span><span class="sxs-lookup"><span data-stu-id="79f70-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="79f70-112">(Para obter controle mais detalhado, clique em **avançado** na caixa de diálogo **permissões** .)</span><span class="sxs-lookup"><span data-stu-id="79f70-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="79f70-113">Clique em **aplicar**e, em seguida, clique em **OK** na caixa de diálogo **permissões** .</span><span class="sxs-lookup"><span data-stu-id="79f70-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="79f70-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="79f70-114">Additional considerations</span></span>

-   <span data-ttu-id="79f70-115">Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="79f70-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="79f70-116">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="79f70-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="79f70-117">Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** .</span><span class="sxs-lookup"><span data-stu-id="79f70-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="79f70-118">Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM.</span><span class="sxs-lookup"><span data-stu-id="79f70-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="79f70-119">Defina a permissão para aplicar a **esse objeto e a objetos aninhados**.</span><span class="sxs-lookup"><span data-stu-id="79f70-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="79f70-120">Outras permissões devem ser explicitamente delegadas.</span><span class="sxs-lookup"><span data-stu-id="79f70-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="79f70-121">Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="79f70-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="79f70-122">A associação no grupo proprietários criadores de política de grupo deve ser restrita para que não seja usada para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="79f70-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="79f70-123">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="79f70-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="79f70-124">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="79f70-124">Additional references</span></span>

-   [<span data-ttu-id="79f70-125">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="79f70-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





