---
title: Mensagens do log de eventos da MED-V
description: Mensagens do log de eventos da MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799200"
---
# <span data-ttu-id="c1ee9-103">Mensagens do log de eventos da MED-V</span><span class="sxs-lookup"><span data-stu-id="c1ee9-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="c1ee9-104">Os arquivos de log para o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 fornecem informações detalhadas sobre como implantar e gerenciar o MED-V na sua empresa e ajudar a verificar a funcionalidade ou ajudar a solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="c1ee9-105">IDs de evento</span><span class="sxs-lookup"><span data-stu-id="c1ee9-105">Event IDs</span></span>


<span data-ttu-id="c1ee9-106">Veja a seguir uma lista de IDs de eventos do MED-V para ajudar a solucionar problemas que podem ocorrer ao implantar ou gerenciar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="c1ee9-107">Fts</span><span class="sxs-lookup"><span data-stu-id="c1ee9-107">Fts</span></span>

<span data-ttu-id="c1ee9-108">Mostra as identificações de eventos da primeira configuração de hora.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="c1ee9-109">IDENTIFICAÇÃO do evento 3066</span><span class="sxs-lookup"><span data-stu-id="c1ee9-109">Event ID 3066</span></span>

<span data-ttu-id="c1ee9-110">Falha na operação iniciar máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-111">Description</span></span>**  
<span data-ttu-id="c1ee9-112">Há um problema potencial com o disco rígido virtual (VHD) que você está usando para criar um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-113">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-113">Solution</span></span>**  
<span data-ttu-id="c1ee9-114">Verifique se você pode criar uma máquina virtual com o VHD do MED-V e que ela possa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="c1ee9-115">IDENTIFICAÇÃO do evento 3071</span><span class="sxs-lookup"><span data-stu-id="c1ee9-115">Event ID 3071</span></span>

<span data-ttu-id="c1ee9-116">Falha na preparação da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-117">Description</span></span>**  
<span data-ttu-id="c1ee9-118">Ocorreu um problema com uma configuração de primeira vez que pode ter sido causada por muitos problemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="c1ee9-119">Isso inclui problemas com a conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-120">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-120">Solution</span></span>**  
<span data-ttu-id="c1ee9-121">Reinicie o agente do host do MED-V para executar a instalação novamente pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="c1ee9-122">IDENTIFICAÇÃO do evento 3078</span><span class="sxs-lookup"><span data-stu-id="c1ee9-122">Event ID 3078</span></span>

<span data-ttu-id="c1ee9-123">Falha na preparação da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-124">Description</span></span>**  
<span data-ttu-id="c1ee9-125">Há um problema potencial com o VHD que você está usando para criar um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-126">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-126">Solution</span></span>**  
<span data-ttu-id="c1ee9-127">Verifique se você pode criar uma máquina virtual com o VHD do MED-V e que ela possa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="c1ee9-128">IDENTIFICAÇÃO do evento 3079</span><span class="sxs-lookup"><span data-stu-id="c1ee9-128">Event ID 3079</span></span>

<span data-ttu-id="c1ee9-129">Tentando preparar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-130">Description</span></span>**  
<span data-ttu-id="c1ee9-131">O MED-V está tentando preparar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-132">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-132">Solution</span></span>**  
<span data-ttu-id="c1ee9-133">Nenhuma ação é necessária.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-133">No action is required.</span></span> <span data-ttu-id="c1ee9-134">Na primeira vez que a configuração é concluída.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-134">Let first time setup finish.</span></span>

### <span data-ttu-id="c1ee9-135">IDENTIFICAÇÃO do evento 3080</span><span class="sxs-lookup"><span data-stu-id="c1ee9-135">Event ID 3080</span></span>

<span data-ttu-id="c1ee9-136">O cliente foi interrompido ao preparar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-137">Description</span></span>**  
<span data-ttu-id="c1ee9-138">O MED-V é interrompido inesperadamente quando ele tenta preparar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-139">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-139">Solution</span></span>**  
<span data-ttu-id="c1ee9-140">Iniciar o agente de host do MED-V e concluir a configuração da primeira vez</span><span class="sxs-lookup"><span data-stu-id="c1ee9-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="c1ee9-141">IDENTIFICAÇÃO do evento 3084</span><span class="sxs-lookup"><span data-stu-id="c1ee9-141">Event ID 3084</span></span>

