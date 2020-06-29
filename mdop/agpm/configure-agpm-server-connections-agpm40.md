---
title: Configurar conexões de servidor do AGPM
description: Configurar conexões de servidor do AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797452"
---
# <span data-ttu-id="781fa-103">Configurar conexões de servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="781fa-103">Configure AGPM Server Connections</span></span>


<span data-ttu-id="781fa-104">Todas as versões de cada objeto de política de grupo controlado (GPO) são armazenadas em um arquivo morto central para que os administradores de política de grupo possam exibir e modificar os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="781fa-104">All versions of each controlled Group Policy Object (GPO) are stored in a central archive so that Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="781fa-105">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo (AGPM) é necessária para concluir esses procedimentos para configurar centralmente locais de arquivamento para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="781fa-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="781fa-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="781fa-107">Configurando conexões do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="781fa-107">Configuring AGPM Server connections</span></span>


<span data-ttu-id="781fa-108">Como administrador do AGPM, você pode garantir que todos os administradores de política de grupo se conectem ao mesmo servidor de AGPM, definindo centralmente a configuração associada.</span><span class="sxs-lookup"><span data-stu-id="781fa-108">As an AGPM Administrator, you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the associated setting.</span></span> <span data-ttu-id="781fa-109">Se o ambiente exigir servidores de AGPM separados para alguns ou todos os domínios, configure esses servidores do AGPM adicionais como exceções para o padrão.</span><span class="sxs-lookup"><span data-stu-id="781fa-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="781fa-110">Se você não configurar as conexões do servidor do AGPM de forma centralizada, cada administrador da política de grupo deve configurar manualmente o servidor do AGPM para ser exibido para cada domínio.</span><span class="sxs-lookup"><span data-stu-id="781fa-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="781fa-111">Configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="781fa-111">Configure an AGPM Server connection for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="781fa-112">Configurar conexões do servidor do AGPM adicionais para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="781fa-112">Configure additional AGPM Server connections for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="781fa-113">Configurar manualmente uma conexão com o servidor do AGPM para a sua conta</span><span class="sxs-lookup"><span data-stu-id="781fa-113">Manually configure an AGPM Server connection for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="781fa-114">Para configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="781fa-114">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="781fa-115">Na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="781fa-116">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="781fa-116">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="781fa-117">Na janela **Editor de gerenciamento de política de grupo** , clique em **configuração do usuário**, **políticas**, **modelos administrativos**, **componentes do Windows**e **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="781fa-117">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="781fa-118">No painel detalhes, clique duas vezes em **AGPM: especifique o servidor do AGPM padrão (todos os domínios)**.</span><span class="sxs-lookup"><span data-stu-id="781fa-118">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

4.  <span data-ttu-id="781fa-119">Na janela **Propriedades** , marque a caixa de seleção **habilitado** e digite o nome do computador e a porta totalmente qualificados (por exemplo, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="781fa-119">In the **Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

5.  <span data-ttu-id="781fa-120">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="781fa-120">Click **OK**.</span></span> <span data-ttu-id="781fa-121">A menos que você queira configurar outras conexões do servidor do AGPM, feche a janela do **Editor de gerenciamento de política de grupo** e implante o GPO.</span><span class="sxs-lookup"><span data-stu-id="781fa-121">Unless you want to configure additional AGPM Server connections, close the **Group Policy Management Editor** window and deploy the GPO.</span></span> <span data-ttu-id="781fa-122">(Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).) Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-122">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="781fa-123">Para configurar conexões do servidor do AGPM adicionais para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="781fa-123">To configure additional AGPM Server connections for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="781fa-124">Se nenhuma conexão do servidor do AGPM tiver sido configurada, siga o procedimento anterior para configurar um servidor do AGPM padrão para todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="781fa-124">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="781fa-125">Para configurar servidores de AGPM separados para alguns ou todos os domínios (substituindo o servidor do AGPM padrão), na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-125">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="781fa-126">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="781fa-126">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

