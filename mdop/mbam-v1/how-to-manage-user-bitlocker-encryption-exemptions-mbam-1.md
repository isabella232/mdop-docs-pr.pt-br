---
title: Como gerenciar isenções de criptografia BitLocker para usuários
description: Como gerenciar isenções de criptografia BitLocker para usuários
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796131"
---
# <span data-ttu-id="e5bbf-103">Como gerenciar isenções de criptografia BitLocker para usuários</span><span class="sxs-lookup"><span data-stu-id="e5bbf-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="e5bbf-104">O Microsoft BitLocker Administration and Monitoring (MBAM) pode ser usado para gerenciar a proteção do BitLocker, isentando os usuários que não precisam ou querem que suas unidades sejam criptografadas.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="e5bbf-105">Para isolar os usuários da proteção BitLocker, uma organização deve primeiro criar uma infraestrutura para dar suporte a tais isenções.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="e5bbf-106">A infraestrutura de suporte pode incluir um número de telefone de contato, uma página da Web ou um endereço para correspondência para solicitar a isenção.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="e5bbf-107">Além disso, qualquer usuário isento precisará ser adicionado a um grupo de segurança para a política de grupo criada especificamente para usuários isentos.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="e5bbf-108">Quando os membros desse grupo de segurança fizerem logon em um computador, a política de grupo de usuários mostrará que o usuário está isento da proteção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="e5bbf-109">A política do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="e5bbf-110">**Observação**  Se o computador já estiver protegido pelo BitLocker, a política de isenção de usuário não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="e5bbf-111">A tabela a seguir mostra como a proteção do BitLocker é aplicada com base na maneira como as isenções são definidas.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5bbf-112">Status do usuário</span><span class="sxs-lookup"><span data-stu-id="e5bbf-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="e5bbf-113">Computador não isento</span><span class="sxs-lookup"><span data-stu-id="e5bbf-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="e5bbf-114">Isento de computador</span><span class="sxs-lookup"><span data-stu-id="e5bbf-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e5bbf-115">O usuário não está isento</span><span class="sxs-lookup"><span data-stu-id="e5bbf-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e5bbf-116">A proteção do BitLocker é imposta no computador.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5bbf-117">A proteção do BitLocker não é imposta no computador.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e5bbf-118">Isento de usuário</span><span class="sxs-lookup"><span data-stu-id="e5bbf-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e5bbf-119">A proteção do BitLocker não é imposta no computador.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5bbf-120">A proteção do BitLocker não é imposta no computador.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="e5bbf-121">Para isentar um usuário da criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="e5bbf-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="e5bbf-122">Crie um grupo de segurança ActiveDirectoryDomainServices que será usado para gerenciar isenções de usuário da criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="e5bbf-123">Crie uma configuração de objeto de política de grupo usando o modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="e5bbf-124">Associe o objeto de política de grupo ao grupo do Active Directory que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="e5bbf-125">Para obter mais informações sobre as configurações de política necessárias para permitir que os usuários solicitem a isenção da criptografia BitLocker, consulte a seção configurar política de isenção de usuário em [planejamento para requisitos de política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5bbf-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="e5bbf-126">Depois de criar um grupo de segurança para usuários isentos do BitLocker, adicione a este grupo os nomes dos usuários que estão solicitando isenção.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="e5bbf-127">Quando um usuário faz logon em um computador controlado pelo BitLocker, o cliente MBAM verifica a configuração da política de isenção do usuário e suspende a proteção de acordo com a forma como o usuário faz parte do grupo de segurança de isenção de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="e5bbf-128">**Observação**  Cenários de computador compartilhado exigem uma consideração especial sobre isenção de usuário.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="e5bbf-129">Se um usuário não isento fizer logon em um computador compartilhado com um usuário isento, o computador pode estar criptografado.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="e5bbf-130">Para permitir que os usuários solicitem a isenção da criptografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="e5bbf-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="e5bbf-131">Depois de configurar políticas de isenção de usuários pela usingwith modelo de política MBAM, um usuário pode solicitar isenção de proteção BitLocker por meio do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="e5bbf-132">Quando um usuário faz logon em um computador marcado como **compatível** na lista de compatibilidade de hardware do MBAM, o sistema apresenta ao usuário uma notificação de que o computador está sendo criptografado.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="e5bbf-133">O usuário pode selecionar **solicitação de isenção** e adiar a criptografia selecionando **mais tarde**ou selecionar **Iniciar** para aceitar a criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="e5bbf-134">**Observação**  Selecionar a **isenção de solicitação** adiará a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="e5bbf-135">Quando um usuário seleciona a **isenção de solicitação**, o usuário é notificado a contatar o grupo de administração do BitLocker da organização.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="e5bbf-136">Dependendo de como a configuração de política de isenção de usuário é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:</span><span class="sxs-lookup"><span data-stu-id="e5bbf-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="e5bbf-137">Número de telefone</span><span class="sxs-lookup"><span data-stu-id="e5bbf-137">Phone Number</span></span>

    -   <span data-ttu-id="e5bbf-138">URL da página da Web</span><span class="sxs-lookup"><span data-stu-id="e5bbf-138">Webpage URL</span></span>

    -   <span data-ttu-id="e5bbf-139">Endereço para correspondência</span><span class="sxs-lookup"><span data-stu-id="e5bbf-139">Mailing Address</span></span>

    <span data-ttu-id="e5bbf-140">Depois de enviar a solicitação, o administrador do MBAM pode decidir se é apropriado adicionar o usuário ao grupo do Active Directory de isenção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="e5bbf-141">**Observação**  Quando o limite de tempo adiado da política de isenção do usuário tiver expirado, os usuários não verão a opção de solicitar isenção à política de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="e5bbf-142">Nesse momento, os usuários devem entrar em contato com o administrador do MBAM diretamente para receber a isenção da proteção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5bbf-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="e5bbf-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5bbf-143">Related topics</span></span>


[<span data-ttu-id="e5bbf-144">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e5bbf-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





