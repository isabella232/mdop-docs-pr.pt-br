---
title: Solução de problemas da MED-V
description: Solução de problemas da MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799757"
---
# <span data-ttu-id="b0eb8-103">Solução de problemas da MED-V</span><span class="sxs-lookup"><span data-stu-id="b0eb8-103">Troubleshooting MED-V</span></span>


<span data-ttu-id="b0eb8-104">Esta seção fornece informações para ajudar a solucionar problemas gerais com a virtualização de área de trabalho do Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="b0eb8-104">This section provides information to help troubleshoot general issues with Microsoft Enterprise Desktop Virtualization (MED-V).</span></span>

## <span data-ttu-id="b0eb8-105">Alterar a resolução do host e, em seguida, maximizar o espaço de trabalho do MED-V faz com que a área de trabalho apareça em preto</span><span class="sxs-lookup"><span data-stu-id="b0eb8-105">Changing the host resolution and then maximizing the MED-V workspace causes the desktop to appear black</span></span>


<span data-ttu-id="b0eb8-106">Ao trabalhar no modo de área de trabalho completo, se você alterar a resolução do host e, em seguida, maximizar a janela do espaço de trabalho do MED-V, a área de trabalho aparecerá em preto e o espaço de trabalho do MED-V pode não</span><span class="sxs-lookup"><span data-stu-id="b0eb8-106">When working in full desktop mode, if you change the host resolution and then maximize the MED-V workspace window, the desktop appears black and the MED-V workspace might not respond.</span></span>

### <span data-ttu-id="b0eb8-107">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-107">Solution</span></span>

<span data-ttu-id="b0eb8-108">Pare e, em seguida, inicie o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-108">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="b0eb8-109">Iniciando um espaço de trabalho do MED-V com um adaptador de rede desabilitado e, posteriormente, habilitar o adaptador não restaura a conectividade de rede</span><span class="sxs-lookup"><span data-stu-id="b0eb8-109">Starting a MED-V workspace with a network adapter disabled and then later enabling the adapter does not restore network connectivity</span></span>


<span data-ttu-id="b0eb8-110">Se você configurar um espaço de trabalho do MED-V no modo de ponte e, em seguida, iniciar o espaço de trabalho do MED-V enquanto um adaptador de rede estiver desabilitado, se o adaptador for habilitado posteriormente, a conectividade de rede por meio desse adaptador não será restaurada.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-110">If you configure a MED-V workspace in bridge mode and then start the MED-V workspace while a network adapter is disabled, if the adapter is later enabled, the network connectivity through that adapter is not restored.</span></span>

### <span data-ttu-id="b0eb8-111">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-111">Solution</span></span>

<span data-ttu-id="b0eb8-112">Pare e, em seguida, inicie o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-112">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="b0eb8-113">Uma imagem pode ser usada por apenas um usuário do Windows por computador</span><span class="sxs-lookup"><span data-stu-id="b0eb8-113">An image can be used by only one Windows user per computer</span></span>


<span data-ttu-id="b0eb8-114">Uma imagem do espaço de trabalho do MED-V pode ser usada somente pelo usuário do Windows que baixou ou importou a imagem.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-114">A MED-V workspace image can be used only by the Windows user who downloaded or imported the image.</span></span> <span data-ttu-id="b0eb8-115">Esse usuário é o único usuário além dos administradores que têm permissões para a pasta onde as imagens baixadas estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-115">This user is the only user aside from administrators who have permissions to the folder where the downloaded images are located.</span></span>

### <span data-ttu-id="b0eb8-116">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-116">Solution</span></span>

<span data-ttu-id="b0eb8-117">Altere manualmente a ACL (lista de controle de acesso) no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-117">Manually change the access control list (ACL) on the image store.</span></span>

## <span data-ttu-id="b0eb8-118">Ao instalar o MED-V usando o Configuration Manager com direitos de usuários habilitados, a desinstalação falha</span><span class="sxs-lookup"><span data-stu-id="b0eb8-118">When installing MED-V by using Configuration Manager with users rights enabled, uninstall fails</span></span>


