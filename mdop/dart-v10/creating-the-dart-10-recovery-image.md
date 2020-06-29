---
title: Criação da imagem de recuperação do DaRT 10
description: Criação da imagem de recuperação do DaRT 10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796192"
---
# <span data-ttu-id="8ea8a-103">Criação da imagem de recuperação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8ea8a-103">Creating the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="8ea8a-104">Depois de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 10, você cria uma imagem de recuperação do DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you create a DaRT 10 recovery image.</span></span> <span data-ttu-id="8ea8a-105">A imagem de recuperação inicia o Windows RE, no qual você pode iniciar as ferramentas do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="8ea8a-106">Você pode gerar arquivos ISO (International Organization for Standardization) e imagens WIM (Windows Imaging Format).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="8ea8a-107">Além disso, você pode usar o PowerShell para gerar scripts que usam as configurações selecionadas no assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="8ea8a-108">Você pode usar o script mais tarde para reconstruir imagens de recuperação usando as mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="8ea8a-109">A imagem de recuperação fornece uma variedade de ferramentas de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="8ea8a-110">Para obter uma descrição das ferramentas, consulte [visão geral das ferramentas no DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-110">For a description of the tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

<span data-ttu-id="8ea8a-111">Após inicializar o computador no DaRT, você pode executar as diferentes ferramentas do DaRT para tentar diagnosticar e reparar o computador.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="8ea8a-112">Esta seção apresenta o processo de criação da imagem de recuperação DaRT e permite selecionar as ferramentas e os recursos que você deseja incluir como parte da imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="8ea8a-113">Você pode criar a imagem de recuperação do DaRT usando um destes dois métodos:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="8ea8a-114">Use o assistente de imagem de recuperação DaRT, que é executado em um ambiente do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="8ea8a-115">Modifique um exemplo de script do PowerShell com os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="8ea8a-116">Para obter mais informações, consulte [como usar um script do PowerShell para criar a imagem de recuperação](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="8ea8a-117">Você pode escrever o ISO em um CD ou DVD gravável, salvá-lo em uma unidade flash USB ou salvá-lo em um formato que você pode usar para inicializar o DaRT a partir de uma partição remota ou de uma partição de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="8ea8a-118">Depois de criar a imagem ISO, você pode gravá-la em um CD ou DVD em branco (se o computador tiver uma unidade de CD ou DVD).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="8ea8a-119">Se o seu computador não tiver uma unidade para essa finalidade, você pode usar os programas mais genéricos que são usados para gravar CDs ou DVDs.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="8ea8a-120">Selecione a arquitetura da imagem e especifique o caminho</span><span class="sxs-lookup"><span data-stu-id="8ea8a-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="8ea8a-121">Na página mídia do Windows 10, selecione se deseja criar uma imagem de recuperação do DaRT de 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-121">On the Windows 10 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="8ea8a-122">Use o Windows de 32 bits para compilar as imagens de recuperação do DaRT de 32 bits e o Windows de 64 bits para criar imagens de recuperação de 64 bits do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="8ea8a-123">Você pode usar um único computador para criar imagens de recuperação para os dois tipos de arquitetura, mas não pode criar uma imagem que funcione nas arquiteturas de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="8ea8a-124">Você também pode indicar o caminho da mídia de instalação do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-124">You also indicate the path of the Windows 10 installation media.</span></span> <span data-ttu-id="8ea8a-125">Escolha a arquitetura que corresponde a uma das imagens de recuperação que você está criando.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="8ea8a-126">Para selecionar a arquitetura da imagem e especificar o caminho</span><span class="sxs-lookup"><span data-stu-id="8ea8a-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="8ea8a-127">Na página **mídia do Windows 10** , selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-127">On the **Windows 10 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="8ea8a-128">Se você estiver criando uma imagem de recuperação para computadores de 64 bits, selecione **criar uma imagem do DART x64 (64 bits)**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="8ea8a-129">Se você estiver criando uma imagem de recuperação para computadores de 32 bits, selecione **criar uma imagem do DART x86 (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="8ea8a-130">Na caixa **especificar o caminho raiz da mídia de instalação do Windows 10 &lt; 64 bits ou do 32-bit &gt; install** , digite o caminho dos arquivos de instalação do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-130">In the **Specify the root path of the Windows 10 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 10 installation files.</span></span> <span data-ttu-id="8ea8a-131">Use um caminho que corresponda à arquitetura da imagem de recuperação que você está criando.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="8ea8a-132">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-132">Click **Next**.</span></span>

## <span data-ttu-id="8ea8a-133">Selecionar as ferramentas a serem incluídas na imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="8ea8a-134">Na página ferramentas, você pode selecionar várias ferramentas para incluir na imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="8ea8a-135">Essas ferramentas estarão disponíveis para os usuários finais quando forem inicializadas na imagem do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="8ea8a-136">No entanto, se você habilitar a conectividade remota ao criar a imagem DaRT, todas as ferramentas estarão disponíveis quando um trabalho de suporte técnico se conectar ao computador do usuário final, independentemente de quais ferramentas você escolheu incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="8ea8a-137">Para restringir o acesso do usuário final a essas ferramentas, mas ainda manter o acesso completo às ferramentas por meio do Visualizador de conexão remota, não selecione essas ferramentas na página ferramentas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="8ea8a-138">Os usuários finais poderão usar somente a conexão remota e poderão ver, mas não poderão, acessar qualquer ferramenta que você excluir da imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="8ea8a-139">Para selecionar as ferramentas a serem incluídas na imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="8ea8a-140">Na página **ferramentas** , marque a caixa de seleção ao lado de cada ferramenta que você deseja incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="8ea8a-141">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-141">Click **Next**.</span></span>

## <span data-ttu-id="8ea8a-142">Escolha se deseja permitir a conectividade remota por um suporte técnico</span><span class="sxs-lookup"><span data-stu-id="8ea8a-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="8ea8a-143">Na página conexão remota, você pode optar por habilitar um trabalhador de suporte técnico para conectar-se remotamente e executar as ferramentas DaRT no computador de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="8ea8a-144">A opção conectividade remota é exibida como uma opção disponível na janela diagnóstico e recuperação do conjunto de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="8ea8a-145">Depois que os funcionários do suporte técnico estabelecerem uma conexão remota, eles poderão executar as ferramentas DaRT no computador do usuário final a partir de um local remoto.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="8ea8a-146">Para escolher se a conectividade remota será permitida por profissionais de suporte técnico</span><span class="sxs-lookup"><span data-stu-id="8ea8a-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="8ea8a-147">Na página **conexão remota** , marque a caixa de seleção **permitir conexões remotas** para permitir conexões remotas ou desmarque a caixa de seleção para impedir conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="8ea8a-148">Se você desmarcou a caixa de seleção **permitir conexões remotas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="8ea8a-149">Caso contrário, vá para a próxima etapa para continuar a configuração da conectividade remota.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="8ea8a-150">Selecione uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-150">Select one of the following:</span></span>

    -   <span data-ttu-id="8ea8a-151">Deixe o Windows escolher um número de porta aberto.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="8ea8a-152">Especifique o número da porta.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-152">Specify the port number.</span></span> <span data-ttu-id="8ea8a-153">Se você selecionar essa opção, insira um número de porta entre 1 e 65535 no campo abaixo da opção.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="8ea8a-154">Este número de porta será usado ao estabelecer uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="8ea8a-155">Recomendamos que o número da porta seja 1024 ou superior para minimizar a possibilidade de um conflito.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="8ea8a-156">(Opcional) na caixa de mensagem de **boas-vindas conexão remota** , crie uma mensagem personalizada que os usuários finais recebem quando estabelecem uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="8ea8a-157">A mensagem pode ter no máximo 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="8ea8a-158">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-158">Click **Next**.</span></span>

    <span data-ttu-id="8ea8a-159">Para obter mais informações sobre como executar as ferramentas do DaRT remotamente, consulte [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

## <span data-ttu-id="8ea8a-160">Adicionar drivers à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="8ea8a-161">Na guia Drivers da página de opções avançadas, você pode adicionar outros drivers de dispositivo que talvez sejam necessários ao reparar um computador.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="8ea8a-162">Geralmente, eles podem incluir armazenamento ou controladores de rede que o Windows 10 não fornece.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-162">These may typically include storage or network controllers that Windows 10 does not provide.</span></span> <span data-ttu-id="8ea8a-163">Os drivers são instalados quando a imagem é criada.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="8ea8a-164">**Importante**  Quando você selecionar os drivers a serem incluídos, lembre-se de que a conectividade sem fio (como Bluetooth ou 802.11 a/b/g/n) não é compatível com o DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="8ea8a-165">Para adicionar drivers à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="8ea8a-166">Na página **Opções avançadas** , clique na guia **drivers** .</span><span class="sxs-lookup"><span data-stu-id="8ea8a-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="8ea8a-167">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-167">Click **Add**.</span></span>

3.  <span data-ttu-id="8ea8a-168">Navegue até o arquivo a ser adicionado ao driver e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="8ea8a-169">**Observação**  O arquivo de driver é fornecido pelo fabricante do controlador de armazenamento ou de rede.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="8ea8a-170">Repita as etapas 2 e 3 para cada driver que você deseja incluir.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="8ea8a-171">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-171">Click **Next**.</span></span>

## <span data-ttu-id="8ea8a-172">Adicionar pacotes opcionais do WinPE à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="8ea8a-173">Na guia WinPE da página de opções avançadas, você pode adicionar pacotes opcionais do WinPE à imagem do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="8ea8a-174">Esses pacotes fazem parte do Windows ADK, que é um pré-requisito para a instalação do assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="8ea8a-175">As ferramentas que você pode selecionar são todas opcionais.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="8ea8a-176">Todos os pacotes obrigatórios são adicionados automaticamente, com base nas ferramentas que você selecionou na página ferramentas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="8ea8a-177">Você também pode especificar o tamanho do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="8ea8a-178">Espaço transitório é a quantidade de espaço em disco RAM que é reservada para que o DaRT seja executado.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="8ea8a-179">O espaço transitório é útil para o caso de o disco rígido do usuário final não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="8ea8a-180">Se você estiver executando ferramentas e drivers adicionais, talvez queira aumentar o espaço transitório.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="8ea8a-181">Para adicionar pacotes opcionais do WinPE à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="8ea8a-182">Na página **Opções avançadas** , clique na guia **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="8ea8a-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="8ea8a-183">Marque a caixa de seleção ao lado de cada pacote que você deseja incluir na imagem ou clique na caixa de seleção **nome** para selecionar todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="8ea8a-184">No campo **espaço transitório** , selecione a quantidade de espaço em disco RAM a ser alocada para executar o DART para o caso de o disco rígido do usuário final não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="8ea8a-185">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-185">Click **Next**.</span></span>

## <span data-ttu-id="8ea8a-186">Adicionar as ferramentas de depuração do Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="8ea8a-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="8ea8a-187">Se você incluir a ferramenta Crash Analyzer na imagem ISO, também deverá incluir as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="8ea8a-188">Na guia Crash Analyzer da página de opções avançadas, você insere o caminho das ferramentas de depuração do Windows 10, que o analisador de falha usa para analisar os arquivos de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 10 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="8ea8a-189">Você pode usar as ferramentas que estão no computador em que você está executando o assistente de imagem de recuperação DaRT ou pode usar as ferramentas que estão no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="8ea8a-190">Se você decidir usar as ferramentas no computador do usuário final, lembre-se de que cada computador que você diagnostica deve ter as ferramentas de depuração instaladas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="8ea8a-191">Se você tiver instalado o Microsoft Windows Software Development Kit (SDK) ou o Microsoft Windows Development Kit (WDK), as ferramentas de depuração do Windows 10 serão adicionadas à imagem de recuperação por padrão, e o caminho para as ferramentas de depuração será automaticamente preenchido.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 10 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="8ea8a-192">Você pode alterar o caminho das ferramentas de depuração do Windows 10 se os arquivos estiverem localizados em outro lugar além do local indicado pelo caminho de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-192">You can change the path of the Windows 10 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="8ea8a-193">Um link no assistente permite baixar e instalar as ferramentas de depuração para Windows, caso ainda não estejam instaladas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="8ea8a-194">Para baixar as ferramentas de depuração do Windows, consulte [ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="8ea8a-195">Instale as ferramentas de depuração para o local padrão.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="8ea8a-196">**Observação**  O assistente do DaRT verifica as ferramentas na `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` chave do registro.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="8ea8a-197">Se o valor do registro não estiver lá, o assistente procurará em um dos seguintes locais, dependendo da arquitetura do sistema:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**<span data-ttu-id="8ea8a-198">Para adicionar as ferramentas de depuração do Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="8ea8a-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="8ea8a-199">Na página **Opções avançadas** , clique na guia **analisador de falhas** .</span><span class="sxs-lookup"><span data-stu-id="8ea8a-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="8ea8a-200">Adicionais Clique em **baixar as ferramentas de depuração** para baixar as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="8ea8a-201">Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="8ea8a-202">**Inclua as ferramentas de depuração do Windows 10 &lt; 64 bits ou &gt; do 32-bit**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-202">**Include the Windows 10 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="8ea8a-203">Se você selecionar essa opção, navegue até e selecione o local das ferramentas se o caminho ainda não estiver sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="8ea8a-204">**Use as ferramentas de depuração do sistema que está sendo depurado**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="8ea8a-205">Se você selecionar essa opção, o Crash Analyzer não funcionará se as ferramentas de depuração para Windows não forem encontradas no computador com problema.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="8ea8a-206">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-206">Click **Next**.</span></span>

## <span data-ttu-id="8ea8a-207">Selecionar os tipos de arquivos de imagem de recuperação a serem criados</span><span class="sxs-lookup"><span data-stu-id="8ea8a-207">Select the types of recovery image files to create</span></span>


<span data-ttu-id="8ea8a-208">Na página Criar imagem, escolha uma pasta de saída para a imagem de recuperação, insira um nome de imagem e selecione os tipos de arquivos de imagem de recuperação do DaRT a serem criados.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-208">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="8ea8a-209">Durante o processo de criação da imagem de recuperação, os arquivos de origem do Windows são descompactados, os arquivos DaRT são copiados para ele e a imagem é então "reempacotada" nos formatos de arquivo que você seleciona nesta página.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-209">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="8ea8a-210">Os tipos de arquivos de imagem disponíveis são:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-210">The available image file types are:</span></span>

-   <span data-ttu-id="8ea8a-211">**Arquivo de imagem do Windows (WIM)** – usado para implantar o DART em um PXE (ambiente de execução de pré-inicialização) ou uma partição local).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-211">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="8ea8a-212">**ISO (International Standards Organization)** – usada para implantação em CD ou DVD, ou para uso em máquinas virtuais (VM) s).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-212">**International Standards Organization (ISO)** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="8ea8a-213">O assistente requer que a imagem ISO tenha uma extensão de nome de arquivo. ISO porque a maioria dos programas que grava um CD ou DVD requer essa extensão.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-213">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="8ea8a-214">Se você não especificar um local diferente, a imagem ISO será criada na área de trabalho com o nome DaRT10. ISO.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-214">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT10.ISO.</span></span>

-   <span data-ttu-id="8ea8a-215">**Script do PowerShell** – cria uma imagem de recuperação do DART com comandos que fornecem essencialmente as mesmas opções que você pode selecionar usando o assistente de imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-215">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="8ea8a-216">O script também permite que você adicione ou altere arquivos na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-216">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="8ea8a-217">Se você marcar a caixa de seleção Editar imagem nesta página, poderá personalizar a imagem de recuperação durante o processo de criação da imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-217">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="8ea8a-218">Por exemplo, você pode alterar o arquivo "winpeshl.ini" para criar uma ordem de inicialização personalizada ou adicionar ferramentas de terceiros.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-218">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="8ea8a-219">Para selecionar os tipos de arquivos de imagem de recuperação a serem criados</span><span class="sxs-lookup"><span data-stu-id="8ea8a-219">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="8ea8a-220">Na página **criar imagem** , clique em **procurar** para escolher a pasta de saída para o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-220">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="8ea8a-221">**Observação**  O tamanho da imagem vai variar, dependendo das ferramentas selecionadas e dos arquivos que você adicionar no assistente.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-221">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="8ea8a-222">Na caixa **nome da imagem** , insira um nome para a imagem de recuperação do DART ou aceite o nome padrão, que é DaRT10.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-222">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT10.</span></span>

    <span data-ttu-id="8ea8a-223">O assistente cria uma subpasta no caminho de saída com esse nome.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-223">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="8ea8a-224">Selecione os tipos de arquivos de imagem que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-224">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="8ea8a-225">Escolha uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="8ea8a-225">Choose one of the following:</span></span>

    -   <span data-ttu-id="8ea8a-226">Para alterar os arquivos na imagem de recuperação antes de criar os arquivos de imagem, marque a caixa de seleção **Editar imagem** e clique em **preparar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-226">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="8ea8a-227">Para criar a imagem de recuperação sem alterar os arquivos, clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-227">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="8ea8a-228">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-228">Click **Next**.</span></span>

## <span data-ttu-id="8ea8a-229">Editar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-229">Edit the recovery image files</span></span>


<span data-ttu-id="8ea8a-230">Você pode editar a imagem de recuperação somente se tiver marcado a caixa de seleção Editar imagem na página Criar imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-230">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="8ea8a-231">Depois que a imagem de recuperação tiver sido preparada para edição, você poderá adicionar e modificar os arquivos de imagem de recuperação antes de criar a mídia inicializável.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-231">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="8ea8a-232">Por exemplo, você pode criar uma ordem personalizada para a inicialização, adicionar várias ferramentas de terceiros e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-232">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="8ea8a-233">Para editar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-233">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="8ea8a-234">Na página **Editar imagem** , clique em **abrir** no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-234">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="8ea8a-235">Crie uma subpasta na pasta listada na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-235">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="8ea8a-236">Copie os arquivos que você deseja para a nova subpasta ou remova os arquivos que não deseja.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-236">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="8ea8a-237">Clique em **criar** para começar a criar a imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-237">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="8ea8a-238">Gerar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-238">Generate the recovery image files</span></span>


<span data-ttu-id="8ea8a-239">Na página gerar arquivos, a imagem de recuperação do DaRT é gerada para os tipos de arquivo selecionados na página Criar imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-239">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="8ea8a-240">Para gerar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="8ea8a-240">To generate the recovery image files</span></span>**

-   <span data-ttu-id="8ea8a-241">Na página **gerar arquivos** , clique em **Avançar** para gerar os arquivos de imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-241">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="8ea8a-242">Copiar a imagem de recuperação para um CD, DVD ou USB</span><span class="sxs-lookup"><span data-stu-id="8ea8a-242">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="8ea8a-243">Na página Criar mídia inicializável, você pode copiar opcionalmente o arquivo de imagem para um CD, DVD ou unidade flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="8ea8a-243">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="8ea8a-244">Você também pode criar mídia inicializável adicional desta página reiniciando o assistente.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-244">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="8ea8a-245">**Observação**  O ambiente de execução de pré-inicialização (PXE) e a implantação de imagens locais não são suportados nativamente por essa ferramenta, pois exigem ferramentas empresariais adicionais, como o System Center Configuration Manager Server e o Microsoft Development Toolkit.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-245">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="8ea8a-246">Para copiar a imagem de recuperação para um CD, DVD ou USB</span><span class="sxs-lookup"><span data-stu-id="8ea8a-246">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="8ea8a-247">Na página **criar mídia inicializável** , selecione o arquivo ISO que você deseja copiar.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-247">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="8ea8a-248">Insira um CD, DVD ou USB e selecione a unidade.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-248">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="8ea8a-249">**Observação**  Se uma unidade não for reconhecida e você instalar uma nova unidade, você poderá clicar em **Atualizar** para forçar o assistente a atualizar a lista de unidades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-249">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="8ea8a-250">Clique no botão **criar mídia inicializável** .</span><span class="sxs-lookup"><span data-stu-id="8ea8a-250">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="8ea8a-251">Para criar outra imagem de recuperação, clique em reiniciar ou clique em **fechar** se terminar de criar todas as mídias desejadas.</span><span class="sxs-lookup"><span data-stu-id="8ea8a-251">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="8ea8a-252">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ea8a-252">Related topics</span></span>


[<span data-ttu-id="8ea8a-253">Visão geral das ferramentas do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8ea8a-253">Overview of the Tools in DaRT 10</span></span>](overview-of-the-tools-in-dart-10.md)

[<span data-ttu-id="8ea8a-254">Implantação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8ea8a-254">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





