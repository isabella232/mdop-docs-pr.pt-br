---
title: Solução de problemas de operações
description: Solução de problemas de operações
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796075"
---
# <span data-ttu-id="4f356-103">Solução de problemas de operações</span><span class="sxs-lookup"><span data-stu-id="4f356-103">Operations Troubleshooting</span></span>


<span data-ttu-id="4f356-104">Este tópico inclui informações que você pode usar para ajudar a solucionar problemas operacionais gerais na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="4f356-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="4f356-105">Solucionando problemas em operações do MED-V</span><span class="sxs-lookup"><span data-stu-id="4f356-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="4f356-106">Veja a seguir alguns problemas que os usuários finais podem encontrar quando executarem o MED-V e soluções para ajudar a solucionar esses problemas:</span><span class="sxs-lookup"><span data-stu-id="4f356-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="4f356-107">**Falha no redirecionamento da documentação**.</span><span class="sxs-lookup"><span data-stu-id="4f356-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="4f356-108">Geralmente, esse problema ocorre quando a pasta meus documentos de um usuário final aponta para um local de rede.</span><span class="sxs-lookup"><span data-stu-id="4f356-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="4f356-109">O Windows não dá suporte à criação de um compartilhamento de outra pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="4f356-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="4f356-110">Quando uma unidade ou pasta é redirecionada para o convidado, o RDP\\Windows Virtual PC cria um compartilhamento para essa pasta.</span><span class="sxs-lookup"><span data-stu-id="4f356-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="4f356-111">Portanto, se a pasta meus documentos do host já estiver apontando para um compartilhamento, o RDP\\Windows Virtual PC não poderá criar um compartilhamento de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="4f356-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="4f356-112">Outra causa possível desse problema é que as credenciais necessárias para se conectar ao recurso de rede podem ser diferentes das credenciais de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="4f356-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="4f356-113">O MED-V pode estar detectando que os documentos são redirecionados no host, envie essas informações para o convidado e, em seguida, tente reconectar o recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="4f356-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="4f356-114">Se as credenciais do usuário não forem autenticadas, o MED-V pode parar de tentar autenticar.</span><span class="sxs-lookup"><span data-stu-id="4f356-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="4f356-115">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-115">Solution</span></span>**

<span data-ttu-id="4f356-116">Para solucionar esse problema, tente um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="4f356-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="4f356-117">Defina o diretório raiz do usuário dentro do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f356-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="4f356-118">O convidado e o host devem, então, se conectar ao mesmo recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="4f356-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="4f356-119">Em vez de redirecionar a pasta meus documentos para um caminho UNC, mapeie-a para uma letra de unidade (no host, mapeie uma unidade que aponte para o recurso de rede).</span><span class="sxs-lookup"><span data-stu-id="4f356-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="4f356-120">A pasta meus documentos pode ser definida para usar a letra da unidade em vez do caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="4f356-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="4f356-121">O convidado será redirecionado para essa mesma unidade mapeada conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="4f356-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="4f356-122">Crie um script de inicialização no convidado que redireciona a pasta meus documentos para o recurso de rede e fornece credenciais adicionais conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="4f356-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="4f356-123">**Falha no redirecionamento de URL**.</span><span class="sxs-lookup"><span data-stu-id="4f356-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="4f356-124">Uma URL que você especificou para o redirecionamento do host para o convidado não é redirecionada conforme o esperado ou está retornando uma mensagem de erro indicando que o site não existe.</span><span class="sxs-lookup"><span data-stu-id="4f356-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="4f356-125">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-125">Solution</span></span>**

<span data-ttu-id="4f356-126">Esse erro pode ocorrer quando há um uso incorreto de caracteres, como asterisco (\ \*), nas informações de redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="4f356-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="4f356-127">Verifique o valor do registro para redirecionamento de URL e corrija os erros.</span><span class="sxs-lookup"><span data-stu-id="4f356-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="4f356-128">A chave do registro é chamada `RedirectUrls` e geralmente está localizada em:</span><span class="sxs-lookup"><span data-stu-id="4f356-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="4f356-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="4f356-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="4f356-130">**Ícone na barra de tarefas enganosa**.</span><span class="sxs-lookup"><span data-stu-id="4f356-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="4f356-131">Por padrão, o ícone que aparece na barra de tarefas de um usuário final para aplicativos publicados e URLs redirecionadas é o ícone do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="4f356-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="4f356-132">Se um usuário final não reconhece esse comportamento padrão, ele pode ficar confuso ao olhar na barra de tarefas para localizar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f356-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="4f356-133">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-133">Solution</span></span>**

