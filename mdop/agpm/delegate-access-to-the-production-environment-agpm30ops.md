---
title: Delegar acesso ao ambiente de produção
description: Delegar acesso ao ambiente de produção
author: dansimp
ms.assetid: c1ebae2e-909b-4e64-b368-b7d3cc67b1eb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4667a23f1584d7aab6143860721e326da6407afb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797840"
---
# <span data-ttu-id="eb74a-103">Delegar acesso ao ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="eb74a-103">Delegate Access to the Production Environment</span></span>


<span data-ttu-id="eb74a-104">Você pode alterar o acesso aos objetos de política de grupo (GPOs) no ambiente de produção, substituindo as permissões existentes nesses GPOs.</span><span class="sxs-lookup"><span data-stu-id="eb74a-104">You can change access to Group Policy Objects (GPOs) in the production environment, replacing any existing permissions on those GPOs.</span></span> <span data-ttu-id="eb74a-105">Você pode configurar permissões no nível do domínio para permitir ou impedir que os usuários editem, excluam ou modifiquem a segurança de GPOs no ambiente de produção quando não estiverem usando a pasta de **controle de alterações** no GPMC (console de gerenciamento de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="eb74a-105">You can configure permissions at the domain level to either allow or prevent users from editing, deleting, or modifying the security of GPOs in the production environment when they are not using the **Change Control** folder in the Group Policy Management Console (GPMC).</span></span>

**<span data-ttu-id="eb74a-106">Observação</span><span class="sxs-lookup"><span data-stu-id="eb74a-106">Note</span></span>**  
-   <span data-ttu-id="eb74a-107">Delegar o acesso ao ambiente de produção não afeta a capacidade dos usuários de vincular GPOs.</span><span class="sxs-lookup"><span data-stu-id="eb74a-107">Delegating access to the production environment does not affect users’ ability to link GPOs.</span></span>

-   <span data-ttu-id="eb74a-108">Quando os GPOs são controlados ou implantados, o acesso a todas as outras contas, exceto aquelas com permissões de **leitura** e **aplicação** , é removido.</span><span class="sxs-lookup"><span data-stu-id="eb74a-108">When GPOs are controlled or deployed, access for any other accounts except those with **Read** and **Apply** permissions is removed.</span></span>

 

<span data-ttu-id="eb74a-109">Uma conta de usuário que tenha as permissões necessárias no AGPM (gerenciamento avançado de política de grupo) ou a função do administrador do AGPM (controle total) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="eb74a-109">A user account that has either the necessary permissions in Advanced Group Policy Management (AGPM) or the role of AGPM Administrator (Full Control) is required to complete this procedure.</span></span> <span data-ttu-id="eb74a-110">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="eb74a-110">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="eb74a-111">Para alterar o acesso a GPOs no ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="eb74a-111">To change access to GPOs in the production environment</span></span>**

1.  <span data-ttu-id="eb74a-112">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="eb74a-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="eb74a-113">Clique na guia **delegação de produção** .</span><span class="sxs-lookup"><span data-stu-id="eb74a-113">Click the **Production Delegation** tab.</span></span>

3.  <span data-ttu-id="eb74a-114">Para adicionar permissões para um usuário ou grupo que não tenha acesso ao ambiente de produção ou para substituir as permissões de um usuário ou grupo que tem acesso:</span><span class="sxs-lookup"><span data-stu-id="eb74a-114">To add permissions for a user or group that does not have access to the production environment, or to replace the permissions for a user or group that does have access:</span></span>

    1.  <span data-ttu-id="eb74a-115">Clique em **Adicionar**, selecione um usuário ou grupo e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb74a-115">Click **Add**, select a user or group, and then click **OK**.</span></span>

    2.  <span data-ttu-id="eb74a-116">Selecione permissões para delegar a esse usuário ou grupo para o ambiente de produção e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb74a-116">Select permissions to delegate to that user or group for the production environment, and then click **OK**.</span></span>

4.  <span data-ttu-id="eb74a-117">Para remover todas as permissões para o ambiente de produção de um usuário ou grupo, selecione o usuário ou grupo, clique em **remover**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb74a-117">To remove all permissions to the production environment for a user or group, select the user or group, click **Remove**, and then click **OK**.</span></span>

### <span data-ttu-id="eb74a-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="eb74a-118">Additional considerations</span></span>

-   <span data-ttu-id="eb74a-119">Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="eb74a-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="eb74a-120">Especificamente, você deve ter permissão de **modificação de segurança** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="eb74a-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="eb74a-121">As permissões para a conta de serviço do AGPM não podem ser alteradas na guia de **delegação de produção** .</span><span class="sxs-lookup"><span data-stu-id="eb74a-121">Permissions for the AGPM Service Account cannot be changed on the **Production Delegation** tab.</span></span>

-   <span data-ttu-id="eb74a-122">Por padrão, as contas a seguir têm permissões para GPOs no ambiente de produção:</span><span class="sxs-lookup"><span data-stu-id="eb74a-122">By default, the following accounts have permissions for GPOs in the production environment:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="eb74a-123">Account</span><span class="sxs-lookup"><span data-stu-id="eb74a-123">Account</span></span></th>
    <th align="left"><span data-ttu-id="eb74a-124">Permissões padrão para GPOs</span><span class="sxs-lookup"><span data-stu-id="eb74a-124">Default Permissions for GPOs</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="eb74a-125">&lt;Conta de serviço do AGPM&gt;</span><span class="sxs-lookup"><span data-stu-id="eb74a-125">&lt;AGPM Service Account&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb74a-126">Editar configurações, excluir, modificar segurança</span><span class="sxs-lookup"><span data-stu-id="eb74a-126">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="eb74a-127">Usuários autenticados</span><span class="sxs-lookup"><span data-stu-id="eb74a-127">Authenticated Users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb74a-128">Ler, aplicar</span><span class="sxs-lookup"><span data-stu-id="eb74a-128">Read, Apply</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="eb74a-129">Administradores de domínio</span><span class="sxs-lookup"><span data-stu-id="eb74a-129">Domain Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb74a-130">Editar configurações, excluir, modificar segurança</span><span class="sxs-lookup"><span data-stu-id="eb74a-130">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="eb74a-131">Administradores de empresas</span><span class="sxs-lookup"><span data-stu-id="eb74a-131">Enterprise Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb74a-132">Editar configurações, excluir, modificar segurança</span><span class="sxs-lookup"><span data-stu-id="eb74a-132">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="eb74a-133">Controladores de domínio da empresa</span><span class="sxs-lookup"><span data-stu-id="eb74a-133">Enterprise Domain Controllers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb74a-134">Leitura</span><span class="sxs-lookup"><span data-stu-id="eb74a-134">Read</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="eb74a-135">Sistema</span><span class="sxs-lookup"><span data-stu-id="eb74a-135">System</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb74a-136">Editar configurações, excluir, modificar segurança</span><span class="sxs-lookup"><span data-stu-id="eb74a-136">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="eb74a-137">A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="eb74a-137">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="eb74a-138">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="eb74a-138">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="eb74a-139">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="eb74a-139">Additional references</span></span>

-   [<span data-ttu-id="eb74a-140">Configuração do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="eb74a-140">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





