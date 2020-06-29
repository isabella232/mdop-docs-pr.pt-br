---
title: Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V
description: Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V
author: dansimp
ms.assetid: eae1e4f8-f14f-4bc8-9867-052561c37297
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15376ae52a19b2d220f9ea0031f3ad5649ca487d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796458"
---
# <span data-ttu-id="6f84c-103">Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="6f84c-103">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>


**<span data-ttu-id="6f84c-104">Importante</span><span class="sxs-lookup"><span data-stu-id="6f84c-104">Important</span></span>**  
<span data-ttu-id="6f84c-105">O sequenciador do App-V 5,1 não concede direitos de licença para o aplicativo de software que você usa para criar o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-105">The App-V 5.1 Sequencer does not grant any license rights to the software application that you use to create the Package Accelerator.</span></span> <span data-ttu-id="6f84c-106">Você deve obedecer a todos os termos de licença de usuário final para o aplicativo que você usa.</span><span class="sxs-lookup"><span data-stu-id="6f84c-106">You must abide by all end user license terms for the application that you use.</span></span> <span data-ttu-id="6f84c-107">É sua responsabilidade ter certeza de que os termos de licença do aplicativo de software permitem que você crie um acelerador de pacote com o sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6f84c-107">It is your responsibility to make sure that the software application’s license terms allow you to create a Package Accelerator with the App-V 5.1 Sequencer.</span></span>



<span data-ttu-id="6f84c-108">Use o procedimento a seguir para criar um pacote de aplicativo virtual com o acelerador de pacote do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6f84c-108">Use the following procedure to create a virtual application package with the App-V 5.1 Package Accelerator.</span></span>

**<span data-ttu-id="6f84c-109">Observação</span><span class="sxs-lookup"><span data-stu-id="6f84c-109">Note</span></span>**  
<span data-ttu-id="6f84c-110">Antes de iniciar este procedimento, copie o acelerador de pacote necessário localmente para o computador que executa o sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6f84c-110">Before you start this procedure, copy the required Package Accelerator locally to the computer that runs the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="6f84c-111">Você também deve copiar todos os arquivos de instalação necessários para o pacote para um diretório local no computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="6f84c-111">You should also copy all required installation files for the package to a local directory on the computer that runs the Sequencer.</span></span> <span data-ttu-id="6f84c-112">Este é o diretório que você precisa especificar na etapa 5 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="6f84c-112">This is the directory that you have to specify in step 5 of this procedure.</span></span>



**<span data-ttu-id="6f84c-113">Para criar um pacote de aplicativo virtual com um acelerador de pacote do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="6f84c-113">To create a virtual application package with an App-V 5.1 Package Accelerator</span></span>**

1.  <span data-ttu-id="6f84c-114">Para iniciar o sequenciador do App-v, no computador que executa o sequenciador do App-v 5,1, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6f84c-114">To start the App-V Sequencer, on the computer that runs the App-V 5.1 Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="6f84c-115">Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-115">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="6f84c-116">Para criar o pacote, marque a caixa de seleção **criar um pacote usando um acelerador de pacote** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-116">To create the package, select the **Create Package using a Package Accelerator** check box, and then click **Next**.</span></span>

3.  <span data-ttu-id="6f84c-117">Para especificar o acelerador de pacote que será usado para criar o novo pacote de aplicativo virtual, clique em **procurar** na página **selecionar acelerador de pacote** .</span><span class="sxs-lookup"><span data-stu-id="6f84c-117">To specify the package accelerator that will be used to create the new virtual application package, click **Browse** on the **Select Package Accelerator** page.</span></span> <span data-ttu-id="6f84c-118">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-118">Click **Next**.</span></span>

    **<span data-ttu-id="6f84c-119">Importante</span><span class="sxs-lookup"><span data-stu-id="6f84c-119">Important</span></span>**  
    <span data-ttu-id="6f84c-120">Se o fornecedor do acelerador de pacote não puder ser validado e não contiver uma assinatura digital válida, antes de clicar em **executar**, você precisará confirmar que confia na fonte do acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-120">If the publisher of the package accelerator cannot be verified and does not contain a valid digital signature, then before you click **Run**, you must confirm that you trust the source of the package accelerator.</span></span> <span data-ttu-id="6f84c-121">Confirme sua escolha na caixa de diálogo **aviso de segurança** .</span><span class="sxs-lookup"><span data-stu-id="6f84c-121">Confirm your choice in the **Security Warning** dialog box.</span></span>



