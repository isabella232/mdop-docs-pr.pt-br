---
title: Como recuperar computadores locais usando a imagem de recuperação do DaRT
description: Como recuperar computadores locais usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799337"
---
# <span data-ttu-id="f3db8-103">Como recuperar computadores locais usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="f3db8-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="f3db8-104">Para recuperar um computador local usando o Microsoft Diagnostic and Recovery Toolset (DaRT) 7, você deve estar fisicamente presente no computador do usuário final que está apresentando problemas que exigem o DaRT.</span><span class="sxs-lookup"><span data-stu-id="f3db8-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="f3db8-105">Você também pode executar o DaRT remotamente seguindo as instruções em [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="f3db8-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="f3db8-106">Para recuperar um computador local usando o DaRT</span><span class="sxs-lookup"><span data-stu-id="f3db8-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="f3db8-107">Quando o computador estiver sendo inicializado na imagem de recuperação do DaRT, a caixa de diálogo **netstart** será exibida.</span><span class="sxs-lookup"><span data-stu-id="f3db8-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="f3db8-108">Você será perguntado se deseja inicializar serviços de rede.</span><span class="sxs-lookup"><span data-stu-id="f3db8-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="f3db8-109">Se você clicar em **Sim**, presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="f3db8-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="f3db8-110">Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="f3db8-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="f3db8-111">Para ignorar o processo de inicialização de rede, clique em **não**.</span><span class="sxs-lookup"><span data-stu-id="f3db8-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="f3db8-112">Após a caixa de diálogo inicialização de rede, será perguntado se você deseja remapear as letras da unidade.</span><span class="sxs-lookup"><span data-stu-id="f3db8-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="f3db8-113">Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão.</span><span class="sxs-lookup"><span data-stu-id="f3db8-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="f3db8-114">Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online.</span><span class="sxs-lookup"><span data-stu-id="f3db8-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="f3db8-115">O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="f3db8-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="f3db8-116">Após a caixa de diálogo remapeamento, uma caixa de diálogo **Opções de recuperação do sistema** é exibida e solicita que você selecione um layout de teclado.</span><span class="sxs-lookup"><span data-stu-id="f3db8-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="f3db8-117">Em seguida, ele exibe o diretório raiz do sistema, o tipo de sistema operacional instalado e o tamanho da partição.</span><span class="sxs-lookup"><span data-stu-id="f3db8-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="f3db8-118">Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos.</span><span class="sxs-lookup"><span data-stu-id="f3db8-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="f3db8-119">Isso solicitará que você insira a mídia de instalação para o dispositivo e selecione o driver.</span><span class="sxs-lookup"><span data-stu-id="f3db8-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="f3db8-120">Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f3db8-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="f3db8-121">Observação</span><span class="sxs-lookup"><span data-stu-id="f3db8-121">Note</span></span>**  
    <span data-ttu-id="f3db8-122">Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 7 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f3db8-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="f3db8-123">Na janela **Opções de recuperação do sistema** , clique em **conjunto de ferramentas de diagnóstico e recuperação da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="f3db8-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="f3db8-124">A janela **diagnóstico e Recovery Toolset** é aberta.</span><span class="sxs-lookup"><span data-stu-id="f3db8-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="f3db8-125">Agora você pode executar qualquer uma das ferramentas ou assistentes individuais que foram incluídos quando a imagem de recuperação do DaRT foi criada.</span><span class="sxs-lookup"><span data-stu-id="f3db8-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="f3db8-126">Você pode clicar em **ajuda** na janela do **conjunto de ferramentas de diagnóstico e recuperação** para abrir o arquivo de ajuda do cliente que fornece instruções e informações detalhadas necessárias para executar as ferramentas individuais do DART.</span><span class="sxs-lookup"><span data-stu-id="f3db8-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="f3db8-127">Você também pode clicar no **Assistente de solução** na janela **diagnóstico e recuperação de conjunto de ferramentas** para escolher a melhor ferramenta para a situação, com base em uma breve entrevista que o assistente fornece.</span><span class="sxs-lookup"><span data-stu-id="f3db8-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="f3db8-128">Para obter informações gerais sobre qualquer uma das ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="f3db8-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="f3db8-129">Para executar o DaRT no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="f3db8-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="f3db8-130">Você pode executar o DaRT no prompt de comando especificando o comando **netstart.exe** e usando qualquer um dos seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="f3db8-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f3db8-131">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3db8-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="f3db8-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3db8-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f3db8-133">-rede</span><span class="sxs-lookup"><span data-stu-id="f3db8-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3db8-134">Inicializa os serviços de rede.</span><span class="sxs-lookup"><span data-stu-id="f3db8-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f3db8-135">-remontar</span><span class="sxs-lookup"><span data-stu-id="f3db8-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3db8-136">Remapeia as letras de unidade.</span><span class="sxs-lookup"><span data-stu-id="f3db8-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f3db8-137">-aviso</span><span class="sxs-lookup"><span data-stu-id="f3db8-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3db8-138">Exibe mensagens solicitando que o usuário final especifique se deseja inicializar a rede e remapear as unidades.</span><span class="sxs-lookup"><span data-stu-id="f3db8-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f3db8-139">Importante</span><span class="sxs-lookup"><span data-stu-id="f3db8-139">Important</span></span></strong><br/><p><span data-ttu-id="f3db8-140">A resposta do usuário final às solicitações substitui as opções-Network e-Remount.</span><span class="sxs-lookup"><span data-stu-id="f3db8-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f3db8-141">Você pode personalizar o DaRT para que um computador inicializado pelo DaRT abra automaticamente a ferramenta **conexão remota** que é usada para estabelecer uma conexão remota com o suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="f3db8-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="f3db8-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3db8-142">Related topics</span></span>


[<span data-ttu-id="f3db8-143">Recuperar computadores usando o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="f3db8-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