<span data-ttu-id="b0eb8-119">Se o MED-V estiver instalado usando o Microsoft System Center Configuration Manager e o modo de execução do pacote for definido como direitos de usuário, a desinstalação falhará com uma mensagem de erro que diz que somente os usuários administrativos podem desinstalar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-119">If MED-V is installed by using Microsoft System Center Configuration Manager and the run mode of the package is set to users rights, uninstall fails with an error message that says that only administrative users can uninstall MED-V.</span></span>

### <span data-ttu-id="b0eb8-120">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-120">Solution</span></span>

<span data-ttu-id="b0eb8-121">Ao criar um pacote do Configuration Manager para MED-V, defina o modo de execução como direitos administrativos.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-121">When creating a Configuration Manager package for MED-V, set the run mode to administrative rights.</span></span>

## <span data-ttu-id="b0eb8-122">Ao instalar o MED-V usando um sistema de implantação corporativa, no qual a instalação está configurada para executar o cliente após a instalação, não é possível executar o cliente</span><span class="sxs-lookup"><span data-stu-id="b0eb8-122">When installing MED-V by using a corporate deployment system, where the installation is configured to run the client following installation, you cannot run the client</span></span>


<span data-ttu-id="b0eb8-123">Se o MED-V estiver instalado usando um sistema de implantação corporativo e o pacote de instalação estiver configurado para executar o cliente MED-V após a instalação, após a execução do cliente na conta do sistema, você não poderá ver que o cliente está em execução (exceto na área de notificação) e não pode interagir com ele.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-123">If MED-V is installed by using a corporate deployment system and the installation package is configured to run MED-V client following the installation, after the client is running under the system account, you cannot see that the client is running (except in the notification area), and you cannot interact with it.</span></span>

### <span data-ttu-id="b0eb8-124">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-124">Solution</span></span>

<span data-ttu-id="b0eb8-125">Ao instalar o MED-V usando um sistema de implantação corporativo, use o parâmetro *Start \ _MEDV = 0* . msi.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-125">When installing MED-V by using a corporate deployment system, use the *START\_MEDV=0* .msi parameter.</span></span>

## <span data-ttu-id="b0eb8-126">A imagem de teste do MED-V falha ao iniciar</span><span class="sxs-lookup"><span data-stu-id="b0eb8-126">MED-V test image fails to start</span></span>


<span data-ttu-id="b0eb8-127">Se uma imagem de teste do MED-V não for iniciada, ela nunca será recuperada e todas as futuras inicializações falharão com a mensagem de erro "GINA falha ao carregar".</span><span class="sxs-lookup"><span data-stu-id="b0eb8-127">If a MED-V test image fails to start, it will never recover and all future startups will fail with a “GINA fail to load” error message.</span></span>

### <span data-ttu-id="b0eb8-128">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-128">Solution</span></span>

<span data-ttu-id="b0eb8-129">Exclua a imagem de teste existente e crie-a novamente.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-129">Delete the existing test image and then re-create it.</span></span>

## <span data-ttu-id="b0eb8-130">Depois de tentar ingressar em um domínio com as credenciais erradas, a imagem nunca é bem-sucedida ao ingressar no domínio</span><span class="sxs-lookup"><span data-stu-id="b0eb8-130">After attempting to join a domain with the wrong credentials, the image never succeeds in joining the domain</span></span>


<span data-ttu-id="b0eb8-131">Se houver um erro de configuração no bloco de construção de domínio ingressar, que faz parte do script de configuração da máquina virtual pela primeira vez, isso causará falha no espaço de trabalho do MED-V ao tentar ingressar em um domínio.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-131">If there is a configuration error in the join domain building block, which is part of the virtual machine first-time setup script, it causes the MED-V workspace to fail when attempting to join a domain.</span></span> <span data-ttu-id="b0eb8-132">Depois que o erro de configuração for reparado, a imagem incluída no espaço de trabalho do MED-V não poderá ingressar no domínio.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-132">After the configuration error is repaired, the image included in the MED-V workspace cannot join the domain.</span></span>