4.  <span data-ttu-id="6f84c-122">Na página **orientação** , examine as informações de orientação de publicação exibidas no painel de informações.</span><span class="sxs-lookup"><span data-stu-id="6f84c-122">On the **Guidance** page, review the publishing guidance information that is displayed in the information pane.</span></span> <span data-ttu-id="6f84c-123">Essas informações foram adicionadas quando o acelerador de pacote foi criado e contém orientação sobre como criar e publicar o pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-123">This information was added when the Package Accelerator was created and it contains guidance about how to create and publish the package.</span></span> <span data-ttu-id="6f84c-124">Para exportar as informações de orientação para um arquivo de texto (. txt), clique em **Exportar** e especifique o local onde o arquivo deve ser salvo e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-124">To export the guidance information to a text (.txt) file, click **Export** and specify the location where the file should be saved, and then click **Next**.</span></span>

5.  <span data-ttu-id="6f84c-125">Na página **selecionar arquivos de instalação** , clique em **criar nova pasta** para criar uma pasta local que contenha todos os arquivos de instalação necessários para o pacote e especifique onde a pasta deve ser salva.</span><span class="sxs-lookup"><span data-stu-id="6f84c-125">On the **Select Installation Files** page, click **Make New Folder** to create a local folder that contains all required installation files for the package, and specify where the folder should be saved.</span></span> <span data-ttu-id="6f84c-126">Você também deve especificar um nome a ser atribuído à pasta.</span><span class="sxs-lookup"><span data-stu-id="6f84c-126">You must also specify a name to be assigned to the folder.</span></span> <span data-ttu-id="6f84c-127">Em seguida, você deve copiar todos os arquivos de instalação necessários para o local que você especificou.</span><span class="sxs-lookup"><span data-stu-id="6f84c-127">You must then copy all required installation files to the location that you specified.</span></span> <span data-ttu-id="6f84c-128">Se a pasta que contém os arquivos de instalação já existir no computador que executa o sequenciador, clique em **procurar** para selecionar a pasta.</span><span class="sxs-lookup"><span data-stu-id="6f84c-128">If the folder that contains the installation files already exists on the computer that runs the Sequencer, click **Browse** to select the folder.</span></span>

    <span data-ttu-id="6f84c-129">Ou, se você já tiver copiado os arquivos de instalação para um diretório neste computador, clique em **criar nova pasta**, navegue até a pasta que contém os arquivos de instalação e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-129">Alternatively, if you have already copied the installation files to a directory on this computer, click **Make New Folder**, browse to the folder that contains the installation files, and then click **Next**.</span></span>

    **<span data-ttu-id="6f84c-130">Observação</span><span class="sxs-lookup"><span data-stu-id="6f84c-130">Note</span></span>**  
    <span data-ttu-id="6f84c-131">Você pode especificar os seguintes tipos de arquivos de instalação com suporte:</span><span class="sxs-lookup"><span data-stu-id="6f84c-131">You can specify the following types of supported installation files:</span></span>

    -   <span data-ttu-id="6f84c-132">Arquivos do Windows Installer (**. msi**)</span><span class="sxs-lookup"><span data-stu-id="6f84c-132">Windows Installer files (**.msi**)</span></span>

    -   <span data-ttu-id="6f84c-133">Arquivos cabinet (. cab)</span><span class="sxs-lookup"><span data-stu-id="6f84c-133">Cabinet files (.cab)</span></span>

    -   <span data-ttu-id="6f84c-134">Arquivos compactados com uma extensão de nome de arquivo. zip</span><span class="sxs-lookup"><span data-stu-id="6f84c-134">Compressed files with a .zip file name extension</span></span>

    -   <span data-ttu-id="6f84c-135">Os arquivos de aplicativo reais</span><span class="sxs-lookup"><span data-stu-id="6f84c-135">The actual application files</span></span>

    <span data-ttu-id="6f84c-136">Não há suporte para os seguintes tipos de arquivo: arquivos **. msp** e **. exe** .</span><span class="sxs-lookup"><span data-stu-id="6f84c-136">The following file types are not supported: **.msp** and **.exe** files.</span></span> <span data-ttu-id="6f84c-137">Se você especificar um arquivo **. exe** , deverá extrair os arquivos de instalação manualmente.</span><span class="sxs-lookup"><span data-stu-id="6f84c-137">If you specify an **.exe** file, you must extract the installation files manually.</span></span>



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. <span data-ttu-id="6f84c-138">Na página **nome do pacote** , especifique um nome que será associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-138">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="6f84c-139">O nome que você especificar identifica o pacote no console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="6f84c-139">The name that you specify identifies the package in the App-V Management Console.</span></span> <span data-ttu-id="6f84c-140">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-140">Click **Next**.</span></span>

