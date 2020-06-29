---
title: Delegar o gerenciamento de um GPO controlado
description: Delegar o gerenciamento de um GPO controlado
author: dansimp
ms.assetid: 96b4bfb3-5657-4267-8326-85d7a0db87ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0833e6b002d15c64e3b60fa0570640f8ea7fb2ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797838"
---
# <span data-ttu-id="1521a-103">Delegar o gerenciamento de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="1521a-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="1521a-104">Um Aprovador pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado criado pelo aprovador.</span><span class="sxs-lookup"><span data-stu-id="1521a-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="1521a-105">Como um administrador do AGPM (controle total), o aprovador pode delegar o acesso a tal GPO para que os editores selecionados possam editá-lo, os revisores podem revisá-lo e outros Aprovadores possam aprová-lo.</span><span class="sxs-lookup"><span data-stu-id="1521a-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="1521a-106">Por padrão, um aprovador não pode delegar o acesso a GPOs criados por outro administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="1521a-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="1521a-107">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="1521a-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="1521a-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1521a-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1521a-109">Para delegar o gerenciamento de um GPO controlado</span><span class="sxs-lookup"><span data-stu-id="1521a-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="1521a-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="1521a-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1521a-111">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado:</span><span class="sxs-lookup"><span data-stu-id="1521a-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="1521a-112">Para adicionar acesso para um usuário ou grupo, clique no botão **Adicionar** , selecione o usuário ou grupo e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1521a-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="1521a-113">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione uma função e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1521a-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="1521a-114">Para remover o acesso de um usuário ou grupo, selecione o usuário ou grupo e clique no botão **remover** .</span><span class="sxs-lookup"><span data-stu-id="1521a-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="1521a-115">**Observação**  Se um usuário ou grupo herda o acesso de todo o domínio, o botão **remover** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="1521a-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="1521a-116">Você pode modificar o acesso em todo o domínio na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="1521a-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="1521a-117">Para modificar as funções e permissões delegadas a um usuário ou grupo, clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="1521a-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="1521a-118">Na caixa de diálogo **permissões** , selecione o usuário ou grupo, marque a caixa de seleção de cada função a ser atribuída a esse usuário ou grupo e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1521a-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="1521a-119">**Observação**  O editor e o aprovador incluem permissões do revisor.</span><span class="sxs-lookup"><span data-stu-id="1521a-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="1521a-120">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="1521a-120">Additional considerations</span></span>

-   <span data-ttu-id="1521a-121">Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="1521a-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1521a-122">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="1521a-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="1521a-123">Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** .</span><span class="sxs-lookup"><span data-stu-id="1521a-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="1521a-124">Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM.</span><span class="sxs-lookup"><span data-stu-id="1521a-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="1521a-125">Outras permissões devem ser explicitamente delegadas.</span><span class="sxs-lookup"><span data-stu-id="1521a-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="1521a-126">Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="1521a-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="1521a-127">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="1521a-127">Additional references</span></span>

-   [<span data-ttu-id="1521a-128">Criar ou controlar um GPO</span><span class="sxs-lookup"><span data-stu-id="1521a-128">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





