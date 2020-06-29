---
title: Considerações de segurança para o MBAM 1.0
description: Considerações de segurança para o MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799823"
---
# <span data-ttu-id="86661-103">Considerações de segurança para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86661-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="86661-104">Este tópico contém uma breve visão geral das contas e dos grupos, dos arquivos de log e outras considerações relacionadas à segurança do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="86661-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="86661-105">Para obter mais informações, siga os links deste artigo.</span><span class="sxs-lookup"><span data-stu-id="86661-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="86661-106">Considerações gerais sobre segurança</span><span class="sxs-lookup"><span data-stu-id="86661-106">General security considerations</span></span>


**<span data-ttu-id="86661-107">Compreender os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="86661-107">Understand the security risks.</span></span>** <span data-ttu-id="86661-108">O risco mais sério para o MBAM é que sua funcionalidade pode ser seqüestrada por um usuário não autorizado que poderia reconfigurar a criptografia do BitLocker e obter dados da chave de criptografia BitLocker em clientes do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="86661-109">No entanto, a perda de funcionalidade do MBAM por um curto período de tempo devido a um ataque de negação de serviço geralmente não teria um impacto catastrófico.</span><span class="sxs-lookup"><span data-stu-id="86661-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="86661-110">**Proteja seus computadores fisicamente**.</span><span class="sxs-lookup"><span data-stu-id="86661-110">**Physically secure your computers**.</span></span> <span data-ttu-id="86661-111">A segurança está incompleta sem segurança física.</span><span class="sxs-lookup"><span data-stu-id="86661-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="86661-112">Qualquer pessoa com acesso físico a um servidor MBAM pode atacar potencialmente toda a base de clientes.</span><span class="sxs-lookup"><span data-stu-id="86661-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="86661-113">Qualquer ataque físico potencial deve ser considerado de alto risco e diminuído apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="86661-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="86661-114">Os servidores MBAM devem ser armazenados em uma sala de servidor fisicamente seguro com acesso controlado.</span><span class="sxs-lookup"><span data-stu-id="86661-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="86661-115">Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.</span><span class="sxs-lookup"><span data-stu-id="86661-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="86661-116">**Aplicar as atualizações de segurança mais recentes a todos os computadores**.</span><span class="sxs-lookup"><span data-stu-id="86661-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="86661-117">Mantenha-se informado sobre novas atualizações para sistemas operacionais, Microsoft SQL Server e MBAM ao assinar o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="86661-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="86661-118">**Use senhas fortes ou frases secretas**.</span><span class="sxs-lookup"><span data-stu-id="86661-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="86661-119">Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do MBAM e do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="86661-120">Nunca use senhas em branco.</span><span class="sxs-lookup"><span data-stu-id="86661-120">Never use blank passwords.</span></span> <span data-ttu-id="86661-121">Para obter mais informações sobre os conceitos de senha, consulte o White Paper "senhas de conta e políticas" no TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="86661-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="86661-122">Contas e grupos no MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="86661-123">Uma prática recomendada para o gerenciamento de contas de usuários é criar grupos globais de domínio e adicionar contas de usuário a eles.</span><span class="sxs-lookup"><span data-stu-id="86661-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="86661-124">Em seguida, adicione as contas globais do domínio aos grupos locais MBAM necessários nos servidores MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="86661-125">Grupos do ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="86661-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="86661-126">Nenhum grupo é criado automaticamente durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="86661-127">No entanto, você deve criar os seguintes grupos globais do ActiveDirectoryDomainServices para gerenciar as operações do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86661-128">Nome do Grupo</span><span class="sxs-lookup"><span data-stu-id="86661-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="86661-129">Detalhes</span><span class="sxs-lookup"><span data-stu-id="86661-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-130">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-131">Crie esse grupo para gerenciar os membros do grupo local de usuários da assistência técnica avançada do MBAM que foram criados durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-132">Acesso ao banco de dados de auditoria de conformidade MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-133">Crie esse grupo para gerenciar os membros do grupo local de acesso ao banco de dados de auditoria de conformidade do MBAM criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-134">Usuários de hardware MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-135">Crie esse grupo para gerenciar os membros do grupo local usuários de hardware do MBAM que foi criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-136">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-137">Crie esse grupo para gerenciar os membros do grupo local usuários da assistência técnica do MBAM que foi criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-138">Recuperação do MBAM e acesso ao banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="86661-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-139">Crie esse grupo para gerenciar os membros do grupo local de recuperação de banco de dados de MBAM de dados de recuperação e de hardware criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-140">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-141">Crie esse grupo para gerenciar os membros do grupo local usuários do relatório do MBAM que foi criado durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-142">Administradores do sistema do MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-143">Crie esse grupo para gerenciar os membros do grupo local de administradores do sistema MBAM criados durante a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-144">Isenções de criptografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="86661-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-145">Crie esse grupo para gerenciar contas de usuário que devem ser isentadas da criptografia do BitLocker a partir de computadores nos quais eles fazem logon.</span><span class="sxs-lookup"><span data-stu-id="86661-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="86661-146">Grupos locais do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="86661-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="86661-147">A instalação do MBAM cria grupos locais para dar suporte às operações do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="86661-148">Você deve adicionar os grupos globais do ActiveDirectoryDomainServices aos grupos locais MBAM apropriados para configurar as permissões de segurança MBAM e acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="86661-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86661-149">Nome do Grupo</span><span class="sxs-lookup"><span data-stu-id="86661-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="86661-150">Detalhes</span><span class="sxs-lookup"><span data-stu-id="86661-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-151">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-152">Os membros deste grupo têm acesso expandido aos recursos de assistência técnica do Microsoft BitLocker Administration and Monitoring.</span><span class="sxs-lookup"><span data-stu-id="86661-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-153">Acesso ao banco de dados de auditoria de conformidade MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-154">Esse grupo contém as máquinas que têm acesso ao banco de dados de auditoria de conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-155">Usuários de hardware MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-156">Os membros desse grupo têm acesso a alguns dos recursos de recursos de hardware da administração e do monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="86661-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-157">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-158">Os membros desse grupo têm acesso a alguns dos recursos de helpdesk da administração e do monitoramento do BitLocker da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="86661-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-159">Recuperação do MBAM e acesso ao banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="86661-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-160">Esse grupo contém os computadores que têm acesso ao banco de dados de recuperação e hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86661-161">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-162">Os membros desse grupo têm acesso aos relatórios de conformidade e auditoria do Microsoft BitLocker Administration and Monitoring.</span><span class="sxs-lookup"><span data-stu-id="86661-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86661-163">Administradores do sistema do MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="86661-164">Os membros desse grupo têm acesso a todos os recursos da administração e do monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="86661-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="86661-165">Conta de acesso a relatórios do SSRS</span><span class="sxs-lookup"><span data-stu-id="86661-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="86661-166">A conta de serviço relatórios do SQL Server Reporting Services (SSRS) fornece o contexto de segurança para executar os relatórios do MBAM disponíveis por meio do SSRS.</span><span class="sxs-lookup"><span data-stu-id="86661-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="86661-167">Esta conta é configurada durante a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="86661-168">Arquivos de log do MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-168">MBAM Log Files</span></span>


