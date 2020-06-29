---
title: Sobre o App-V 5.0 SP2
description: Sobre o App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796635"
---
# <span data-ttu-id="7fe42-103">Sobre o App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fe42-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="7fe42-104">O App-V 5.0 SP2 fornece uma plataforma integrada aprimorada, virtualização mais flexível e gerenciamento eficiente para aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="7fe42-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="7fe42-105">Para obter mais informações, consulte [visão geral do App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="7fe42-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="7fe42-106">Alterações na funcionalidade padrão do SP2 do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7fe42-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="7fe42-107">As seções a seguir contêm informações sobre as alterações na funcionalidade padrão do App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fe42-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="7fe42-108">Suporte para Windows Server 2012 R2 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7fe42-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="7fe42-109">O App-V 5,0 inclui suporte para Windows Server 2012 R2 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7fe42-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="7fe42-110">O App-V 5.0 SP2 agora oferece suporte ao redirecionamento de pastas para o diretório roaming de AppData do usuário</span><span class="sxs-lookup"><span data-stu-id="7fe42-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="7fe42-111">O aplicativo do App-V 5.0 SP2 dá suporte a roaming AppData (% AppData%) redirecionamento de pastas.</span><span class="sxs-lookup"><span data-stu-id="7fe42-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="7fe42-112">Para obter mais informações, consulte o [planejamento para usar o redirecionamento de pastas com o App-V](planning-to-use-folder-redirection-with-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="7fe42-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="7fe42-113">Melhorias na atualização do pacote e tarefas pendentes</span><span class="sxs-lookup"><span data-stu-id="7fe42-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="7fe42-114">No App-V 5.0 SP2, você não é mais solicitado a fechar um aplicativo virtual em execução quando uma versão mais recente do grupo ou do grupo de conexão é publicada.</span><span class="sxs-lookup"><span data-stu-id="7fe42-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="7fe42-115">Se um pacote ou grupo de conexão estiver em uso quando você tentar executar uma tarefa relacionada, uma mensagem será exibida para indicar que o objeto está em uso e que a operação será tentada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="7fe42-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="7fe42-116">As tarefas que foram colocadas em um estado pendente serão realizadas de acordo com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="7fe42-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7fe42-117">Tipo de tarefa</span><span class="sxs-lookup"><span data-stu-id="7fe42-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="7fe42-118">Regra aplicável</span><span class="sxs-lookup"><span data-stu-id="7fe42-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe42-119">Tarefa baseada em usuário, por exemplo, publicar um pacote para um usuário</span><span class="sxs-lookup"><span data-stu-id="7fe42-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe42-120">A tarefa pendente será executada após o usuário fazer logoff e, em seguida, fazer logon novamente.</span><span class="sxs-lookup"><span data-stu-id="7fe42-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe42-121">Tarefa com base global, por exemplo, habilitar um grupo de conexão globalmente</span><span class="sxs-lookup"><span data-stu-id="7fe42-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe42-122">A tarefa pendente será executada quando o computador for desligado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="7fe42-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7fe42-123">Quando uma tarefa é colocada em um estado pendente, o cliente App-V também gera uma chave do registro para a tarefa pendente, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7fe42-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7fe42-124">Tarefa baseada em usuário ou globalmente</span><span class="sxs-lookup"><span data-stu-id="7fe42-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="7fe42-125">Onde a chave do registro é gerada</span><span class="sxs-lookup"><span data-stu-id="7fe42-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe42-126">Tarefas baseadas em usuário</span><span class="sxs-lookup"><span data-stu-id="7fe42-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe42-127">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="7fe42-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe42-128">Tarefas com base global</span><span class="sxs-lookup"><span data-stu-id="7fe42-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe42-129">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="7fe42-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="7fe42-130">Virtualizando o Microsoft Office 2013 e o Microsoft Office 2010 usando o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7fe42-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="7fe42-131">Use o link a seguir para obter mais informações sobre os cenários do Microsoft Office com suporte para o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7fe42-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="7fe42-132">Virtualização do Microsoft Office 2013 para Application Virtualization (App-V) 5.0</span><span class="sxs-lookup"><span data-stu-id="7fe42-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="7fe42-133">**Observação**  Este documento enfoca a criação de um pacote do Microsoft Office 2013 App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7fe42-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="7fe42-134">No entanto, ele também fornece informações sobre cenários do Microsoft Office 2010 com o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7fe42-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="7fe42-135">Aplicativo da interface de usuário do gerenciamento de cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7fe42-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="7fe42-136">Em versões anteriores do App-V 5,0, a interface do usuário de gerenciamento do cliente (UI) foi fornecida com a instalação do aplicativo do aplicativo-V 5,0 Client.</span><span class="sxs-lookup"><span data-stu-id="7fe42-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="7fe42-137">Com o App-V 5.0 SP2, isso não é mais o caso.</span><span class="sxs-lookup"><span data-stu-id="7fe42-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="7fe42-138">Os administradores agora têm a opção de implantar a interface do usuário do cliente do App-V 5,0 como um aplicativo virtual (usando todas as configurações de implantação do App-V com suporte) ou como um aplicativo instalado.</span><span class="sxs-lookup"><span data-stu-id="7fe42-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="7fe42-139">Para obter mais informações, consulte [aplicativo da interface do usuário do cliente do Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="7fe42-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="7fe42-140">Empacotamento e implantação automáticos do assembly lado a lado (SxS)</span><span class="sxs-lookup"><span data-stu-id="7fe42-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="7fe42-141">O App-V 5.0 SP2 agora detecta automaticamente assemblies lado a lado (SxS) e a implantação no computador que executa o cliente App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fe42-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="7fe42-142">Um assembly SxS consiste principalmente em dependências do tempo de execução do VC + + Runtime ou MSXML.</span><span class="sxs-lookup"><span data-stu-id="7fe42-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="7fe42-143">Em versões anteriores do App-V, os aplicativos virtuais que tinham dependências em tempo de execução do VC exigiam que essas dependências fossem localmente no computador executando o cliente App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fe42-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="7fe42-144">Agora há suporte para a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="7fe42-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="7fe42-145">O sequenciador do App-V 5,0 captura automaticamente o assembly SxS no pacote, independentemente de o tempo de execução do VC já ter sido instalado no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="7fe42-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="7fe42-146">O cliente App-V 5,0 instala automaticamente o assembly SxS obrigatório para o computador que está executando o cliente, conforme necessário no momento da publicação.</span><span class="sxs-lookup"><span data-stu-id="7fe42-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="7fe42-147">O sequenciador do App-V 5,0 relata a dependência do tempo de execução do VC usando o mecanismo de relatório do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="7fe42-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="7fe42-148">O sequenciador do App-V 5,0 agora permite que você exclua a dependência do tempo de execução do VC no caso de que a dependência já esteja disponível no computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="7fe42-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="7fe42-149">Melhorias na atualização de publicação</span><span class="sxs-lookup"><span data-stu-id="7fe42-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="7fe42-150">O App-V 5,0 dá suporte a vários recursos foram adicionados para melhorar a experiência geral da atualização de um conjunto de aplicativos para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="7fe42-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="7fe42-151">A lista a seguir mostra os aprimoramentos de atualização de publicação:</span><span class="sxs-lookup"><span data-stu-id="7fe42-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="7fe42-152">A lista a seguir contém mais informações sobre como habilitar os novos aprimoramentos de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="7fe42-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="7fe42-153">**EnablePublishingRefreshUI** -habilita a barra de progresso de atualização de publicação do computador que está executando o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7fe42-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="7fe42-154">**HideUI** -oculta a barra de progresso de atualização de publicação durante uma sincronização manual.</span><span class="sxs-lookup"><span data-stu-id="7fe42-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="7fe42-155">Configuração do novo cliente</span><span class="sxs-lookup"><span data-stu-id="7fe42-155">New Client Configuration Setting</span></span>

