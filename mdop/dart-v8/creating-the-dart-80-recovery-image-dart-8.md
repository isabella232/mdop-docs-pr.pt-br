---
title: Criação da imagem de recuperação do DaRT 8.0
description: Criação da imagem de recuperação do DaRT 8.0
author: dansimp
ms.assetid: 39001b8e-86c0-45ef-8f34-2d6199f9922d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/21/2017
ms.openlocfilehash: 79ce5859e7d0eacf95124c2a7409ff6c21890d65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796028"
---
# <span data-ttu-id="dbafa-103">Criação da imagem de recuperação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="dbafa-103">Creating the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="dbafa-104">Depois de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, você cria uma imagem de recuperação do DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="dbafa-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you create a DaRT 8.0 recovery image.</span></span> <span data-ttu-id="dbafa-105">A imagem de recuperação inicia o Windows RE, no qual você pode iniciar as ferramentas do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="dbafa-106">Você pode gerar arquivos ISO (International Organization for Standardization) e imagens WIM (Windows Imaging Format).</span><span class="sxs-lookup"><span data-stu-id="dbafa-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="dbafa-107">Além disso, você pode usar o PowerShell para gerar scripts que usam as configurações selecionadas no assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="dbafa-108">Você pode usar o script mais tarde para reconstruir imagens de recuperação usando as mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="dbafa-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="dbafa-109">A imagem de recuperação fornece uma variedade de ferramentas de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dbafa-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="dbafa-110">Para obter uma descrição das ferramentas, consulte [visão geral das ferramentas no DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="dbafa-110">For a description of the tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

