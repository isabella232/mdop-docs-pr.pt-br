---
title: Como recuperar computadores locais usando a imagem de recuperação do DaRT
description: Como recuperar computadores locais usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: f679d522-49ab-429c-93d0-294c3f3e5639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1b5faa0eb9ac24b33c66f1d5262a050b92e11e52
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799446"
---
# <span data-ttu-id="6b2ab-103">Como recuperar computadores locais usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="6b2ab-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="6b2ab-104">Use estas instruções para recuperar um computador quando você estiver fisicamente presente no computador do usuário final que está apresentando problemas.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="6b2ab-105">Como recuperar um computador local usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="6b2ab-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="6b2ab-106">Inicializar o computador do usuário final usando a imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

    <span data-ttu-id="6b2ab-107">Quando o computador estiver sendo inicializado na imagem de recuperação do DaRT 8,0, a caixa de diálogo **netstart** será exibida.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-107">As the computer is booting into the DaRT 8.0 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="6b2ab-108">Quando for perguntado se você deseja inicializar serviços de rede, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="6b2ab-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="6b2ab-109">**Sim** -presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="6b2ab-110">Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="6b2ab-111">**Não** -ignore o processo de inicialização de rede.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="6b2ab-112">Indique se deseja remapear as letras da unidade.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="6b2ab-113">Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="6b2ab-114">Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="6b2ab-115">O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="6b2ab-116">Na caixa de diálogo **Opções de recuperação do sistema** , selecione um layout de teclado.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="6b2ab-117">Verifique o diretório raiz do sistema exibido, o tipo de sistema operacional instalado e o tamanho da partição.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="6b2ab-118">Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos e, em seguida, insira a mídia de instalação para o dispositivo e selecione o driver.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="6b2ab-119">Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="6b2ab-120">Observação</span><span class="sxs-lookup"><span data-stu-id="6b2ab-120">Note</span></span>**  
    <span data-ttu-id="6b2ab-121">Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 8 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 8 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="6b2ab-122">Na janela **Opções de recuperação do sistema** , clique em **conjunto de ferramentas de diagnóstico e recuperação da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="6b2ab-123">A janela **diagnóstico e Recovery Toolset** é aberta.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="6b2ab-124">Agora você pode executar qualquer uma das ferramentas ou assistentes individuais que foram incluídos quando a imagem de recuperação do DaRT foi criada.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="6b2ab-125">Você pode clicar em **ajuda** na janela do **conjunto de ferramentas de diagnóstico e recuperação** para abrir o arquivo de ajuda do cliente que fornece instruções e informações detalhadas necessárias para executar as ferramentas individuais do DART.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="6b2ab-126">Você também pode clicar no **Assistente de solução** na janela **diagnóstico e recuperação de conjunto de ferramentas** para escolher a melhor ferramenta para a situação, com base em uma breve entrevista que o assistente fornece.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="6b2ab-127">Para obter informações gerais sobre qualquer uma das ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="6b2ab-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

**<span data-ttu-id="6b2ab-128">Como executar o DaRT no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="6b2ab-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="6b2ab-129">Para executar o DaRT no prompt de comando, especifique o comando **netstart.exe** e use qualquer um dos seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="6b2ab-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="6b2ab-130">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b2ab-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="6b2ab-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b2ab-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="6b2ab-132">-rede</span><span class="sxs-lookup"><span data-stu-id="6b2ab-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="6b2ab-133">Inicializa os serviços de rede.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="6b2ab-134">-remontar</span><span class="sxs-lookup"><span data-stu-id="6b2ab-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="6b2ab-135">Remapeia as letras de unidade.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="6b2ab-136">-aviso</span><span class="sxs-lookup"><span data-stu-id="6b2ab-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="6b2ab-137">Exibe mensagens que solicitam que o usuário final especifique se deseja inicializar a rede e remapear as unidades.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="6b2ab-138">Aviso</span><span class="sxs-lookup"><span data-stu-id="6b2ab-138">Warning</span></span></strong><br/><p><span data-ttu-id="6b2ab-139">A resposta do usuário final para o prompt substitui as opções – Network e-Remount.</span><span class="sxs-lookup"><span data-stu-id="6b2ab-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="6b2ab-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b2ab-140">Related topics</span></span>


[<span data-ttu-id="6b2ab-141">Operações do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="6b2ab-141">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="6b2ab-142">Recuperar computadores usando o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="6b2ab-142">Recovering Computers Using DaRT 8.0</span></span>](recovering-computers-using-dart-80-dart-8.md)