<span data-ttu-id="86661-169">Durante a configuração do MBAM, os seguintes arquivos de log de instalação do MBAM são criados na pasta% Temp% do usuário que instala o</span><span class="sxs-lookup"><span data-stu-id="86661-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="86661-170">Arquivos de log de instalação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="86661-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="86661-171">MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="86661-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="86661-172">Registra as ações executadas durante a instalação do MBAM e a instalação do recurso MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="86661-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="86661-173">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="86661-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="86661-174">Registra as ações executadas para criar a configuração do banco de dados de status de conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="86661-175">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="86661-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="86661-176">Registra as ações executadas para criar a recuperação do MBAM e o banco de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="86661-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="86661-177">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="86661-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="86661-178">Registra as ações executadas para criar os logons do SQL Server no banco de dados de status de conformidade do MBAM e autorizar o serviço Web de helpdesk ao banco de dados para relatórios.</span><span class="sxs-lookup"><span data-stu-id="86661-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="86661-179">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="86661-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="86661-180">Registra as ações executadas para autorizar serviços Web para o banco de dados para recuperação de chave e criar logons para o banco de dados de recuperação e hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="86661-181">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="86661-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="86661-182">Registra as ações executadas para autorizar os serviços Web a MBAM banco de dados de status de conformidade para relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="86661-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="86661-183">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="86661-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="86661-184">Registra as ações executadas para autorizar serviços Web a recuperar e MBAM o banco de dados de hardware para a recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="86661-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="86661-185">**Observação**  Para obter arquivos de log de instalação do MBAM adicionais, você deve instalar a administração e o monitoramento do Microsoft BitLocker usando o pacote **msiexec** e a opção de localização **/l** &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="86661-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="86661-186">Os arquivos de log são criados no local especificado.</span><span class="sxs-lookup"><span data-stu-id="86661-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="86661-187">Arquivos de log de configuração do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="86661-188">MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="86661-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="86661-189">Registra as ações executadas durante a instalação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="86661-190">Considerações sobre o TDE do banco de dados MBAM</span><span class="sxs-lookup"><span data-stu-id="86661-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="86661-191">O recurso de criptografia de dados transparente (TDE) disponível no SQL Server 2008 é um pré-requisito de instalação obrigatório para as instâncias de banco de dados que hospedarão os recursos de banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="86661-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="86661-192">Com o TDE, você pode executar a criptografia em nível de banco de dados completa em tempo real.</span><span class="sxs-lookup"><span data-stu-id="86661-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="86661-193">TDE é uma opção bem adequada para a criptografia em massa para atender aos padrões de segurança de dados corporativos ou conformidade normativa.</span><span class="sxs-lookup"><span data-stu-id="86661-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="86661-194">O TDE funciona no nível de arquivo, que é semelhante a dois recursos do Windows: o sistema de arquivos com criptografia (EFS) e a criptografia de unidade de disco BitLocker, ambos também criptografam dados no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="86661-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="86661-195">O TDE não substitui a criptografia, o EFS ou o BitLocker no nível da célula.</span><span class="sxs-lookup"><span data-stu-id="86661-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="86661-196">Quando o TDE está habilitado em um banco de dados, todos os backups são criptografados.</span><span class="sxs-lookup"><span data-stu-id="86661-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="86661-197">Portanto, deve-se tomar cuidado especial para garantir que o certificado que foi usado para proteger a chave de criptografia do banco de dados (DEK) seja backup e mantido com o backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="86661-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="86661-198">Sem um certificado, os dados serão ilegíveis.</span><span class="sxs-lookup"><span data-stu-id="86661-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="86661-199">Faça backup do certificado juntamente com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="86661-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="86661-200">Cada backup de certificado deve ter dois arquivos; esses dois arquivos devem ser arquivados. É melhor arquivá-los separadamente do arquivo de backup do banco de dados para segurança.</span><span class="sxs-lookup"><span data-stu-id="86661-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="86661-201">Para obter um exemplo de como habilitar o TDE para instâncias de banco de dados do MBAM, consulte [avaliando MBAM 1,0](evaluating-mbam-10.md).</span><span class="sxs-lookup"><span data-stu-id="86661-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="86661-202">Para obter mais informações sobre o TDE no SQLServer 2008, consulte [criptografia de banco de dados no SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span><span class="sxs-lookup"><span data-stu-id="86661-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="86661-203">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86661-203">Related topics</span></span>


[<span data-ttu-id="86661-204">Segurança e Privacidade para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86661-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 





