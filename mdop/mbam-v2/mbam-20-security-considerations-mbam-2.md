---
title: Considerações de segurança do MBAM 2.0
description: Considerações de segurança do MBAM 2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799367"
---
# <span data-ttu-id="6cf79-103">Considerações de segurança do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6cf79-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="6cf79-104">Este tópico contém uma breve visão geral sobre as contas e grupos, arquivos de log e outras considerações relacionadas à segurança para administração e monitoramento do Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="6cf79-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="6cf79-105">Para obter mais informações, siga os links neste artigo.</span><span class="sxs-lookup"><span data-stu-id="6cf79-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="6cf79-106">Considerações gerais sobre segurança</span><span class="sxs-lookup"><span data-stu-id="6cf79-106">General Security Considerations</span></span>


**<span data-ttu-id="6cf79-107">Compreender os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="6cf79-107">Understand the security risks.</span></span>** <span data-ttu-id="6cf79-108">O risco mais sério da administração e do monitoramento do Microsoft BitLocker é que sua funcionalidade pode ser seqüestrada por um usuário não autorizado que poderia então reconfigurar a criptografia do BitLocker e obter dados da chave de criptografia do BitLocker em clientes do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="6cf79-109">No entanto, a perda de funcionalidade do MBAM por um curto período de tempo, devido a um ataque de negação de serviço, geralmente não tem um impacto catastrófico, ao contrário, por exemplo, e-mail, comunicações de rede, luz e energia.</span><span class="sxs-lookup"><span data-stu-id="6cf79-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="6cf79-110">**Proteja seus computadores fisicamente**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-110">**Physically secure your computers**.</span></span> <span data-ttu-id="6cf79-111">Não há segurança sem segurança física.</span><span class="sxs-lookup"><span data-stu-id="6cf79-111">There is no security without physical security.</span></span> <span data-ttu-id="6cf79-112">Um invasor que obtém acesso físico a um servidor MBAM pode usá-lo para atacar toda a base de clientes.</span><span class="sxs-lookup"><span data-stu-id="6cf79-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="6cf79-113">Todos os possíveis ataques físicos devem ser considerados de alto risco e diminuídos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="6cf79-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="6cf79-114">Os servidores MBAM devem ser armazenados em uma sala de servidor seguro com acesso controlado.</span><span class="sxs-lookup"><span data-stu-id="6cf79-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="6cf79-115">Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.</span><span class="sxs-lookup"><span data-stu-id="6cf79-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="6cf79-116">**Aplicar as atualizações de segurança mais recentes a todos os computadores**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="6cf79-117">Mantenha-se informado sobre novas atualizações para sistemas operacionais, Microsoft SQL Server e MBAM ao assinar o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="6cf79-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="6cf79-118">**Use senhas fortes ou frases secretas**.</span><span class="sxs-lookup"><span data-stu-id="6cf79-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="6cf79-119">Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do MBAM e do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="6cf79-120">Nunca use senhas em branco.</span><span class="sxs-lookup"><span data-stu-id="6cf79-120">Never use blank passwords.</span></span> <span data-ttu-id="6cf79-121">Para obter mais informações sobre os conceitos de senha, consulte o White Paper "senhas de conta e políticas" no TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="6cf79-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="6cf79-122">Contas e grupos no MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="6cf79-123">A prática recomendada para gerenciar contas de usuário é criar grupos globais de domínio e adicionar contas de usuário a eles.</span><span class="sxs-lookup"><span data-stu-id="6cf79-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="6cf79-124">Em seguida, adicione as contas globais do domínio aos grupos locais MBAM necessários nos servidores MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="6cf79-125">Grupos do ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="6cf79-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="6cf79-126">Nenhum grupo do Active Directory é criado automaticamente durante o processo de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="6cf79-127">No entanto, é recomendável que você crie os seguintes grupos globais do ActiveDirectoryDomainServices para gerenciar as operações do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6cf79-128">Nome do Grupo</span><span class="sxs-lookup"><span data-stu-id="6cf79-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="6cf79-129">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6cf79-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-130">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-131">Crie esse grupo para gerenciar os membros do grupo local de usuários da assistência técnica avançada do MBAM criados durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cf79-132">Acesso ao banco de dados de auditoria de conformidade MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-133">Crie esse grupo para gerenciar os membros do grupo local de acesso ao banco de dados de auditoria de conformidade do MBAM criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-134">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-135">Crie esse grupo para gerenciar os membros do grupo local usuários da assistência técnica do MBAM, criados durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cf79-136">Recuperação do MBAM e acesso ao banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="6cf79-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-137">Crie esse grupo para gerenciar os membros do grupo local de MBAM de acesso ao banco de dados de recuperação e de dados de hardware criado durante a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-138">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-139">Crie esse grupo para gerenciar os membros do grupo local usuários do relatório do MBAM criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cf79-140">Administradores do sistema do MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-141">Crie esse grupo para gerenciar os membros do grupo local Administradores do sistema MBAM criados durante a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-142">Isenções de criptografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="6cf79-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-143">Crie esse grupo para gerenciar contas de usuário que devem ser isentadas da criptografia do BitLocker a partir de computadores nos quais eles fazem logon.</span><span class="sxs-lookup"><span data-stu-id="6cf79-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="6cf79-144">Grupos locais do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="6cf79-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="6cf79-145">A instalação do MBAM cria grupos locais para dar suporte às operações do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="6cf79-146">Você deve adicionar os grupos globais do ActiveDirectoryDomainServices aos grupos locais MBAM apropriados para configurar as permissões de segurança MBAM e acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="6cf79-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6cf79-147">Nome do Grupo</span><span class="sxs-lookup"><span data-stu-id="6cf79-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="6cf79-148">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6cf79-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-149">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-150">Os membros deste grupo melhoraram o acesso aos recursos de suporte técnico do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cf79-151">Acesso ao banco de dados de auditoria de conformidade MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-152">Contém as máquinas que têm acesso ao banco de dados de auditoria e conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-153">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-154">Os membros desse grupo têm acesso a alguns dos recursos de suporte técnico da MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cf79-155">Recuperação do MBAM e acesso ao banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="6cf79-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-156">Contém as máquinas que têm acesso ao banco de dados de recuperação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cf79-157">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-158">Os membros desse grupo têm acesso aos relatórios de conformidade e auditoria do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cf79-159">Administradores do sistema do MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cf79-160">Os membros desse grupo têm acesso a todos os recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6cf79-161">Conta de serviço de relatórios SSRS</span><span class="sxs-lookup"><span data-stu-id="6cf79-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="6cf79-162">A conta de serviço relatórios SSRS fornece o contexto de segurança para executar os relatórios do MBAM disponíveis por meio do SSRS.</span><span class="sxs-lookup"><span data-stu-id="6cf79-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="6cf79-163">Ele é configurado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="6cf79-164">Ao configurar a conta de serviço relatórios SSRS, especifique uma conta de usuário de domínio e configure a senha para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="6cf79-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="6cf79-165">**Observação**  Se você alterar o nome da conta de serviço após a implantação do MBAM, será necessário reconfigurar a fonte de dados de relatório para usar as novas credenciais da conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cf79-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="6cf79-166">Caso contrário, você não será capaz de acessar o portal de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="6cf79-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="6cf79-167">Arquivos de log do MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-167">MBAM Log Files</span></span>


