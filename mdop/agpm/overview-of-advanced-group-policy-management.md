---
title: Visão geral do Gerenciamento Avançado de Política de Grupo
description: Visão geral do Gerenciamento Avançado de Política de Grupo
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799081"
---
# <span data-ttu-id="55db9-103">Visão geral do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="55db9-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="55db9-104">Você pode usar o gerenciamento de política de grupo avançado (AGPM) para estender os recursos do console de gerenciamento de política de grupo (GPMC), fornecendo controle de alterações abrangente e gerenciamento aprimorado para GPOs (objetos de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="55db9-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="55db9-105">Desenvolvimento de objetos de política de grupo com controle de alterações</span><span class="sxs-lookup"><span data-stu-id="55db9-105">Group Policy object development with change control</span></span>


<span data-ttu-id="55db9-106">Com o AGPM, você pode armazenar uma cópia de cada GPO em um arquivo morto central, portanto, os administradores de política de grupo podem exibi-lo e modificá-lo offline sem afetar imediatamente a versão implantada do GPO.</span><span class="sxs-lookup"><span data-stu-id="55db9-106">With AGPM, you can store a copy of each GPO in a central archive, so Group Policy administrators can view and modify it offline without immediately impacting the deployed version of the GPO.</span></span> <span data-ttu-id="55db9-107">Além disso, o AGPM armazena uma cópia de cada versão de cada GPO controlado no arquivo para que você possa reverter para uma versão anterior, se necessário.</span><span class="sxs-lookup"><span data-stu-id="55db9-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if needed.</span></span>

<span data-ttu-id="55db9-108">Os termos "check-in" e "check-out" são usados da mesma maneira que em uma biblioteca (ou em aplicativos que fornecem controle de alterações, controle de versão ou controle de código-fonte para desenvolvimento de programação).</span><span class="sxs-lookup"><span data-stu-id="55db9-108">The terms "check in" and "check out" are used in much the same way as in a library (or in applications that provide change control, version control, or source code control for programming development).</span></span> <span data-ttu-id="55db9-109">Para usar um livro que esteja em uma biblioteca, verifique-o na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="55db9-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="55db9-110">Ninguém mais pode usá-lo enquanto você estiver com check-out. Quando terminar o livro, verifique-o novamente na biblioteca para que outras pessoas possam usá-lo.</span><span class="sxs-lookup"><span data-stu-id="55db9-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="55db9-111">Ao desenvolver GPOs usando o AGPM:</span><span class="sxs-lookup"><span data-stu-id="55db9-111">When developing GPOs using AGPM:</span></span>

1.  <span data-ttu-id="55db9-112">Crie um novo GPO controlado ou controle um GPO previamente controlado.</span><span class="sxs-lookup"><span data-stu-id="55db9-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="55db9-113">Confira o GPO, para que você e somente você possa modificá-lo.</span><span class="sxs-lookup"><span data-stu-id="55db9-113">Check out the GPO, so you and only you can modify it.</span></span>

3.  <span data-ttu-id="55db9-114">Edite o GPO.</span><span class="sxs-lookup"><span data-stu-id="55db9-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="55db9-115">Verifique o GPO editado, para que outras pessoas possam modificá-lo, ou para que ele possa ser implantado.</span><span class="sxs-lookup"><span data-stu-id="55db9-115">Check in the edited GPO, so others can modify it, or so it can be deployed.</span></span>

5.  <span data-ttu-id="55db9-116">Revise as alterações.</span><span class="sxs-lookup"><span data-stu-id="55db9-116">Review the changes.</span></span>

6.  <span data-ttu-id="55db9-117">Implante o GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="55db9-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="55db9-118">Delegação baseada em função</span><span class="sxs-lookup"><span data-stu-id="55db9-118">Role-based delegation</span></span>


<span data-ttu-id="55db9-119">O AGPM oferece delegação completa e fácil de usar com base em funções.</span><span class="sxs-lookup"><span data-stu-id="55db9-119">AGPM provides comprehensive, easy-to-use role-based delegation.</span></span> <span data-ttu-id="55db9-120">As permissões no nível do domínio permitem que os administradores do AGPM forneçam acesso a domínios individuais sem fornecer acesso a outros domínios.</span><span class="sxs-lookup"><span data-stu-id="55db9-120">Domain-level permissions allow AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="55db9-121">A delegação baseada em GPO permite que administradores do AGPM permitam acesso somente a GPOs específicos.</span><span class="sxs-lookup"><span data-stu-id="55db9-121">GPO-based delegation enables AGPM Administrators to allow access only to specific GPOs.</span></span>

<span data-ttu-id="55db9-122">No AGPM, há funções especificamente definidas: administrador do AGPM (controle total), Aprovador, editor e revisor.</span><span class="sxs-lookup"><span data-stu-id="55db9-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="55db9-123">A função de administrador do AGPM inclui as permissões para todas as outras funções.</span><span class="sxs-lookup"><span data-stu-id="55db9-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="55db9-124">Por padrão, somente os aprovadores têm a capacidade de implantar GPOs no ambiente de produção, protegendo o ambiente contra erros inadvertidos por editores menos experientes.</span><span class="sxs-lookup"><span data-stu-id="55db9-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from inadvertent mistakes by less experienced Editors.</span></span> <span data-ttu-id="55db9-125">Além disso, por padrão, todas as funções incluem a função de revisor e, portanto, a capacidade de visualizar as configurações de GPO em relatórios.</span><span class="sxs-lookup"><span data-stu-id="55db9-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="55db9-126">No entanto, o AGPM fornece um administrador do AGPM com a flexibilidade de personalizar o acesso ao GPO para atender às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="55db9-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="55db9-127">Delegação em um ambiente de administrador de política de grupo múltiplo</span><span class="sxs-lookup"><span data-stu-id="55db9-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="55db9-128">Em um ambiente em que várias pessoas fazem alterações em GPOs, um administrador do AGPM delega a permissão para editores, Aprovadores e revisores, como grupos ou indivíduos.</span><span class="sxs-lookup"><span data-stu-id="55db9-128">In an environment where multiple people make changes to GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="55db9-129">Para um processo de desenvolvimento de GPO típico para um editor e um aprovador, consulte [lista de verificação: criar, editar e implantar um GPO](checklist-create-edit-and-deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="55db9-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo.md).</span></span>

### <span data-ttu-id="55db9-130">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="55db9-130">Additional references</span></span>

-   [<span data-ttu-id="55db9-131">Lista de verificação: Criar, editar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="55db9-131">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="55db9-132">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="55db9-132">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="55db9-133">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="55db9-133">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="55db9-134">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="55db9-134">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="55db9-135">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="55db9-135">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="55db9-136">Solução de problemas do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="55db9-136">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="55db9-137">Interface do usuário: Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="55db9-137">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





