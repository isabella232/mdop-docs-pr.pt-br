---
title: Visão geral do Gerenciamento Avançado de Política de Grupo
description: Visão geral do Gerenciamento Avançado de Política de Grupo
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799082"
---
# <span data-ttu-id="5e06a-103">Visão geral do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="5e06a-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="5e06a-104">Você pode usar o gerenciamento de política de grupo avançado (AGPM) para estender os recursos do console de gerenciamento de política de grupo (GPMC) para fornecer controle de alterações abrangente e gerenciamento aprimorado para objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="5e06a-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="5e06a-105">Desenvolvimento de objetos de política de grupo com controle de alterações</span><span class="sxs-lookup"><span data-stu-id="5e06a-105">Group Policy object development with change control</span></span>


<span data-ttu-id="5e06a-106">Com o AGPM, você pode armazenar uma cópia de cada GPO em um arquivo morto central para que os administradores de política de grupo possam exibir e alterá-lo offline sem afetar imediatamente a versão implantada do GPO.</span><span class="sxs-lookup"><span data-stu-id="5e06a-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="5e06a-107">Além disso, o AGPM armazena uma cópia de cada versão de cada GPO controlado no arquivo para que você possa reverter para uma versão anterior, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5e06a-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="5e06a-108">Os termos "check-in" e "check-out" são usados apenas como em uma biblioteca (ou em aplicativos que fornecem controle de alterações, controle de versão ou controle de origem para o desenvolvimento de programação).</span><span class="sxs-lookup"><span data-stu-id="5e06a-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="5e06a-109">Para usar um livro que esteja em uma biblioteca, verifique-o na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5e06a-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="5e06a-110">Ninguém mais pode usá-lo enquanto você estiver com check-out. Quando terminar o livro, verifique-o novamente na biblioteca para que outras pessoas possam usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5e06a-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="5e06a-111">Para usar esses recursos de controle de GPO, clique em um nó de controle de alterações no editor de gerenciamento de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="5e06a-111">To use these GPO control features, you will click a Change Control node in the Group Policy Management editor.</span></span> <span data-ttu-id="5e06a-112">O nó de controle de alterações só aparecerá se você tiver instalado o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="5e06a-112">The Change Control node appears only if you have installed the AGPM Client.</span></span>

<span data-ttu-id="5e06a-113">Ao desenvolver GPOs usando o AGPM:</span><span class="sxs-lookup"><span data-stu-id="5e06a-113">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="5e06a-114">Crie um novo GPO controlado ou controle um GPO previamente controlado.</span><span class="sxs-lookup"><span data-stu-id="5e06a-114">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="5e06a-115">Confira o GPO para que você e somente você possa alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="5e06a-115">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="5e06a-116">Edite o GPO.</span><span class="sxs-lookup"><span data-stu-id="5e06a-116">Edit the GPO.</span></span>

4.  <span data-ttu-id="5e06a-117">Faça o check-in do GPO editado para que outras pessoas possam alterá-lo, ou para que ele possa ser implantado.</span><span class="sxs-lookup"><span data-stu-id="5e06a-117">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="5e06a-118">Revise as alterações.</span><span class="sxs-lookup"><span data-stu-id="5e06a-118">Review the changes.</span></span>

6.  <span data-ttu-id="5e06a-119">Implante o GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="5e06a-119">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="5e06a-120">Delegação baseada em função</span><span class="sxs-lookup"><span data-stu-id="5e06a-120">Role-based delegation</span></span>


<span data-ttu-id="5e06a-121">O AGPM oferece delegação completa e fácil de usar com base em funções para o gerenciamento do acesso a GPOs no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e06a-121">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="5e06a-122">As permissões no nível do domínio permitem que os administradores do AGPM forneçam acesso a domínios individuais sem fornecer acesso a outros domínios.</span><span class="sxs-lookup"><span data-stu-id="5e06a-122">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="5e06a-123">A delegação baseada em GPO permite que os administradores do AGPM forneçam acesso a GPOs específicos sem fornecer acesso em todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="5e06a-123">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="5e06a-124">No AGPM, há funções especificamente definidas: administrador do AGPM (controle total), Aprovador, editor e revisor.</span><span class="sxs-lookup"><span data-stu-id="5e06a-124">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="5e06a-125">A função de administrador do AGPM inclui as permissões para todas as outras funções.</span><span class="sxs-lookup"><span data-stu-id="5e06a-125">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="5e06a-126">Por padrão, somente os aprovadores têm a capacidade de implantar GPOs no ambiente de produção de um domínio, protegendo o ambiente contra erros de editores menos experientes.</span><span class="sxs-lookup"><span data-stu-id="5e06a-126">By default, only Approvers have the power to deploy GPOs to the production environment of a domain, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="5e06a-127">Além disso, por padrão, todas as funções incluem a função de revisor e, portanto, a capacidade de visualizar as configurações de GPO em relatórios.</span><span class="sxs-lookup"><span data-stu-id="5e06a-127">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="5e06a-128">No entanto, o AGPM fornece um administrador do AGPM com a flexibilidade de personalizar o acesso ao GPO para atender às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="5e06a-128">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="5e06a-129">Delegação em um ambiente de administrador de política de grupo múltiplo</span><span class="sxs-lookup"><span data-stu-id="5e06a-129">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="5e06a-130">Em um ambiente onde várias pessoas alteram os GPOs, um administrador do AGPM delega a permissão para editores, Aprovadores e revisores, como grupos ou indivíduos.</span><span class="sxs-lookup"><span data-stu-id="5e06a-130">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="5e06a-131">Para um processo de desenvolvimento de GPO típico para um editor e um aprovador, consulte [lista de verificação: criar, editar e implantar um GPO](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="5e06a-131">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="5e06a-132">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="5e06a-132">Additional references</span></span>

-   [<span data-ttu-id="5e06a-133">Gerenciamento Avançado de Política de Grupo 4.0</span><span class="sxs-lookup"><span data-stu-id="5e06a-133">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





