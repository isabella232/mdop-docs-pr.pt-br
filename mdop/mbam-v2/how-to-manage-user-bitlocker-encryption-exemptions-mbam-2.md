---
title: Como gerenciar isenções de criptografia BitLocker para usuários
description: Como gerenciar isenções de criptografia BitLocker para usuários
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799599"
---
# <span data-ttu-id="5ea38-103">Como gerenciar isenções de criptografia BitLocker para usuários</span><span class="sxs-lookup"><span data-stu-id="5ea38-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="5ea38-104">O Microsoft BitLocker Administration and Monitoring (MBAM) pode ser usado para gerenciar a proteção do BitLocker isentando os usuários se houver usuários que não precisam ou querem que suas unidades sejam criptografadas.</span><span class="sxs-lookup"><span data-stu-id="5ea38-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="5ea38-105">Para isolar os usuários da proteção BitLocker, uma organização precisará criar uma infraestrutura para dar suporte a usuários isentos, como conceder ao usuário um número de telefone, uma página da Web ou endereço para correspondência a ser usado para solicitar uma isenção.</span><span class="sxs-lookup"><span data-stu-id="5ea38-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="5ea38-106">Além disso, um usuário isento precisará ser adicionado a um grupo de segurança para um objeto de política de grupo criado especificamente para usuários isentos.</span><span class="sxs-lookup"><span data-stu-id="5ea38-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="5ea38-107">Quando os membros desse grupo de segurança fazem logon em um computador, a configuração de política de grupo do usuário mostra que o usuário está isento da proteção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ea38-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="5ea38-108">A configuração de política de grupo do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ea38-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="5ea38-109">**Observação**  Se o computador já estiver protegido pelo BitLocker, a política de isenção de usuário não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="5ea38-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="5ea38-110">A tabela a seguir mostra como a proteção do BitLocker é aplicada com base na maneira como as isenções são definidas.</span><span class="sxs-lookup"><span data-stu-id="5ea38-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ea38-111">Status do usuário</span><span class="sxs-lookup"><span data-stu-id="5ea38-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="5ea38-112">Computador não isento</span><span class="sxs-lookup"><span data-stu-id="5ea38-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="5ea38-113">Isento de computador</span><span class="sxs-lookup"><span data-stu-id="5ea38-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ea38-114">O usuário não está isento</span><span class="sxs-lookup"><span data-stu-id="5ea38-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ea38-115">A proteção do BitLocker é imposta no computador</span><span class="sxs-lookup"><span data-stu-id="5ea38-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ea38-116">A proteção BitLocker não é imposta no computador</span><span class="sxs-lookup"><span data-stu-id="5ea38-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ea38-117">Isento de usuário</span><span class="sxs-lookup"><span data-stu-id="5ea38-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ea38-118">A proteção BitLocker não é imposta no computador</span><span class="sxs-lookup"><span data-stu-id="5ea38-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ea38-119">A proteção BitLocker não é imposta no computador</span><span class="sxs-lookup"><span data-stu-id="5ea38-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="5ea38-120">Para isentar um usuário da criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="5ea38-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="5ea38-121">Crie um grupo de segurança ActiveDirectoryDomainServices que será usado para gerenciar isenções de usuário dos requisitos de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ea38-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="5ea38-122">Crie uma configuração de objeto de política de grupo usando o modelo de política de grupo Administração e monitoramento do Microsoft BitLocker e associe-o ao grupo do Active Directory que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="5ea38-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="5ea38-123">As configurações de política para usuários isentos podem ser encontradas em **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="5ea38-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="5ea38-124">Depois de criar um grupo de segurança para usuários isentos do BitLocker, adicione a este grupo os nomes dos usuários que estão solicitando uma isenção.</span><span class="sxs-lookup"><span data-stu-id="5ea38-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="5ea38-125">Quando os usuários fizerem logon em um computador controlado pelo BitLocker, o cliente MBAM verificará a configuração de política de isenção de usuário e suspenderá a proteção dependendo se o usuário fizer parte do grupo de segurança de isenção de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ea38-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="5ea38-126">**Importante**  Cenários de computador compartilhado exigem consideração especial ao usar isenções de usuário.</span><span class="sxs-lookup"><span data-stu-id="5ea38-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="5ea38-127">Se um usuário não isento fizer logon em um computador compartilhado com um usuário isento, o computador pode estar criptografado.</span><span class="sxs-lookup"><span data-stu-id="5ea38-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="5ea38-128">Para permitir que os usuários solicitem uma isenção da criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="5ea38-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="5ea38-129">Se você configurou políticas de isenção de usuário usando o modelo de política MBAM, um usuário pode solicitar uma isenção da proteção BitLocker por meio do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ea38-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="5ea38-130">Quando os usuários fazem logon em um computador que precisa ser criptografado, eles recebem uma notificação de que o computador está sendo criptografado.</span><span class="sxs-lookup"><span data-stu-id="5ea38-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="5ea38-131">Eles podem selecionar a **isenção de solicitação** e adiar a criptografia selecionando **mais tarde**ou selecionar **Iniciar** para aceitar a criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ea38-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="5ea38-132">**Observação**  A seleção de **isenção de solicitação** adia a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="5ea38-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="5ea38-133">Se os usuários selecionarem **solicitar isenção**, receberão uma notificação solicitando que entrem em contato com o grupo de administração do BitLocker da sua organização.</span><span class="sxs-lookup"><span data-stu-id="5ea38-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="5ea38-134">Dependendo de como a configuração de política de isenção de usuário é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:</span><span class="sxs-lookup"><span data-stu-id="5ea38-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="5ea38-135">Número de telefone</span><span class="sxs-lookup"><span data-stu-id="5ea38-135">Phone Number</span></span>

    -   <span data-ttu-id="5ea38-136">URL da página da Web</span><span class="sxs-lookup"><span data-stu-id="5ea38-136">Webpage URL</span></span>

    -   <span data-ttu-id="5ea38-137">Endereço para correspondência</span><span class="sxs-lookup"><span data-stu-id="5ea38-137">Mailing Address</span></span>

    <span data-ttu-id="5ea38-138">Depois que a solicitação de isenção for recebida, o administrador do MBAM poderá decidir se é adequado para adicionar o usuário ao grupo do Active Directory de isenção de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ea38-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="5ea38-139">**Observação**  Depois que um usuário envia uma solicitação de isenção, o agente MBAM relata o usuário como "isento temporariamente" e, em seguida, aguarda um número de dias configurável antes de verificar a conformidade do computador novamente.</span><span class="sxs-lookup"><span data-stu-id="5ea38-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="5ea38-140">Se o administrador do MBAM rejeita a solicitação de isenção, a opção de solicitação de isenção é desativada, o que impede que o usuário possa solicitar a isenção novamente.</span><span class="sxs-lookup"><span data-stu-id="5ea38-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="5ea38-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ea38-141">Related topics</span></span>


[<span data-ttu-id="5ea38-142">Administrando os Recursos do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5ea38-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





