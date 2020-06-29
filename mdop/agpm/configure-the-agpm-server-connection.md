---
title: Configurar a conexão de servidor do AGPM
description: Configurar a conexão de servidor do AGPM
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797420"
---
# <span data-ttu-id="6f173-103">Configurar a conexão de servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="6f173-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="6f173-104">O gerenciamento avançado de política de grupo (AGPM) armazena todas as versões de cada objeto de política de grupo (GPO) controlado em um arquivo central, portanto, os administradores de política de grupo podem exibir e modificar os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="6f173-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="6f173-105">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir esses procedimentos para configurar centralmente locais de arquivamento para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="6f173-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6f173-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="6f173-107">Configurando a conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="6f173-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="6f173-108">Como administrador do AGPM (controle total), você pode garantir que todos os administradores de política de grupo se conectem ao mesmo servidor do AGPM, definindo centralmente a configuração.</span><span class="sxs-lookup"><span data-stu-id="6f173-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="6f173-109">Se o ambiente exigir servidores de AGPM separados para alguns ou todos os domínios, configure esses servidores do AGPM adicionais como exceções para o padrão.</span><span class="sxs-lookup"><span data-stu-id="6f173-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="6f173-110">Se você não configurar as conexões do servidor do AGPM de forma centralizada, cada administrador da política de grupo deve configurar manualmente o servidor do AGPM para ser exibido para cada domínio.</span><span class="sxs-lookup"><span data-stu-id="6f173-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="6f173-111">Configurar um servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="6f173-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="6f173-112">Configurar servidores de AGPM adicionais para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="6f173-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="6f173-113">Configurar manualmente um servidor do AGPM para a sua conta</span><span class="sxs-lookup"><span data-stu-id="6f173-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="6f173-114">Para configurar um servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="6f173-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="6f173-115">Na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="6f173-116">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="6f173-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="6f173-117">No **Editor de objeto de política de grupo**, clique em configuração do **usuário**, **modelos administrativos**e **componentes do Windows**.</span><span class="sxs-lookup"><span data-stu-id="6f173-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="6f173-118">Se o **AGPM** não estiver listado em **componentes do Windows**:</span><span class="sxs-lookup"><span data-stu-id="6f173-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="6f173-119">Clique com o botão direito do mouse em **modelos administrativos** e clique em **Adicionar/remover modelos**.</span><span class="sxs-lookup"><span data-stu-id="6f173-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="6f173-120">Clique **em Adicionar**, selecione **AGPM. admx** ou **AGPM. adm**, clique em **abrir**e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="6f173-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="6f173-121">Em **componentes do Windows**, clique duas vezes em **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="6f173-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="6f173-122">No painel de detalhes, clique duas vezes em **servidor do AGPM (todos os domínios)**.</span><span class="sxs-lookup"><span data-stu-id="6f173-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="6f173-123">Na janela de **Propriedades do servidor do AGPM (todos os domínios)** , marque a caixa de seleção **habilitado** e digite o nome do computador e a porta totalmente qualificados (por exemplo, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="6f173-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="6f173-124">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f173-124">Click **OK**.</span></span> <span data-ttu-id="6f173-125">A menos que você queira configurar outras conexões do servidor do AGPM, feche o **Editor de objeto de política de grupo** e implante o GPO.</span><span class="sxs-lookup"><span data-stu-id="6f173-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="6f173-126">(Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo.md).) Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="6f173-127">Para configurar servidores de AGPM adicionais para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="6f173-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="6f173-128">Se nenhuma conexão do servidor do AGPM tiver sido configurada, siga o procedimento anterior para configurar um servidor do AGPM padrão para todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="6f173-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="6f173-129">Para configurar servidores de AGPM separados para alguns ou todos os domínios (substituindo o servidor do AGPM padrão), na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="6f173-130">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="6f173-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="6f173-131">Em **configuração do usuário** no **Editor de objeto de política de grupo**, clique duas vezes em **modelos administrativos**, **componentes do Windows**e **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="6f173-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="6f173-132">No painel de detalhes, clique duas vezes em **servidor do AGPM**.</span><span class="sxs-lookup"><span data-stu-id="6f173-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="6f173-133">Na janela **Propriedades do servidor de AGPM** , marque a caixa de seleção **habilitado** e clique em **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="6f173-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="6f173-134">Na janela **Mostrar conteúdo** :</span><span class="sxs-lookup"><span data-stu-id="6f173-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="6f173-135">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="6f173-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="6f173-136">Para **nome do valor**, digite o nome do domínio (por exemplo, server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="6f173-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="6f173-137">Para **valor**, digite o nome e a porta do servidor de AGPM a ser usado para esse domínio (por exemplo, server2.contoso.com:4600) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f173-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="6f173-138">(Por padrão, o serviço do AGPM escuta na porta 4600.</span><span class="sxs-lookup"><span data-stu-id="6f173-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="6f173-139">Para usar uma porta diferente, confira [Modificar a porta na qual o serviço do AGPM escuta](modify-the-port-on-which-the-agpm-service-listens.md).)</span><span class="sxs-lookup"><span data-stu-id="6f173-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="6f173-140">Repita para cada domínio que não use o servidor do AGPM padrão.</span><span class="sxs-lookup"><span data-stu-id="6f173-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="6f173-141">Clique em **OK** para fechar as janelas **Mostrar conteúdo** e **Propriedades do servidor de AGPM** .</span><span class="sxs-lookup"><span data-stu-id="6f173-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="6f173-142">Feche o **Editor de objeto de política de grupo**.</span><span class="sxs-lookup"><span data-stu-id="6f173-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="6f173-143">(Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo.md).) Quando a política de grupo é atualizada, as novas conexões do servidor do AGPM são configuradas para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="6f173-144">Se você configurou a conexão do servidor do AGPM de forma centralizada, a opção de fazê-lo manualmente não estará disponível para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="6f173-145">Para configurar manualmente o servidor do AGPM para exibição na sua conta</span><span class="sxs-lookup"><span data-stu-id="6f173-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="6f173-146">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="6f173-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6f173-147">No painel detalhes, clique na guia **servidor do AGPM** .</span><span class="sxs-lookup"><span data-stu-id="6f173-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="6f173-148">Digite o nome do computador totalmente qualificado para o servidor do AGPM que gerencia o arquivo morto usado para esse domínio (por exemplo, server.contoso.com) e a porta na qual o serviço do AGPM escuta (por padrão, a porta 4600).</span><span class="sxs-lookup"><span data-stu-id="6f173-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="6f173-149">Clique em **aplicar**e, em seguida, clique em **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="6f173-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="6f173-150">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="6f173-150">Additional considerations</span></span>

-   <span data-ttu-id="6f173-151">Você deve ser capaz de editar e implantar um GPO para executar os procedimentos de configuração centralizada das conexões do servidor do AGPM para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6f173-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="6f173-152">Consulte [editando um GPO](editing-a-gpo.md) e [implante um GPO](deploy-a-gpo.md) para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="6f173-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="6f173-153">O servidor do AGPM selecionado determina quais GPOs são exibidos na guia **conteúdo** e para qual local as configurações da guia de **delegação de domínio** são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="6f173-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="6f173-154">Se não for gerenciado centralmente por meio do modelo administrativo, cada administrador da política de grupo deve definir essa configuração para apontar para o servidor do AGPM do domínio.</span><span class="sxs-lookup"><span data-stu-id="6f173-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="6f173-155">A associação no grupo proprietários criadores de política de grupo deve ser restrita para que não seja usada para burlar o gerenciamento do acesso a GPOs pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="6f173-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="6f173-156">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="6f173-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="6f173-157">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="6f173-157">Additional references</span></span>

-   [<span data-ttu-id="6f173-158">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="6f173-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





