---
title: SFTTRAY Referência de comandos
description: SFTTRAY Referência de comandos
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796708"
---
# <span data-ttu-id="f79e8-103">SFTTRAY Referência de comandos</span><span class="sxs-lookup"><span data-stu-id="f79e8-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="f79e8-104">O aplicativo da bandeja do cliente do Microsoft Application Virtualization (App-V), sfttray.exe, é o principal elemento de interface do usuário do cliente App-V com o qual os usuários irão interagir durante o uso normal.</span><span class="sxs-lookup"><span data-stu-id="f79e8-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="f79e8-105">Este programa controla o streaming e a inicialização de todos os aplicativos virtuais e é acessado clicando com o botão direito do mouse no ícone exibido na área de notificação para exibir o menu de funções do cliente.</span><span class="sxs-lookup"><span data-stu-id="f79e8-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="f79e8-106">O menu permite que o usuário carregue aplicativos, inicie uma atualização de publicação, cancele uma solicitação ou altere o cliente para o modo offline.</span><span class="sxs-lookup"><span data-stu-id="f79e8-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="f79e8-107">O usuário também pode fechar o aplicativo da bandeja cliente do aplicativo virtualização e todos os aplicativos ativos clicando em **sair**.</span><span class="sxs-lookup"><span data-stu-id="f79e8-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="f79e8-108">Por padrão, o ícone é exibido sempre que um aplicativo virtual é iniciado, embora você possa controlar esse comportamento usando comandos SFTTRAY.</span><span class="sxs-lookup"><span data-stu-id="f79e8-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="f79e8-109">O aplicativo de bandeja do cliente do Application Virtualization também exibe uma barra de progresso para cada aplicativo que é iniciado, bem como mensagens de status sobre aplicativos ativos.</span><span class="sxs-lookup"><span data-stu-id="f79e8-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="f79e8-110">Clicar na barra de progresso exibe uma mensagem que permite que você cancele o carregamento ou o início de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f79e8-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="f79e8-111">Comandos SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="f79e8-111">SFTTRAY Commands</span></span>


<span data-ttu-id="f79e8-112">A lista de comandos e opções de linha de comando pode ser exibida executando o seguinte comando em uma janela de comando.</span><span class="sxs-lookup"><span data-stu-id="f79e8-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="f79e8-113">Observação</span><span class="sxs-lookup"><span data-stu-id="f79e8-113">Note</span></span>**  
<span data-ttu-id="f79e8-114">Há apenas uma instância de bandeja de cliente do aplicativo virtualização para cada contexto de usuário, portanto, se você iniciar um novo comando SFTTRAY, ele será passado para o programa que já está em execução.</span><span class="sxs-lookup"><span data-stu-id="f79e8-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="f79e8-115">Uso de comandos</span><span class="sxs-lookup"><span data-stu-id="f79e8-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="f79e8-116">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="f79e8-116">Command-Line Switches</span></span>

