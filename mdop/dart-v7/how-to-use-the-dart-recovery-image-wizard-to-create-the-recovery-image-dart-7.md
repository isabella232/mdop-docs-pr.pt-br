---
title: Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação
description: Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799169"
---
# <span data-ttu-id="54bd6-103">Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="54bd6-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="54bd6-104">O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 inclui o **Assistente de imagem de recuperação do DART** que é usado no Windows para criar uma imagem ISO (organização internacional) inicializável (ISO).</span><span class="sxs-lookup"><span data-stu-id="54bd6-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="54bd6-105">Uma imagem ISO é um arquivo que representa o conteúdo bruto de um CD.</span><span class="sxs-lookup"><span data-stu-id="54bd6-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="54bd6-106">O **Assistente de imagem de recuperação do DART** requer as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="54bd6-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="54bd6-107">**Imagem de inicialização**° °, você deve fornecer o caminho de um DVD do Windows 7 ou arquivos de origem do Windows 7 necessários para criar a imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="54bd6-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="54bd6-108">**Seleção**de ferramentas ° °, você pode selecionar as ferramentas a serem incluídas na imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="54bd6-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="54bd6-109">**Conexões remotas**° °, você pode selecionar se deseja que a imagem de recuperação do DART inclua a capacidade de estabelecer uma conexão remota entre o helpdesk e o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="54bd6-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="54bd6-110">**Ferramentas de depuração para Windows**° °, você será solicitado a fornecer o local das ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="54bd6-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="54bd6-111">**Definições para sistema autônomo do sistema de limpeza do sistema**, você pode decidir entre baixar as definições mais recentes no momento em que cria a imagem de recuperação ou baixar as definições mais tarde.</span><span class="sxs-lookup"><span data-stu-id="54bd6-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="54bd6-112">**Drivers**° ° onde você será perguntado se deseja adicionar drivers à imagem ISO.</span><span class="sxs-lookup"><span data-stu-id="54bd6-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="54bd6-113">**Arquivos adicionais**° °, você pode adicionar arquivos à imagem ISO que podem ajudar a diagnosticar problemas.</span><span class="sxs-lookup"><span data-stu-id="54bd6-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="54bd6-114">**Local da imagem ISO**° °, você será solicitado a especificar onde a imagem ISO deve ser localizada.</span><span class="sxs-lookup"><span data-stu-id="54bd6-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="54bd6-115">**Unidade de CD/DVD**° °, você será solicitado a especificar se a unidade de CD ou DVD deve ser usada para gravar o CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="54bd6-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="54bd6-116">**Observação**  O tamanho da imagem ISO pode variar, dependendo das ferramentas que foram selecionadas no assistente de **imagem de recuperação do DART**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="54bd6-117">Para criar a imagem de recuperação usando o assistente de imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="54bd6-118">Siga estas instruções para usar o **Assistente de imagem de recuperação DART** para criar a imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="54bd6-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="54bd6-119">Para selecionar as ferramentas a serem incluídas na imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="54bd6-120">O **Assistente de imagem de recuperação do DART** apresenta uma caixa de diálogo de **seleção de ferramenta** .</span><span class="sxs-lookup"><span data-stu-id="54bd6-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="54bd6-121">Você pode selecionar ou remover as ferramentas da lista de ferramentas a serem incluídas na imagem de recuperação do DaRT, realçando uma ferramenta e clicando nos botões **habilitar** ou **desabilitar** .</span><span class="sxs-lookup"><span data-stu-id="54bd6-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="54bd6-122">Depois de selecionar todas as ferramentas que você deseja incluir na imagem de recuperação, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="54bd6-123">Para adicionar a opção de permitir conectividade remota</span><span class="sxs-lookup"><span data-stu-id="54bd6-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="54bd6-124">Você pode marcar a caixa de seleção **permitir conexões remotas** para fornecer a opção na janela do **conjunto de ferramentas de diagnóstico e recuperação** para estabelecer uma conexão remota entre o agente da assistência técnica e um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="54bd6-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="54bd6-125">Depois que um agente de helpdesk estabelece uma conexão remota, ele pode executar as ferramentas DaRT no computador do usuário final a partir de um local remoto.</span><span class="sxs-lookup"><span data-stu-id="54bd6-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="54bd6-126">Você pode marcar a caixa de seleção **especificar o número da porta** para inserir um número de porta específico que será usado ao estabelecer uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="54bd6-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="54bd6-127">Você pode especificar um número de porta entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="54bd6-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="54bd6-128">Recomendamos que o número da porta seja 1024 ou superior para minimizar a possibilidade de um conflito.</span><span class="sxs-lookup"><span data-stu-id="54bd6-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="54bd6-129">Você também pode criar uma mensagem personalizada que será recebida por um usuário final quando ele estabelecer uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="54bd6-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="54bd6-130">A mensagem pode ter no máximo 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="54bd6-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="54bd6-131">Para obter mais informações sobre como executar remotamente as ferramentas DaRT, consulte [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="54bd6-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="54bd6-132">Para adicionar as ferramentas de depuração para Windows à imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="54bd6-133">Na caixa de diálogo **analisador de falha** do **Assistente de imagem de recuperação DART**, você será solicitado a especificar o local das ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="54bd6-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="54bd6-134">Se não tiver uma cópia das ferramentas, você poderá baixá-las da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="54bd6-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="54bd6-135">O link a seguir para a página de download é fornecido no assistente: [baixar e instalar as ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="54bd6-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="54bd6-136">Você pode especificar o local das ferramentas de depuração no computador no qual você está executando o **Assistente de imagem de recuperação DART**ou pode decidir usar as ferramentas localizadas no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="54bd6-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="54bd6-137">Se você decidir usar uma cópia em outro computador, deve verificar se as ferramentas estão instaladas em cada computador no qual você está diagnosticando uma falha.</span><span class="sxs-lookup"><span data-stu-id="54bd6-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="54bd6-138">**Observação**  Se você incluir o **Crash Analyzer** na imagem ISO, recomendamos que você também inclua as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="54bd6-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="54bd6-139">Siga estas etapas para adicionar as ferramentas de depuração para Windows:</span><span class="sxs-lookup"><span data-stu-id="54bd6-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="54bd6-140">Adicionais Clique no hiperlink para baixar as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="54bd6-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="54bd6-141">Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="54bd6-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="54bd6-142">**Use as ferramentas de depuração para Windows no local a seguir**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="54bd6-143">Se você selecionar essa opção, poderá navegar até o local das ferramentas.</span><span class="sxs-lookup"><span data-stu-id="54bd6-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="54bd6-144">**Localize as ferramentas de depuração para Windows no sistema que você está reparando**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="54bd6-145">Se você selecionar essa opção, o **Crash Analyzer** não funcionará se as ferramentas de depuração para Windows não forem encontradas no computador com problema.</span><span class="sxs-lookup"><span data-stu-id="54bd6-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="54bd6-146">Depois de concluir, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="54bd6-147">Para adicionar definições do standalone System Sweeper à imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="54bd6-148">As definições são um repositório de malware e outros softwares potencialmente indesejados conhecidos.</span><span class="sxs-lookup"><span data-stu-id="54bd6-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="54bd6-149">Como o malware está sendo desenvolvido continuamente, o **standalone System Sweeper** depende das definições atuais para determinar se o software que está tentando instalar, executar ou alterar as configurações em um computador é um software potencialmente indesejado ou mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="54bd6-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="54bd6-150">Para incluir as definições mais recentes na imagem de recuperação do DaRT (recomendado), clique em **Sim, baixar as definições mais recentes.**</span><span class="sxs-lookup"><span data-stu-id="54bd6-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="54bd6-151">A atualização de definição é iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="54bd6-151">The definition update starts automatically.</span></span> <span data-ttu-id="54bd6-152">Você deve estar conectado à Internet para concluir esse processo.</span><span class="sxs-lookup"><span data-stu-id="54bd6-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="54bd6-153">Para ignorar a atualização de definição, clique em **não, baixar manualmente as definições mais tarde**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="54bd6-154">As definições não serão incluídas na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="54bd6-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="54bd6-155">Se você decidir não incluir as definições mais recentes na imagem de recuperação ou se as definições incluídas na imagem de recuperação não estiverem mais atualizadas na hora em que você está pronto para usar a **limpeza do sistema autônomo**, obtenha as definições mais recentes antes de iniciar uma verificação seguindo as instruções fornecidas na limpeza do **sistema autônomo**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="54bd6-156">**Importante**  Não é possível verificar se não há definições.</span><span class="sxs-lookup"><span data-stu-id="54bd6-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="54bd6-157">Depois de concluir, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="54bd6-158">Para adicionar drivers à imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="54bd6-159">**Cuidado**  Por padrão, quando você adiciona um driver à imagem de recuperação do DaRT, todos os arquivos e subpastas adicionais localizados nessa pasta são adicionados à imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="54bd6-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="54bd6-160">Para obter mais informações, consulte solução de problemas para o [DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="54bd6-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="54bd6-161">Você deve incluir drivers adicionais na imagem de recuperação do DaRT7 que pode ser necessário ao reparar um computador.</span><span class="sxs-lookup"><span data-stu-id="54bd6-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="54bd6-162">Geralmente, eles podem incluir armazenamento ou controladores de rede que não estão incluídos no DVD do Windows.</span><span class="sxs-lookup"><span data-stu-id="54bd6-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="54bd6-163">**Importante**  Quando você selecionar os drivers a serem incluídos, lembre-se de que a conectividade sem fio (como Bluetooth ou 802.11 a/b/g/n) não é compatível com o DaRT.</span><span class="sxs-lookup"><span data-stu-id="54bd6-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="54bd6-164">Para adicionar um driver de controlador de rede ou armazenamento à imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="54bd6-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="54bd6-165">Na caixa de diálogo **drivers adicionais** do **Assistente de imagem de recuperação DART**, clique em **Adicionar dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="54bd6-166">Navegue até o arquivo a ser adicionado ao driver e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="54bd6-167">**Observação**  O arquivo de **Driver** é fornecido pelo fabricante do controlador de armazenamento ou de rede.</span><span class="sxs-lookup"><span data-stu-id="54bd6-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="54bd6-168">Repita as etapas 1 e 2 para cada driver que você deseja incluir.</span><span class="sxs-lookup"><span data-stu-id="54bd6-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="54bd6-169">Depois de concluir, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="54bd6-170">Para adicionar arquivos à imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="54bd6-171">Siga estas etapas para adicionar arquivos à imagem de recuperação para que você possa usá-los para diagnosticar problemas do computador.</span><span class="sxs-lookup"><span data-stu-id="54bd6-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="54bd6-172">Na caixa de diálogo **arquivos adicionais** do **Assistente de imagem de recuperação DART**, clique em **Mostrar arquivos**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="54bd6-173">Isso abre uma janela do Explorer que exibe a pasta que contém os arquivos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="54bd6-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="54bd6-174">Crie uma subpasta na pasta listada na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="54bd6-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="54bd6-175">Copie os arquivos que você deseja para a nova subpasta.</span><span class="sxs-lookup"><span data-stu-id="54bd6-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="54bd6-176">Depois de concluir, clique em **Avançar.**</span><span class="sxs-lookup"><span data-stu-id="54bd6-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="54bd6-177">Para selecionar um local para o ISO que contém a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="54bd6-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="54bd6-178">Siga estas etapas para especificar o local onde a imagem ISO é criada:</span><span class="sxs-lookup"><span data-stu-id="54bd6-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="54bd6-179">Na caixa de diálogo **criar imagem de inicialização** do **Assistente de imagem de recuperação DART**, clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="54bd6-180">Navegue até o local preferencial na janela **salvar como** e, em seguida, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="54bd6-181">Depois de concluir, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="54bd6-182">O tamanho da imagem ISO vai variar, dependendo das ferramentas selecionadas e dos arquivos que você adicionar no assistente.</span><span class="sxs-lookup"><span data-stu-id="54bd6-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="54bd6-183">O assistente requer que a imagem ISO tenha uma extensão de nome de arquivo **. ISO** porque a maioria dos programas que grava um CD ou DVD requer essa extensão.</span><span class="sxs-lookup"><span data-stu-id="54bd6-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="54bd6-184">Se você não especificar um local diferente, a imagem ISO será criada na área de trabalho com o nome **DaRT70. ISO**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="54bd6-185">Para gravar a imagem de recuperação em um CD ou DVD</span><span class="sxs-lookup"><span data-stu-id="54bd6-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="54bd6-186">Se o **Assistente de imagem de recuperação do DART** detectar uma unidade de CD-RW compatível em seu computador, ele será disponibilizado para gravar a imagem ISO em um disco para você.</span><span class="sxs-lookup"><span data-stu-id="54bd6-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="54bd6-187">Se você quiser gravar um CD ou DVD e o assistente não reconhecer sua unidade, você deverá usar outro programa, como o programa incluído na unidade.</span><span class="sxs-lookup"><span data-stu-id="54bd6-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="54bd6-188">Você pode usar um duplicador, um serviço de duplicação ou um CD ou um software de gravação de DVD para fazer cópias adicionais.</span><span class="sxs-lookup"><span data-stu-id="54bd6-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="54bd6-189">Na caixa de diálogo **gravar em CD/DVD gravável** do **Assistente de imagem de recuperação do DART**, selecione **gravar a imagem na seguinte unidade de CD/DVD gravável**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="54bd6-190">Selecione a unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="54bd6-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="54bd6-191">**Observação**  Se uma unidade não for reconhecida e você instalar uma nova unidade, você poderá clicar em **Atualizar lista de unidades** para forçar o assistente a atualizar a lista de unidades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="54bd6-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="54bd6-192">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="54bd6-192">Click **Next**.</span></span>

## <span data-ttu-id="54bd6-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54bd6-193">Related topics</span></span>


[<span data-ttu-id="54bd6-194">Criação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="54bd6-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





