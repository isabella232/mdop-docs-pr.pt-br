---
title: Delegar acesso a um GPO individual no arquivo morto
description: Delegar acesso a um GPO individual no arquivo morto
author: dansimp
ms.assetid: 284d2aa2-7c10-4ffa-8978-bbe30867c1c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9da2a699568f961d030b05a966b76e08aef3aec8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797845"
---
# <span data-ttu-id="39b8f-103">Delegar acesso a um GPO individual no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="39b8f-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="39b8f-104">Como administrador do AGPM (controle total), você pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado no arquivo para que os grupos e editores selecionados possam editá-lo, os revisores podem revisá-lo e os aprovadores podem aprová-lo.</span><span class="sxs-lookup"><span data-stu-id="39b8f-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="39b8f-105">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="39b8f-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="39b8f-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="39b8f-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="39b8f-107">Para delegar o gerenciamento de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="39b8f-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="39b8f-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="39b8f-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="39b8f-109">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado:</span><span class="sxs-lookup"><span data-stu-id="39b8f-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="39b8f-110">Para adicionar acesso para um usuário ou grupo, clique no botão **Adicionar** , selecione o usuário ou grupo e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="39b8f-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="39b8f-111">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione uma função e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="39b8f-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="39b8f-112">Para remover o acesso de um usuário ou grupo, selecione o usuário ou grupo e clique no botão **remover** .</span><span class="sxs-lookup"><span data-stu-id="39b8f-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="39b8f-113">**Observação**  Se um usuário ou grupo herda o acesso de todo o domínio, o botão **remover** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="39b8f-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="39b8f-114">Você pode modificar o acesso em todo o domínio na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="39b8f-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="39b8f-115">Para modificar as funções e permissões delegadas a um usuário ou grupo, clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="39b8f-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="39b8f-116">Na caixa de diálogo **permissões** , selecione o usuário ou grupo, marque a caixa de seleção de cada função a ser atribuída a esse usuário ou grupo e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="39b8f-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="39b8f-117">**Observação**  O editor e o aprovador incluem permissões do revisor.</span><span class="sxs-lookup"><span data-stu-id="39b8f-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="39b8f-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="39b8f-118">Additional considerations</span></span>

-   <span data-ttu-id="39b8f-119">Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="39b8f-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="39b8f-120">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="39b8f-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="39b8f-121">Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** .</span><span class="sxs-lookup"><span data-stu-id="39b8f-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="39b8f-122">Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM.</span><span class="sxs-lookup"><span data-stu-id="39b8f-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="39b8f-123">Outras permissões devem ser explicitamente delegadas.</span><span class="sxs-lookup"><span data-stu-id="39b8f-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="39b8f-124">Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="39b8f-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="39b8f-125">A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="39b8f-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="39b8f-126">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="39b8f-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="39b8f-127">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="39b8f-127">Additional references</span></span>

-   [<span data-ttu-id="39b8f-128">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="39b8f-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