<span data-ttu-id="c1ee9-142">A máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-142">Virtual machine is not valid.</span></span> <span data-ttu-id="c1ee9-143">Na primeira vez que a instalação precisa ser executada novamente.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-144">Description</span></span>**  
<span data-ttu-id="c1ee9-145">O agente de host do MED-V detectou um problema com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-146">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-146">Solution</span></span>**  
<span data-ttu-id="c1ee9-147">Nenhuma ação é necessária.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-147">No action is required.</span></span> <span data-ttu-id="c1ee9-148">Na primeira vez que a configuração é concluída.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-148">Let first time setup finish.</span></span>

### <span data-ttu-id="c1ee9-149">IDENTIFICAÇÃO do evento 3099</span><span class="sxs-lookup"><span data-stu-id="c1ee9-149">Event ID 3099</span></span>

<span data-ttu-id="c1ee9-150">Falha na chamada para iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-151">Description</span></span>**  
<span data-ttu-id="c1ee9-152">Há um problema potencial com o VHD que você está usando para criar um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-153">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-153">Solution</span></span>**  
<span data-ttu-id="c1ee9-154">Verifique se você pode criar uma máquina virtual com o VHD do MED-V e que ele possa ser aberto.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="c1ee9-155">Gerenciamento de VM</span><span class="sxs-lookup"><span data-stu-id="c1ee9-155">VM Management</span></span>

### <span data-ttu-id="c1ee9-156">IDENTIFICAÇÃO do evento 4022</span><span class="sxs-lookup"><span data-stu-id="c1ee9-156">Event ID 4022</span></span>

<span data-ttu-id="c1ee9-157">VMManagerException erro fatal durante a emissão do comando para a VM.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-158">Description</span></span>**  
<span data-ttu-id="c1ee9-159">O usuário final tentou sair do MED-V fazendo logoff ou desligando o host do MED-V, e a configuração de configuração do VMTaskTimeout foi excedida.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-160">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-160">Solution</span></span>**  
<span data-ttu-id="c1ee9-161">Reinicie o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-161">Restart MED-V.</span></span>

### <span data-ttu-id="c1ee9-162">IDENTIFICAÇÃO do evento 4028</span><span class="sxs-lookup"><span data-stu-id="c1ee9-162">Event ID 4028</span></span>

<span data-ttu-id="c1ee9-163">Tempo limite da operação da VM.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-164">Description</span></span>**  
<span data-ttu-id="c1ee9-165">O usuário final tentou sair do MED-V fazendo logoff ou desligando o host e a configuração de configuração do VMTaskTimeout foi excedida.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-166">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-166">Solution</span></span>**  
<span data-ttu-id="c1ee9-167">Reinicie o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-167">Restart MED-V.</span></span>

### <span data-ttu-id="c1ee9-168">IDENTIFICAÇÃO do evento 4038</span><span class="sxs-lookup"><span data-stu-id="c1ee9-168">Event ID 4038</span></span>

<span data-ttu-id="c1ee9-169">Vmsal postou uma mensagem de erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-170">Description</span></span>**  
<span data-ttu-id="c1ee9-171">Uma mensagem de erro é exibida para o usuário final informando que o MED-V não pôde iniciar o aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-172">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-172">Solution</span></span>**  
<span data-ttu-id="c1ee9-173">Se o erro for registrado duas ou mais vezes em uma linha, interrompa o MED-V e conecte-se à máquina virtual usando o console do Windows Virtual PC e tente iniciar o aplicativo em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="c1ee9-174">IDENTIFICAÇÃO do evento 4040</span><span class="sxs-lookup"><span data-stu-id="c1ee9-174">Event ID 4040</span></span>