<span data-ttu-id="f79e8-117">As opções de linha de comando SFTTRAY estão descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f79e8-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f79e8-118">Opção</span><span class="sxs-lookup"><span data-stu-id="f79e8-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="f79e8-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f79e8-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f79e8-120">/HIDE</span><span class="sxs-lookup"><span data-stu-id="f79e8-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-121">Oculta o ícone do SFTTRAY na área de notificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="f79e8-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f79e8-122">/SHOW</span><span class="sxs-lookup"><span data-stu-id="f79e8-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-123">Exibe o ícone do SFTTRAY na área de notificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="f79e8-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f79e8-124">/QUIET</span><span class="sxs-lookup"><span data-stu-id="f79e8-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-125">Oferece suporte ao uso autônomo impedindo que erros exibam caixas de mensagens que exijam confirmação de usuário.</span><span class="sxs-lookup"><span data-stu-id="f79e8-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f79e8-126">/EXE &lt; alternativo-exe&gt;</span><span class="sxs-lookup"><span data-stu-id="f79e8-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-127">Usado com/LAUNCH para especificar que um programa executável deve ser iniciado no ambiente virtual quando um aplicativo virtual é iniciado no lugar do arquivo de destino especificado no OSD.</span><span class="sxs-lookup"><span data-stu-id="f79e8-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f79e8-128">Observação</span><span class="sxs-lookup"><span data-stu-id="f79e8-128">Note</span></span></strong><br/><p><span data-ttu-id="f79e8-129">Por exemplo, use "SFTTRAY.EXE/EXE REGEDIT.EXE aplicativo de/LAUNCH &lt; &gt; " para permitir que você examine o registro do ambiente virtual no qual o aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="f79e8-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f79e8-130">&lt;Aplicativo/Launch &gt; [ &lt; args &gt; ]</span><span class="sxs-lookup"><span data-stu-id="f79e8-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-131">Inicia um aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="f79e8-131">Starts a virtual application.</span></span> <span data-ttu-id="f79e8-132">Especifique o nome e a versão de um aplicativo ou o caminho para um arquivo OSD.</span><span class="sxs-lookup"><span data-stu-id="f79e8-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="f79e8-133">Opcionalmente, argumentos de linha de comando podem ser passados para o aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="f79e8-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f79e8-134">Observação</span><span class="sxs-lookup"><span data-stu-id="f79e8-134">Note</span></span></strong><br/><p><span data-ttu-id="f79e8-135">Use o comando "SFTMIME.EXE/QUERY OBJ: APP/SHORT" para obter uma lista dos nomes e versões dos aplicativos virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f79e8-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f79e8-136">/LOAD</span><span class="sxs-lookup"><span data-stu-id="f79e8-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-137">Carrega ou importa um aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="f79e8-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f79e8-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="f79e8-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-139">Carrega todos os aplicativos no cache.</span><span class="sxs-lookup"><span data-stu-id="f79e8-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f79e8-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="f79e8-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-141">Inicia uma atualização de publicação para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f79e8-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f79e8-142">&lt;ID exclusiva do/LAUNCHRESULT&gt;</span><span class="sxs-lookup"><span data-stu-id="f79e8-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-143">Retorna o código do resultado do lançamento para o processo que inicia sfttray.exe usando um evento global e um arquivo mapeado na memória que se baseia no nome raiz especificado para o ID exclusivo. ¹</span><span class="sxs-lookup"><span data-stu-id="f79e8-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f79e8-144">&lt;SFT/SFTFILE&gt;</span><span class="sxs-lookup"><span data-stu-id="f79e8-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-145">Opção opcional usada com/LOAD para especificar o caminho para o arquivo SFT do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f79e8-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="f79e8-146">Se especificado, o aplicativo será importado em vez de ser carregado.</span><span class="sxs-lookup"><span data-stu-id="f79e8-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f79e8-147">/EXIT</span><span class="sxs-lookup"><span data-stu-id="f79e8-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f79e8-148">Fecha o programa SFTTRAY e todos os aplicativos virtuais ativos e remove o ícone da área de notificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="f79e8-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f79e8-149">Observação</span><span class="sxs-lookup"><span data-stu-id="f79e8-149">Note</span></span>**  
<span data-ttu-id="f79e8-150">¹ o parâmetro de linha de comando */LAUNCHRESULT* fornece um meio para o processo que inicia sfttray.exe para especificar o nome raiz para um evento global e um arquivo de memória mapeada que são usados para retornar o código do resultado do lançamento para o processo.</span><span class="sxs-lookup"><span data-stu-id="f79e8-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="f79e8-151">O nome do identificador exclusivo deve começar com "SFT-" para impedir que o nome do evento seja virtualizado quando o processo de inicialização for invocado dentro de um ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="f79e8-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="f79e8-152">A região mapeada na memória terá 64 bits em tamanho.</span><span class="sxs-lookup"><span data-stu-id="f79e8-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="f79e8-153">Para usar esse parâmetro, o processo de inicialização cria um evento com o nome " &lt; identificação exclusiva &gt; -resultado \ _event", um arquivo mapeado na memória com o nome " &lt; identificação exclusiva &gt; -resultado \ _value" e, opcionalmente, um evento com o nome " &lt; identificação exclusiva &gt; -Shutdown \ _event" e, em seguida, o processo de inicialização inicia sfttray.exe e aguarda o evento ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="f79e8-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="f79e8-154">Após o evento " &lt; ID exclusivo &gt; -resultado \ _event" ser sinalizado, o processo de inicialização recupera o código de retorno de 64 bits da região mapeada na memória.</span><span class="sxs-lookup"><span data-stu-id="f79e8-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="f79e8-155">Se o evento opcional " &lt; ID exclusiva &gt; -shutdown \ _event" existir quando o aplicativo virtual sair, sfttray.exe abrir e sinalizar o evento.</span><span class="sxs-lookup"><span data-stu-id="f79e8-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="f79e8-156">O processo de inicialização aguardará nesse evento de desligamento se precisar determinar quando o aplicativo virtual será encerrado.</span><span class="sxs-lookup"><span data-stu-id="f79e8-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











