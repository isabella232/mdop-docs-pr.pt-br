---
title: Executar tarefas de administração de AGPM
description: Executar tarefas de administração de AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799069"
---
# <span data-ttu-id="ad2b3-103">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="ad2b3-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="ad2b3-104">No gerenciamento avançado de política de grupo (AGPM), um administrador do AGPM (controle total) configura as opções de todo o domínio e delega permissões para Aprovadores, editores, revisores e outros administradores do AGPM.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-104">In Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="ad2b3-105">Por padrão, um administrador do AGPM é um indivíduo com controle total (todas as permissões do AGPM) e quem, portanto, pode executar tarefas associadas a qualquer função.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-105">By default, an AGPM Administrator is an individual with Full Control—all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="ad2b3-106">Em um ambiente no qual várias pessoas desenvolvem objetos de política de grupo (GPOs), você pode escolher se todos os usuários do AGPM executarão as mesmas tarefas e têm o mesmo nível de acesso ou se os administradores do AGPM delegam permissões para editores que fazem alterações em GPOs e para Aprovadores que implantam GPOs no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose whether all AGPM users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="ad2b3-107">Os administradores do AGPM podem configurar permissões para atender às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="ad2b3-108">[Configurando o gerenciamento avançado de política de grupo](configuring-advanced-group-policy-management.md): Configure a conexão do servidor de AGPM e a notificação por email, acesse o acesso a GPOs no ambiente de produção e configure o registro em log e o rastreamento para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-108">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="ad2b3-109">[Gerenciar o arquivo](managing-the-archive.md): delegar o acesso a GPOs no arquivo morto e limitar o número de versões de cada GPO armazenado.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-109">[Managing the Archive](managing-the-archive.md): Delegate access to GPOs in the archive and limit the number of versions of each GPO stored.</span></span>

-   <span data-ttu-id="ad2b3-110">[Gerenciando o serviço do AGPM](managing-the-agpm-service-agpm30ops.md): Pare e inicie o serviço do AGPM ou altere o caminho do arquivo do AGPM, a conta de serviço do AGPM ou a porta que o serviço do AGPM escuta.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-110">[Managing the AGPM Service](managing-the-agpm-service-agpm30ops.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="ad2b3-111">[Mova o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive.md): Mova o serviço do AGPM, o arquivo ou ambos para um servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-111">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="ad2b3-112">Além disso, como a função de administrador do AGPM inclui as permissões para todas as outras funções, um administrador do AGPM pode executar as tarefas normalmente associadas a qualquer outra função.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-112">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="ad2b3-113">[Executar tarefas do aprovador](performing-approver-tasks-agpm30ops.md), como criar, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="ad2b3-113">[Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="ad2b3-114">[Executar tarefas do editor](performing-editor-tasks-agpm30ops.md), como editar, renomear, rotular ou importar GPOs, criar modelos ou definir um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="ad2b3-114">[Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="ad2b3-115">[Executar tarefas do revisor](performing-reviewer-tasks-agpm30ops.md), como configurações de revisão e comparar GPOs</span><span class="sxs-lookup"><span data-stu-id="ad2b3-115">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="ad2b3-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="ad2b3-116">Additional considerations</span></span>

<span data-ttu-id="ad2b3-117">Por padrão, a função de administrador do AGPM tem controle total – todas as permissões do AGPM:</span><span class="sxs-lookup"><span data-stu-id="ad2b3-117">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="ad2b3-118">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="ad2b3-118">List Contents</span></span>

-   <span data-ttu-id="ad2b3-119">Ler configurações</span><span class="sxs-lookup"><span data-stu-id="ad2b3-119">Read Settings</span></span>

-   <span data-ttu-id="ad2b3-120">Editar configurações</span><span class="sxs-lookup"><span data-stu-id="ad2b3-120">Edit Settings</span></span>

-   <span data-ttu-id="ad2b3-121">Criar GPO</span><span class="sxs-lookup"><span data-stu-id="ad2b3-121">Create GPO</span></span>

-   <span data-ttu-id="ad2b3-122">Implantar GPO</span><span class="sxs-lookup"><span data-stu-id="ad2b3-122">Deploy GPO</span></span>

-   <span data-ttu-id="ad2b3-123">Excluir GPO</span><span class="sxs-lookup"><span data-stu-id="ad2b3-123">Delete GPO</span></span>

-   <span data-ttu-id="ad2b3-124">Opções de modificação</span><span class="sxs-lookup"><span data-stu-id="ad2b3-124">Modify Options</span></span>

-   <span data-ttu-id="ad2b3-125">Modificar a segurança</span><span class="sxs-lookup"><span data-stu-id="ad2b3-125">Modify Security</span></span>

-   <span data-ttu-id="ad2b3-126">Criar modelo</span><span class="sxs-lookup"><span data-stu-id="ad2b3-126">Create Template</span></span>

<span data-ttu-id="ad2b3-127">As permissões de **modificação** e **modificação de segurança** são exclusivas da função de administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="ad2b3-127">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