<span data-ttu-id="c1ee9-175">Recycling Additions porque TerminalServices não está inicializado no convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-176">Description</span></span>**  
<span data-ttu-id="c1ee9-177">O MED-V reinicializou a máquina virtual porque os serviços de área de trabalho remota não foram inicializados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-178">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-178">Solution</span></span>**  
<span data-ttu-id="c1ee9-179">Se o erro for registrado duas ou mais vezes em uma linha, interrompa o MED-V e conecte-se à máquina virtual usando o console do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="c1ee9-180">IDENTIFICAÇÃO do evento 4042</span><span class="sxs-lookup"><span data-stu-id="c1ee9-180">Event ID 4042</span></span>

<span data-ttu-id="c1ee9-181">Falha ao reciclar adições no convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-182">Description</span></span>**  
<span data-ttu-id="c1ee9-183">O MED-V não pôde reciclar adições de máquina virtual na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-184">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-184">Solution</span></span>**  
<span data-ttu-id="c1ee9-185">Se o erro for registrado duas ou mais vezes em uma linha, interrompa o MED-V e conecte-se à máquina virtual usando o console do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="c1ee9-186">IDENTIFICAÇÃO do evento 4043</span><span class="sxs-lookup"><span data-stu-id="c1ee9-186">Event ID 4043</span></span>

<span data-ttu-id="c1ee9-187">Falha ao redefinir a senha expirada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-188">Description</span></span>**  
<span data-ttu-id="c1ee9-189">O usuário final não redefiniu a senha na máquina virtual antes de ela ter expirado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="c1ee9-190">Como resultado, o usuário pode não conseguir acessar os recursos da rede nem salvar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-191">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-191">Solution</span></span>**  
<span data-ttu-id="c1ee9-192">Desligue o MED-V Guest e reinicie-o.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="c1ee9-193">Redirecionamento de URL</span><span class="sxs-lookup"><span data-stu-id="c1ee9-193">URL Redirection</span></span>

### <span data-ttu-id="c1ee9-194">IDENTIFICAÇÃO do evento 5005</span><span class="sxs-lookup"><span data-stu-id="c1ee9-194">Event ID 5005</span></span>

<span data-ttu-id="c1ee9-195">Não foi possível obter o nome da VM da configuração; Não é possível iniciar o navegador convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-196">Description</span></span>**  
<span data-ttu-id="c1ee9-197">O redirecionamento de URL não pôde obter o nome do espaço de trabalho do MED-V na configuração.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="c1ee9-198">Como resultado, ele não pode informar ao PC virtual do Windows para abrir a URL redirecionada no navegador de espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-199">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-199">Solution</span></span>**  
<span data-ttu-id="c1ee9-200">Certifique-se de que o nome do espaço de trabalho do MED-V esteja definido e que ele corresponda a um nome de máquina virtual no &lt; *user* &gt; diretório de computadores \\Virtual usuários do C:\\Users\\.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="c1ee9-201">O nome do espaço de trabalho do MED-V está localizado em HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="c1ee9-202">Por exemplo, se o usuário for "Matt" e o nome do espaço de trabalho for "mattsworkspace", o valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve ser "mattsworkspace", e deve haver um arquivo chamado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="c1ee9-203">IDENTIFICAÇÃO do evento 5006</span><span class="sxs-lookup"><span data-stu-id="c1ee9-203">Event ID 5006</span></span>

<span data-ttu-id="c1ee9-204">Falha ao criar servidor de pipe.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-205">Description</span></span>**  
<span data-ttu-id="c1ee9-206">O serviço de redirecionamento de URL não pôde criar o servidor de pipe para se comunicar com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-207">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-207">Solution</span></span>**  
<span data-ttu-id="c1ee9-208">Verifique os logs de eventos do sistema para tentar criar um arquivo ou um recurso cujo caminho comece semelhante ao seguinte: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" e termina com o nome de usuário e o nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="c1ee9-209">Se isso não estiver presente no log de eventos, reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="c1ee9-210">ConfigMgr (convidado)</span><span class="sxs-lookup"><span data-stu-id="c1ee9-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="c1ee9-211">IDENTIFICAÇÃO do evento 7001</span><span class="sxs-lookup"><span data-stu-id="c1ee9-211">Event ID 7001</span></span>

