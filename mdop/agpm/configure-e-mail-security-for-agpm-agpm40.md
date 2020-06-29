---
title: Configurar segurança de email para o AGPM
description: Configurar segurança de email para o AGPM
author: dansimp
ms.assetid: b9c48894-0a10-4d03-8027-50ed3b02485a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a384c2a21f912ca7ec55a5e4c74ca7062bfe864c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797436"
---
# <span data-ttu-id="b3ee4-103">Configurar segurança de email para o AGPM</span><span class="sxs-lookup"><span data-stu-id="b3ee4-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="b3ee4-104">Por padrão, as notificações por email enviadas devido a ações no AGPM (gerenciamento avançado de política de grupo) não são criptografadas e são enviadas por meio da porta 25 SMTP.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="b3ee4-105">No entanto, você pode configurar a segurança de email para o AGPM usando configurações do registro para especificar se deseja usar a criptografia SSL (Secure Sockets Layer) e qual porta SMTP usar.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="b3ee4-106">Ao criptografar notificações por email do AGPM, você pode proteger melhor as pessoas que podem revelar informações confidenciais sobre a segurança da sua organização.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="b3ee4-107">As notificações de criptografia de email são recomendadas quando elas são retransmitidas por servidores de email remotos e podem ser necessárias para alguns regulamentos sobre conformidade.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="b3ee4-108">**Cuidado**  A edição incorreta do registro pode danificar seriamente seu sistema.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="b3ee4-109">Antes de fazer alterações no registro, você deve fazer backup de todos os dados importantes do computador.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="b3ee4-110">Uma conta de usuário que tem a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o objeto de política de grupo (GPO) usado nesses procedimentos ou uma conta de usuário que tenha as permissões necessárias no AGPM é necessária para concluir estes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="b3ee4-111">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b3ee4-112">Para configurar a segurança de email para o AGPM usando as preferências de política de grupo</span><span class="sxs-lookup"><span data-stu-id="b3ee4-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="b3ee4-113">Na árvore do **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os servidores do AGPM para os quais você deseja configurar a segurança de email.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="b3ee4-114">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="b3ee4-115">Na janela **Editor de gerenciamento de política de grupo** , expanda a **configuração do computador**, **preferências**, **configurações do Windows**e pastas **do registro** .</span><span class="sxs-lookup"><span data-stu-id="b3ee4-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="b3ee4-116">Na árvore do console, clique com o botão direito do mouse em **registro**, aponte para **novo**, clique em **item da coleção**e digite segurança de email do **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="b3ee4-117">Crie um item de preferência Registry para ativar a criptografia:</span><span class="sxs-lookup"><span data-stu-id="b3ee4-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="b3ee4-118">Na árvore de console, clique com o botão direito do mouse em **segurança de email do AGPM**, aponte para **novo**e clique em **item do registro**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="b3ee4-119">Na caixa de diálogo **novas propriedades do registro** , selecione a ação **Atualizar** .</span><span class="sxs-lookup"><span data-stu-id="b3ee4-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="b3ee4-120">Para **Hive**, selecione **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="b3ee4-121">Para o **caminho da chave**, digite **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="b3ee4-122">Para **nome do valor**, digite **EncryptSmtp**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="b3ee4-123">Para **tipo de valor**, selecione **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="b3ee4-124">Para **base**, selecione **decimal**e para **dados de valor**, digite **1** para usar a criptografia SSL ou **0** para permitir que o email seja enviado sem criptografia.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="b3ee4-125">Por padrão, o email é enviado sem criptografia.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-125">By default, e-mail is sent without encryption.</span></span> <span data-ttu-id="b3ee4-126">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-126">Click **OK**.</span></span>

5.  <span data-ttu-id="b3ee4-127">Crie um item de preferência Registry para especificar a porta SMTP:</span><span class="sxs-lookup"><span data-stu-id="b3ee4-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="b3ee4-128">Na árvore de console, clique com o botão direito do mouse em **segurança de email do AGPM**, aponte para **novo**e clique em **item do registro**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="b3ee4-129">Na caixa de diálogo **novas propriedades do registro** , selecione a ação **Atualizar** .</span><span class="sxs-lookup"><span data-stu-id="b3ee4-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="b3ee4-130">Para **Hive**, selecione **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="b3ee4-131">Para a caixa de diálogo **caminho da chave** , digite **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="b3ee4-132">Para **nome do valor**, digite **SMTPPORT**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="b3ee4-133">Para **tipo de valor**, selecione **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="b3ee4-134">Para **base**, selecione **decimal**e para **dados de valor**, digite um número de porta para a porta SMTP.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="b3ee4-135">Por padrão, a porta SMTP é a porta 25 se a criptografia não estiver habilitada ou porta 587 se a criptografia SSL estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span> <span data-ttu-id="b3ee4-136">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-136">Click **OK**.</span></span>

6.  <span data-ttu-id="b3ee4-137">Feche a janela do **Editor de gerenciamento de política de grupo** e, em seguida, faça check-in e implante o GPO.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="b3ee4-138">Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="b3ee4-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="b3ee4-139">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="b3ee4-139">Additional considerations</span></span>

-   <span data-ttu-id="b3ee4-140">Você deve ser capaz de editar e implantar um GPO para definir as configurações do registro usando as preferências de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="b3ee4-141">Consulte [editando um GPO](editing-a-gpo-agpm40.md) e [implante um GPO](deploy-a-gpo-agpm40.md) para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-141">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="b3ee4-142">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="b3ee4-142">Additional references</span></span>

-   [<span data-ttu-id="b3ee4-143">Configuração do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="b3ee4-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