<span data-ttu-id="4f356-134">A única maneira de evitar esse comportamento padrão é alterar as configurações do usuário para as propriedades da barra de tarefas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4f356-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="4f356-135">Clique com o botão direito do mouse na barra de tarefas e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="4f356-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="4f356-136">Na caixa de diálogo **Propriedades da barra de tarefas e do menu iniciar** , clique na guia **barra de tarefas** .</span><span class="sxs-lookup"><span data-stu-id="4f356-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="4f356-137">Na barra suspensa da caixa de botões da **barra de tarefas** , selecione **nunca combinar**.</span><span class="sxs-lookup"><span data-stu-id="4f356-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="4f356-138">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f356-138">Click **OK**.</span></span>

<span data-ttu-id="4f356-139">Os ícones esperados para aplicativos publicados e URLs redirecionadas são exibidos.</span><span class="sxs-lookup"><span data-stu-id="4f356-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="4f356-140">**Aviso emitido se o segundo usuário tentar fazer logon ou se a máquina virtual estiver em uso**.</span><span class="sxs-lookup"><span data-stu-id="4f356-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="4f356-141">Uma mensagem de aviso é emitida quando um segundo usuário se conecta a um espaço de trabalho do MED-V enquanto um primeiro usuário ainda está executando o MED-V.</span><span class="sxs-lookup"><span data-stu-id="4f356-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="4f356-142">O aviso também será emitido se MED-V for iniciado enquanto a máquina virtual estiver sendo usada, por exemplo, se a máquina virtual tiver sido iniciada por meio do PC virtual do Windows no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="4f356-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="4f356-143">Quando o usuário final aceita a mensagem de aviso, o MED-V é desligado.</span><span class="sxs-lookup"><span data-stu-id="4f356-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="4f356-144">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-144">Solution</span></span>**

<span data-ttu-id="4f356-145">Um usuário final deve verificar se todos os outros usuários fazem logoff do MED-V antes de tentarem fazer logon.</span><span class="sxs-lookup"><span data-stu-id="4f356-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="4f356-146">Isso garante que nenhuma outra instância do MED-V esteja em execução e que o computador virtual do Windows não esteja no controle da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4f356-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="4f356-147">**Bipes ouvidos durante a primeira configuração**.</span><span class="sxs-lookup"><span data-stu-id="4f356-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="4f356-148">Ocasionalmente, os bipes são ouvidos enquanto o MED-V estiver sendo executado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="4f356-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="4f356-149">Isso pode ser confuso para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="4f356-149">This can be confusing to an end user.</span></span> <span data-ttu-id="4f356-150">Os bipes estão originários da máquina virtual quando executam determinadas ações, como desligar.</span><span class="sxs-lookup"><span data-stu-id="4f356-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="4f356-151">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-151">Solution</span></span>**

<span data-ttu-id="4f356-152">Você pode interromper o serviço de bipe especificando o comando "net stop beep" no início de cada sequência de início de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4f356-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="4f356-153">Ou você pode desativar o serviço de bipe especificando o comando "sc config beep start = disabled".</span><span class="sxs-lookup"><span data-stu-id="4f356-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="4f356-154">Você pode especificar esses comandos antes de lacrar a imagem ou como parte do Sysprep.</span><span class="sxs-lookup"><span data-stu-id="4f356-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="4f356-155">**Várias conexões de rede criadas para os espaços de trabalho do MED-V no modo de ponte**.</span><span class="sxs-lookup"><span data-stu-id="4f356-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="4f356-156">Se a primeira configuração estiver criando um espaço de trabalho do MED-V configurado para o modo NAT, ele somente criará uma única conexão de rede no PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f356-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="4f356-157">No entanto, se a primeira configuração estiver criando um espaço de trabalho do MED-V configurado para o modo de ponte, ele criará uma conexão de rede separada para cada adaptador de rede instalado no computador, pois o MED-V não pode determinar qual adaptador de rede está ativo.</span><span class="sxs-lookup"><span data-stu-id="4f356-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="4f356-158">Isso também garante que os usuários móveis sempre tenham um adaptador de rede disponível para conexões com fio e sem fio.</span><span class="sxs-lookup"><span data-stu-id="4f356-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="4f356-159">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-159">Solution</span></span>**

<span data-ttu-id="4f356-160">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="4f356-160">None.</span></span>

<span data-ttu-id="4f356-161">O **aplicativo MED-V não responde por muito tempo durante o fechamento**.</span><span class="sxs-lookup"><span data-stu-id="4f356-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="4f356-162">Em alguns casos, um aplicativo MED-V pára de responder quando está tentando fechar.</span><span class="sxs-lookup"><span data-stu-id="4f356-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="4f356-163">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-163">Solution</span></span>**