<span data-ttu-id="c1ee9-212">Os dados de configuração de rede do host não estão formatados corretamente.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-213">Description</span></span>**  
<span data-ttu-id="c1ee9-214">A configuração de rede recebida do host é uma cadeia de caracteres XML formatada incorretamente ou as informações de rede retornadas do host não podem ser gravadas em um documento XML.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-215">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-215">Solution</span></span>**  
<span data-ttu-id="c1ee9-216">Reinicie o computador host e a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="c1ee9-217">IDENTIFICAÇÃO do evento 7005</span><span class="sxs-lookup"><span data-stu-id="c1ee9-217">Event ID 7005</span></span>

<span data-ttu-id="c1ee9-218">Uma alteração na configuração de rede do host foi detectada, mas não pôde ser aplicada porque os dados de configuração de rede do host não estavam formatados corretamente.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-219">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-219">Description</span></span>**  
<span data-ttu-id="c1ee9-220">Uma alteração na configuração de rede do host foi comunicada à máquina virtual, mas não foi possível processá-la na máquina virtual devido a um erro.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="c1ee9-221">Esse erro pode ser causado por dados formatados incorretamente ou pela incapacidade de definir as informações na instância CCMNetworkAdapter da instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c1ee9-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-222">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-222">Solution</span></span>**  
<span data-ttu-id="c1ee9-223">Reinicie o host e a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="c1ee9-224">ConfigMgr (host)</span><span class="sxs-lookup"><span data-stu-id="c1ee9-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="c1ee9-225">IDENTIFICAÇÃO do evento 8006</span><span class="sxs-lookup"><span data-stu-id="c1ee9-225">Event ID 8006</span></span>

<span data-ttu-id="c1ee9-226">Não é possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-227">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-227">Description</span></span>**  
<span data-ttu-id="c1ee9-228">O Windows Virtual PC 7 não consegue localizar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="c1ee9-229">A máquina virtual pode ter sido excluída, movida, removida ou o acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-230">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-230">Solution</span></span>**  
<span data-ttu-id="c1ee9-231">Reinstale a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="c1ee9-232">IDENTIFICAÇÃO do evento 8008</span><span class="sxs-lookup"><span data-stu-id="c1ee9-232">Event ID 8008</span></span>

<span data-ttu-id="c1ee9-233">As informações de configuração de rede da estação de trabalho não puderam ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-234">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-234">Description</span></span>**  
<span data-ttu-id="c1ee9-235">As informações de configuração de rede não puderam ser coletadas do host do MED-V, provavelmente devido a uma falha na chamada do sistema no .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="c1ee9-236">Essa falha também pode ocorrer se as informações de rede retornadas do host MED-V não puderem ser gravadas em um documento XML.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-237">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-237">Solution</span></span>**  
<span data-ttu-id="c1ee9-238">Reinicie a estação de trabalho host.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-238">Restart the host workstation.</span></span>

### <span data-ttu-id="c1ee9-239">IDENTIFICAÇÃO do evento 8010</span><span class="sxs-lookup"><span data-stu-id="c1ee9-239">Event ID 8010</span></span>

<span data-ttu-id="c1ee9-240">Os dados de configuração de rede não puderam ser definidos na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-241">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-241">Description</span></span>**  
<span data-ttu-id="c1ee9-242">A conversão de endereços (NAT) do MED-V hostnetwork (NAT) não pôde ser comunicada à máquina virtual, provavelmente porque a máquina virtual está em um estado incorreto ou o Windows Virtual PC Additions não foi instalado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-243">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-243">Solution</span></span>**  
<span data-ttu-id="c1ee9-244">Desligue e reinicie a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="c1ee9-245">Além disso, talvez seja necessário reinstalar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="c1ee9-246">IDENTIFICAÇÃO do evento 8011</span><span class="sxs-lookup"><span data-stu-id="c1ee9-246">Event ID 8011</span></span>

<span data-ttu-id="c1ee9-247">Não foi possível redefinir os dados de configuração de rede na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-248">Description</span></span>**  
<span data-ttu-id="c1ee9-249">A configuração hostnetwork do MED-V (com ponte) não pôde ser comunicada à máquina virtual, provavelmente porque a máquina virtual está em um estado incorreto ou o Windows Virtual PC Additions não foi instalado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-250">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-250">Solution</span></span>**  
<span data-ttu-id="c1ee9-251">Desligue e reinicie a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="c1ee9-252">Além disso, talvez seja necessário reinstalar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="c1ee9-253">Redirecionamento de impressora</span><span class="sxs-lookup"><span data-stu-id="c1ee9-253">Printer Redirection</span></span>

