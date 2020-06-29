---
title: Executar tarefas de administração de AGPM
description: Executar tarefas de administração de AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797733"
---
# <span data-ttu-id="e35a9-103">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="e35a9-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="e35a9-104">Um administrador do AGPM (controle total) configura as permissões de todo o domínio e delega permissões para Aprovadores, editores, revisores e outros administradores do AGPM.</span><span class="sxs-lookup"><span data-stu-id="e35a9-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="e35a9-105">Por padrão, um administrador do AGPM é um indivíduo com controle total (todas as permissões do gerenciamento avançado de política de grupo \ [AGPM \]) e, portanto, também pode executar tarefas associadas a qualquer função.</span><span class="sxs-lookup"><span data-stu-id="e35a9-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="e35a9-106">Em um ambiente no qual várias pessoas desenvolvem objetos de política de grupo (GPOs), você pode escolher se todos os usuários de gerenciamento de política de grupo (AGPM) avançados executarão as mesmas tarefas e têm o mesmo nível de acesso ou se os administradores do AGPM delegam permissões para editores que fazem alterações em GPOs e para Aprovadores que implantam GPOs no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="e35a9-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="e35a9-107">Os administradores do AGPM podem configurar permissões para atender às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="e35a9-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="e35a9-108">Configurar a conexão de servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="e35a9-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="e35a9-109">Configurar notificações por email</span><span class="sxs-lookup"><span data-stu-id="e35a9-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="e35a9-110">Delegar acesso no nível do domínio</span><span class="sxs-lookup"><span data-stu-id="e35a9-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="e35a9-111">Delegar acesso a um GPO individual</span><span class="sxs-lookup"><span data-stu-id="e35a9-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="e35a9-112">Configurar log e rastreamento</span><span class="sxs-lookup"><span data-stu-id="e35a9-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="e35a9-113">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="e35a9-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="e35a9-114">Iniciar e parar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="e35a9-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="e35a9-115">Modificar o caminho do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="e35a9-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="e35a9-116">Modificar a conta de serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="e35a9-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="e35a9-117">Modificar a porta na qual o serviço do AGPM escuta</span><span class="sxs-lookup"><span data-stu-id="e35a9-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="e35a9-118">Além disso, como a função de administrador do AGPM inclui as permissões para todas as outras funções, um administrador do AGPM pode executar as tarefas normalmente associadas a qualquer outra função.</span><span class="sxs-lookup"><span data-stu-id="e35a9-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="e35a9-119">[Executar tarefas do aprovador](performing-approver-tasks.md), como criar, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="e35a9-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="e35a9-120">[Executar tarefas do editor](performing-editor-tasks.md), como editar, renomear, rotular ou importar GPOs, criar modelos ou definir um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="e35a9-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="e35a9-121">[Executar tarefas do revisor](performing-reviewer-tasks.md), como configurações de revisão e comparar GPOs</span><span class="sxs-lookup"><span data-stu-id="e35a9-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="e35a9-122">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="e35a9-122">Additional considerations</span></span>

<span data-ttu-id="e35a9-123">Por padrão, a função de administrador do AGPM tem controle total – todas as permissões do AGPM:</span><span class="sxs-lookup"><span data-stu-id="e35a9-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="e35a9-124">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="e35a9-124">List Contents</span></span>

-   <span data-ttu-id="e35a9-125">Ler configurações</span><span class="sxs-lookup"><span data-stu-id="e35a9-125">Read Settings</span></span>

-   <span data-ttu-id="e35a9-126">Editar configurações</span><span class="sxs-lookup"><span data-stu-id="e35a9-126">Edit Settings</span></span>

-   <span data-ttu-id="e35a9-127">Criar GPO</span><span class="sxs-lookup"><span data-stu-id="e35a9-127">Create GPO</span></span>

-   <span data-ttu-id="e35a9-128">Implantar GPO</span><span class="sxs-lookup"><span data-stu-id="e35a9-128">Deploy GPO</span></span>

-   <span data-ttu-id="e35a9-129">Excluir GPO</span><span class="sxs-lookup"><span data-stu-id="e35a9-129">Delete GPO</span></span>

-   <span data-ttu-id="e35a9-130">Opções de modificação</span><span class="sxs-lookup"><span data-stu-id="e35a9-130">Modify Options</span></span>

-   <span data-ttu-id="e35a9-131">Modificar a segurança</span><span class="sxs-lookup"><span data-stu-id="e35a9-131">Modify Security</span></span>

-   <span data-ttu-id="e35a9-132">Criar modelo</span><span class="sxs-lookup"><span data-stu-id="e35a9-132">Create Template</span></span>

<span data-ttu-id="e35a9-133">As permissões de **modificação** e **modificação de segurança** são exclusivas da função de administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="e35a9-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