<span data-ttu-id="4f356-164">Você pode especificar o período de tempo que o MED-V aguarda para fechar aplicativos que não respondem definindo a chave do registro WaitToKillAppTimeout na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="4f356-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="4f356-165">Para obter mais informações, consulte [como aumentar o tempo de desligamento para que os processos possam ser encerrados corretamente no Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="4f356-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="4f356-166">A **renomeação de um atalho de aplicativo publicado na máquina virtual convidada não altera o nome publicado no host**.</span><span class="sxs-lookup"><span data-stu-id="4f356-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="4f356-167">Quando você publica um aplicativo Criando um atalho e, em seguida, renomeia o atalho na máquina virtual convidada, o nome do aplicativo original permanece no menu de **início** do host.</span><span class="sxs-lookup"><span data-stu-id="4f356-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="4f356-168">O programa continua a ser executado conforme o esperado, no entanto, o programa sempre manterá o nome original.</span><span class="sxs-lookup"><span data-stu-id="4f356-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="4f356-169">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-169">Solution</span></span>**

<span data-ttu-id="4f356-170">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="4f356-170">None.</span></span> <span data-ttu-id="4f356-171">Esse é um comportamento conhecido do PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f356-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="4f356-172">**Mover um atalho na máquina virtual convidada não atualiza o local no menu Iniciar do computador host**.</span><span class="sxs-lookup"><span data-stu-id="4f356-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="4f356-173">Os atalhos do aplicativo MED-V publicados no menu **Iniciar** do computador host são catalogados no registro.</span><span class="sxs-lookup"><span data-stu-id="4f356-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="4f356-174">Se você mover um atalho do aplicativo para uma subpasta, o registro não será atualizado para refletir a alteração.</span><span class="sxs-lookup"><span data-stu-id="4f356-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="4f356-175">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-175">Solution</span></span>**

<span data-ttu-id="4f356-176">Siga estas etapas para alterar o local de um atalho do aplicativo MED-V:</span><span class="sxs-lookup"><span data-stu-id="4f356-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="4f356-177">Quando o MED-V estiver em execução, abra o Windows Explorer na máquina virtual de convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4f356-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="4f356-178">Navegue até o diretório "%ALLUSERSPROFILE%\\Start Menu\\Programs".</span><span class="sxs-lookup"><span data-stu-id="4f356-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="4f356-179">Mova os atalhos do aplicativo para fora das pastas StartMenu ou programas.</span><span class="sxs-lookup"><span data-stu-id="4f356-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="4f356-180">Após cerca de 30 segundos, valide se os atalhos foram removidos do menu **Iniciar** do computador host.</span><span class="sxs-lookup"><span data-stu-id="4f356-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="4f356-181">Mova os atalhos do aplicativo de volta para as novas pastas do programa no diretório inicial do Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="4f356-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="4f356-182">Após cerca de 30 segundos, valide se os atalhos são atualizados no menu **Iniciar** do computador host.</span><span class="sxs-lookup"><span data-stu-id="4f356-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="4f356-183">**Aplicativos publicados podem expirar após ficar ocioso**.</span><span class="sxs-lookup"><span data-stu-id="4f356-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="4f356-184">Em alguns casos, os aplicativos publicados expirarão se ficarão inativos por algum tempo.</span><span class="sxs-lookup"><span data-stu-id="4f356-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="4f356-185">Essa situação ocorre apenas se o IPsec estiver habilitado e o espaço de trabalho do MED-V estiver configurado para o modo NAT.</span><span class="sxs-lookup"><span data-stu-id="4f356-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="4f356-186">Essa situação não ocorrerá se estiver em execução no modo de ponte.</span><span class="sxs-lookup"><span data-stu-id="4f356-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="4f356-187">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-187">Solution</span></span>**

<span data-ttu-id="4f356-188">Desative o IPsec quando você estiver executando o espaço de trabalho do MED-V no modo NAT.</span><span class="sxs-lookup"><span data-stu-id="4f356-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="4f356-189">**Fixar um aplicativo publicado na barra de tarefas ignora o MED-V**.</span><span class="sxs-lookup"><span data-stu-id="4f356-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="4f356-190">Se um usuário final fixar um aplicativo publicado na barra de tarefas e, em seguida, fechar o aplicativo, o MED-V será ignorado na próxima vez que o aplicativo for aberto no ícone da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4f356-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="4f356-191">Em vez disso, o aplicativo é aberto diretamente em uma janela do VMSAL.</span><span class="sxs-lookup"><span data-stu-id="4f356-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="4f356-192">Solução</span><span class="sxs-lookup"><span data-stu-id="4f356-192">Solution</span></span>**

<span data-ttu-id="4f356-193">Não fixe os aplicativos publicados no MED-V à barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4f356-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="4f356-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f356-194">Related topics</span></span>


[<span data-ttu-id="4f356-195">Práticas recomendadas de segurança para operações da MED-V</span><span class="sxs-lookup"><span data-stu-id="4f356-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="4f356-196">Solução de problemas de implantação</span><span class="sxs-lookup"><span data-stu-id="4f356-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