### <span data-ttu-id="c1ee9-254">IDENTIFICAÇÃO do evento 9001</span><span class="sxs-lookup"><span data-stu-id="c1ee9-254">Event ID 9001</span></span>

<span data-ttu-id="c1ee9-255">Erro de permissão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-256">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-256">Description</span></span>**  
<span data-ttu-id="c1ee9-257">O usuário final não está autorizado a acessar a pasta necessária para abrir ou criar o arquivo da impressora MED-V para leitura.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-258">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-258">Solution</span></span>**  
<span data-ttu-id="c1ee9-259">Verifique se o caminho User\\AppData\\ pode ser acessado e se o usuário tem permissão para ler e gravar nele.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="c1ee9-260">Por exemplo, se o usuário for "Matt", o caminho C:\\Users\\Matt\\AppData\\, e todos os arquivos contidos deverão ter permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="c1ee9-261">E, se existir, o caminho C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="c1ee9-262">IDENTIFICAÇÃO do evento 9002</span><span class="sxs-lookup"><span data-stu-id="c1ee9-262">Event ID 9002</span></span>

<span data-ttu-id="c1ee9-263">Erro de permissão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-264">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-264">Description</span></span>**  
<span data-ttu-id="c1ee9-265">O usuário final não está autorizado a acessar a pasta necessária para abrir ou criar o arquivo da impressora MED-V para gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-266">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-266">Solution</span></span>**  
<span data-ttu-id="c1ee9-267">Verifique se o caminho User\\AppData\\ pode ser acessado e se o usuário tem permissão para lê-lo e escrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="c1ee9-268">Por exemplo, se o usuário for "Matt", o caminho C:\\Users\\Matt\\AppData\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="c1ee9-269">E, se existir, o caminho C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="c1ee9-270">IDENTIFICAÇÃO do evento 9004</span><span class="sxs-lookup"><span data-stu-id="c1ee9-270">Event ID 9004</span></span>

<span data-ttu-id="c1ee9-271">Não foi possível criar o caminho para armazenar arquivos de impressora MEDV.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-272">Description</span></span>**  
<span data-ttu-id="c1ee9-273">O serviço de redirecionamento de impressora não pôde acessar arquivos ou criar diretórios necessários para armazenar as informações da impressora.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-274">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-274">Solution</span></span>**  
<span data-ttu-id="c1ee9-275">Verifique se o caminho User\\AppData\\ pode ser acessado e se o usuário tem permissão para ler e gravar nele.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="c1ee9-276">Por exemplo, se o usuário for "Matt", o caminho C:\\Users\\Matt\\AppData\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="c1ee9-277">E, se existir, o caminho C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="c1ee9-278">IDENTIFICAÇÃO do evento 9005</span><span class="sxs-lookup"><span data-stu-id="c1ee9-278">Event ID 9005</span></span>

<span data-ttu-id="c1ee9-279">Não foi possível obter o nome da VM da configuração; Não é possível iniciar o instalador convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="c1ee9-280">Não é possível atualizar o MED-V – nenhuma rede de host detectada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-281">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-281">Description</span></span>**  
<span data-ttu-id="c1ee9-282">O serviço de redirecionamento de impressora não pôde obter o nome do espaço de trabalho do MED-V na configuração do MED-V e não pode informar ao PC virtual do Windows para iniciar o instalador no MED-V Guest.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-283">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-283">Solution</span></span>**  
<span data-ttu-id="c1ee9-284">Certifique-se de que o nome do espaço de trabalho do MED-V esteja definido e que ele corresponda a um nome de máquina virtual no &lt; *user* &gt; diretório de computadores \\Virtual usuários do C:\\Users\\.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="c1ee9-285">O nome do espaço de trabalho do MED-V está localizado em HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="c1ee9-286">Por exemplo, se o usuário for "Matt" e o nome do espaço de trabalho for "mattsworkspace", o valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve ser "mattsworkspace" e deve haver um arquivo chamado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="c1ee9-287">Publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c1ee9-287">Application Publishing</span></span>