7. <span data-ttu-id="6f84c-141">Na página **criar pacote** , forneça comentários que serão associados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-141">On the **Create Package** page, provide comments that will be associated with the package.</span></span> <span data-ttu-id="6f84c-142">Os comentários devem conter informações de identificação sobre o pacote que você está criando.</span><span class="sxs-lookup"><span data-stu-id="6f84c-142">The comments should contain identifying information about the package that you are creating.</span></span> <span data-ttu-id="6f84c-143">Para confirmar o local em que o pacote foi criado, revise as informações exibidas no **local de salvamento**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-143">To confirm the location where the package is created, review the information that is displayed in **Save Location**.</span></span> <span data-ttu-id="6f84c-144">Para compactar o pacote, selecione **compactar pacote**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-144">To compress the package, select **Compress Package**.</span></span> <span data-ttu-id="6f84c-145">Marque a caixa de seleção **compactar pacote** se o pacote for transmitido na rede ou quando o tamanho do pacote exceder 4 GB.</span><span class="sxs-lookup"><span data-stu-id="6f84c-145">Select the **Compress Package** check box if the package will be streamed across the network, or when the package size exceeds 4 GB.</span></span>

   <span data-ttu-id="6f84c-146">Para criar o pacote, clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-146">To create the package, click **Create**.</span></span> <span data-ttu-id="6f84c-147">Após a criação do pacote, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-147">After the package is created, click **Next**.</span></span>

