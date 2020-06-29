---
title: Guia Delegação de Domínio
description: Guia Delegação de Domínio
author: dansimp
ms.assetid: 5be5841e-92fb-4af6-aa68-0ae50f8d5141
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5f3b5c3b7d8799b383ab48870fcccad0b0c3f73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797365"
---
# <span data-ttu-id="3156c-103">Guia Delegação de Domínio</span><span class="sxs-lookup"><span data-stu-id="3156c-103">Domain Delegation Tab</span></span>


<span data-ttu-id="3156c-104">A guia de **delegação de domínio** no painel de **controle alterar** fornece uma lista de administradores de política de grupo que têm acesso ao arquivo no nível do domínio e indicam as funções de cada um.</span><span class="sxs-lookup"><span data-stu-id="3156c-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="3156c-105">Além disso, esta guia habilita os administradores do AGPM (controle total) a configurar permissões no nível do domínio para editores, Aprovadores, revisores e outros administradores do AGPM.</span><span class="sxs-lookup"><span data-stu-id="3156c-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="3156c-106">Há duas seções na guia de **delegação de domínio** – configuração de notificação por email e delegação baseada em função para gerenciamento avançado de política de grupo (AGPM) no nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="3156c-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="3156c-107">Configuração de notificação por email</span><span class="sxs-lookup"><span data-stu-id="3156c-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="3156c-108">A seção de notificação por email desta guia identifica os aprovadores que receberão notificações quando as operações estiverem pendentes no AGPM.</span><span class="sxs-lookup"><span data-stu-id="3156c-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3156c-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="3156c-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="3156c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3156c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3156c-111">Endereço de email de</span><span class="sxs-lookup"><span data-stu-id="3156c-111">From e-mail address</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-112">O alias do AGPM do qual a notificação é enviada aos aprovadores.</span><span class="sxs-lookup"><span data-stu-id="3156c-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="3156c-113">Em um ambiente com vários domínios, isso pode ser o mesmo alias em todo o ambiente ou um alias diferente para cada domínio.</span><span class="sxs-lookup"><span data-stu-id="3156c-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3156c-114">Para endereço de email</span><span class="sxs-lookup"><span data-stu-id="3156c-114">To e-mail address</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-115">Uma lista delimitada por vírgulas de endereços de email de aprovadores para quem a notificação deve ser enviada</span><span class="sxs-lookup"><span data-stu-id="3156c-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3156c-116">Servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="3156c-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-117">O nome do servidor de email, como mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3156c-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3156c-118">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="3156c-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-119">Um usuário com acesso ao servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="3156c-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3156c-120">Senha</span><span class="sxs-lookup"><span data-stu-id="3156c-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-121">Senha do usuário para autenticação para o servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="3156c-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3156c-122">Confirmar senha</span><span class="sxs-lookup"><span data-stu-id="3156c-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-123">Confirmar senha do usuário</span><span class="sxs-lookup"><span data-stu-id="3156c-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3156c-124">Delegação baseada em função no nível de domínio</span><span class="sxs-lookup"><span data-stu-id="3156c-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="3156c-125">A seção delegação baseada em função desta guia exibe e permite que um administrador do AGPM delegue permissões permitidas, negadas e herdadas para cada grupo e usuário no domínio com acesso ao arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="3156c-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="3156c-126">Um administrador do AGPM pode configurar permissões de todo o domínio usando funções de AGPM padrão (editor, Aprovador, revisor e administrador do AGPM) ou uma combinação personalizada de permissões para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="3156c-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3156c-127">Botão</span><span class="sxs-lookup"><span data-stu-id="3156c-127">Button</span></span></th>
<th align="left"><span data-ttu-id="3156c-128">Efeito</span><span class="sxs-lookup"><span data-stu-id="3156c-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3156c-129">Adicionar</span><span class="sxs-lookup"><span data-stu-id="3156c-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-130">Adicione uma nova entrada ao descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="3156c-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="3156c-131">Qualquer usuário ou grupo no Active Directory pode ser adicionado como administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="3156c-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3156c-132">Remover</span><span class="sxs-lookup"><span data-stu-id="3156c-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-133">Remover os administradores de política de grupo selecionados da lista controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="3156c-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3156c-134">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3156c-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-135">Exibir as propriedades dos administradores de política de grupo selecionados.</span><span class="sxs-lookup"><span data-stu-id="3156c-135">Display the properties for the selected Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3156c-136">Avançado</span><span class="sxs-lookup"><span data-stu-id="3156c-136">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3156c-137">Abrir o <strong> Editor de lista de controle de acesso </strong> .</span><span class="sxs-lookup"><span data-stu-id="3156c-137">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3156c-138">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="3156c-138">Additional considerations</span></span>

-   <span data-ttu-id="3156c-139">Para obter informações sobre funções e permissões relacionadas a tarefas específicas, consulte as tarefas em [executando tarefas do administrador do AGPM](performing-agpm-administrator-tasks-agpm40.md), [executando tarefas do editor](performing-editor-tasks-agpm40.md), [executando tarefas do aprovador](performing-approver-tasks-agpm40.md)e [executando tarefas do revisor](performing-reviewer-tasks-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="3156c-139">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="3156c-140">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="3156c-140">Additional references</span></span>

-   [<span data-ttu-id="3156c-141">Interface do usuário: Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="3156c-141">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="3156c-142">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="3156c-142">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





