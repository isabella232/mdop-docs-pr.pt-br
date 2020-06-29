---
title: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
description: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: c0062208-39cd-4e01-adf8-36a11386e2ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 42d49c6c5c494da866785764e1c93a6bda2d667e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799103"
---
# <span data-ttu-id="9fd75-103">Como recuperar computadores remotos usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="9fd75-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="9fd75-104">Use o recurso conexão remota no Microsoft Diagnostic and Recovery Toolset (DaRT) 10 para executar as ferramentas do DaRT remotamente em um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="9fd75-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="9fd75-105">Depois que o usuário final fornece o trabalho de administrador ou de suporte técnico com determinadas informações, o administrador de ti ou o trabalhador de suporte técnico pode assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.</span><span class="sxs-lookup"><span data-stu-id="9fd75-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="9fd75-106">Se você desativou as ferramentas DaRT ao criar a imagem de recuperação, ainda tem acesso a todas as ferramentas.</span><span class="sxs-lookup"><span data-stu-id="9fd75-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="9fd75-107">Todas as ferramentas, exceto conexão remota, não estão disponíveis para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="9fd75-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="9fd75-108">Para recuperar um computador remoto usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="9fd75-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="9fd75-109">Inicialize um computador de usuário final usando a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="9fd75-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="9fd75-110">Você geralmente usará um dos seguintes métodos para inicializar o DaRT para recuperar um computador remoto, dependendo de como você implanta a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="9fd75-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="9fd75-111">Para obter mais informações sobre como implantar a imagem de recuperação do DaRT, consulte [implantando o DART 10](deploying-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="9fd75-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 10](deploying-dart-10.md).</span></span>

    -   <span data-ttu-id="9fd75-112">Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="9fd75-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="9fd75-113">Inicialize no DaRT a partir de uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="9fd75-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="9fd75-114">Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="9fd75-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

    <span data-ttu-id="9fd75-115">Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="9fd75-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="9fd75-116">Observação</span><span class="sxs-lookup"><span data-stu-id="9fd75-116">Note</span></span>**  
    <span data-ttu-id="9fd75-117">A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="9fd75-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="9fd75-118">Quando for perguntado se você deseja inicializar serviços de rede, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="9fd75-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="9fd75-119">**Sim** -presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="9fd75-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="9fd75-120">Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="9fd75-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="9fd75-121">**Não** -ignore o processo de inicialização de rede.</span><span class="sxs-lookup"><span data-stu-id="9fd75-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="9fd75-122">Indique se deseja remapear as letras da unidade.</span><span class="sxs-lookup"><span data-stu-id="9fd75-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="9fd75-123">Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão.</span><span class="sxs-lookup"><span data-stu-id="9fd75-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="9fd75-124">Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online.</span><span class="sxs-lookup"><span data-stu-id="9fd75-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="9fd75-125">O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9fd75-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="9fd75-126">Na caixa de diálogo **Opções de recuperação do sistema** , selecione um layout de teclado.</span><span class="sxs-lookup"><span data-stu-id="9fd75-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="9fd75-127">Verifique o diretório raiz do sistema exibido, o tipo de sistema operacional instalado e o tamanho da partição.</span><span class="sxs-lookup"><span data-stu-id="9fd75-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="9fd75-128">Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos e, em seguida, insira a mídia de instalação para o dispositivo e selecione o driver.</span><span class="sxs-lookup"><span data-stu-id="9fd75-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="9fd75-129">Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9fd75-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="9fd75-130">Observação</span><span class="sxs-lookup"><span data-stu-id="9fd75-130">Note</span></span>**  
   <span data-ttu-id="9fd75-131">Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 10 não foi iniciado corretamente na última vez em que ele foi tentado, o **reparo de inicialização** poderá começar a ser executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9fd75-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="9fd75-132">Para obter informações sobre como resolver esse problema, consulte [solução de problemas do DART 10](troubleshooting-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="9fd75-132">For information about how to resolve this issue, see [Troubleshooting DaRT 10](troubleshooting-dart-10.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="9fd75-133">Na janela **Opções de recuperação do sistema** , clique em **conjunto de ferramentas de diagnóstico e recuperação da Microsoft** para abrir o conjunto de **ferramentas diagnóstico e recuperação**.</span><span class="sxs-lookup"><span data-stu-id="9fd75-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="9fd75-134">Na janela **diagnóstico e recuperação de conjunto de ferramentas** , clique em **conexão remota** para abrir a janela **conexão remota DART** .</span><span class="sxs-lookup"><span data-stu-id="9fd75-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="9fd75-135">Se você for solicitado a fornecer o acesso remoto do suporte técnico, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fd75-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="9fd75-136">A janela conexão remota DaRT abre e exibe um número de tíquete, um endereço IP e informações de porta.</span><span class="sxs-lookup"><span data-stu-id="9fd75-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="9fd75-137">No computador de suporte técnico, abra o **Visualizador de conexão remota do DART**.</span><span class="sxs-lookup"><span data-stu-id="9fd75-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="9fd75-138">Clique em **Iniciar**, em **todos os programas**, em **Microsoft DART 10**e, em seguida, clique em **Visualizador de conexão remota do DART**.</span><span class="sxs-lookup"><span data-stu-id="9fd75-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 10**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="9fd75-139">Na janela **conexão remota DART** , insira a permissão necessária, o endereço IP e as informações sobre a porta.</span><span class="sxs-lookup"><span data-stu-id="9fd75-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="9fd75-140">Observação</span><span class="sxs-lookup"><span data-stu-id="9fd75-140">Note</span></span>**  
   <span data-ttu-id="9fd75-141">Essas informações são criadas no computador do usuário final e devem ser fornecidas pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="9fd75-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="9fd75-142">Pode haver vários endereços IP a serem escolhidos, dependendo de quantos estão disponíveis no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="9fd75-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="9fd75-143">Clique em **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="9fd75-143">Click **Connect**.</span></span>

<span data-ttu-id="9fd75-144">O administrador de ti agora assume o controle do computador do usuário final e pode executar as ferramentas do DaRT remotamente.</span><span class="sxs-lookup"><span data-stu-id="9fd75-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="9fd75-145">Observação</span><span class="sxs-lookup"><span data-stu-id="9fd75-145">Note</span></span>**  
<span data-ttu-id="9fd75-146">É fornecido um arquivo chamado inv32.xml e contém informações de conexão remota, como o número da porta e o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="9fd75-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="9fd75-147">Por padrão, o arquivo está localizado geralmente em%windir%\\System32.</span><span class="sxs-lookup"><span data-stu-id="9fd75-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="9fd75-148">Para personalizar o processo de conexão remota</span><span class="sxs-lookup"><span data-stu-id="9fd75-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="9fd75-149">Você pode personalizar o processo de conexão remota editando o arquivo winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="9fd75-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="9fd75-150">Para obter mais informações sobre como editar o arquivo winpeshl.ini, consulte [Winpeshl.ini arquivos](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="9fd75-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="9fd75-151">Especifique os seguintes comandos e parâmetros para personalizar a forma como uma conexão remota é estabelecida com um computador de usuário final:</span><span class="sxs-lookup"><span data-stu-id="9fd75-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="9fd75-152">Comando</span><span class="sxs-lookup"><span data-stu-id="9fd75-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="9fd75-153">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fd75-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="9fd75-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fd75-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="9fd75-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="9fd75-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="9fd75-156">-nomessage</span><span class="sxs-lookup"><span data-stu-id="9fd75-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9fd75-157">Especifica que o prompt de confirmação não será exibido.</span><span class="sxs-lookup"><span data-stu-id="9fd75-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="9fd75-158">A conexão remota </strong> continua da mesma forma que se o usuário final tiver respondido &quot; Sim &quot; à solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="9fd75-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="9fd75-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="9fd75-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="9fd75-160">nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="9fd75-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9fd75-161">Impede que um script personalizado continue até que a <strong> conexão remota </strong> não esteja em execução ou uma conexão válida seja estabelecida com o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="9fd75-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="9fd75-162">Importante</span><span class="sxs-lookup"><span data-stu-id="9fd75-162">Important</span></span></strong><br/><p><span data-ttu-id="9fd75-163">Esse comando não serve nenhuma função se for especificado independentemente.</span><span class="sxs-lookup"><span data-stu-id="9fd75-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="9fd75-164">Ele deve ser especificado em um script para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="9fd75-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="9fd75-165">Veja a seguir um exemplo de um arquivo winpeshl.ini que é personalizado para abrir a ferramenta **conexão remota** assim que uma tentativa é feita para inicializar o DART:</span><span class="sxs-lookup"><span data-stu-id="9fd75-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="9fd75-166">Quando o DaRT é iniciado, ele cria o arquivo inv32.xml em \\Windows\\System32\\ no disco de RAM.</span><span class="sxs-lookup"><span data-stu-id="9fd75-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="9fd75-167">Este arquivo contém informações de conexão: endereço IP, porta e número do tíquete.</span><span class="sxs-lookup"><span data-stu-id="9fd75-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="9fd75-168">Você pode copiar esse arquivo em um compartilhamento de rede para disparar um fluxo de trabalho de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="9fd75-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="9fd75-169">Por exemplo, um programa personalizado pode verificar o compartilhamento de rede para arquivos de conexão e, em seguida, criar um tíquete de suporte ou enviar notificações por email.</span><span class="sxs-lookup"><span data-stu-id="9fd75-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="9fd75-170">Para executar o Visualizador de conexão remota no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="9fd75-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="9fd75-171">Para executar o **Visualizador de conexão remota do DART** no prompt de comando, especifique o comando **DartRemoteViewer.exe** e use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9fd75-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="9fd75-172">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fd75-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="9fd75-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fd75-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9fd75-174">-bilhete = &lt; <em> TicketNumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="9fd75-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9fd75-175">Onde &lt; <em> TicketNumber </em> &gt; é o número do bilhete, incluindo os traços, que é gerado pela conexão remota.</span><span class="sxs-lookup"><span data-stu-id="9fd75-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9fd75-176">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="9fd75-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9fd75-177">Onde &lt; <em> IPAddress </em> &gt; é o endereço IP gerado pela conexão remota.</span><span class="sxs-lookup"><span data-stu-id="9fd75-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9fd75-178">-Port = &lt; <em> porta</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="9fd75-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9fd75-179">Em que &lt; <em> porta </em> &gt; é a porta correspondente ao endereço IP especificado.</span><span class="sxs-lookup"><span data-stu-id="9fd75-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="9fd75-180">Se todos os três parâmetros forem especificados e os dados forem válidos, uma conexão será imediatamente tentada quando o programa for iniciado.</span><span class="sxs-lookup"><span data-stu-id="9fd75-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="9fd75-181">Se algum parâmetro não for válido, o programa será iniciado como se não houvesse parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="9fd75-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="9fd75-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fd75-182">Related topics</span></span>


[<span data-ttu-id="9fd75-183">Operações do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9fd75-183">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="9fd75-184">Recuperar computadores usando o DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9fd75-184">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