<span data-ttu-id="7fe42-156">A configuração do novo cliente a seguir está disponível com o App-V 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="7fe42-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="7fe42-157">**EnableDynamicVirtualization** -habilita as extensões do shell com suporte, objetos auxiliares do navegador e controles ActiveX para serem virtualizados e executados com aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="7fe42-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="7fe42-158">Para obter mais informações, consulte [sobre as definições de configuração do cliente](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7fe42-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="7fe42-159">Extensões do shell do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7fe42-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="7fe42-160">O App-V 5,0 SP2 agora oferece suporte a extensões do Shell.</span><span class="sxs-lookup"><span data-stu-id="7fe42-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="7fe42-161">Para obter mais informações, consulte a seção **suporte para extensão do shell do App-v 5.0 SP2** de [criação e gerenciamento de aplicativos virtualizados do app-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7fe42-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="7fe42-162">Atualizações da documentação do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7fe42-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="7fe42-163">O App-V 5,0 SP2 fornece documentação atualizada para os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="7fe42-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="7fe42-164">Migração de uma versão anterior</span><span class="sxs-lookup"><span data-stu-id="7fe42-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="7fe42-165">Sobre o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7fe42-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="7fe42-166">[Sobre relatórios do App-V 5,0](about-app-v-50-reporting.md) (seção de perguntas frequentes)</span><span class="sxs-lookup"><span data-stu-id="7fe42-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="7fe42-167">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="7fe42-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="7fe42-168">O App-V 5,0 é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="7fe42-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="7fe42-169">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="7fe42-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="7fe42-170">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="7fe42-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="7fe42-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fe42-171">Related topics</span></span>


[<span data-ttu-id="7fe42-172">Notas de versão do App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fe42-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





