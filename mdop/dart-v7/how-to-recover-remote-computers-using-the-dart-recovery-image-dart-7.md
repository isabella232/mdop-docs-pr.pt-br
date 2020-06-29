---
title: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
description: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799143"
---
# <span data-ttu-id="697e7-103">Como recuperar computadores remotos usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="697e7-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="697e7-104">O recurso de conexão remota no Microsoft Diagnostics and Recovery Toolset (DaRT) 7 permite que um administrador de ti execute as ferramentas do DaRT remotamente em um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="697e7-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="697e7-105">Depois que determinadas informações forem fornecidas pelo usuário final (ou por um profissional de assistência técnica em funcionamento no computador do usuário final), o administrador de ti ou o agente de helpdesk poderá assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.</span><span class="sxs-lookup"><span data-stu-id="697e7-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="697e7-106">Importante</span><span class="sxs-lookup"><span data-stu-id="697e7-106">Important</span></span>**  
<span data-ttu-id="697e7-107">Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.</span><span class="sxs-lookup"><span data-stu-id="697e7-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="697e7-108">Para recuperar um computador remoto usando o DaRT</span><span class="sxs-lookup"><span data-stu-id="697e7-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="697e7-109">Inicialize um computador de usuário final usando a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="697e7-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="697e7-110">Você geralmente usará um dos seguintes métodos para inicializar o DaRT para recuperar um computador remoto, dependendo de como você implanta a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="697e7-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="697e7-111">Para obter mais informações sobre a implantação da imagem de recuperação do DaRT, consulte [implantando a imagem de recuperação do dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="697e7-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="697e7-112">Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="697e7-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="697e7-113">Inicialize no DaRT a partir de uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="697e7-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="697e7-114">Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="697e7-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="697e7-115">Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="697e7-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="697e7-116">Observação</span><span class="sxs-lookup"><span data-stu-id="697e7-116">Note</span></span>**  
    <span data-ttu-id="697e7-117">A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="697e7-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="697e7-118">Quando o computador estiver sendo inicializado na imagem de recuperação do DaRT, a caixa de diálogo **netstart** será exibida.</span><span class="sxs-lookup"><span data-stu-id="697e7-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="697e7-119">Você será perguntado se deseja inicializar serviços de rede.</span><span class="sxs-lookup"><span data-stu-id="697e7-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="697e7-120">Se você clicar em **Sim**, presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="697e7-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="697e7-121">Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="697e7-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="697e7-122">Para ignorar o processo de inicialização de rede, clique em **não**.</span><span class="sxs-lookup"><span data-stu-id="697e7-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="697e7-123">Após a caixa de diálogo inicialização de rede, será perguntado se você deseja remapear as letras da unidade.</span><span class="sxs-lookup"><span data-stu-id="697e7-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="697e7-124">Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão.</span><span class="sxs-lookup"><span data-stu-id="697e7-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="697e7-125">Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online.</span><span class="sxs-lookup"><span data-stu-id="697e7-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="697e7-126">O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="697e7-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="697e7-127">Após a caixa de diálogo remapeamento, uma caixa de diálogo **Opções de recuperação do sistema** é exibida e solicita que você selecione um layout de teclado.</span><span class="sxs-lookup"><span data-stu-id="697e7-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="697e7-128">Em seguida, ele exibe o diretório raiz do sistema, o tipo de sistema operacional instalado e o tamanho da partição.</span><span class="sxs-lookup"><span data-stu-id="697e7-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="697e7-129">Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos.</span><span class="sxs-lookup"><span data-stu-id="697e7-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="697e7-130">Isso solicitará que você insira a mídia de instalação para o dispositivo e selecione o driver.</span><span class="sxs-lookup"><span data-stu-id="697e7-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="697e7-131">Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="697e7-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="697e7-132">Observação</span><span class="sxs-lookup"><span data-stu-id="697e7-132">Note</span></span>**  
    <span data-ttu-id="697e7-133">Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 7 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="697e7-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="697e7-134">Para obter informações sobre essa situação, incluindo como resolvê-la, consulte [solução de problemas do DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="697e7-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="697e7-135">Na janela **Opções de recuperação do sistema** , selecione **diagnósticos e conjunto de ferramentas de recuperação da Microsoft** para abrir a janela **diagnóstico e conjunto de ferramentas de recuperação** .</span><span class="sxs-lookup"><span data-stu-id="697e7-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="697e7-136">Na janela **diagnóstico e recuperação de conjunto de ferramentas** , clique em **conexão remota** para abrir a janela **conexão remota DART** .</span><span class="sxs-lookup"><span data-stu-id="697e7-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="697e7-137">Se você for solicitado a fornecer o acesso remoto do suporte técnico, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="697e7-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="697e7-138">A janela conexão remota DaRT abre e exibe um número de tíquete, um endereço IP e informações de porta.</span><span class="sxs-lookup"><span data-stu-id="697e7-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="697e7-139">No computador do agente da assistência técnica, abra o **Visualizador de conexão remota do DART**.</span><span class="sxs-lookup"><span data-stu-id="697e7-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="697e7-140">Clique em **Iniciar**, em **todos os programas**, em **Microsoft DART 7**e, em seguida, clique em **Visualizador de conexão remota do DART**.</span><span class="sxs-lookup"><span data-stu-id="697e7-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="697e7-141">Na janela **conexão remota DART** , insira a permissão necessária, o endereço IP e as informações sobre a porta.</span><span class="sxs-lookup"><span data-stu-id="697e7-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="697e7-142">Observação</span><span class="sxs-lookup"><span data-stu-id="697e7-142">Note</span></span>**  
   <span data-ttu-id="697e7-143">Essas informações são criadas no computador do usuário final e devem ser fornecidas pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="697e7-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="697e7-144">Pode haver vários endereços IP a serem escolhidos, dependendo de quantos estão disponíveis no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="697e7-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="697e7-145">Clique em **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="697e7-145">Click **Connect**.</span></span>

<span data-ttu-id="697e7-146">O administrador de ti agora assume o controle do computador do usuário final e pode executar as ferramentas do DaRT remotamente.</span><span class="sxs-lookup"><span data-stu-id="697e7-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="697e7-147">Observação</span><span class="sxs-lookup"><span data-stu-id="697e7-147">Note</span></span>**  
<span data-ttu-id="697e7-148">É fornecido um arquivo chamado inv32.xml e contém informações de conexão remota, como o número da porta e o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="697e7-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="697e7-149">Por padrão, o arquivo está localizado geralmente em%windir%\\System32.</span><span class="sxs-lookup"><span data-stu-id="697e7-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="697e7-150">Para personalizar o processo de conexão remota</span><span class="sxs-lookup"><span data-stu-id="697e7-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="697e7-151">Você pode personalizar o processo de conexão remota editando o arquivo winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="697e7-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="697e7-152">Para obter mais informações sobre como editar o arquivo winpeshl.ini, consulte [Winpeshl.ini arquivos](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="697e7-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="697e7-153">Especifique os seguintes comandos e parâmetros para personalizar a forma como uma conexão remota é estabelecida com um computador de usuário final:</span><span class="sxs-lookup"><span data-stu-id="697e7-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="697e7-154">Comando</span><span class="sxs-lookup"><span data-stu-id="697e7-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="697e7-155">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="697e7-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="697e7-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="697e7-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="697e7-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="697e7-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="697e7-158">-nomessage</span><span class="sxs-lookup"><span data-stu-id="697e7-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="697e7-159">Especifica que o prompt de confirmação não será exibido.</span><span class="sxs-lookup"><span data-stu-id="697e7-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="697e7-160">A conexão remota </strong> continua da mesma forma que se o usuário final tiver respondido &quot; Sim &quot; à solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="697e7-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="697e7-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="697e7-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="697e7-162">nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="697e7-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="697e7-163">Impede que um script personalizado continue até que a <strong> conexão remota </strong> não esteja em execução ou uma conexão válida seja estabelecida com o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="697e7-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="697e7-164">Importante</span><span class="sxs-lookup"><span data-stu-id="697e7-164">Important</span></span></strong><br/><p><span data-ttu-id="697e7-165">Esse comando não serve nenhuma função se for especificado independentemente.</span><span class="sxs-lookup"><span data-stu-id="697e7-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="697e7-166">Ele deve ser especificado em um script para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="697e7-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="697e7-167">Veja a seguir um exemplo de um arquivo winpeshl.ini que é personalizado para abrir a ferramenta **conexão remota** assim que uma tentativa é feita para inicializar o DART:</span><span class="sxs-lookup"><span data-stu-id="697e7-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="697e7-168">Para executar o Visualizador de conexão remota no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="697e7-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="697e7-169">Você pode executar o **Visualizador de conexão remota do DART** no prompt de comando especificando o comando **DartRemoteViewer.exe** e usando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="697e7-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="697e7-170">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="697e7-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="697e7-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="697e7-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="697e7-172">-bilhete = &lt; <em> TicketNumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="697e7-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="697e7-173">Onde &lt; <em> TicketNumber </em> &gt; é o número do bilhete, incluindo os traços, que é gerado pela conexão remota.</span><span class="sxs-lookup"><span data-stu-id="697e7-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="697e7-174">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="697e7-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="697e7-175">Onde &lt; <em> IPAddress </em> &gt; é o endereço IP gerado pela conexão remota.</span><span class="sxs-lookup"><span data-stu-id="697e7-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="697e7-176">-Port = &lt; <em> porta</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="697e7-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="697e7-177">Em que &lt; <em> porta </em> &gt; é a porta correspondente ao endereço IP especificado.</span><span class="sxs-lookup"><span data-stu-id="697e7-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="697e7-178">Se todos os três parâmetros forem especificados e os dados forem válidos, uma conexão será imediatamente tentada quando o programa for iniciado.</span><span class="sxs-lookup"><span data-stu-id="697e7-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="697e7-179">Se algum parâmetro não for válido, o programa será iniciado como se não houvesse parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="697e7-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="697e7-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="697e7-180">Related topics</span></span>


[<span data-ttu-id="697e7-181">Recuperar computadores usando o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="697e7-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









