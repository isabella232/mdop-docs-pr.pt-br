---
title: Editar um GPO offline
description: Editar um GPO offline
author: dansimp
ms.assetid: 9c75eb3c-d4d5-41e0-b65e-8b4464a42cd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7ba0f72d7bfa8e2c597f62f7675a754807525ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797816"
---
# <span data-ttu-id="336ba-103">Editar um GPO offline</span><span class="sxs-lookup"><span data-stu-id="336ba-103">Edit a GPO Offline</span></span>


<span data-ttu-id="336ba-104">Para fazer alterações em um GPO (objeto de política de grupo) controlado, você deve primeiro fazer o check-out de uma cópia do GPO do arquivo.</span><span class="sxs-lookup"><span data-stu-id="336ba-104">To make changes to a controlled Group Policy Object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="336ba-105">Ninguém mais conseguirá modificar o GPO até que ele seja novamente verificado, evitando a introdução de alterações conflitantes por vários administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="336ba-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="336ba-106">Quando terminar de modificar o GPO, faça o check-in do arquivo morto para que ele possa ser revisado e implantado no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="336ba-106">When you have finished modifying the GPO, you check it into the archive so that it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="336ba-107">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo (AGPM) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="336ba-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="336ba-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="336ba-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="336ba-109">Editando um GPO offline</span><span class="sxs-lookup"><span data-stu-id="336ba-109">Editing a GPO offline</span></span>


<span data-ttu-id="336ba-110">Para editar um GPO, você pode fazer o check-out do GPO, editar o GPO offline e, em seguida, verificar o GPO no arquivo morto para que ele possa ser revisado e implantado (ou modificado por outros editores).</span><span class="sxs-lookup"><span data-stu-id="336ba-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive so that it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="336ba-111">Fazer check-out de um GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="336ba-111">Check out a GPO from the archive for editing</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="336ba-112">Editar um GPO offline</span><span class="sxs-lookup"><span data-stu-id="336ba-112">Edit a GPO offline</span></span>](#bkmk-edit)

-   [<span data-ttu-id="336ba-113">Verificar um GPO no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="336ba-113">Check a GPO into the archive</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="336ba-114">Para fazer check-out de um GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="336ba-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="336ba-115">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="336ba-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="336ba-116">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="336ba-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="336ba-117">Clique com o botão direito do mouse no GPO a ser editado e, em seguida, clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="336ba-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="336ba-118">Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="336ba-118">Type a comment to be displayed in the History of the GPO while it is checked out, and then click **OK**.</span></span>

5.  <span data-ttu-id="336ba-119">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="336ba-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="336ba-120">Na guia **controlado** , o estado do GPO agora está identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="336ba-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="336ba-121">Para editar um GPO offline</span><span class="sxs-lookup"><span data-stu-id="336ba-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="336ba-122">Na guia **controlado** , clique com o botão direito do mouse no GPO a ser editado e, em seguida, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="336ba-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="336ba-123">Na janela **Editor de gerenciamento de política de grupo** , faça alterações em uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="336ba-123">In the **Group Policy Management Editor** window, make changes to an offline copy of the GPO.</span></span>

    <span data-ttu-id="336ba-124">**Observação**  Para desabilitar todas as configurações do computador ou todas as configurações do usuário, clique com o botão direito do mouse no GPO na janela do **Editor de gerenciamento de política de grupo** e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="336ba-124">**Note** To disable all Computer Configuration settings or all User Configuration settings, right-click the GPO in the **Group Policy Management Editor** window and click **Properties**.</span></span> <span data-ttu-id="336ba-125">Selecione **desabilitar configurações do computador** ou **desativar as configurações do usuário** , conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="336ba-125">Select **Disable Computer Configuration settings** or **Disable User Configuration settings** as appropriate.</span></span>

     

3.  <span data-ttu-id="336ba-126">Quando terminar de modificar o GPO, feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="336ba-126">When you have finished modifying the GPO, close the **Group Policy Management Editor** window.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="336ba-127">Para verificar um GPO no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="336ba-127">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="336ba-128">Na guia **controlado** :</span><span class="sxs-lookup"><span data-stu-id="336ba-128">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="336ba-129">Se você não fez alterações no GPO, clique com o botão direito do mouse no GPO e clique em **desfazer check-out**e, em seguida, clique em **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="336ba-129">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="336ba-130">Se você fez alterações no GPO, clique com o botão direito do mouse no GPO e clique em **fazer check-in**.</span><span class="sxs-lookup"><span data-stu-id="336ba-130">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="336ba-131">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="336ba-131">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="336ba-132">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="336ba-132">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="336ba-133">Na guia **controlado** , o estado do GPO é identificado como **checked-in**.</span><span class="sxs-lookup"><span data-stu-id="336ba-133">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="336ba-134">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="336ba-134">Additional considerations</span></span>

-   <span data-ttu-id="336ba-135">Para fazer check-out e editar um GPO, por padrão, você deve ser o aprovador que criou ou controlado o GPO, um editor ou um administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="336ba-135">To check out and edit a GPO, by default you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="336ba-136">Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="336ba-136">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="336ba-137">Além disso, para editar o GPO, você deve ser a pessoa que fez check-out do GPO.</span><span class="sxs-lookup"><span data-stu-id="336ba-137">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="336ba-138">Para fazer check-in de um GPO, por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="336ba-138">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="336ba-139">Especificamente, você deve ter o **conteúdo da lista** e **Editar as** permissões do **GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="336ba-139">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="336ba-140">Se você não for um Aprovador ou administrador do AGPM (ou outro administrador da política de grupo com a permissão **implantar GPO** ), você deve ser o editor que fez check-out do GPO.</span><span class="sxs-lookup"><span data-stu-id="336ba-140">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="336ba-141">Durante a edição de um GPO, qualquer atualização de instalação de software de política de grupo de um pacote em outro GPO deve referenciar o GPO implantado e não a cópia com check-out.</span><span class="sxs-lookup"><span data-stu-id="336ba-141">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, and not the checked-out copy.</span></span>

### <span data-ttu-id="336ba-142">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="336ba-142">Additional references</span></span>

-   [<span data-ttu-id="336ba-143">Editando um GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-143">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   <span data-ttu-id="336ba-144">Revisando um GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-144">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="336ba-145">Analisar configurações do GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-145">Review GPO Settings</span></span>](review-gpo-settings-agpm40.md)

    -   [<span data-ttu-id="336ba-146">Analisar links do GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-146">Review GPO Links</span></span>](review-gpo-links-agpm40.md)

    -   [<span data-ttu-id="336ba-147">Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos</span><span class="sxs-lookup"><span data-stu-id="336ba-147">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md)

-   <span data-ttu-id="336ba-148">Implantando um GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-148">Deploying a GPO</span></span>

    -   [<span data-ttu-id="336ba-149">Solicitar a implantação de um GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-149">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

    -   [<span data-ttu-id="336ba-150">Implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="336ba-150">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

 

 





