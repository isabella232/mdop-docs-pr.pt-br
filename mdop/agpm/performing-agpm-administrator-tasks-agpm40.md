---
title: Executar tarefas de administração de AGPM
description: Executar tarefas de administração de AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799068"
---
# <span data-ttu-id="b8f94-103">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="b8f94-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="b8f94-104">O gerenciamento avançado de política de grupo (AGPM) permite que um administrador do AGPM (controle total) Configure opções em todo o domínio e delegue permissões para Aprovadores, editores, revisores e administradores do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b8f94-104">Advanced Group Policy Management (AGPM) lets an AGPM Administrator (Full Control) configure domain-wide options and delegate permissions to Approvers, Editors, Reviewers, and AGPM Administrators.</span></span> <span data-ttu-id="b8f94-105">Por padrão, um administrador do AGPM é alguém que tem controle total – todas as permissões do AGPM e, portanto, podem executar tarefas associadas a qualquer função.</span><span class="sxs-lookup"><span data-stu-id="b8f94-105">By default, an AGPM Administrator is someone who has Full Control— all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="b8f94-106">Em um ambiente no qual várias pessoas desenvolvem objetos de política de grupo (GPOs), você pode optar por permitir que todos os administradores de política de grupo realizem as mesmas tarefas e tenham o mesmo nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="b8f94-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose to let all Group Policy administrators perform the same tasks and have the same level of access.</span></span> <span data-ttu-id="b8f94-107">Ou você pode optar por permitir que os administradores do AGPM deleguem permissões para editores que podem alterar GPOs e para Aprovadores que implantam GPOs no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="b8f94-107">Or, you can choose to let AGPM Administrators delegate permissions to Editors who can change GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="b8f94-108">Os administradores do AGPM podem configurar permissões para atender às necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="b8f94-108">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="b8f94-109">[Configurando o gerenciamento avançado de política de grupo](configuring-advanced-group-policy-management-agpm40.md): Configure a conexão do servidor de AGPM e a notificação por email, acesse o acesso a GPOs no ambiente de produção e configure o registro em log e o rastreamento para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="b8f94-109">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="b8f94-110">[Gerenciar o arquivo](managing-the-archive-agpm40.md): delegar o acesso a GPOs no arquivo morto, limitar o número de versões de cada GPO armazenado, importar um GPO de outro domínio e fazer backup e restaurar o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b8f94-110">[Managing the Archive](managing-the-archive-agpm40.md): Delegate access to GPOs in the archive, limit the number of versions of each GPO stored, import a GPO from another domain, and back up and restore the archive.</span></span>

-   <span data-ttu-id="b8f94-111">[Gerenciando o serviço do AGPM](managing-the-agpm-service-agpm40.md): Pare e inicie o serviço do AGPM ou altere o caminho do arquivo do AGPM, a conta de serviço do AGPM ou a porta que o serviço do AGPM escuta.</span><span class="sxs-lookup"><span data-stu-id="b8f94-111">[Managing the AGPM Service](managing-the-agpm-service-agpm40.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="b8f94-112">[Mova o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive-agpm40.md): Mova o serviço do AGPM, o arquivo ou ambos para um servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="b8f94-112">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="b8f94-113">**Observação**  Como a função de administrador do AGPM inclui as permissões para todas as outras funções, um administrador do AGPM pode executar as tarefas geralmente associadas a qualquer outra função.</span><span class="sxs-lookup"><span data-stu-id="b8f94-113">**Note** Because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks usually associated with any other role.</span></span>

<span data-ttu-id="b8f94-114">[Executar tarefas do aprovador](performing-approver-tasks-agpm40.md), como criar, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="b8f94-114">[Performing Approver Tasks](performing-approver-tasks-agpm40.md), such as creating, deploying, or deleting GPOs</span></span>

<span data-ttu-id="b8f94-115">[Executar tarefas do editor](performing-editor-tasks-agpm40.md), como editar, renomear, rotular ou importar GPOs, criar modelos ou definir um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="b8f94-115">[Performing Editor Tasks](performing-editor-tasks-agpm40.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

<span data-ttu-id="b8f94-116">[Executar tarefas do revisor](performing-reviewer-tasks-agpm40.md), como configurações de revisão e comparar GPOs</span><span class="sxs-lookup"><span data-stu-id="b8f94-116">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md), such as reviewing settings and comparing GPOs</span></span>

 

### <span data-ttu-id="b8f94-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="b8f94-117">Additional considerations</span></span>

<span data-ttu-id="b8f94-118">Por padrão, a função de administrador do AGPM tem controle total – todas as permissões do AGPM:</span><span class="sxs-lookup"><span data-stu-id="b8f94-118">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="b8f94-119">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="b8f94-119">List Contents</span></span>

-   <span data-ttu-id="b8f94-120">Ler configurações</span><span class="sxs-lookup"><span data-stu-id="b8f94-120">Read Settings</span></span>

-   <span data-ttu-id="b8f94-121">Editar configurações</span><span class="sxs-lookup"><span data-stu-id="b8f94-121">Edit Settings</span></span>

-   <span data-ttu-id="b8f94-122">Criar GPO</span><span class="sxs-lookup"><span data-stu-id="b8f94-122">Create GPO</span></span>

-   <span data-ttu-id="b8f94-123">Implantar GPO</span><span class="sxs-lookup"><span data-stu-id="b8f94-123">Deploy GPO</span></span>

-   <span data-ttu-id="b8f94-124">Excluir GPO</span><span class="sxs-lookup"><span data-stu-id="b8f94-124">Delete GPO</span></span>

-   <span data-ttu-id="b8f94-125">GPO de exportação</span><span class="sxs-lookup"><span data-stu-id="b8f94-125">Export GPO</span></span>

-   <span data-ttu-id="b8f94-126">Importar GPO</span><span class="sxs-lookup"><span data-stu-id="b8f94-126">Import GPO</span></span>

-   <span data-ttu-id="b8f94-127">Criar modelo</span><span class="sxs-lookup"><span data-stu-id="b8f94-127">Create Template</span></span>

-   <span data-ttu-id="b8f94-128">Opções de modificação</span><span class="sxs-lookup"><span data-stu-id="b8f94-128">Modify Options</span></span>

-   <span data-ttu-id="b8f94-129">Modificar a segurança</span><span class="sxs-lookup"><span data-stu-id="b8f94-129">Modify Security</span></span>

<span data-ttu-id="b8f94-130">As permissões de **modificação** e **modificação de segurança** são exclusivas da função de administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="b8f94-130">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





