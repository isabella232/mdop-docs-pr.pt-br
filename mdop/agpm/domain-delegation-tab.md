---
title: Guia Delegação de Domínio
description: Guia Delegação de Domínio
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797363"
---
# <span data-ttu-id="72373-103">Guia Delegação de Domínio</span><span class="sxs-lookup"><span data-stu-id="72373-103">Domain Delegation Tab</span></span>


<span data-ttu-id="72373-104">A guia de **delegação de domínio** no painel de **controle alterar** fornece uma lista de administradores de política de grupo que têm acesso ao arquivo no nível do domínio e indicam as funções de cada um.</span><span class="sxs-lookup"><span data-stu-id="72373-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="72373-105">Além disso, esta guia habilita os administradores do AGPM (controle total) a configurar permissões no nível do domínio para editores, Aprovadores, revisores e outros administradores do AGPM.</span><span class="sxs-lookup"><span data-stu-id="72373-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="72373-106">Há duas seções na guia de **delegação de domínio** – configuração de notificação por email e delegação baseada em função para gerenciamento avançado de política de grupo (AGPM) no nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="72373-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="72373-107">Configuração de notificação por email</span><span class="sxs-lookup"><span data-stu-id="72373-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="72373-108">A seção de notificação por email desta guia identifica os aprovadores que receberão notificações quando as operações estiverem pendentes no AGPM.</span><span class="sxs-lookup"><span data-stu-id="72373-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72373-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="72373-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="72373-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="72373-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72373-111">De</span><span class="sxs-lookup"><span data-stu-id="72373-111">From</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-112">O alias do AGPM do qual a notificação é enviada aos aprovadores.</span><span class="sxs-lookup"><span data-stu-id="72373-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="72373-113">Em um ambiente com vários domínios, isso pode ser o mesmo alias em todo o ambiente ou um alias diferente para cada domínio.</span><span class="sxs-lookup"><span data-stu-id="72373-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72373-114">Para</span><span class="sxs-lookup"><span data-stu-id="72373-114">To</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-115">Uma lista delimitada por vírgulas de endereços de email de aprovadores para quem a notificação deve ser enviada</span><span class="sxs-lookup"><span data-stu-id="72373-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72373-116">Servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="72373-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-117">O nome do servidor de email, como mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72373-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72373-118">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="72373-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-119">Um usuário com acesso ao servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="72373-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72373-120">Senha</span><span class="sxs-lookup"><span data-stu-id="72373-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-121">Senha do usuário para autenticação para o servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="72373-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72373-122">Confirmar senha</span><span class="sxs-lookup"><span data-stu-id="72373-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-123">Confirmar senha do usuário</span><span class="sxs-lookup"><span data-stu-id="72373-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72373-124">Delegação baseada em função no nível de domínio</span><span class="sxs-lookup"><span data-stu-id="72373-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="72373-125">A seção delegação baseada em função desta guia exibe e permite que um administrador do AGPM delegue permissões permitidas, negadas e herdadas para cada grupo e usuário no domínio com acesso ao arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="72373-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="72373-126">Um administrador do AGPM pode configurar permissões de todo o domínio usando funções de AGPM padrão (editor, Aprovador, revisor e administrador do AGPM) ou uma combinação personalizada de permissões para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="72373-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72373-127">Botão</span><span class="sxs-lookup"><span data-stu-id="72373-127">Button</span></span></th>
<th align="left"><span data-ttu-id="72373-128">Efeito</span><span class="sxs-lookup"><span data-stu-id="72373-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72373-129">Adicionar</span><span class="sxs-lookup"><span data-stu-id="72373-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-130">Adicione uma nova entrada ao descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="72373-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="72373-131">Qualquer usuário ou grupo no Active Directory pode ser adicionado como administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="72373-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72373-132">Remover</span><span class="sxs-lookup"><span data-stu-id="72373-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-133">Remover os administradores de política de grupo selecionados da lista controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="72373-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72373-134">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72373-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-135">Exibir as propriedades dos administradores de política de grupo selecionados.</span><span class="sxs-lookup"><span data-stu-id="72373-135">Display the properties for the selected Group Policy administrators.</span></span> <span data-ttu-id="72373-136">A página Propriedades é a mesma exibida para um objeto em <strong> usuários e computadores do Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="72373-136">The properties page is the same one displayed for an object in <strong>Active Directory User and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72373-137">Avançado</span><span class="sxs-lookup"><span data-stu-id="72373-137">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72373-138">Abrir o <strong> Editor de lista de controle de acesso </strong> .</span><span class="sxs-lookup"><span data-stu-id="72373-138">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="72373-139">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="72373-139">Additional considerations</span></span>

-   <span data-ttu-id="72373-140">Para obter informações sobre funções e permissões relacionadas a tarefas específicas, consulte as tarefas em [executando tarefas do administrador do AGPM](performing-agpm-administrator-tasks.md), [executando tarefas do editor](performing-editor-tasks.md), [executando tarefas do aprovador](performing-approver-tasks.md)e [executando tarefas do revisor](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="72373-140">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="72373-141">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="72373-141">Additional references</span></span>

-   [<span data-ttu-id="72373-142">Interface do usuário: Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="72373-142">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

-   [<span data-ttu-id="72373-143">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="72373-143">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