### <span data-ttu-id="b0eb8-133">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-133">Solution</span></span>

<span data-ttu-id="b0eb8-134">Se a imagem foi implantada, redistribua a imagem.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-134">If the image was deployed, redistribute the image.</span></span> <span data-ttu-id="b0eb8-135">Se a imagem for uma imagem de teste, recrie a imagem.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-135">If the image was a test image, re-create the image.</span></span>

## <span data-ttu-id="b0eb8-136">O MED-V não oferece suporte a vários monitores</span><span class="sxs-lookup"><span data-stu-id="b0eb8-136">MED-V does not support multiple monitors</span></span>


<span data-ttu-id="b0eb8-137">O MED-V não é compatível com a exibição de aplicativos publicados em vários monitores.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-137">MED-V does not support displaying published applications across multiple monitors.</span></span> <span data-ttu-id="b0eb8-138">Aplicativos publicados e outras janelas de cliente podem ser exibidas na tela errada e, às vezes, quando uma tela é desconectada, o MED-V tenta enviar a tela para o monitor para que o monitor conectado apareça em branco.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-138">Published applications and other client windows may be displayed in the wrong screen, and sometimes after a screen is disconnected, MED-V attempts to send the screen to the monitor so that the connected monitor appears blank.</span></span>

### <span data-ttu-id="b0eb8-139">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-139">Solution</span></span>

<span data-ttu-id="b0eb8-140">Desconecte a tela adicional e reinicie o cliente.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-140">Disconnect the additional screen, and restart the client.</span></span>

## <span data-ttu-id="b0eb8-141">O espaço de trabalho do MED-V pode falhar ao iniciar quando o host falha durante a inicialização do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="b0eb8-141">MED-V workspace might fail to start if the host crashes during MED-V workspace startup</span></span>


<span data-ttu-id="b0eb8-142">Se o host falha durante o processo de inicialização do espaço de trabalho do MED-V e uma mensagem de erro é exibida dizendo que "o elemento raiz está ausente," o espaço de trabalho do MED-V pode adicionar dados a um arquivo de configuração de máquina virtual (VMC) vazio, o que fará com que o processo de inicialização falhe.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-142">If the host crashes during the MED-V workspace startup process and an error message appears that says “Root element is missing,” the MED-V workspace might add data to an empty virtual machine configuration (VMC) file, which will cause the startup process to fail.</span></span>

### <span data-ttu-id="b0eb8-143">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-143">Solution</span></span>

<span data-ttu-id="b0eb8-144">Substitua o arquivo VMC vazio por um arquivo VMC da imagem base.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-144">Replace the empty VMC file with a VMC file from the base image.</span></span>

## <span data-ttu-id="b0eb8-145">O teclado não responde nas janelas de aplicativos publicados</span><span class="sxs-lookup"><span data-stu-id="b0eb8-145">The keyboard does not respond in published application windows</span></span>


<span data-ttu-id="b0eb8-146">Em um espaço de trabalho do MED-V, se você pressionar a tecla do logotipo do Windows quando um aplicativo publicado estiver em foco, o teclado não responderá mais nas janelas de aplicativos publicadas.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-146">In a MED-V workspace, if you press the Windows logo key when a published application is in focus, the keyboard no longer responds in published application windows.</span></span>

### <span data-ttu-id="b0eb8-147">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-147">Solution</span></span>

<span data-ttu-id="b0eb8-148">Pressione a tecla do logotipo do Windows enquanto um aplicativo publicado estiver em foco.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-148">Press the Windows logo key while a published application is in focus.</span></span>

## <span data-ttu-id="b0eb8-149">Um espaço de trabalho do domínio MED-V não atualiza as credenciais do domínio</span><span class="sxs-lookup"><span data-stu-id="b0eb8-149">A domain MED-V workspace does not update domain credentials</span></span>