### <span data-ttu-id="c1ee9-288">IDENTIFICAÇÃO do evento 10015</span><span class="sxs-lookup"><span data-stu-id="c1ee9-288">Event ID 10015</span></span>

<span data-ttu-id="c1ee9-289">Ocorreu um erro no sistema de arquivos durante o processo de reconciliação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="c1ee9-290">O processo de reconciliação não processará o &lt; *nome* do arquivo &gt; , mas continuará processando outras alterações.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-291">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-291">Description</span></span>**  
<span data-ttu-id="c1ee9-292">Ocorreu um erro de acesso não autorizado ou de e/s ao criar ou excluir um atalho.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-293">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-293">Solution</span></span>**  
<span data-ttu-id="c1ee9-294">Verifique se o caminho do arquivo pode ser acessado e se o usuário tem permissões para criar ou excluir o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="c1ee9-295">IDENTIFICAÇÃO do evento 10021</span><span class="sxs-lookup"><span data-stu-id="c1ee9-295">Event ID 10021</span></span>

<span data-ttu-id="c1ee9-296">&lt; *Erro de erro \ _information* &gt; para operação de operação de arquivo &lt; *\ _name* &gt; no arquivo de nome do arquivo &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-297">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-297">Description</span></span>**  
<span data-ttu-id="c1ee9-298">Ocorreu um erro de acesso não autorizado ou de e/s ao criar ou excluir um atalho.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-299">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-299">Solution</span></span>**  
<span data-ttu-id="c1ee9-300">Verifique se o caminho do arquivo pode ser acessado e se o usuário tem permissões para criar ou excluir o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="c1ee9-301">Correção de convidado</span><span class="sxs-lookup"><span data-stu-id="c1ee9-301">Guest Patching</span></span>

### <span data-ttu-id="c1ee9-302">IDENTIFICAÇÃO do evento 11001</span><span class="sxs-lookup"><span data-stu-id="c1ee9-302">Event ID 11001</span></span>

<span data-ttu-id="c1ee9-303">Mensagem de uso da tarefa de ativação de convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-304">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-304">Description</span></span>**  
<span data-ttu-id="c1ee9-305">MedvHost.exe com a opção/GuestWakeup foi executada incorretamente, ou o comando está formatado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-306">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-306">Solution</span></span>**  
<span data-ttu-id="c1ee9-307">Certifique-se de que o comando seja executado com o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="c1ee9-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="c1ee9-308">Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *Workspace \ _name* &gt; " onde</span><span class="sxs-lookup"><span data-stu-id="c1ee9-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="c1ee9-309">&lt;*Duration \ _in \ _minutes* &gt; é o número de minutos em que a máquina virtual deve ficar em dia (o padrão é 240) e</span><span class="sxs-lookup"><span data-stu-id="c1ee9-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="c1ee9-310">&lt;*espaço de trabalho \ _name* &gt; é o nome da máquina virtual que deve ser ativado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="c1ee9-311">IDENTIFICAÇÃO do evento 11002</span><span class="sxs-lookup"><span data-stu-id="c1ee9-311">Event ID 11002</span></span>

<span data-ttu-id="c1ee9-312">Não é possível atualizar o MED-V – nenhuma rede de host detectada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-313">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-313">Description</span></span>**  
<span data-ttu-id="c1ee9-314">O patch de convidado não pôde ser concluído porque nenhuma conexão de rede de host foi detectada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-315">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-315">Solution</span></span>**  
<span data-ttu-id="c1ee9-316">Conecte o host do MED-V a uma conexão de rede ativa antes de executar o patch de convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="c1ee9-317">IDENTIFICAÇÃO do evento 11003</span><span class="sxs-lookup"><span data-stu-id="c1ee9-317">Event ID 11003</span></span>

