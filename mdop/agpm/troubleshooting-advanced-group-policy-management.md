---
title: Solução de problemas do Gerenciamento Avançado de Política de Grupo
description: Solução de problemas do Gerenciamento Avançado de Política de Grupo
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797288"
---
# <span data-ttu-id="8fb9b-103">Solução de problemas do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="8fb9b-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="8fb9b-104">Esta seção lista alguns problemas comuns que você pode encontrar ao usar o gerenciamento avançado de política de grupo (AGPM) para gerenciar objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="8fb9b-105">Quais são os problemas que você está tendo?</span><span class="sxs-lookup"><span data-stu-id="8fb9b-105">What problems are you having?</span></span>


-   [<span data-ttu-id="8fb9b-106">Não consigo acessar um arquivo morto</span><span class="sxs-lookup"><span data-stu-id="8fb9b-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="8fb9b-107">O estado do GPO varia de acordo com os diferentes administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="8fb9b-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="8fb9b-108">Não consigo modificar a conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="8fb9b-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="8fb9b-109">Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="8fb9b-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="8fb9b-110">Não consigo usar um nome de GPO específico</span><span class="sxs-lookup"><span data-stu-id="8fb9b-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="8fb9b-111">Não estou recebendo notificações por email do AGPM</span><span class="sxs-lookup"><span data-stu-id="8fb9b-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="8fb9b-112">Não consigo usar a porta 4600 para o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="8fb9b-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="8fb9b-113">O serviço do AGPM não será iniciado</span><span class="sxs-lookup"><span data-stu-id="8fb9b-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="8fb9b-114">A instalação do software de política de grupo falha ao instalar o software</span><span class="sxs-lookup"><span data-stu-id="8fb9b-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="8fb9b-115">Não consigo acessar um arquivo morto</span><span class="sxs-lookup"><span data-stu-id="8fb9b-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="8fb9b-116">**Causa**: você não selecionou o servidor e a porta corretos para o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="8fb9b-117">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-117">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-118">Se você for um administrador do AGPM: consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="8fb9b-119">Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="8fb9b-120">Consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="8fb9b-121">**Causa**: o serviço de gerenciamento de política de grupo avançado não está em execução.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="8fb9b-122">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-122">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-123">Se você for um administrador do AGPM: Inicie o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="8fb9b-124">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="8fb9b-125">Se você não for um administrador do AGPM: entre em contato com um administrador do AGPM para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="8fb9b-126">O estado do GPO varia de acordo com os diferentes administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="8fb9b-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="8fb9b-127">**Causa**: os administradores de política de grupo diferentes selecionaram servidores de AGPM diferentes para o mesmo arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="8fb9b-128">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-128">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-129">Se você for um administrador do AGPM: consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="8fb9b-130">Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="8fb9b-131">Consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="8fb9b-132">Não consigo modificar a conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="8fb9b-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="8fb9b-133">**Causa**: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, o servidor do AGPM foi configurado centralmente usando um modelo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="8fb9b-134">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-134">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-135">Se você for um administrador do AGPM: se as configurações na guia **servidor de AGPM** não estiverem disponíveis, consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="8fb9b-136">Se você não for um administrador do AGPM: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, você não precisará modificar o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="8fb9b-137">Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs</span><span class="sxs-lookup"><span data-stu-id="8fb9b-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="8fb9b-138">**Causa**: você não recebeu uma função com as permissões necessárias para executar a tarefa ou tarefas.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="8fb9b-139">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-139">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-140">Se você for um administrador do AGPM: consulte [delegar](delegate-domain-level-access.md) acesso a nível de domínio e [acesso de representante a um GPO individual](delegate-access-to-an-individual-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="8fb9b-141">As permissões do AGPM serão em cascata do domínio para todos os GPOs no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="8fb9b-142">Como novos administradores de política de grupo são adicionados no nível do domínio, suas permissões devem ser definidas para aplicar-se a **esse objeto e a objetos aninhados**.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="8fb9b-143">Para obter detalhes sobre quais funções podem executar uma tarefa e quais permissões são necessárias para executar uma tarefa, consulte a ajuda da tarefa.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="8fb9b-144">Se você não for um administrador do AGPM e precisar de funções ou permissões adicionais: entre em contato com um administrador do AGPM para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="8fb9b-145">Observe que, se você for um editor, você pode iniciar o processo de criação de um GPO, implantação de um GPO ou exclusão de um GPO do ambiente de produção, mas um Aprovador ou administrador do AGPM deve aprovar sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="8fb9b-146">Não consigo usar um nome de GPO específico</span><span class="sxs-lookup"><span data-stu-id="8fb9b-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="8fb9b-147">**Causa**: o nome do GPO já está em uso ou você não tem permissão para listar o GPO.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="8fb9b-148">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-148">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-149">Se o nome do GPO aparecer na guia **controlado**, não **controlado**ou **pendente** , escolha outro nome.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="8fb9b-150">Se um GPO que foi implantado for renomeado mas ainda não reimplantado, ele será exibido em seu nome antigo no ambiente de produção – portanto, o nome antigo ainda estará em uso.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="8fb9b-151">Reimplante o GPO para atualizar seu nome no ambiente de produção e libere o nome para ser usado por outro GPO.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="8fb9b-152">Se o nome do GPO não aparecer na guia **controlado**, não **controlado**ou **pendente** , talvez você não tenha permissão para listar o GPO.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="8fb9b-153">Para solicitar permissão, entre em contato com um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="8fb9b-154">Não estou recebendo notificações por email do AGPM</span><span class="sxs-lookup"><span data-stu-id="8fb9b-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="8fb9b-155">**Causa**: um servidor de email SMTP e um endereço de email válidos não foram fornecidos, ou nenhuma ação foi tomada e gera uma notificação por email.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="8fb9b-156">**Solução**:</span><span class="sxs-lookup"><span data-stu-id="8fb9b-156">**Solution**:</span></span>

    -   <span data-ttu-id="8fb9b-157">Se você for um administrador do AGPM: para notificações por email sobre ações pendentes a serem enviadas pelo AGPM, um administrador do AGPM deve fornecer um servidor de email SMTP válido e endereços de email para aprovadores na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="8fb9b-158">As notificações por email são geradas apenas quando um editor, um revisor ou outro administrador de política de grupo que não tem a permissão necessária para criar, implantar ou excluir um GPO envia uma solicitação para que uma dessas ações ocorra.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="8fb9b-159">Não há nenhuma notificação automática de aprovação ou rejeição de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="8fb9b-160">Não consigo usar a porta 4600 para o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="8fb9b-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="8fb9b-161">**Causa**: por padrão, a porta na qual o serviço do AGPM escuta é a porta 4600.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="8fb9b-162">**Solução**: se a porta 4600 não estiver disponível para o serviço do AGPM, modifique cada arquivo de índice do arquivo para usar outra porta e, em seguida, atualize o servidor do AGPM para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="8fb9b-163">Para obter mais informações, consulte [Modificar a porta na qual o serviço do AGPM escuta](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="8fb9b-164">O serviço do AGPM não será iniciado</span><span class="sxs-lookup"><span data-stu-id="8fb9b-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="8fb9b-165">**Causa**: você modificou as configurações do serviço do AGPM no sistema operacional em **Ferramentas administrativas** e **Serviços**.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="8fb9b-166">**Solução**: modifique as configurações para **gerenciamento avançado de política de grupo da Microsoft-servidor** em **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="8fb9b-167">Para obter mais informações, consulte [Modificar a conta do serviço do AGPM](modify-the-agpm-service-account.md).</span><span class="sxs-lookup"><span data-stu-id="8fb9b-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="8fb9b-168">A instalação do software de política de grupo falha ao instalar o software</span><span class="sxs-lookup"><span data-stu-id="8fb9b-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="8fb9b-169">**Causa**: o AGPM preserva a integridade dos pacotes de instalação do software de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="8fb9b-170">Embora os GPOs sejam editados offline, os links entre pacotes e as informações de cliente armazenadas em cache são preservados.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="8fb9b-171">Isso ocorre por design.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-171">This is by design.</span></span>

-   <span data-ttu-id="8fb9b-172">**Solução**: ao editar um GPO offline com o AGPM, configure qualquer atualização de instalação de software de política de grupo de um pacote em outro GPO para fazer referência ao GPO implantado e não à cópia com check-out.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="8fb9b-173">O editor deve ter permissão de **leitura** para o GPO implantado.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 