<span data-ttu-id="b0eb8-150">Ao usar um espaço de trabalho do MED-V persistente em um ambiente de domínio, se você alterar a senha do domínio, o cliente MED-V não atualizará as credenciais de domínio do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-150">When using a persistent MED-V workspace in a domain environment, if you change your domain password, the MED-V client does not update the MED-V workspace domain credentials.</span></span> <span data-ttu-id="b0eb8-151">Quando um aplicativo publicado tenta acessar um recurso de rede, você receberá uma mensagem de erro informando que suas credenciais venceram.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-151">When a published application attempts to access a network resource, you will receive an error message notifying you that your credentials expired.</span></span>

### <span data-ttu-id="b0eb8-152">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-152">Solution</span></span>

<span data-ttu-id="b0eb8-153">Reinicie o sistema operacional do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-153">Restart the MED-V workspace operating system.</span></span>

## <span data-ttu-id="b0eb8-154">Aplicativo de publicação maximizada Windows cover The host Taskbar</span><span class="sxs-lookup"><span data-stu-id="b0eb8-154">Maximized published application windows cover the host taskbar</span></span>


<span data-ttu-id="b0eb8-155">Se você maximizar uma janela de aplicativo publicada para tela inteira, talvez ela cubra a barra de tarefas do host.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-155">If you maximize a published application window to full screen, it might cover the host taskbar.</span></span>

### <span data-ttu-id="b0eb8-156">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-156">Solution</span></span>

<span data-ttu-id="b0eb8-157">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="b0eb8-157">Do one of the following:</span></span>

<span data-ttu-id="b0eb8-158">Minimize a janela do aplicativo publicado para obter acesso à área de notificação e reinicie o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-158">Minimize the published application window to gain access to the notification area, and restart the MED-V workspace.</span></span>

<span data-ttu-id="b0eb8-159">Minimize a janela do aplicativo publicado e restaure a janela ao seu estado maximizado.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-159">Minimize the published application window, and then restore the window to its maximized state.</span></span>

## <span data-ttu-id="b0eb8-160">A adição de usuários ou grupos no Gerenciador de configuração do MED-V Server não funciona</span><span class="sxs-lookup"><span data-stu-id="b0eb8-160">Adding users or groups in the MED-V Server Configuration Manager does not work</span></span>


<span data-ttu-id="b0eb8-161">Ao adicionar usuários ou grupos na caixa de diálogo **Selecionar usuários ou grupos** , os usuários ou grupos selecionados não são adicionados à lista de controle de acesso no Gerenciador de configuração do MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-161">When adding users or groups in the **Select Users or Groups** dialog box, the selected users or groups are not added to the access control list in the MED-V Server Configuration Manager.</span></span>

### <span data-ttu-id="b0eb8-162">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-162">Solution</span></span>