3.  <span data-ttu-id="781fa-127">Na janela **Editor de gerenciamento de política de grupo** , clique em **configuração do usuário**, **políticas**, **modelos administrativos**, **componentes do Windows**e, em seguida, **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="781fa-127">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="781fa-128">No painel de detalhes, clique duas vezes em **AGPM: especificar servidores de AGPM**.</span><span class="sxs-lookup"><span data-stu-id="781fa-128">In the details pane, double-click **AGPM: Specify AGPM Servers**.</span></span>

5.  <span data-ttu-id="781fa-129">Na janela **Propriedades** , marque a caixa de seleção **habilitado** e clique em **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="781fa-129">In the **Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="781fa-130">Na janela **Mostrar conteúdo** :</span><span class="sxs-lookup"><span data-stu-id="781fa-130">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="781fa-131">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="781fa-131">Click **Add**.</span></span>

    2.  <span data-ttu-id="781fa-132">Para **nome do valor**, digite o nome do domínio (por exemplo, server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="781fa-132">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="781fa-133">Para **valor**, digite o nome e a porta do servidor de AGPM a ser usado para esse domínio (por exemplo, server2.contoso.com:4600) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="781fa-133">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="781fa-134">(Por padrão, o serviço do AGPM escuta na porta 4600.</span><span class="sxs-lookup"><span data-stu-id="781fa-134">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="781fa-135">Para usar uma porta diferente, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="781fa-135">To use a different port, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).)</span></span>

    4.  <span data-ttu-id="781fa-136">Repita para cada domínio que não use o servidor do AGPM padrão.</span><span class="sxs-lookup"><span data-stu-id="781fa-136">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="781fa-137">Clique em **OK** para fechar as janelas **Mostrar conteúdo** e **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="781fa-137">Click **OK** to close the **Show Contents** and **Properties** windows.</span></span>

8.  <span data-ttu-id="781fa-138">Feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="781fa-138">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="781fa-139">(Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).) Quando a política de grupo é atualizada, as novas conexões do servidor do AGPM são configuradas para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-139">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="781fa-140">Se você configurou a conexão do servidor do AGPM de forma centralizada, a opção de configurá-lo manualmente não está disponível para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-140">If you have centrally configured the AGPM Server connection, the option to manually configure it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="781fa-141">Para configurar manualmente o servidor de AGPM a ser exibido para a sua conta</span><span class="sxs-lookup"><span data-stu-id="781fa-141">To manually configure which AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="781fa-142">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="781fa-142">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="781fa-143">No painel detalhes, clique na guia **servidor do AGPM** .</span><span class="sxs-lookup"><span data-stu-id="781fa-143">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="781fa-144">Digite o nome do computador totalmente qualificado para o servidor do AGPM que gerencia o arquivo morto usado para esse domínio (por exemplo, server.contoso.com) e a porta na qual o serviço do AGPM escuta (por padrão, a porta 4600).</span><span class="sxs-lookup"><span data-stu-id="781fa-144">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="781fa-145">Clique em **aplicar**e, em seguida, clique em **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="781fa-145">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="781fa-146">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="781fa-146">Additional considerations</span></span>

-   <span data-ttu-id="781fa-147">Você deve ser capaz de editar e implantar um GPO para executar os procedimentos de configuração centralizada das conexões do servidor do AGPM para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="781fa-147">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="781fa-148">Consulte [editando um GPO](editing-a-gpo-agpm40.md) e [implante um GPO](deploy-a-gpo-agpm40.md) para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="781fa-148">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

-   <span data-ttu-id="781fa-149">O servidor do AGPM selecionado determina quais GPOs são exibidos na guia **conteúdo** e para qual local as configurações da guia de **delegação de domínio** são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="781fa-149">The selected AGPM Server determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="781fa-150">Se não for gerenciado centralmente por meio do modelo administrativo, cada administrador da política de grupo deve definir essa configuração para apontar para o servidor do AGPM do domínio.</span><span class="sxs-lookup"><span data-stu-id="781fa-150">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="781fa-151">A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="781fa-151">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="781fa-152">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="781fa-152">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="781fa-153">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="781fa-153">Additional references</span></span>

-   [<span data-ttu-id="781fa-154">Configuração do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="781fa-154">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