<span data-ttu-id="c1ee9-318">Não é possível atualizar o MED-V – o host não está em execução em A/C powerFailed para criar um servidor de pipe.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-319">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-319">Description</span></span>**  
<span data-ttu-id="c1ee9-320">O patch de convidado não pôde ser concluído porque o host parece estar em execução na energia da bateria, em vez de em um fio de alimentação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-321">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-321">Solution</span></span>**  
<span data-ttu-id="c1ee9-322">Conecte o computador host a um cabo de alimentação antes de executar o patch de convidado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="c1ee9-323">UX do cliente</span><span class="sxs-lookup"><span data-stu-id="c1ee9-323">Client UX</span></span>

### <span data-ttu-id="c1ee9-324">IDENTIFICAÇÃO do evento 14003</span><span class="sxs-lookup"><span data-stu-id="c1ee9-324">Event ID 14003</span></span>

<span data-ttu-id="c1ee9-325">A mensagem de status da bandeja a seguir era muito longa e não pôde ser exibida: &lt; *tray \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="c1ee9-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-326">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-326">Description</span></span>**  
<span data-ttu-id="c1ee9-327">O MED-V criou uma cadeia de caracteres não esperada muito longa para a dica de ferramenta de bandeja ou a mensagem de balão.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="c1ee9-328">Como resultado, a mensagem exibida foi truncada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-329">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-329">Solution</span></span>**  
<span data-ttu-id="c1ee9-330">Esse é um erro raro que pode ocorrer quando o MED-V cria aleatoriamente o texto da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="c1ee9-331">Não há solução.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-331">There is no solution.</span></span>

### <span data-ttu-id="c1ee9-332">IDENTIFICAÇÃO do evento 14004</span><span class="sxs-lookup"><span data-stu-id="c1ee9-332">Event ID 14004</span></span>

<span data-ttu-id="c1ee9-333">O MED-V parou devido a uma exceção não tratada.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-334">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-334">Description</span></span>**  
<span data-ttu-id="c1ee9-335">Uma exceção não tratada fez o MED-V parar inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-336">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-336">Solution</span></span>**  
<span data-ttu-id="c1ee9-337">Reinicie o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-337">Restart MED-V.</span></span>

### <span data-ttu-id="c1ee9-338">IDENTIFICAÇÃO do evento 14005</span><span class="sxs-lookup"><span data-stu-id="c1ee9-338">Event ID 14005</span></span>

<span data-ttu-id="c1ee9-339">O servidor tentou criar o mutex, mas já existia.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-340">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-340">Description</span></span>**  
<span data-ttu-id="c1ee9-341">Uma segunda instância do MedvHost.exe está presa na memória.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-342">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-342">Solution</span></span>**  
<span data-ttu-id="c1ee9-343">Abra o taskmanager e encerre todos os processos de MedvHost.exe.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="c1ee9-344">IDENTIFICAÇÃO do evento 14006</span><span class="sxs-lookup"><span data-stu-id="c1ee9-344">Event ID 14006</span></span>

<span data-ttu-id="c1ee9-345">Erro ao modificar ou excluir o registro de valor do registro &lt; *\ _value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-346">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-346">Description</span></span>**  
<span data-ttu-id="c1ee9-347">O MED-V não pode modificar a entrada especificada no registro.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-348">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-348">Solution</span></span>**  
<span data-ttu-id="c1ee9-349">Verifique se você instalou ou desinstalou o MED-V com credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="c1ee9-350">IDENTIFICAÇÃO do evento 14007</span><span class="sxs-lookup"><span data-stu-id="c1ee9-350">Event ID 14007</span></span>

<span data-ttu-id="c1ee9-351">O arquivo especificado ( &lt; *filename* &gt; ) não é válido.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-352">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-352">Description</span></span>**  
<span data-ttu-id="c1ee9-353">Durante a instalação ou desinstalação, um arquivo temporário corrompido foi passado para o host do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-354">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-354">Solution</span></span>**  
<span data-ttu-id="c1ee9-355">Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="c1ee9-356">IDENTIFICAÇÃO do evento 14008</span><span class="sxs-lookup"><span data-stu-id="c1ee9-356">Event ID 14008</span></span>