<span data-ttu-id="6cf79-168">Os seguintes arquivos de log de instalação do MBAM são criados na pasta% Temp% do usuário de instalação durante a configuração do MBAM:</span><span class="sxs-lookup"><span data-stu-id="6cf79-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="6cf79-169">Arquivos de log de instalação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="6cf79-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="6cf79-170">MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="6cf79-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="6cf79-171">Registra as ações executadas durante a instalação do MBAM e a instalação do recurso MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="6cf79-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="6cf79-172">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="6cf79-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="6cf79-173">Registra as ações executadas para criar a configuração de banco de dados de auditoria e conformidade com o MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="6cf79-174">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="6cf79-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="6cf79-175">Registra ações executadas para criar o banco de dados de recuperação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="6cf79-176">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="6cf79-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="6cf79-177">Registra ações executadas para criar os logons do SQL Server no banco de dados de conformidade e conformidade do MBAM e autorizar o serviço Web do HelpDesk ao banco de dados para relatórios.</span><span class="sxs-lookup"><span data-stu-id="6cf79-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="6cf79-178">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6cf79-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="6cf79-179">Registra as ações executadas para autorizar serviços Web para o banco de dados para recuperação de chave e criar logons para o banco de dados de recuperação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="6cf79-180">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6cf79-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="6cf79-181">Registra as ações executadas para autorizar os serviços Web a MBAM banco de dados de auditoria e conformidade para relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="6cf79-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="6cf79-182">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6cf79-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="6cf79-183">Registra ações executadas para autorizar serviços Web ao banco de dados de recuperação do MBAM para recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="6cf79-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="6cf79-184">**Observação**  Para obter arquivos de log de instalação do MBAM adicionais, você precisa instalar o MBAM usando o pacote msiexec e a &lt; opção/l Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="6cf79-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="6cf79-185">Os arquivos de log são criados no local especificado.</span><span class="sxs-lookup"><span data-stu-id="6cf79-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="6cf79-186">Arquivos de log de configuração do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="6cf79-187">MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="6cf79-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="6cf79-188">Registra as ações executadas durante a instalação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="6cf79-189">Considerações sobre o TDE do banco de dados MBAM</span><span class="sxs-lookup"><span data-stu-id="6cf79-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="6cf79-190">O recurso de criptografia de dados transparente (TDE) que está disponível no SQL Server é uma instalação opcional para as instâncias de banco de dados que hospedam os recursos de banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cf79-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="6cf79-191">Com o TDE, você pode executar a criptografia em nível de banco de dados completa em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6cf79-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="6cf79-192">O TDE é a melhor opção para a criptografia em massa para atender aos padrões de segurança de dados corporativos ou conformidade normativa.</span><span class="sxs-lookup"><span data-stu-id="6cf79-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="6cf79-193">O TDE funciona no nível de arquivo, que é semelhante a dois recursos do Windows: o sistema de arquivos com criptografia (EFS) e a criptografia de unidade de disco BitLocker, ambos também criptografam dados no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="6cf79-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="6cf79-194">O TDE não substitui a criptografia, o EFS ou o BitLocker no nível da célula.</span><span class="sxs-lookup"><span data-stu-id="6cf79-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="6cf79-195">Quando o TDE está habilitado em um banco de dados, todos os backups são criptografados.</span><span class="sxs-lookup"><span data-stu-id="6cf79-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="6cf79-196">Portanto, deve-se tomar cuidado especial para garantir que o certificado que foi usado para proteger a chave de criptografia do banco de dados tenha backup e seja mantido com o backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6cf79-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="6cf79-197">Se esse certificado (ou certificados) for perdido, os dados serão ilegíveis.</span><span class="sxs-lookup"><span data-stu-id="6cf79-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="6cf79-198">Faça backup do certificado juntamente com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6cf79-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="6cf79-199">Cada backup de certificado deve ter dois arquivos.</span><span class="sxs-lookup"><span data-stu-id="6cf79-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="6cf79-200">Esses dois arquivos devem ser arquivados (idealmente separadamente do arquivo de backup de banco de dados para segurança).</span><span class="sxs-lookup"><span data-stu-id="6cf79-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="6cf79-201">Você também pode considerar o uso do recurso EKM (gerenciamento de chaves extensível) (consulte gerenciamento extensível de chaves) para armazenamento e manutenção de chaves usadas para TDE.</span><span class="sxs-lookup"><span data-stu-id="6cf79-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="6cf79-202">Para obter um exemplo de como habilitar o TDE para instâncias de banco de dados do MBAM, consulte [avaliando MBAM 2,0](evaluating-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="6cf79-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="6cf79-203">Para obter mais informações sobre o TDE no SQLServer 2008, consulte [criptografia do SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).</span><span class="sxs-lookup"><span data-stu-id="6cf79-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="6cf79-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cf79-204">Related topics</span></span>


[<span data-ttu-id="6cf79-205">Segurança e privacidade para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6cf79-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





