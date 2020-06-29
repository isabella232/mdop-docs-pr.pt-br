---
title: Delegar acesso no nível do domínio ao arquivo morto
description: Delegar acesso no nível do domínio ao arquivo morto
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797382"
---
# <span data-ttu-id="300d6-103">Delegar acesso no nível do domínio ao arquivo morto</span><span class="sxs-lookup"><span data-stu-id="300d6-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="300d6-104">Configure a delegação do seu ambiente para que os administradores de política de grupo tenham o acesso e o controle apropriados em GPOs (objetos de política de grupo) no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="300d6-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="300d6-105">Há permissões de linha de base que você pode aplicar para fazer a operação ser mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="300d6-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="300d6-106">Você pode conceder permissões de qualquer maneira que atenda às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="300d6-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="300d6-107">Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="300d6-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="300d6-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="300d6-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="300d6-109">Para delegar o acesso para que os usuários e grupos tenham permissões apropriadas para todos os GPOs em todo o domínio</span><span class="sxs-lookup"><span data-stu-id="300d6-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="300d6-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="300d6-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="300d6-111">Clique na guia **delegação de domínio** e configure o acesso a todos os GPOs no domínio:</span><span class="sxs-lookup"><span data-stu-id="300d6-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="300d6-112">Para adicionar acesso para um usuário ou grupo, clique no botão **Adicionar** , selecione o usuário ou grupo e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="300d6-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="300d6-113">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione uma função e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="300d6-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="300d6-114">Para remover o acesso de um usuário ou grupo, selecione o usuário ou grupo e clique no botão **remover** .</span><span class="sxs-lookup"><span data-stu-id="300d6-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="300d6-115">Para modificar as funções e permissões delegadas a um usuário ou grupo, selecione clique no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="300d6-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="300d6-116">Na caixa de diálogo **permissões** , selecione o usuário ou grupo, marque a caixa de seleção de cada função a ser atribuída a esse usuário ou grupo e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="300d6-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="300d6-117">**Observação**  O editor e o aprovador incluem permissões do revisor.</span><span class="sxs-lookup"><span data-stu-id="300d6-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="300d6-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="300d6-118">Additional considerations</span></span>

-   <span data-ttu-id="300d6-119">Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="300d6-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="300d6-120">Especificamente, você deve ter permissão de **modificação de segurança** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="300d6-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="300d6-121">Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** .</span><span class="sxs-lookup"><span data-stu-id="300d6-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="300d6-122">Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM.</span><span class="sxs-lookup"><span data-stu-id="300d6-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="300d6-123">Outras permissões devem ser explicitamente delegadas.</span><span class="sxs-lookup"><span data-stu-id="300d6-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="300d6-124">Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="300d6-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="300d6-125">A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="300d6-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="300d6-126">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="300d6-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="300d6-127">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="300d6-127">Additional references</span></span>

-   [<span data-ttu-id="300d6-128">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="300d6-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





