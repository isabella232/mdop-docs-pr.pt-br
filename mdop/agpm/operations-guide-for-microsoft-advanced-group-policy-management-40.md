---
title: Guia operacional do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
description: Guia operacional do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
author: dansimp
ms.assetid: 0bafeba3-20a9-4360-be5d-03f786df11ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b51956c319f1b0a77e4a4bdf71090be4f322236e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797734"
---
# <span data-ttu-id="bf62d-103">Guia operacional do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="bf62d-103">Operations Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="bf62d-104">Você pode usar o gerenciamento avançado de política de grupo (AGPM) da Microsoft para estender os recursos do GPMC (console de gerenciamento de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="bf62d-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="bf62d-105">O AGPM oferece controle de alterações abrangente e gerenciamento aprimorado dos objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="bf62d-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="bf62d-106">Usando o AGPM, você pode realizar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="bf62d-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="bf62d-107">Realize a edição offline de GPOs para que você possa criá-los e testá-los antes de implantá-los em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="bf62d-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="bf62d-108">Mantenha várias versões de um GPO em um arquivo central para que você possa reverter se ocorrer um problema.</span><span class="sxs-lookup"><span data-stu-id="bf62d-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="bf62d-109">Compartilhe a responsabilidade de edição, aprovação e revisão de GPOs entre várias pessoas usando a delegação baseada em função.</span><span class="sxs-lookup"><span data-stu-id="bf62d-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="bf62d-110">Elimine o perigo de vários administradores de política de grupo substituirem um do outro usando o recurso de check-in e check-out para GPOs.</span><span class="sxs-lookup"><span data-stu-id="bf62d-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="bf62d-111">Analisar alterações em um GPO, comparando-a com outro GPO ou outra versão do mesmo GPO usando o relatório de diferença.</span><span class="sxs-lookup"><span data-stu-id="bf62d-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="bf62d-112">Simplifique a criação de novos GPOs usando modelos de GPO, o armazenamento de configurações de política e de preferências comuns a serem usadas como pontos de partida para novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="bf62d-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="bf62d-113">Acesso de representante ao ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="bf62d-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="bf62d-114">Pesquisar GPOs com atributos específicos e filtrar a lista de GPOs exibida.</span><span class="sxs-lookup"><span data-stu-id="bf62d-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="bf62d-115">Exportar um GPO para um arquivo para que você possa copiá-lo de um domínio em uma floresta de teste para um domínio em uma floresta de produção.</span><span class="sxs-lookup"><span data-stu-id="bf62d-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="bf62d-116">O AGPM adiciona uma pasta de **controle de alterações** em cada domínio exibido no GPMC, além de uma guia **histórico** para cada GPO e link de política de grupo exibido no GPMC.</span><span class="sxs-lookup"><span data-stu-id="bf62d-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="bf62d-117">Visão geral do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="bf62d-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="bf62d-118">Práticas recomendadas para o controle de versão</span><span class="sxs-lookup"><span data-stu-id="bf62d-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="bf62d-119">Lista de verificação: Administrar o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="bf62d-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="bf62d-120">Lista de verificação: Criar, editar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="bf62d-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="bf62d-121">Pesquisar e filtrar a lista de GPOs</span><span class="sxs-lookup"><span data-stu-id="bf62d-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="bf62d-122">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="bf62d-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="bf62d-123">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="bf62d-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="bf62d-124">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="bf62d-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="bf62d-125">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="bf62d-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="bf62d-126">Solução de problemas do AGPM</span><span class="sxs-lookup"><span data-stu-id="bf62d-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="bf62d-127">Interface do usuário: Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="bf62d-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





