---
title: Como gerenciar isenções de criptografia BitLocker para usuários
description: Como gerenciar isenções de criptografia BitLocker para usuários
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799943"
---
# <span data-ttu-id="fa906-103">Como gerenciar isenções de criptografia BitLocker para usuários</span><span class="sxs-lookup"><span data-stu-id="fa906-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="fa906-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) permitem que você destenha usuários dos requisitos de criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="fa906-105">Para isolar os usuários da proteção BitLocker, você precisa:</span><span class="sxs-lookup"><span data-stu-id="fa906-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa906-106">Tarefa</span><span class="sxs-lookup"><span data-stu-id="fa906-106">Task</span></span></th>
<th align="left"><span data-ttu-id="fa906-107">Detalhes</span><span class="sxs-lookup"><span data-stu-id="fa906-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa906-108">Criar uma infraestrutura para dar suporte a usuários isentos.</span><span class="sxs-lookup"><span data-stu-id="fa906-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa906-109">Exemplos dessa infraestrutura incluem aos usuários um número de telefone de contato, uma página da Web ou um endereço para correspondência que eles podem usar para solicitar uma isenção.</span><span class="sxs-lookup"><span data-stu-id="fa906-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa906-110">Adicione o usuário isento a um grupo de segurança para um objeto de política de grupo configurado especificamente para usuários isentos.</span><span class="sxs-lookup"><span data-stu-id="fa906-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa906-111">Quando os membros desse grupo de segurança entram em um computador, a configuração de política de grupo do usuário isenta o usuário da proteção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="fa906-112">A configuração de política de grupo do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fa906-113">Observação</span><span class="sxs-lookup"><span data-stu-id="fa906-113">Note</span></span></strong><br/><p><span data-ttu-id="fa906-114">O MBAM não enact a política de criptografia se o computador já estiver protegido pelo BitLocker e se o usuário estiver isento de o usuário.</span><span class="sxs-lookup"><span data-stu-id="fa906-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="fa906-115">No entanto, se outro usuário que não está isento da política de criptografia entrar no computador, ocorrerá a criptografia.</span><span class="sxs-lookup"><span data-stu-id="fa906-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="fa906-116">As etapas a seguir descrevem o que ocorre quando os usuários finais solicitam uma isenção do processo de isenção de criptografia de unidade BitLocker por meio do cliente MBAM ou de qualquer processo que sua organização usa.</span><span class="sxs-lookup"><span data-stu-id="fa906-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="fa906-117">Você deve definir configurações da política de grupo do MBAM para permitir que os usuários finais solicitem uma isenção da criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="fa906-118">Quando os usuários finais entram em um computador que precisa ser criptografado, eles recebem uma notificação de que o computador será criptografado.</span><span class="sxs-lookup"><span data-stu-id="fa906-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="fa906-119">Eles podem selecionar a **isenção de solicitação** e adiar a criptografia selecionando **adiar**ou podem selecionar **Iniciar criptografia** para aceitar a criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="fa906-120">Observação</span><span class="sxs-lookup"><span data-stu-id="fa906-120">Note</span></span>**  
    <span data-ttu-id="fa906-121">A seleção de **isenção de solicitação** adia a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa906-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="fa906-122">Se os usuários finais selecionarem **solicitação de isenção**, receberão uma notificação informando que eles devem contatar o grupo de administração do BitLocker da organização.</span><span class="sxs-lookup"><span data-stu-id="fa906-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="fa906-123">Dependendo de como a configuração de **política de isenção de usuário** é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:</span><span class="sxs-lookup"><span data-stu-id="fa906-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="fa906-124">Número de telefone</span><span class="sxs-lookup"><span data-stu-id="fa906-124">Phone number</span></span>

    -   <span data-ttu-id="fa906-125">URL da página da Web</span><span class="sxs-lookup"><span data-stu-id="fa906-125">Webpage URL</span></span>

    -   <span data-ttu-id="fa906-126">Endereço para correspondência</span><span class="sxs-lookup"><span data-stu-id="fa906-126">Mailing address</span></span>

