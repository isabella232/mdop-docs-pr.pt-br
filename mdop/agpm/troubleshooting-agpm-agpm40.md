---
title: Solução de problemas do AGPM
description: Solução de problemas do AGPM
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797668"
---
# <span data-ttu-id="87d1a-103">Solução de problemas do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-103">Troubleshooting AGPM</span></span>


<span data-ttu-id="87d1a-104">Esta seção lista alguns problemas comuns que você pode encontrar ao usar o gerenciamento avançado de política de grupo (AGPM) para gerenciar objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="87d1a-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="87d1a-105">Para diagnosticar problemas não listados aqui, pode ser útil para um administrador do AGPM (controle total) para usar o log e o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="87d1a-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="87d1a-106">Para obter mais informações, consulte [configurar log e rastreamento](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

**<span data-ttu-id="87d1a-107">Observação</span><span class="sxs-lookup"><span data-stu-id="87d1a-107">Note</span></span>**  
-   <span data-ttu-id="87d1a-108">Para obter informações sobre como reverter para uma versão anterior de um GPO se houver problemas, confira [reverter para uma versão anterior de um GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

-   <span data-ttu-id="87d1a-109">Para obter informações sobre como recuperar de um desastre restaurando o arquivo completo de um backup, consulte [restaurar o arquivo de um backup](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

 

## <span data-ttu-id="87d1a-110">Quais são os problemas que você está tendo?</span><span class="sxs-lookup"><span data-stu-id="87d1a-110">What problems are you having?</span></span>


-   [<span data-ttu-id="87d1a-111">Não consigo acessar um arquivo morto</span><span class="sxs-lookup"><span data-stu-id="87d1a-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="87d1a-112">O estado do GPO varia de acordo com os diferentes administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="87d1a-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="87d1a-113">Não consigo modificar a conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="87d1a-114">Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="87d1a-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="87d1a-115">Não consigo usar um nome de GPO específico</span><span class="sxs-lookup"><span data-stu-id="87d1a-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="87d1a-116">Não estou recebendo notificações por email do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="87d1a-117">Não consigo usar a porta 4600 para o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="87d1a-118">O serviço do AGPM não será iniciado</span><span class="sxs-lookup"><span data-stu-id="87d1a-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="87d1a-119">A instalação do software de política de grupo falha ao instalar o software</span><span class="sxs-lookup"><span data-stu-id="87d1a-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="87d1a-120">Ocorreu um erro ao restaurar o arquivo morto para um novo servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="87d1a-121">Não consigo acessar um arquivo morto</span><span class="sxs-lookup"><span data-stu-id="87d1a-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="87d1a-122">**Causa**: você não selecionou o servidor e a porta corretos para o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="87d1a-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="87d1a-123">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-123">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-124">Se você for um administrador do AGPM: consulte [Configurar conexões do servidor do AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="87d1a-125">Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87d1a-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="87d1a-126">Consulte [Configurar uma conexão com o servidor do AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

-   <span data-ttu-id="87d1a-127">**Causa**: o serviço do AGPM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="87d1a-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="87d1a-128">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-128">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-129">Se você for um administrador do AGPM: Inicie o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87d1a-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="87d1a-130">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    -   <span data-ttu-id="87d1a-131">Se você não for um administrador do AGPM: entre em contato com um administrador do AGPM para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="87d1a-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="87d1a-132">O estado do GPO varia de acordo com os diferentes administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="87d1a-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="87d1a-133">**Causa**: os administradores de política de grupo diferentes selecionaram servidores de AGPM diferentes para o mesmo arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="87d1a-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="87d1a-134">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-134">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-135">Se você for um administrador do AGPM: consulte [Configurar conexões do servidor do AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="87d1a-136">Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87d1a-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="87d1a-137">Consulte [Configurar uma conexão com o servidor do AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="87d1a-138">Não consigo modificar a conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="87d1a-139">**Causa**: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, o servidor do AGPM foi configurado centralmente usando um modelo administrativo.</span><span class="sxs-lookup"><span data-stu-id="87d1a-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="87d1a-140">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-140">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-141">Se você for um administrador do AGPM: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, consulte [Configurar conexões do servidor do AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="87d1a-142">Se você não for um administrador do AGPM: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, você não precisará modificar o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87d1a-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="87d1a-143">Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="87d1a-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="87d1a-144">**Causa**: você não recebeu uma função com as permissões necessárias para executar a tarefa ou tarefas.</span><span class="sxs-lookup"><span data-stu-id="87d1a-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="87d1a-145">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-145">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-146">Se você for um administrador do AGPM: consulte [delegar acesso ao nível do domínio ao arquivo morto](delegate-domain-level-access-to-the-archive-agpm40.md) e [delegar o acesso a um GPO individual no arquivo morto](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span></span> <span data-ttu-id="87d1a-147">As permissões do AGPM serão em cascata do domínio para todos os GPOs no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="87d1a-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="87d1a-148">Para obter detalhes sobre quais funções podem executar uma tarefa e quais permissões são necessárias para executar uma tarefa, consulte a ajuda da tarefa.</span><span class="sxs-lookup"><span data-stu-id="87d1a-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="87d1a-149">Se você não for um administrador do AGPM e precisar de funções ou permissões adicionais: entre em contato com um administrador do AGPM para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="87d1a-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="87d1a-150">Lembre-se de que, se você for um editor, poderá iniciar o processo de criação de um GPO, implantação de um GPO ou exclusão de um GPO do ambiente de produção do domínio, mas um Aprovador ou administrador do AGPM deve aprovar sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="87d1a-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment of the domain, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="87d1a-151">Não consigo usar um nome de GPO específico</span><span class="sxs-lookup"><span data-stu-id="87d1a-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="87d1a-152">**Causa**: o nome do GPO já está em uso ou você não tem permissão para listar o GPO.</span><span class="sxs-lookup"><span data-stu-id="87d1a-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="87d1a-153">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-153">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-154">Se o nome do GPO aparecer na guia **controlado**, não **controlado**ou **pendente** , escolha outro nome.</span><span class="sxs-lookup"><span data-stu-id="87d1a-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="87d1a-155">Se um GPO implantado for renomeado mas ainda não reimplantado, ele será exibido em seu nome antigo no ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="87d1a-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment of the domain.</span></span> <span data-ttu-id="87d1a-156">Portanto, o nome antigo ainda está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="87d1a-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="87d1a-157">Reimplante o GPO para atualizar seu nome no ambiente de produção e libere o nome para ser usado por outro GPO.</span><span class="sxs-lookup"><span data-stu-id="87d1a-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="87d1a-158">Se o nome do GPO não aparecer na guia **controlado**, não **controlado**ou **pendente** , talvez você não tenha permissão para listar o GPO.</span><span class="sxs-lookup"><span data-stu-id="87d1a-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="87d1a-159">Para solicitar permissão, entre em contato com um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87d1a-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="87d1a-160">Não estou recebendo notificações por email do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="87d1a-161">**Causa**: um servidor de email SMTP e um endereço de email válidos não foram fornecidos, ou nenhuma ação foi tomada e gera uma notificação por email.</span><span class="sxs-lookup"><span data-stu-id="87d1a-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="87d1a-162">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="87d1a-162">**Solution**:</span></span>

    -   <span data-ttu-id="87d1a-163">Se você for um administrador do AGPM: para notificações por email sobre ações pendentes a serem enviadas pelo AGPM, um administrador do AGPM deve fornecer um servidor de email SMTP válido e endereços de email para aprovadores na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

    -   <span data-ttu-id="87d1a-164">As notificações por email são geradas apenas quando um editor, um revisor ou outro administrador de política de grupo que não tem a permissão necessária para criar, implantar ou excluir um GPO envia uma solicitação para que uma dessas ações ocorra.</span><span class="sxs-lookup"><span data-stu-id="87d1a-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="87d1a-165">Não há nenhuma notificação automática de aprovação ou rejeição de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="87d1a-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="87d1a-166">Não consigo usar a porta 4600 para o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="87d1a-167">**Causa**: por padrão, a porta na qual o serviço do AGPM escuta é a porta 4600.</span><span class="sxs-lookup"><span data-stu-id="87d1a-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="87d1a-168">**Solução**: se a porta 4600 não estiver disponível para o serviço do AGPM, modifique a configuração de porta no servidor do AGPM para usar outra porta e, em seguida, atualize a porta na conexão do servidor do AGPM para clientes do AGPM.</span><span class="sxs-lookup"><span data-stu-id="87d1a-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="87d1a-169">Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="87d1a-170">O serviço do AGPM não será iniciado</span><span class="sxs-lookup"><span data-stu-id="87d1a-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="87d1a-171">**Causa**: você modificou as configurações do serviço do AGPM no sistema operacional em **Ferramentas administrativas** e **Serviços**.</span><span class="sxs-lookup"><span data-stu-id="87d1a-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="87d1a-172">**Solução**: modifique as configurações para **gerenciamento avançado de política de grupo da Microsoft-servidor** em **programas e recursos** no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="87d1a-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="87d1a-173">Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="87d1a-174">A instalação do software de política de grupo falha ao instalar o software</span><span class="sxs-lookup"><span data-stu-id="87d1a-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="87d1a-175">**Causa**: o AGPM preserva a integridade dos pacotes de instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="87d1a-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="87d1a-176">Embora os GPOs sejam editados offline, os links entre pacotes além das informações de cliente armazenadas em cache são preservados.</span><span class="sxs-lookup"><span data-stu-id="87d1a-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="87d1a-177">Isso ocorre por design.</span><span class="sxs-lookup"><span data-stu-id="87d1a-177">This is by design.</span></span>

-   <span data-ttu-id="87d1a-178">**Solução**: ao editar um GPO offline com o AGPM, configure qualquer atualização de instalação de software de política de grupo de um pacote em outro GPO para fazer referência ao GPO implantado, e não à cópia com check-out.</span><span class="sxs-lookup"><span data-stu-id="87d1a-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="87d1a-179">O editor deve ter permissão de **leitura** para o GPO implantado.</span><span class="sxs-lookup"><span data-stu-id="87d1a-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="87d1a-180">Ocorreu um erro ao restaurar o arquivo morto para um novo servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="87d1a-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="87d1a-181">**Causa**: por motivos de segurança, a criptografia que protege a senha inserida na guia de **delegação de domínio** faz com que a senha falhe se o arquivo morto for movido para outro computador.</span><span class="sxs-lookup"><span data-stu-id="87d1a-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="87d1a-182">**Solução**: Digite novamente e confirme a senha na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="87d1a-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

 

 