<span data-ttu-id="dbafa-111">Após inicializar o computador no DaRT, você pode executar as diferentes ferramentas do DaRT para tentar diagnosticar e reparar o computador.</span><span class="sxs-lookup"><span data-stu-id="dbafa-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="dbafa-112">Esta seção apresenta o processo de criação da imagem de recuperação DaRT e permite selecionar as ferramentas e os recursos que você deseja incluir como parte da imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="dbafa-113">Você pode criar a imagem de recuperação do DaRT usando um destes dois métodos:</span><span class="sxs-lookup"><span data-stu-id="dbafa-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="dbafa-114">Use o assistente de imagem de recuperação DaRT, que é executado em um ambiente do Windows.</span><span class="sxs-lookup"><span data-stu-id="dbafa-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="dbafa-115">Modifique um exemplo de script do PowerShell com os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="dbafa-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="dbafa-116">Para obter mais informações, consulte [como usar um script do PowerShell para criar a imagem de recuperação](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="dbafa-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="dbafa-117">Você pode escrever o ISO em um CD ou DVD gravável, salvá-lo em uma unidade flash USB ou salvá-lo em um formato que você pode usar para inicializar o DaRT a partir de uma partição remota ou de uma partição de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dbafa-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="dbafa-118">Depois de criar a imagem ISO, você pode gravá-la em um CD ou DVD em branco (se o computador tiver uma unidade de CD ou DVD).</span><span class="sxs-lookup"><span data-stu-id="dbafa-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="dbafa-119">Se o seu computador não tiver uma unidade para essa finalidade, você pode usar os programas mais genéricos que são usados para gravar CDs ou DVDs.</span><span class="sxs-lookup"><span data-stu-id="dbafa-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="dbafa-120">Selecione a arquitetura da imagem e especifique o caminho</span><span class="sxs-lookup"><span data-stu-id="dbafa-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="dbafa-121">Na página mídia do Windows 8, selecione se deseja criar uma imagem de recuperação do DaRT de 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dbafa-121">On the Windows 8 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="dbafa-122">Use o Windows de 32 bits para compilar as imagens de recuperação do DaRT de 32 bits e o Windows de 64 bits para criar imagens de recuperação de 64 bits do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="dbafa-123">Você pode usar um único computador para criar imagens de recuperação para os dois tipos de arquitetura, mas não pode criar uma imagem que funcione nas arquiteturas de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dbafa-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="dbafa-124">Você também pode indicar o caminho da mídia de instalação do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dbafa-124">You also indicate the path of the Windows 8 installation media.</span></span> <span data-ttu-id="dbafa-125">Escolha a arquitetura que corresponde a uma das imagens de recuperação que você está criando.</span><span class="sxs-lookup"><span data-stu-id="dbafa-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="dbafa-126">Para selecionar a arquitetura da imagem e especificar o caminho</span><span class="sxs-lookup"><span data-stu-id="dbafa-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="dbafa-127">Na página **mídia do Windows 8** , selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="dbafa-127">On the **Windows 8 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="dbafa-128">Se você estiver criando uma imagem de recuperação para computadores de 64 bits, selecione **criar uma imagem do DART x64 (64 bits)**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="dbafa-129">Se você estiver criando uma imagem de recuperação para computadores de 32 bits, selecione **criar uma imagem do DART x86 (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="dbafa-130">Na caixa **especificar o caminho raiz da mídia de instalação do Windows 8 &lt; 64 bits ou do 32-bit &gt; install** , digite o caminho dos arquivos de instalação do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dbafa-130">In the **Specify the root path of the Windows 8 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 8 installation files.</span></span> <span data-ttu-id="dbafa-131">Use um caminho que corresponda à arquitetura da imagem de recuperação que você está criando.</span><span class="sxs-lookup"><span data-stu-id="dbafa-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="dbafa-132">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-132">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-133">Selecionar as ferramentas a serem incluídas na imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="dbafa-134">Na página ferramentas, você pode selecionar várias ferramentas para incluir na imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dbafa-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="dbafa-135">Essas ferramentas estarão disponíveis para os usuários finais quando forem inicializadas na imagem do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="dbafa-136">No entanto, se você habilitar a conectividade remota ao criar a imagem DaRT, todas as ferramentas estarão disponíveis quando um trabalho de suporte técnico se conectar ao computador do usuário final, independentemente de quais ferramentas você escolheu incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="dbafa-137">Para restringir o acesso do usuário final a essas ferramentas, mas ainda manter o acesso completo às ferramentas por meio do Visualizador de conexão remota, não selecione essas ferramentas na página ferramentas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="dbafa-138">Os usuários finais poderão usar somente a conexão remota e poderão ver, mas não poderão, acessar qualquer ferramenta que você excluir da imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dbafa-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="dbafa-139">Para selecionar as ferramentas a serem incluídas na imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="dbafa-140">Na página **ferramentas** , marque a caixa de seleção ao lado de cada ferramenta que você deseja incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="dbafa-141">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-141">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-142">Escolha se deseja permitir a conectividade remota por um suporte técnico</span><span class="sxs-lookup"><span data-stu-id="dbafa-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="dbafa-143">Na página conexão remota, você pode optar por habilitar um trabalhador de suporte técnico para conectar-se remotamente e executar as ferramentas DaRT no computador de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="dbafa-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="dbafa-144">A opção conectividade remota é exibida como uma opção disponível na janela diagnóstico e recuperação do conjunto de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="dbafa-145">Depois que os funcionários do suporte técnico estabelecerem uma conexão remota, eles poderão executar as ferramentas DaRT no computador do usuário final a partir de um local remoto.</span><span class="sxs-lookup"><span data-stu-id="dbafa-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="dbafa-146">Para escolher se a conectividade remota será permitida por profissionais de suporte técnico</span><span class="sxs-lookup"><span data-stu-id="dbafa-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="dbafa-147">Na página **conexão remota** , marque a caixa de seleção **permitir conexões remotas** para permitir conexões remotas ou desmarque a caixa de seleção para impedir conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="dbafa-148">Se você desmarcou a caixa de seleção **permitir conexões remotas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="dbafa-149">Caso contrário, vá para a próxima etapa para continuar a configuração da conectividade remota.</span><span class="sxs-lookup"><span data-stu-id="dbafa-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="dbafa-150">Selecione uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="dbafa-150">Select one of the following:</span></span>

    -   <span data-ttu-id="dbafa-151">Deixe o Windows escolher um número de porta aberto.</span><span class="sxs-lookup"><span data-stu-id="dbafa-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="dbafa-152">Especifique o número da porta.</span><span class="sxs-lookup"><span data-stu-id="dbafa-152">Specify the port number.</span></span> <span data-ttu-id="dbafa-153">Se você selecionar essa opção, insira um número de porta entre 1 e 65535 no campo abaixo da opção.</span><span class="sxs-lookup"><span data-stu-id="dbafa-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="dbafa-154">Este número de porta será usado ao estabelecer uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="dbafa-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="dbafa-155">Recomendamos que o número da porta seja 1024 ou superior para minimizar a possibilidade de um conflito.</span><span class="sxs-lookup"><span data-stu-id="dbafa-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="dbafa-156">(Opcional) na caixa de mensagem de **boas-vindas conexão remota** , crie uma mensagem personalizada que os usuários finais recebem quando estabelecem uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="dbafa-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="dbafa-157">A mensagem pode ter no máximo 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dbafa-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="dbafa-158">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-158">Click **Next**.</span></span>

    <span data-ttu-id="dbafa-159">Para obter mais informações sobre como executar as ferramentas do DaRT remotamente, consulte [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="dbafa-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

## <span data-ttu-id="dbafa-160">Adicionar drivers à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="dbafa-161">Na guia Drivers da página de opções avançadas, você pode adicionar outros drivers de dispositivo que talvez sejam necessários ao reparar um computador.</span><span class="sxs-lookup"><span data-stu-id="dbafa-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="dbafa-162">Geralmente, eles podem incluir armazenamento ou controladores de rede que o Windows 8 não fornece.</span><span class="sxs-lookup"><span data-stu-id="dbafa-162">These may typically include storage or network controllers that Windows 8 does not provide.</span></span> <span data-ttu-id="dbafa-163">Os drivers são instalados quando a imagem é criada.</span><span class="sxs-lookup"><span data-stu-id="dbafa-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="dbafa-164">**Importante**  Quando você selecionar os drivers a serem incluídos, lembre-se de que a conectividade sem fio (como Bluetooth ou 802.11 a/b/g/n) não é compatível com o DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="dbafa-165">Para adicionar drivers à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="dbafa-166">Na página **Opções avançadas** , clique na guia **drivers** .</span><span class="sxs-lookup"><span data-stu-id="dbafa-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="dbafa-167">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-167">Click **Add**.</span></span>

3.  <span data-ttu-id="dbafa-168">Navegue até o arquivo a ser adicionado ao driver e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="dbafa-169">**Observação**  O arquivo de driver é fornecido pelo fabricante do controlador de armazenamento ou de rede.</span><span class="sxs-lookup"><span data-stu-id="dbafa-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="dbafa-170">Repita as etapas 2 e 3 para cada driver que você deseja incluir.</span><span class="sxs-lookup"><span data-stu-id="dbafa-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="dbafa-171">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-171">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-172">Adicionar pacotes opcionais do WinPE à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="dbafa-173">Na guia WinPE da página de opções avançadas, você pode adicionar pacotes opcionais do WinPE à imagem do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="dbafa-174">Esses pacotes fazem parte do Windows ADK, que é um pré-requisito para a instalação do assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="dbafa-175">As ferramentas que você pode selecionar são todas opcionais.</span><span class="sxs-lookup"><span data-stu-id="dbafa-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="dbafa-176">Todos os pacotes obrigatórios são adicionados automaticamente, com base nas ferramentas que você selecionou na página ferramentas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="dbafa-177">Você também pode especificar o tamanho do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dbafa-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="dbafa-178">Espaço transitório é a quantidade de espaço em disco RAM que é reservada para que o DaRT seja executado.</span><span class="sxs-lookup"><span data-stu-id="dbafa-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="dbafa-179">O espaço transitório é útil para o caso de o disco rígido do usuário final não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="dbafa-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="dbafa-180">Se você estiver executando ferramentas e drivers adicionais, talvez queira aumentar o espaço transitório.</span><span class="sxs-lookup"><span data-stu-id="dbafa-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="dbafa-181">Para adicionar pacotes opcionais do WinPE à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="dbafa-182">Na página **Opções avançadas** , clique na guia **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="dbafa-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="dbafa-183">Marque a caixa de seleção ao lado de cada pacote que você deseja incluir na imagem ou clique na caixa de seleção **nome** para selecionar todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="dbafa-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="dbafa-184">No campo **espaço transitório** , selecione a quantidade de espaço em disco RAM a ser alocada para executar o DART para o caso de o disco rígido do usuário final não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="dbafa-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="dbafa-185">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-185">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-186">Adicionar as ferramentas de depuração do Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="dbafa-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="dbafa-187">Se você incluir a ferramenta Crash Analyzer na imagem ISO, também deverá incluir as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="dbafa-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="dbafa-188">Na guia Crash Analyzer da página de opções avançadas, você insere o caminho das ferramentas de depuração do Windows 8, que o analisador de falha usa para analisar os arquivos de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="dbafa-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 8 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="dbafa-189">Você pode usar as ferramentas que estão no computador em que você está executando o assistente de imagem de recuperação DaRT ou pode usar as ferramentas que estão no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="dbafa-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="dbafa-190">Se você decidir usar as ferramentas no computador do usuário final, lembre-se de que cada computador que você diagnostica deve ter as ferramentas de depuração instaladas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="dbafa-191">Se você tiver instalado o Microsoft Windows Software Development Kit (SDK) ou o Microsoft Windows Development Kit (WDK), as ferramentas de depuração do Windows 8 serão adicionadas à imagem de recuperação por padrão, e o caminho para as ferramentas de depuração será automaticamente preenchido.</span><span class="sxs-lookup"><span data-stu-id="dbafa-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 8 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="dbafa-192">Você pode alterar o caminho das ferramentas de depuração do Windows 8 se os arquivos estiverem localizados em outro lugar além do local indicado pelo caminho de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="dbafa-192">You can change the path of the Windows 8 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="dbafa-193">Um link no assistente permite baixar e instalar as ferramentas de depuração para Windows, caso ainda não estejam instaladas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="dbafa-194">Para baixar as ferramentas de depuração do Windows, consulte [ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="dbafa-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="dbafa-195">Instale as ferramentas de depuração para o local padrão.</span><span class="sxs-lookup"><span data-stu-id="dbafa-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="dbafa-196">**Observação**  O assistente do DaRT verifica as ferramentas na `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` chave do registro.</span><span class="sxs-lookup"><span data-stu-id="dbafa-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="dbafa-197">Se o valor do registro não estiver lá, o assistente procurará em um dos seguintes locais, dependendo da arquitetura do sistema:</span><span class="sxs-lookup"><span data-stu-id="dbafa-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x86`

 

**<span data-ttu-id="dbafa-198">Para adicionar as ferramentas de depuração do Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="dbafa-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="dbafa-199">Na página **Opções avançadas** , clique na guia **analisador de falhas** .</span><span class="sxs-lookup"><span data-stu-id="dbafa-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="dbafa-200">Adicionais Clique em **baixar as ferramentas de depuração** para baixar as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="dbafa-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="dbafa-201">Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="dbafa-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="dbafa-202">**Inclua as ferramentas de depuração do Windows 8 &lt; 64 bits ou &gt; do 32-bit**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-202">**Include the Windows 8 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="dbafa-203">Se você selecionar essa opção, navegue até e selecione o local das ferramentas se o caminho ainda não estiver sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="dbafa-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="dbafa-204">**Use as ferramentas de depuração do sistema que está sendo depurado**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="dbafa-205">Se você selecionar essa opção, o Crash Analyzer não funcionará se as ferramentas de depuração para Windows não forem encontradas no computador com problema.</span><span class="sxs-lookup"><span data-stu-id="dbafa-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="dbafa-206">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-206">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-207">Adicionar definições para a ferramenta defender</span><span class="sxs-lookup"><span data-stu-id="dbafa-207">Add definitions for the Defender tool</span></span>


<span data-ttu-id="dbafa-208">Na guia defender da página Opções avançadas, você adiciona definições, que são usadas pela ferramenta defender para determinar se o software que está tentando instalar, executar ou alterar as configurações em um computador é um software indesejado ou mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="dbafa-208">On the Defender tab of the Advanced Options page, you add definitions, which are used by the Defender tool to determine whether software that is trying to install, run, or change settings on a computer is unwanted or malicious software.</span></span>

**<span data-ttu-id="dbafa-209">Para adicionar definições para a ferramenta defender</span><span class="sxs-lookup"><span data-stu-id="dbafa-209">To add definitions for the Defender tool</span></span>**

1.  <span data-ttu-id="dbafa-210">Na página **Opções avançadas** , clique na guia **defender** .</span><span class="sxs-lookup"><span data-stu-id="dbafa-210">On the **Advanced Options** page, click the **Defender** tab.</span></span>

2.  <span data-ttu-id="dbafa-211">Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="dbafa-211">Select one of the following options:</span></span>

    -   <span data-ttu-id="dbafa-212">**Baixar as definições mais recentes (recomendado)** – a atualização de definição inicia automaticamente, e as definições são adicionadas à imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="dbafa-212">**Download the latest definitions (Recommended)** – The definition update starts automatically, and the definitions are added to the DaRT recovery image.</span></span> <span data-ttu-id="dbafa-213">Essa opção é recomendada para ajudar você a evitar casos em que as definições podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dbafa-213">This option is recommended to help you avoid cases where the definitions might not be available.</span></span> <span data-ttu-id="dbafa-214">Você deve estar conectado à Internet para baixar as definições.</span><span class="sxs-lookup"><span data-stu-id="dbafa-214">You must be connected to the Internet to download the definitions.</span></span>

    -   <span data-ttu-id="dbafa-215">**Baixe as definições mais tarde** – as definições não serão incluídas na imagem de recuperação do DART, e você precisará baixar as definições do computador que está executando o DART.</span><span class="sxs-lookup"><span data-stu-id="dbafa-215">**Download the definitions later** – Definitions will not be included in the DaRT recovery image, and you will need to download the definitions from the computer that is running DaRT.</span></span>

        <span data-ttu-id="dbafa-216">Se você decidir não incluir as definições mais recentes na imagem de recuperação ou se as definições incluídas na imagem de recuperação não estiverem mais atualizadas na hora em que você está pronto para usar o defender, obtenha as definições mais recentes antes de iniciar uma verificação seguindo as instruções fornecidas no defender.</span><span class="sxs-lookup"><span data-stu-id="dbafa-216">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use Defender, obtain the latest definitions before you begin a scan by following the instructions that are provided in Defender.</span></span>

        <span data-ttu-id="dbafa-217">**Importante**  Não é possível verificar se não há definições.</span><span class="sxs-lookup"><span data-stu-id="dbafa-217">**Important** You cannot scan if there are no definitions.</span></span>

         

3.  <span data-ttu-id="dbafa-218">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-218">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-219">Selecionar os tipos de arquivos de imagem de recuperação a serem criados</span><span class="sxs-lookup"><span data-stu-id="dbafa-219">Select the types of recovery image files to create</span></span>


<span data-ttu-id="dbafa-220">Na página Criar imagem, escolha uma pasta de saída para a imagem de recuperação, insira um nome de imagem e selecione os tipos de arquivos de imagem de recuperação do DaRT a serem criados.</span><span class="sxs-lookup"><span data-stu-id="dbafa-220">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="dbafa-221">Durante o processo de criação da imagem de recuperação, os arquivos de origem do Windows são descompactados, os arquivos DaRT são copiados para ele e a imagem é então "reempacotada" nos formatos de arquivo que você seleciona nesta página.</span><span class="sxs-lookup"><span data-stu-id="dbafa-221">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="dbafa-222">Os tipos de arquivos de imagem disponíveis são:</span><span class="sxs-lookup"><span data-stu-id="dbafa-222">The available image file types are:</span></span>

-   <span data-ttu-id="dbafa-223">**Arquivo de imagem do Windows (WIM)** – usado para implantar o DART em um PXE (ambiente de execução de pré-inicialização) ou uma partição local).</span><span class="sxs-lookup"><span data-stu-id="dbafa-223">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="dbafa-224">**Arquivo de imagem ISO** – usado para implantar em CD ou DVD, ou para usar em máquinas virtuais (VM) s).</span><span class="sxs-lookup"><span data-stu-id="dbafa-224">**ISO image file** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="dbafa-225">O assistente requer que a imagem ISO tenha uma extensão de nome de arquivo. ISO porque a maioria dos programas que grava um CD ou DVD requer essa extensão.</span><span class="sxs-lookup"><span data-stu-id="dbafa-225">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="dbafa-226">Se você não especificar um local diferente, a imagem ISO será criada na área de trabalho com o nome DaRT8. ISO.</span><span class="sxs-lookup"><span data-stu-id="dbafa-226">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT8.ISO.</span></span>

-   <span data-ttu-id="dbafa-227">**Script do PowerShell** – cria uma imagem de recuperação do DART com comandos que fornecem essencialmente as mesmas opções que você pode selecionar usando o assistente de imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="dbafa-227">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="dbafa-228">O script também permite que você adicione ou altere arquivos na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbafa-228">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="dbafa-229">Se você marcar a caixa de seleção Editar imagem nesta página, poderá personalizar a imagem de recuperação durante o processo de criação da imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-229">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="dbafa-230">Por exemplo, você pode alterar o arquivo "winpeshl.ini" para criar uma ordem de inicialização personalizada ou adicionar ferramentas de terceiros.</span><span class="sxs-lookup"><span data-stu-id="dbafa-230">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="dbafa-231">Para selecionar os tipos de arquivos de imagem de recuperação a serem criados</span><span class="sxs-lookup"><span data-stu-id="dbafa-231">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="dbafa-232">Na página **criar imagem** , clique em **procurar** para escolher a pasta de saída para o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-232">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="dbafa-233">**Observação**  O tamanho da imagem vai variar, dependendo das ferramentas selecionadas e dos arquivos que você adicionar no assistente.</span><span class="sxs-lookup"><span data-stu-id="dbafa-233">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="dbafa-234">Na caixa **nome da imagem** , insira um nome para a imagem de recuperação do DART ou aceite o nome padrão, que é DaRT8.</span><span class="sxs-lookup"><span data-stu-id="dbafa-234">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT8.</span></span>

    <span data-ttu-id="dbafa-235">O assistente cria uma subpasta no caminho de saída com esse nome.</span><span class="sxs-lookup"><span data-stu-id="dbafa-235">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="dbafa-236">Selecione os tipos de arquivos de imagem que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="dbafa-236">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="dbafa-237">Escolha uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="dbafa-237">Choose one of the following:</span></span>

    -   <span data-ttu-id="dbafa-238">Para alterar os arquivos na imagem de recuperação antes de criar os arquivos de imagem, marque a caixa de seleção **Editar imagem** e clique em **preparar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-238">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="dbafa-239">Para criar a imagem de recuperação sem alterar os arquivos, clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-239">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="dbafa-240">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dbafa-240">Click **Next**.</span></span>

## <span data-ttu-id="dbafa-241">Editar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-241">Edit the recovery image files</span></span>


<span data-ttu-id="dbafa-242">Você pode editar a imagem de recuperação somente se tiver marcado a caixa de seleção Editar imagem na página Criar imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-242">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="dbafa-243">Depois que a imagem de recuperação tiver sido preparada para edição, você poderá adicionar e modificar os arquivos de imagem de recuperação antes de criar a mídia inicializável.</span><span class="sxs-lookup"><span data-stu-id="dbafa-243">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="dbafa-244">Por exemplo, você pode criar uma ordem personalizada para a inicialização, adicionar várias ferramentas de terceiros e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="dbafa-244">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="dbafa-245">Para editar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-245">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="dbafa-246">Na página **Editar imagem** , clique em **abrir** no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="dbafa-246">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="dbafa-247">Crie uma subpasta na pasta listada na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dbafa-247">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="dbafa-248">Copie os arquivos que você deseja para a nova subpasta ou remova os arquivos que não deseja.</span><span class="sxs-lookup"><span data-stu-id="dbafa-248">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="dbafa-249">Clique em **criar** para começar a criar a imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dbafa-249">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="dbafa-250">Gerar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-250">Generate the recovery image files</span></span>


<span data-ttu-id="dbafa-251">Na página gerar arquivos, a imagem de recuperação do DaRT é gerada para os tipos de arquivo selecionados na página Criar imagem.</span><span class="sxs-lookup"><span data-stu-id="dbafa-251">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="dbafa-252">Para gerar os arquivos de imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="dbafa-252">To generate the recovery image files</span></span>**

-   <span data-ttu-id="dbafa-253">Na página **gerar arquivos** , clique em **Avançar** para gerar os arquivos de imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dbafa-253">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="dbafa-254">Copiar a imagem de recuperação para um CD, DVD ou USB</span><span class="sxs-lookup"><span data-stu-id="dbafa-254">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="dbafa-255">Na página Criar mídia inicializável, você pode copiar opcionalmente o arquivo de imagem para um CD, DVD ou unidade flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="dbafa-255">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="dbafa-256">Você também pode criar mídia inicializável adicional desta página reiniciando o assistente.</span><span class="sxs-lookup"><span data-stu-id="dbafa-256">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="dbafa-257">**Observação**  O ambiente de execução de pré-inicialização (PXE) e a implantação de imagens locais não são suportados nativamente por essa ferramenta, pois exigem ferramentas empresariais adicionais, como o System Center Configuration Manager Server e o Microsoft Development Toolkit.</span><span class="sxs-lookup"><span data-stu-id="dbafa-257">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="dbafa-258">Para copiar a imagem de recuperação para um CD, DVD ou USB</span><span class="sxs-lookup"><span data-stu-id="dbafa-258">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="dbafa-259">Na página **criar mídia inicializável** , selecione o arquivo ISO que você deseja copiar.</span><span class="sxs-lookup"><span data-stu-id="dbafa-259">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="dbafa-260">Insira um CD, DVD ou USB e selecione a unidade.</span><span class="sxs-lookup"><span data-stu-id="dbafa-260">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="dbafa-261">**Observação**  Se uma unidade não for reconhecida e você instalar uma nova unidade, você poderá clicar em **Atualizar** para forçar o assistente a atualizar a lista de unidades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dbafa-261">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="dbafa-262">Clique no botão **criar mídia inicializável** .</span><span class="sxs-lookup"><span data-stu-id="dbafa-262">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="dbafa-263">Para criar outra imagem de recuperação, clique em reiniciar ou clique em **fechar** se terminar de criar todas as mídias desejadas.</span><span class="sxs-lookup"><span data-stu-id="dbafa-263">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="dbafa-264">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbafa-264">Related topics</span></span>


[<span data-ttu-id="dbafa-265">Visão geral das ferramentas do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="dbafa-265">Overview of the Tools in DaRT 8.0</span></span>](overview-of-the-tools-in-dart-80-dart-8.md)

[<span data-ttu-id="dbafa-266">Implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="dbafa-266">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