3.  <span data-ttu-id="fa906-127">Depois que a solicitação de isenção é recebida, o administrador do MBAM decide se deseja adicionar o usuário ao grupo de serviços de domínio Active Directory (AD DS) de isenção BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="fa906-128">Depois que um usuário final envia uma solicitação de isenção, o cliente MBAM relata o usuário como "isento temporariamente".</span><span class="sxs-lookup"><span data-stu-id="fa906-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="fa906-129">Em seguida, o cliente aguarda um número especificado de dias, que os administradores de ti configuram, antes de verificar a conformidade do computador novamente.</span><span class="sxs-lookup"><span data-stu-id="fa906-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="fa906-130">Se o administrador do MBAM rejeita a solicitação de isenção, a opção de solicitação de isenção é desativada, o que impede que o usuário solicite a isenção novamente.</span><span class="sxs-lookup"><span data-stu-id="fa906-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="fa906-131">O monitoramento e a administração do Microsoft BitLocker (MBAM) permitem que você destenha usuários dos requisitos de criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="fa906-132">Para isolar os usuários da proteção BitLocker, você precisa:</span><span class="sxs-lookup"><span data-stu-id="fa906-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa906-133">Tarefa</span><span class="sxs-lookup"><span data-stu-id="fa906-133">Task</span></span></th>
<th align="left"><span data-ttu-id="fa906-134">Detalhes</span><span class="sxs-lookup"><span data-stu-id="fa906-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa906-135">Criar uma infraestrutura para dar suporte a usuários isentos.</span><span class="sxs-lookup"><span data-stu-id="fa906-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa906-136">Exemplos dessa infraestrutura incluem aos usuários um número de telefone de contato, uma página da Web ou um endereço para correspondência que eles podem usar para solicitar uma isenção.</span><span class="sxs-lookup"><span data-stu-id="fa906-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa906-137">Adicione o usuário isento a um grupo de segurança para um objeto de política de grupo configurado especificamente para usuários isentos.</span><span class="sxs-lookup"><span data-stu-id="fa906-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa906-138">Quando os membros desse grupo de segurança entram em um computador, a configuração de política de grupo do usuário isenta o usuário da proteção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="fa906-139">A configuração de política de grupo do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fa906-140">Observação</span><span class="sxs-lookup"><span data-stu-id="fa906-140">Note</span></span></strong><br/><p><span data-ttu-id="fa906-141">Se o computador já estiver protegido pelo BitLocker, a política de isenção de usuário não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="fa906-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="fa906-142">Além disso, se outro usuário entrar em um computador que não está isento da política de criptografia, ocorrerá a criptografia.</span><span class="sxs-lookup"><span data-stu-id="fa906-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="fa906-143">As etapas a seguir descrevem o que ocorre quando os usuários finais solicitam uma isenção do processo de isenção de criptografia de unidade BitLocker por meio do cliente MBAM ou de qualquer processo que sua organização usa.</span><span class="sxs-lookup"><span data-stu-id="fa906-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="fa906-144">Você deve definir configurações da política de grupo do MBAM para permitir que os usuários finais solicitem uma isenção da criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="fa906-145">Quando os usuários finais entram em um computador que precisa ser criptografado, eles recebem uma notificação de que o computador será criptografado.</span><span class="sxs-lookup"><span data-stu-id="fa906-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="fa906-146">Eles podem selecionar a **isenção de solicitação** e adiar a criptografia selecionando **adiar**ou podem selecionar **Iniciar criptografia** para aceitar a criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="fa906-147">Observação</span><span class="sxs-lookup"><span data-stu-id="fa906-147">Note</span></span>**  
    <span data-ttu-id="fa906-148">A seleção de **isenção de solicitação** adia a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa906-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="fa906-149">Se os usuários finais selecionarem **solicitação de isenção**, receberão uma notificação informando que eles devem contatar o grupo de administração do BitLocker da organização.</span><span class="sxs-lookup"><span data-stu-id="fa906-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="fa906-150">Dependendo de como a configuração de **política de isenção de usuário** é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:</span><span class="sxs-lookup"><span data-stu-id="fa906-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="fa906-151">Número de telefone</span><span class="sxs-lookup"><span data-stu-id="fa906-151">Phone number</span></span>

    -   <span data-ttu-id="fa906-152">URL da página da Web</span><span class="sxs-lookup"><span data-stu-id="fa906-152">Webpage URL</span></span>

    -   <span data-ttu-id="fa906-153">Endereço para correspondência</span><span class="sxs-lookup"><span data-stu-id="fa906-153">Mailing address</span></span>

3.  <span data-ttu-id="fa906-154">Depois que a solicitação de isenção é recebida, o administrador do MBAM decide se deseja adicionar o usuário ao grupo de serviços de domínio Active Directory (AD DS) de isenção BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="fa906-155">Depois que um usuário final envia uma solicitação de isenção, o cliente MBAM relata o usuário como "isento temporariamente".</span><span class="sxs-lookup"><span data-stu-id="fa906-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="fa906-156">Em seguida, o cliente aguarda um número especificado de dias, que os administradores de ti configuram, antes de verificar a conformidade do computador novamente.</span><span class="sxs-lookup"><span data-stu-id="fa906-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="fa906-157">Se o administrador do MBAM rejeita a solicitação de isenção, a opção de solicitação de isenção é desativada, o que impede que o usuário solicite a isenção novamente.</span><span class="sxs-lookup"><span data-stu-id="fa906-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="fa906-158">Para isentar um usuário da criptografia de unidade de disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="fa906-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="fa906-159">Crie um grupo de segurança do AD DS que será usado para gerenciar isenções de usuário dos requisitos de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="fa906-160">Crie um objeto de política de grupo usando os modelos de política de grupo Administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="fa906-161">Associe o objeto de política de grupo ao grupo do AD DS que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="fa906-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="fa906-162">As configurações de política para os usuários isentos estão localizadas em: modelos administrativos do **userconfiguration** &gt; **Administrative Templates** &gt; **componentes** &gt; **do Windows MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="fa906-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="fa906-163">Para o grupo de segurança que você criou para usuários isentos de BitLocker, adicione os nomes dos usuários que estão solicitando uma isenção.</span><span class="sxs-lookup"><span data-stu-id="fa906-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="fa906-164">Quando um usuário entra em um computador controlado pelo BitLocker, o cliente MBAM verifica a configuração da política de isenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa906-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="fa906-165">Se o computador já estiver criptografado, a proteção BitLocker não será suspensa.</span><span class="sxs-lookup"><span data-stu-id="fa906-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="fa906-166">Se o computador não estiver criptografado, o MBAM não solicitará que o usuário criptografe.</span><span class="sxs-lookup"><span data-stu-id="fa906-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="fa906-167">Importante</span><span class="sxs-lookup"><span data-stu-id="fa906-167">Important</span></span>**  
    <span data-ttu-id="fa906-168">Cenários de computador compartilhado exigem consideração especial quando você estiver usando isenções de usuário BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa906-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="fa906-169">Se um usuário não isento entrar em um computador compartilhado com um usuário isento, o computador pode estar criptografado.</span><span class="sxs-lookup"><span data-stu-id="fa906-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="fa906-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa906-170">Related topics</span></span>


[<span data-ttu-id="fa906-171">Administrando os recursos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fa906-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="fa906-172">Planejamento para os requisitos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fa906-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="fa906-173">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="fa906-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fa906-174">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="fa906-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fa906-175">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fa906-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




