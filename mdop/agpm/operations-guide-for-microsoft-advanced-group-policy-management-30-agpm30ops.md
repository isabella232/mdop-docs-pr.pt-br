---
title: Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft
description: Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft
author: dansimp
ms.assetid: aaefe6d1-a9e5-43eb-b4d8-85880798cb8b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4958609444a62560060a565fb8626bcc9680fd9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799086"
---
# <span data-ttu-id="0fd9b-103">Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="0fd9b-103">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="0fd9b-104">Você pode usar o gerenciamento avançado de política de grupo (AGPM) da Microsoft para estender os recursos do console de gerenciamento de política de grupo (GPMC), fornecendo controle de alterações abrangente e gerenciamento aprimorado para GPOs (objetos de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="0fd9b-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="0fd9b-105">Com o AGPM, você pode:</span><span class="sxs-lookup"><span data-stu-id="0fd9b-105">With AGPM you can:</span></span>

-   <span data-ttu-id="0fd9b-106">Realize a edição offline de GPOs para que você possa criá-los e testá-los antes de implantá-los em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="0fd9b-107">Reter várias versões de um GPO em um arquivo central, para que você possa reverter se ocorrer um problema.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="0fd9b-108">Compartilhe a responsabilidade de edição, aprovação e revisão de GPOs entre várias pessoas usando a delegação baseada em função.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="0fd9b-109">Elimine o perigo de vários administradores de política de grupo substituirem o trabalho uns dos outros usando uma funcionalidade de check-in/check-out para GPOs.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="0fd9b-110">Analise as alterações em um GPO, comparando-o a outro GPO ou outra versão do mesmo GPO usando o relatório de diferença.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="0fd9b-111">Simplifique a criação de novos GPOs usando modelos de GPO, armazenando configurações padrão para usar como pontos de partida para novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="0fd9b-112">O AGPM adiciona uma pasta de **controle de alterações** em cada domínio exibido no GPMC, bem como uma guia **histórico** para cada GPO e link de política de grupo exibido no GPMC.</span><span class="sxs-lookup"><span data-stu-id="0fd9b-112">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, as well as a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="0fd9b-113">Visão geral do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0fd9b-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-114">Práticas recomendadas para o controle de versão</span><span class="sxs-lookup"><span data-stu-id="0fd9b-114">Best Practices for Version Control</span></span>](best-practices-for-version-control.md)

-   [<span data-ttu-id="0fd9b-115">Lista de verificação: Administrar o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="0fd9b-115">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive.md)

-   [<span data-ttu-id="0fd9b-116">Lista de verificação: Criar, editar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="0fd9b-116">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-117">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="0fd9b-117">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-118">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="0fd9b-118">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-119">Execução de tarefas do aprovador</span><span class="sxs-lookup"><span data-stu-id="0fd9b-119">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-120">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="0fd9b-120">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-121">Solução de problemas do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0fd9b-121">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="0fd9b-122">Interface do usuário: Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0fd9b-122">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

 

 