<span data-ttu-id="c1ee9-357">Arquivo não encontrado: &lt; *nome_do_arquivo* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-358">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-358">Description</span></span>**  
<span data-ttu-id="c1ee9-359">Durante a instalação ou desinstalação, um caminho de um arquivo temporário obrigatório não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-360">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-360">Solution</span></span>**  
<span data-ttu-id="c1ee9-361">Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="c1ee9-362">IDENTIFICAÇÃO do evento 14009</span><span class="sxs-lookup"><span data-stu-id="c1ee9-362">Event ID 14009</span></span>

<span data-ttu-id="c1ee9-363">Não é possível ler o nome do arquivo do arquivo de parâmetro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-364">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-364">Description</span></span>**  
<span data-ttu-id="c1ee9-365">Durante o processo de instalação ou desinstalação, o MED-V não pôde ler um arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-366">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-366">Solution</span></span>**  
<span data-ttu-id="c1ee9-367">Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="c1ee9-368">Além disso, verifique se o usuário tem as permissões e os direitos necessários para a pasta Temp.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="c1ee9-369">IDENTIFICAÇÃO do evento 14010</span><span class="sxs-lookup"><span data-stu-id="c1ee9-369">Event ID 14010</span></span>

<span data-ttu-id="c1ee9-370">Erro ao desserializar o nome do arquivo de parâmetro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-371">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-371">Description</span></span>**  
<span data-ttu-id="c1ee9-372">Durante o processo de instalação ou desinstalação, o MED-V encontrou um arquivo temporário corrompido.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-373">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-373">Solution</span></span>**  
<span data-ttu-id="c1ee9-374">Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="c1ee9-375">Além disso, verifique se o usuário tem as permissões e os direitos necessários para a pasta Temp.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="c1ee9-376">IDENTIFICAÇÃO do evento 14011</span><span class="sxs-lookup"><span data-stu-id="c1ee9-376">Event ID 14011</span></span>

<span data-ttu-id="c1ee9-377">Erro inesperado ao desserializar o nome do arquivo de parâmetro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-378">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-378">Description</span></span>**  
<span data-ttu-id="c1ee9-379">Durante o processo de instalação ou desinstalação, o MED-V encontrou um arquivo temporário corrompido.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-380">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-380">Solution</span></span>**  
<span data-ttu-id="c1ee9-381">Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="c1ee9-382">Além disso, verifique se o usuário tem as permissões e os direitos necessários para a pasta Temp.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="c1ee9-383">IDENTIFICAÇÃO do evento 14012</span><span class="sxs-lookup"><span data-stu-id="c1ee9-383">Event ID 14012</span></span>

<span data-ttu-id="c1ee9-384">Erro inesperado quando as configurações direitos na &lt; *pasta da pasta \ _name* &gt; para nome de usuário do usuário &lt; *username* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c1ee9-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-385">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-385">Description</span></span>**  
<span data-ttu-id="c1ee9-386">Um erro ocorre quando o MED-V não consegue definir direitos e permissões em determinadas pastas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-387">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-387">Solution</span></span>**  
<span data-ttu-id="c1ee9-388">Verifique as seguintes permissões de administrador nas seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="c1ee9-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="c1ee9-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="c1ee9-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="c1ee9-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="c1ee9-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="c1ee9-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="c1ee9-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="c1ee9-392">IDENTIFICAÇÃO do evento 14013</span><span class="sxs-lookup"><span data-stu-id="c1ee9-392">Event ID 14013</span></span>

<span data-ttu-id="c1ee9-393">Erro inesperado ao criar um arquivo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="c1ee9-394">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ee9-394">Description</span></span>**  
<span data-ttu-id="c1ee9-395">Um erro ocorre quando o MED-V não pode criar um arquivo na pasta @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="c1ee9-396">Solução</span><span class="sxs-lookup"><span data-stu-id="c1ee9-396">Solution</span></span>**  
<span data-ttu-id="c1ee9-397">Verifique os direitos de administrador para a pasta MedvLock.</span><span class="sxs-lookup"><span data-stu-id="c1ee9-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="c1ee9-398">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1ee9-398">Related topics</span></span>


[<span data-ttu-id="c1ee9-399">Solução de problemas da MED-V</span><span class="sxs-lookup"><span data-stu-id="c1ee9-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





