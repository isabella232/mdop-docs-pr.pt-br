---
title: Delegar acesso no nível do domínio
description: Delegar acesso no nível do domínio
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797837"
---
# <span data-ttu-id="562c4-103">Delegar acesso no nível do domínio</span><span class="sxs-lookup"><span data-stu-id="562c4-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="562c4-104">Configurar a delegação do seu ambiente para que os administradores de política de grupo tenham acesso e controle apropriados em GPOs (objetos de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="562c4-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="562c4-105">Há permissões de linha de base que você pode aplicar para fazer com que a operação do gerenciamento avançado de política de grupo (AGPM) seja mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="562c4-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="562c4-106">Você pode conceder permissões de qualquer maneira que atenda às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="562c4-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="562c4-107">Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="562c4-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="562c4-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="562c4-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="562c4-109">Para delegar o acesso para que os usuários e grupos tenham permissões adequadas para todos os GPOs em todo o domínio</span><span class="sxs-lookup"><span data-stu-id="562c4-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="562c4-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="562c4-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="562c4-111">Clique na guia **delegação de domínio** e, em seguida, clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="562c4-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="562c4-112">Na caixa de diálogo **permissões** , clique na caixa de seleção de cada função a ser atribuída a um indivíduo e, em seguida, clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="562c4-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="562c4-113">**Observação**  O editor e o aprovador incluem permissões do revisor.</span><span class="sxs-lookup"><span data-stu-id="562c4-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="562c4-114">Na caixa de diálogo **configurações de segurança avançadas** , selecione um administrador de política de grupo e, em seguida, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="562c4-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="562c4-115">Para **aplicar em**, selecione **este objeto e objetos aninhados**, configure todas as permissões especiais além das funções padrão do AGPM e, em seguida, clique em **OK** na caixa de diálogo **entrada** de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="562c4-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="562c4-116">Na caixa de diálogo **configurações de segurança avançadas** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="562c4-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="562c4-117">Na caixa de diálogo **permissões** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="562c4-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="562c4-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="562c4-118">Additional considerations</span></span>

-   <span data-ttu-id="562c4-119">Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="562c4-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="562c4-120">Especificamente, você deve ter permissão de **modificação de segurança** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="562c4-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="562c4-121">Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** .</span><span class="sxs-lookup"><span data-stu-id="562c4-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="562c4-122">Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM.</span><span class="sxs-lookup"><span data-stu-id="562c4-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="562c4-123">Defina a permissão para aplicar a **esse objeto e a objetos aninhados**.</span><span class="sxs-lookup"><span data-stu-id="562c4-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="562c4-124">Outras permissões devem ser explicitamente delegadas.</span><span class="sxs-lookup"><span data-stu-id="562c4-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="562c4-125">Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="562c4-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="562c4-126">A associação no grupo proprietários criadores de política de grupo deve ser restrita para que não seja usada para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="562c4-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="562c4-127">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="562c4-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="562c4-128">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="562c4-128">Additional references</span></span>

-   [<span data-ttu-id="562c4-129">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="562c4-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





