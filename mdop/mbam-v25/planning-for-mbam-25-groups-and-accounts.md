---
title: Planejamento para contas e grupos do MBAM 2.5
description: Planejamento para contas e grupos do MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799745"
---
# <span data-ttu-id="4c622-103">Planejamento para contas e grupos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4c622-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="4c622-104">Este tópico lista as funções e as contas que você deve criar nos serviços de domínio Active Directory (AD DS) para fornecer direitos de segurança e acesso para os bancos de dados do Microsoft BitLocker Administration and Monitoring (MBAM), relatórios e aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="4c622-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="4c622-105">Para cada função e conta, o campo correspondente no assistente de configuração do servidor MBAM é fornecido.</span><span class="sxs-lookup"><span data-stu-id="4c622-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="4c622-106">Para obter uma lista dos cmdlets e parâmetros do Windows PowerShell correspondentes a essas contas, consulte [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span><span class="sxs-lookup"><span data-stu-id="4c622-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="4c622-107">Observação</span><span class="sxs-lookup"><span data-stu-id="4c622-107">Note</span></span>**  
<span data-ttu-id="4c622-108">O MBAM não dá suporte ao uso de contas de serviço gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4c622-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="4c622-109">Contas de banco de dados</span><span class="sxs-lookup"><span data-stu-id="4c622-109">Database accounts</span></span>


<span data-ttu-id="4c622-110">Crie as contas a seguir para o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4c622-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c622-111">Nome da conta e finalidade</span><span class="sxs-lookup"><span data-stu-id="4c622-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="4c622-112">Tipo de conta</span><span class="sxs-lookup"><span data-stu-id="4c622-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="4c622-113">Campo do assistente de configuração do MBAM Server correspondente a essa conta</span><span class="sxs-lookup"><span data-stu-id="4c622-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="4c622-114">Descrição do campo assistente de configuração do servidor MBAM que corresponde a essa conta</span><span class="sxs-lookup"><span data-stu-id="4c622-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c622-115">Banco de dados de auditoria e conformidade e banco de dados de recuperação ou grupo de leitura/gravação para relatórios</span><span class="sxs-lookup"><span data-stu-id="4c622-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-116">Usuário ou grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-117">Usuário ou grupo de domínio de acesso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4c622-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-118">Usuário ou grupo de domínio que tem acesso de leitura/gravação para o banco de dados de conformidade e auditoria e o banco de dados de recuperação para permitir que os aplicativos Web acessem os dados e relatórios nestes bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="4c622-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="4c622-119">Se você inserir um nome de usuário nesse campo, ele deverá ser o mesmo valor do valor no <strong> campo conta de domínio do pool de aplicativos de serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="4c622-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="4c622-120">Se você inserir um nome de grupo nesse campo, o valor no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> deve ser um membro do grupo que você inserir nesse campo.</span><span class="sxs-lookup"><span data-stu-id="4c622-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c622-121">O banco de dados de auditoria e o usuário ou grupo de auditoria somente leitura para relatórios</span><span class="sxs-lookup"><span data-stu-id="4c622-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-122">Usuário ou grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-123">Usuário ou grupo de domínio de acesso somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c622-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-124">Nome do usuário ou grupo que terá acesso somente leitura ao banco de dados de conformidade e auditoria para permitir que os relatórios acessem os dados de conformidade e auditoria neste banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4c622-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="4c622-125">Se você inserir um nome de usuário nesse campo, ele deverá ser o mesmo usuário que você especificou no <strong> campo conta de domínio de banco de dados de auditoria e conformidade </strong> na <strong> página Configurar relatórios </strong> .</span><span class="sxs-lookup"><span data-stu-id="4c622-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="4c622-126">Se você inserir um nome de grupo nesse campo, o valor especificado no <strong> campo conta de domínio de banco de dados de auditoria e de auditoria </strong> na <strong> página Configurar relatórios </strong> deve ser um membro do grupo especificado nesse campo.</span><span class="sxs-lookup"><span data-stu-id="4c622-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4c622-127">Contas de relatório</span><span class="sxs-lookup"><span data-stu-id="4c622-127">Reporting accounts</span></span>