8. <span data-ttu-id="6f84c-148">Na página **configurar software** , para habilitar o sequenciador para configurar os aplicativos contidos no pacote, selecione **configurar software**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-148">On the **Configure Software** page, to enable the Sequencer to configure the applications that are contained in the package, select **Configure Software**.</span></span> <span data-ttu-id="6f84c-149">Nesta etapa, você pode configurar todas as tarefas associadas que devem ser concluídas para executar o aplicativo nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="6f84c-149">In this step you can configure any associated tasks that must be completed in order to run the application on the target computers.</span></span> <span data-ttu-id="6f84c-150">Por exemplo, você pode configurar qualquer contrato de licença associado.</span><span class="sxs-lookup"><span data-stu-id="6f84c-150">For example, you can configure any associated license agreements.</span></span>

   <span data-ttu-id="6f84c-151">Se você selecionar **configurar software**, os seguintes itens podem ser configurados usando o sequenciador como parte desta etapa:</span><span class="sxs-lookup"><span data-stu-id="6f84c-151">If you select **Configure Software**, the following items can be configured using the Sequencer as part of this step:</span></span>

   -   <span data-ttu-id="6f84c-152">**Carregar pacote**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-152">**Load Package**.</span></span> <span data-ttu-id="6f84c-153">O sequenciador carrega os arquivos associados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-153">The Sequencer loads the files that are associated with the package.</span></span> <span data-ttu-id="6f84c-154">Pode levar vários segundos a uma hora para decodificar o pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-154">It can take several seconds to an hour to decode the package.</span></span>

   -   <span data-ttu-id="6f84c-155">**Executar cada programa**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-155">**Run Each Program**.</span></span> <span data-ttu-id="6f84c-156">Opcionalmente, execute os programas contidos no pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-156">Optionally run the programs that are contained in the package.</span></span> <span data-ttu-id="6f84c-157">Esta etapa é útil para concluir todas as tarefas ou tarefas de configuração associadas que são necessárias para executar o aplicativo antes de implantar e executar o pacote nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="6f84c-157">This step is helpful to complete any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="6f84c-158">Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-158">To run all the programs at once, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="6f84c-159">Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-159">To run specific programs, select the program or programs that you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="6f84c-160">Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6f84c-160">Complete the required configuration tasks, and then close the applications.</span></span> <span data-ttu-id="6f84c-161">Pode demorar vários minutos para que todos os programas sejam executados.</span><span class="sxs-lookup"><span data-stu-id="6f84c-161">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="6f84c-162">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-162">Click **Next**.</span></span>

   -   <span data-ttu-id="6f84c-163">**Salve o pacote**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-163">**Save Package**.</span></span> <span data-ttu-id="6f84c-164">O sequenciador salva o pacote.</span><span class="sxs-lookup"><span data-stu-id="6f84c-164">The Sequencer saves the package.</span></span>

   -   <span data-ttu-id="6f84c-165">**Bloco de recursos primário**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-165">**Primary Feature Block**.</span></span> <span data-ttu-id="6f84c-166">O sequenciador otimiza o pacote para streaming recriando o bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="6f84c-166">The Sequencer optimizes the package for streaming by rebuilding the primary feature block.</span></span>

   <span data-ttu-id="6f84c-167">Se você não quiser configurar os aplicativos, clique em **ignorar esta etapa**e vá para a etapa 9 deste procedimento e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-167">If you do not want to configure the applications, click **Skip this step**, and to go to step 9 of this procedure, and then click **Next**.</span></span>

9. <span data-ttu-id="6f84c-168">Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativo virtual** , clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-168">On the **Completion** page, after you review the information that is displayed in the **Virtual Application Package Report** pane, click **Close**.</span></span>

   <span data-ttu-id="6f84c-169">O pacote agora está disponível no sequenciador.</span><span class="sxs-lookup"><span data-stu-id="6f84c-169">The package is now available in the Sequencer.</span></span> <span data-ttu-id="6f84c-170">Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**.</span><span class="sxs-lookup"><span data-stu-id="6f84c-170">To edit the package properties, click **Edit \[Package Name\]**.</span></span> <span data-ttu-id="6f84c-171">Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente](how-to-modify-an-existing-virtual-application-package-beta.md).</span><span class="sxs-lookup"><span data-stu-id="6f84c-171">For more information about how to modify a package, see [How to Modify an Existing Virtual Application Package](how-to-modify-an-existing-virtual-application-package-beta.md).</span></span>

   <span data-ttu-id="6f84c-172">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="6f84c-172">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6f84c-173">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6f84c-173">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6f84c-174">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="6f84c-174">Got an App-V issue?</span></span>** <span data-ttu-id="6f84c-175">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6f84c-175">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6f84c-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f84c-176">Related topics</span></span>


[<span data-ttu-id="6f84c-177">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="6f84c-177">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