<span data-ttu-id="b0eb8-163">Adicionar usuários ou grupos usando a caixa de diálogo **Inserir nomes de usuários ou grupos** .</span><span class="sxs-lookup"><span data-stu-id="b0eb8-163">Add users or groups using the **Enter User or Group names** dialog box.</span></span> <span data-ttu-id="b0eb8-164">Para obter informações detalhadas, consulte [como instalar e configurar o componente do servidor MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span><span class="sxs-lookup"><span data-stu-id="b0eb8-164">For detailed information, see [How to Install and Configure the MED-V Server Component](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span></span>

## <span data-ttu-id="b0eb8-165">O MED-V não funciona em computadores com o Windows Virtual PC para Windows 7 instalado</span><span class="sxs-lookup"><span data-stu-id="b0eb8-165">MED-V does not work on computers with Windows Virtual PC for Windows 7 installed</span></span>


<span data-ttu-id="b0eb8-166">O MED-V requer o PC2007 virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-166">MED-V requires Windows Virtual PC2007.</span></span> <span data-ttu-id="b0eb8-167">O Windows Virtual PC para Windows e o virtual PC2007 SP1 não podem ser instalados no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-167">Windows Virtual PC for Windows7 and Virtual PC2007 SP1 cannot be installed on the same computer.</span></span>

### <span data-ttu-id="b0eb8-168">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-168">Solution</span></span>

<span data-ttu-id="b0eb8-169">Desinstale o Virtual PC para o Windows7 antes de instalar o PC2007 virtual SP1 e o MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-169">Uninstall Virtual PC for Windows7 before installing Virtual PC2007 SP1 and MED-V.</span></span>

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a><span data-ttu-id="b0eb8-170">O MED-V não é compatível com imagens do modo Virtual PC e WindowsXP</span><span class="sxs-lookup"><span data-stu-id="b0eb8-170">MED-V does not support Virtual PC and WindowsXP Mode images</span></span>


<span data-ttu-id="b0eb8-171">O MED-V 1.0 SP1 não oferece suporte a imagens criadas pelo PC virtual do Windows para o Windows7.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-171">MED-V1.0 SP1 does not support images created by Windows Virtual PC for Windows7.</span></span> <span data-ttu-id="b0eb8-172">Se um PC virtual para a imagem do Windows7 for usado, o cliente falhará durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-172">If a Virtual PC for Windows7 image is used, the client will fail during startup.</span></span>

### <span data-ttu-id="b0eb8-173">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-173">Solution</span></span>

<span data-ttu-id="b0eb8-174">Criar imagens do MED-V usando o virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-174">Create MED-V images by using Virtual PC2007 SP1.</span></span>

## <span data-ttu-id="b0eb8-175">O Firewall do Windows bloqueia a atividade de rede do PC2007 SP1 virtual</span><span class="sxs-lookup"><span data-stu-id="b0eb8-175">Windows firewall blocks Virtual PC2007 SP1 network activity</span></span>


<span data-ttu-id="b0eb8-176">Por padrão, o Firewall do Windows bloqueia a atividade de rede do PC2007 SP1 virtual e, quando o virtual PC2007 SP1 é iniciado no computador cliente, há uma mensagem de firewall que bloqueia a sequência de inicialização e todo o acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-176">By default, Windows firewall blocks Virtual PC2007 SP1 network activity, and when Virtual PC2007 SP1 initiates on the client computer, there is a firewall message that blocks its startup sequence and all network access.</span></span>

### <span data-ttu-id="b0eb8-177">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-177">Solution</span></span>

<span data-ttu-id="b0eb8-178">Atualize a exceção do firewall usando a política de grupo antes de o MED-V ser usado pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-178">Update the firewall exception by using Group Policy before MED-V is used by the end user.</span></span>

## <span data-ttu-id="b0eb8-179">A mensagem de erro ao atualizar o cliente é exibida</span><span class="sxs-lookup"><span data-stu-id="b0eb8-179">When upgrading the client an error message appears</span></span>


<span data-ttu-id="b0eb8-180">Durante a atualização do cliente do MED-V 1.0 para o MED-V 1.0 SP1, uma mensagem poderá ser exibida informando que não há um espaço de trabalho do MED-V definido.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-180">When upgrading the client from MED-V1.0 to MED-V1.0 SP1, a message may appear notifying you that no MED-V workspace is defined.</span></span>

### <span data-ttu-id="b0eb8-181">Solução</span><span class="sxs-lookup"><span data-stu-id="b0eb8-181">Solution</span></span>

<span data-ttu-id="b0eb8-182">Feche o cliente e reinicie-o.</span><span class="sxs-lookup"><span data-stu-id="b0eb8-182">Close the client and restart it.</span></span>

## <span data-ttu-id="b0eb8-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0eb8-183">Related topics</span></span>


[<span data-ttu-id="b0eb8-184">Notas de versão do MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="b0eb8-184">MED-V 1.0 Release Notes</span></span>](med-v-10-release-notesmedv-10.md)

[<span data-ttu-id="b0eb8-185">Notas de versão do MED-V 1.0 SP1 e SP2</span><span class="sxs-lookup"><span data-stu-id="b0eb8-185">MED-V 1.0 SP1 and SP2 Release Notes</span></span>](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