<span data-ttu-id="4c622-128">Crie as contas a seguir para o recurso relatórios.</span><span class="sxs-lookup"><span data-stu-id="4c622-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c622-129">Nome da conta/finalidade</span><span class="sxs-lookup"><span data-stu-id="4c622-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="4c622-130">Tipo de conta</span><span class="sxs-lookup"><span data-stu-id="4c622-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="4c622-131">Campo do assistente de configuração do MBAM Server correspondente a essa conta</span><span class="sxs-lookup"><span data-stu-id="4c622-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="4c622-132">Descrição do campo assistente de configuração do servidor MBAM que corresponde a essa conta</span><span class="sxs-lookup"><span data-stu-id="4c622-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c622-133">Grupo de acesso de domínio somente leitura de relatórios</span><span class="sxs-lookup"><span data-stu-id="4c622-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-134">Grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-135">Grupo de domínio da função de relatório</span><span class="sxs-lookup"><span data-stu-id="4c622-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-136">Especifica o grupo de usuários do domínio que tem acesso somente leitura aos relatórios no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4c622-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="4c622-137">O grupo especificado deve ser o mesmo que você especificou para o parâmetro de grupo de acesso somente leitura de relatórios quando os aplicativos Web estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="4c622-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c622-138">Conta de usuário do domínio de banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="4c622-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-139">Usuário</span><span class="sxs-lookup"><span data-stu-id="4c622-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-140">Conta de domínio de banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="4c622-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-141">Conta e senha de usuário do domínio que a instância local do SQL Server Reporting Services usa para acessar o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="4c622-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="4c622-142">Esta conta exige <strong> logon como direitos de lote </strong> para o servidor do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="4c622-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="4c622-143">Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um nome de usuário, você deverá digitar esse mesmo valor neste campo.</span><span class="sxs-lookup"><span data-stu-id="4c622-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="4c622-144">Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um nome de grupo, o valor que você inserir nesse campo deve ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="4c622-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="4c622-145">Configure a senha desta conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="4c622-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="4c622-146">A conta de usuário deve ser capaz de acessar todos os dados que estão disponíveis para o grupo de usuários do MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="4c622-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="4c622-147">Contas de site de administração e monitoramento (Help Desk)</span><span class="sxs-lookup"><span data-stu-id="4c622-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="4c622-148">Crie as contas a seguir para o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4c622-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c622-149">Nome da conta/finalidade</span><span class="sxs-lookup"><span data-stu-id="4c622-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="4c622-150">Tipo de conta</span><span class="sxs-lookup"><span data-stu-id="4c622-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="4c622-151">Campo do assistente de configuração do MBAM Server correspondente a essa conta</span><span class="sxs-lookup"><span data-stu-id="4c622-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="4c622-152">Descrição do campo assistente de configuração do servidor MBAM que corresponde a essa conta</span><span class="sxs-lookup"><span data-stu-id="4c622-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c622-153">Conta de domínio do pool de aplicativos do serviço Web</span><span class="sxs-lookup"><span data-stu-id="4c622-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-154">Usuário</span><span class="sxs-lookup"><span data-stu-id="4c622-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-155">Conta de domínio do pool de aplicativos do serviço Web</span><span class="sxs-lookup"><span data-stu-id="4c622-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-156">Conta de usuário do domínio a ser usada pelo pool de aplicativos para os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="4c622-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="4c622-157">Se você inserir um nome de usuário no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , você deverá digitar esse mesmo valor neste campo.</span><span class="sxs-lookup"><span data-stu-id="4c622-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="4c622-158">Se você inserir um nome de grupo no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , o valor que você inserir nesse campo deverá ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="4c622-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="4c622-159">Se você não especificar credenciais, as credenciais que foram especificadas para qualquer aplicativo da Web habilitado anteriormente serão usadas.</span><span class="sxs-lookup"><span data-stu-id="4c622-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="4c622-160">Todos os aplicativos Web devem usar as mesmas credenciais de pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4c622-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="4c622-161">Se você especificar credenciais diferentes para diferentes aplicativos da Web, o valor especificado mais recentemente será usado.</span><span class="sxs-lookup"><span data-stu-id="4c622-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4c622-162">Importante</span><span class="sxs-lookup"><span data-stu-id="4c622-162">Important</span></span></strong><br/><p><span data-ttu-id="4c622-163">Para aumentar a segurança, defina a conta especificada nas credenciais para ter direitos de usuário limitados.</span><span class="sxs-lookup"><span data-stu-id="4c622-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c622-164">Grupo de acesso de usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-165">Grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-166">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-167">Grupo de usuários do domínio cujos membros têm acesso a todas as áreas de recuperação do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4c622-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="4c622-168">Os usuários que têm essa função precisam inserir apenas a chave de recuperação, e não o domínio do usuário final e o nome de usuário, ao ajudar os usuários finais a recuperarem suas unidades.</span><span class="sxs-lookup"><span data-stu-id="4c622-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="4c622-169">Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões de grupo usuários da assistência avançada do MBAM poderão substituir as permissões do grupo MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="4c622-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c622-170">Grupo de acesso de usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-171">Grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-172">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-173">Grupo de usuários do domínio cujos membros têm acesso às áreas gerenciar TPM e unidade de recuperação do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="4c622-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="4c622-174">As pessoas que têm essa função devem preencher todos os campos, incluindo o nome do domínio e o nome da conta do usuário final, quando eles usam qualquer uma dessas opções.</span><span class="sxs-lookup"><span data-stu-id="4c622-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="4c622-175">Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões de grupo usuários da assistência avançada do MBAM poderão substituir as permissões do grupo MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="4c622-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c622-176">Grupo de acesso de usuários de relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-177">Grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-178">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-179">Grupo de usuários do domínio cujos membros têm acesso somente leitura aos relatórios na área relatórios do site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4c622-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c622-180">Grupo de usuários de migração de dados MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-181">Grupo</span><span class="sxs-lookup"><span data-stu-id="4c622-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-182">Usuários de migração de dados do MBAM</span><span class="sxs-lookup"><span data-stu-id="4c622-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c622-183">Grupo de usuários de domínio opcional cujos membros têm permissões para gravar dados no MBAM usando o serviço de recuperação e hardware do MBAM em execução no servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="4c622-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="4c622-184">Essa conta geralmente é usada com os cmdlets Write-MBAM \* para gravar dados de recuperação e TPM do Active Directory no banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="4c622-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="4c622-185">Para obter mais informações, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> MBAM 2,5 considerações de segurança </a> .</span><span class="sxs-lookup"><span data-stu-id="4c622-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="4c622-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c622-186">Related topics</span></span>


[<span data-ttu-id="4c622-187">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4c622-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="4c622-188">Pré-requisitos para implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4c622-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="4c622-189">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="4c622-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4c622-190">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4c622-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4c622-191">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4c622-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





