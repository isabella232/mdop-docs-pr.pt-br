---
title: Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)
description: Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797914"
---
# <span data-ttu-id="ece21-103">Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="ece21-103">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>


<span data-ttu-id="ece21-104">Você pode usar aceleradores de pacotes do App-V para gerar automaticamente um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="ece21-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="ece21-105">Para obter mais informações sobre aceleradores de pacote, consulte [sobre o app-v Package Accelerators (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="ece21-105">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="ece21-106">Importante</span><span class="sxs-lookup"><span data-stu-id="ece21-106">Important</span></span>**  
<span data-ttu-id="ece21-107">Aviso de isenção de responsabilidade: o aplicativo de sequência de virtualização do aplicativo não lhe concede nenhum direito de licença para o aplicativo de software que você está usando para criar um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-107">Disclaimer: The Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="ece21-108">Você deve obedecer a todos os termos de licença de usuário final para tal aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ece21-108">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="ece21-109">É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ece21-109">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="ece21-110">Observação</span><span class="sxs-lookup"><span data-stu-id="ece21-110">Note</span></span>**  
<span data-ttu-id="ece21-111">Antes de iniciar este procedimento, copie o acelerador de pacote necessário localmente para o computador executando o sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="ece21-111">Before starting this procedure, copy the required Package Accelerator locally to the computer running the App-V Sequencer.</span></span> <span data-ttu-id="ece21-112">Você também deve copiar todos os arquivos de instalação necessários para o pacote para um diretório local no computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="ece21-112">You should also copy all required installation files for the package to a local directory on the computer running the Sequencer.</span></span> <span data-ttu-id="ece21-113">Este é o diretório que você precisa especificar na etapa 5 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="ece21-113">This is the directory that you have to specify in step 5 of this procedure.</span></span>



<span data-ttu-id="ece21-114">Use o procedimento a seguir para criar um pacote de aplicativo virtual usando um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-114">Use the following procedure to create a virtual application package by using a Package Accelerator.</span></span>

**<span data-ttu-id="ece21-115">Para criar um pacote de aplicativo virtual usando um acelerador de pacote App-V</span><span class="sxs-lookup"><span data-stu-id="ece21-115">To create a virtual application package by using an App-V Package Accelerator</span></span>**

1. <span data-ttu-id="ece21-116">Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ece21-116">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="ece21-117">Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**.</span><span class="sxs-lookup"><span data-stu-id="ece21-117">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="ece21-118">Para criar o pacote, marque a caixa de seleção **criar um pacote usando um acelerador de pacote** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-118">To create the package, select the **Create Package using a Package Accelerator** check box, and then click **Next**.</span></span>

3. <span data-ttu-id="ece21-119">Na página **selecionar acelerador de pacote** , para especificar o acelerador de pacote que será usado para criar o novo pacote de aplicativo virtual, clique em **procurar** para localizar o acelerador de pacote que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="ece21-119">On the **Select Package Accelerator** page, to specify the Package Accelerator that will be used to create the new virtual application package, click **Browse** to locate the Package Accelerator that you want to use.</span></span> <span data-ttu-id="ece21-120">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-120">Click **Next**.</span></span>

   **<span data-ttu-id="ece21-121">Importante</span><span class="sxs-lookup"><span data-stu-id="ece21-121">Important</span></span>**  
   <span data-ttu-id="ece21-122">Se o fornecedor do acelerador de pacote não puder ser validado e não contiver uma assinatura digital válida, na caixa de diálogo **aviso de segurança** , você precisará confirmar que confia na fonte do acelerador de pacote antes de clicar em **executar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-122">If the publisher of the Package Accelerator cannot be verified and does not contain a valid digital signature, in the **Security Warning** dialog box, you must confirm that you trust the source of the Package Accelerator before you click **Run**.</span></span>



4. <span data-ttu-id="ece21-123">Na página **orientação** , examine as informações de orientação de publicação exibidas no painel de informações.</span><span class="sxs-lookup"><span data-stu-id="ece21-123">On the **Guidance** page, review the publishing guidance information displayed in the information pane.</span></span> <span data-ttu-id="ece21-124">As informações exibidas foram adicionadas quando o acelerador do pacote foi criado e contém informações sobre a criação e a publicação do pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-124">The information displayed was added when the Package Accelerator was created and contains information about creating and publishing the package.</span></span> <span data-ttu-id="ece21-125">Para exportar as informações de orientação para um arquivo de texto (. txt), clique em **Exportar** e especifique o local onde o arquivo deve ser salvo e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-125">To export the guidance information to a text (.txt) file, click **Export** and specify the location where the file should be saved, and then click **Next**.</span></span>

5. <span data-ttu-id="ece21-126">Na página **selecionar arquivos de instalação** , para criar uma pasta local que contenha todos os arquivos de instalação necessários para o pacote, clique em **criar nova pasta** e especifique onde a pasta deve ser salva.</span><span class="sxs-lookup"><span data-stu-id="ece21-126">On the **Select Installation Files** page, to create a local folder that contains all required installation files for the package, click **Make New Folder** and specify where the folder should be saved.</span></span> <span data-ttu-id="ece21-127">Você também deve especificar um nome a ser atribuído à pasta.</span><span class="sxs-lookup"><span data-stu-id="ece21-127">You must also specify a name to be assigned to the folder.</span></span> <span data-ttu-id="ece21-128">Em seguida, você deve copiar todos os arquivos de instalação necessários para o local que você especificou.</span><span class="sxs-lookup"><span data-stu-id="ece21-128">You must then copy all required installation files to the location that you specified.</span></span> <span data-ttu-id="ece21-129">Se a pasta que contém os arquivos de instalação já existir no computador que executa o sequenciador, clique em **procurar** para selecionar a pasta.</span><span class="sxs-lookup"><span data-stu-id="ece21-129">If the folder that contains the installation files already exists on the computer running the Sequencer, click **Browse** to select the folder.</span></span>

   <span data-ttu-id="ece21-130">Ou, se você já tiver copiado os arquivos de instalação para um diretório neste computador, clique em **criar nova pasta**, navegue até a pasta que contém os arquivos de instalação e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-130">Alternatively, if you have already copied the installation files to a directory on this computer, click **Make New Folder**, browse to the folder that contains the installation files, and then click **Next**.</span></span>

   **<span data-ttu-id="ece21-131">Observação</span><span class="sxs-lookup"><span data-stu-id="ece21-131">Note</span></span>**  
   <span data-ttu-id="ece21-132">Você pode especificar os seguintes tipos de arquivos de instalação com suporte:</span><span class="sxs-lookup"><span data-stu-id="ece21-132">You can specify the following types of supported installation files:</span></span>

   -   <span data-ttu-id="ece21-133">Arquivos do Windows Installer (**. msi**</span><span class="sxs-lookup"><span data-stu-id="ece21-133">Windows Installer files(**.msi**</span></span>

   -   <span data-ttu-id="ece21-134">arquivos. cab</span><span class="sxs-lookup"><span data-stu-id="ece21-134">.cab files</span></span>

   -   <span data-ttu-id="ece21-135">Arquivos compactados com uma extensão de nome de arquivo. zip</span><span class="sxs-lookup"><span data-stu-id="ece21-135">Compressed files with a .zip file name extension</span></span>

   -   <span data-ttu-id="ece21-136">Os arquivos de aplicativo reais</span><span class="sxs-lookup"><span data-stu-id="ece21-136">The actual application files</span></span>

   <span data-ttu-id="ece21-137">Não há suporte para os seguintes tipos de arquivo: arquivos **. msp** e <strong> . exe </strong> .</span><span class="sxs-lookup"><span data-stu-id="ece21-137">The following file types are not supported: **.msp** and<strong>.exe</strong> files.</span></span> <span data-ttu-id="ece21-138">Se você especificar um arquivo **. exe** , deverá extrair os arquivos de instalação manualmente.</span><span class="sxs-lookup"><span data-stu-id="ece21-138">If you specify an **.exe** file you must extract the installation files manually.</span></span>



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. <span data-ttu-id="ece21-139">Na página **nome do pacote** , especifique um nome que será associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-139">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="ece21-140">O nome especificado identifica o pacote no console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="ece21-140">The name specified identifies the package in the App-V Management Console.</span></span> <span data-ttu-id="ece21-141">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-141">Click **Next**.</span></span>

7. <span data-ttu-id="ece21-142">Na página **criar pacote** , forneça comentários que serão associados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-142">On the **Create Package** page, provide comments that will be associated with the package.</span></span> <span data-ttu-id="ece21-143">Os comentários devem conter informações de identificação sobre o pacote que você está criando.</span><span class="sxs-lookup"><span data-stu-id="ece21-143">The comments should contain identifying information about the package you are creating.</span></span> <span data-ttu-id="ece21-144">Para confirmar o local em que o pacote foi criado, examine as informações exibidas em **local para salvar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-144">To confirm the location where the package is created, review the information displayed in **Save Location**.</span></span> <span data-ttu-id="ece21-145">Para compactar o pacote, selecione **compactar pacote**.</span><span class="sxs-lookup"><span data-stu-id="ece21-145">To compress the package, select **Compress Package**.</span></span> <span data-ttu-id="ece21-146">Marque a caixa de seleção **compactar pacote** se o pacote for transmitido na rede ou quando o tamanho do pacote exceder 4 GB.</span><span class="sxs-lookup"><span data-stu-id="ece21-146">Select the **Compress Package** check box if the package will be streamed across the network, or when the package size exceeds 4 GB.</span></span>

   <span data-ttu-id="ece21-147">Para criar o pacote, clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-147">To create the package, click **Create**.</span></span> <span data-ttu-id="ece21-148">Após a criação do pacote, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-148">After the package has been created, click **Next**.</span></span>

8. <span data-ttu-id="ece21-149">Na página **configurar software** , para habilitar o sequenciador para configurar os aplicativos contidos no pacote, selecione **configurar software**.</span><span class="sxs-lookup"><span data-stu-id="ece21-149">On the **Configure Software** page, to enable the Sequencer to configure the applications contained in the package, select **Configure Software**.</span></span> <span data-ttu-id="ece21-150">Esta etapa é útil para configurar quaisquer tarefas associadas que devem ser concluídas para executar o aplicativo em computadores de destino, como a configuração de qualquer contrato de licença associado.</span><span class="sxs-lookup"><span data-stu-id="ece21-150">This step is useful for configuring any associated tasks that must be completed to run the application on target computers, such as configuring any associated license agreements.</span></span>

   <span data-ttu-id="ece21-151">Se você selecionar **configurar software**, os seguintes itens serão configurados pelo sequenciador como parte desta etapa:</span><span class="sxs-lookup"><span data-stu-id="ece21-151">If you select **Configure Software**, the following items are configured by the Sequencer as part of this step:</span></span>

   -   <span data-ttu-id="ece21-152">**Carregar pacote**.</span><span class="sxs-lookup"><span data-stu-id="ece21-152">**Load Package**.</span></span> <span data-ttu-id="ece21-153">O sequenciador carrega os arquivos associados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-153">The Sequencer loads the files associated with the package.</span></span> <span data-ttu-id="ece21-154">Pode demorar vários segundos até uma hora para decodificar o pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-154">It can take several seconds to up to an hour to decode the package.</span></span>

   -   <span data-ttu-id="ece21-155">**Executar cada programa**.</span><span class="sxs-lookup"><span data-stu-id="ece21-155">**Run Each Program**.</span></span> <span data-ttu-id="ece21-156">Opcionalmente, execute os programas contidos no pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-156">Optionally run the programs contained in the package.</span></span> <span data-ttu-id="ece21-157">Esta etapa é útil para concluir todas as tarefas de configuração ou licença associadas que são necessárias para executar o aplicativo antes de implantar e executar o pacote nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="ece21-157">This step is helpful for completing any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="ece21-158">Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**.</span><span class="sxs-lookup"><span data-stu-id="ece21-158">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="ece21-159">Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**.</span><span class="sxs-lookup"><span data-stu-id="ece21-159">To run specific programs, select the program or programs you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="ece21-160">Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ece21-160">Complete the required configuration tasks, and then close the applications.</span></span> <span data-ttu-id="ece21-161">Pode demorar vários minutos para que todos os programas sejam executados.</span><span class="sxs-lookup"><span data-stu-id="ece21-161">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="ece21-162">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-162">Click **Next**.</span></span>

   -   <span data-ttu-id="ece21-163">**Salve o pacote**.</span><span class="sxs-lookup"><span data-stu-id="ece21-163">**Save Package**.</span></span> <span data-ttu-id="ece21-164">O sequenciador salva o pacote.</span><span class="sxs-lookup"><span data-stu-id="ece21-164">The Sequencer saves the package.</span></span>

   -   <span data-ttu-id="ece21-165">**Bloco de recursos primário**.</span><span class="sxs-lookup"><span data-stu-id="ece21-165">**Primary Feature Block**.</span></span> <span data-ttu-id="ece21-166">O sequenciador otimiza o pacote para streaming recriando o bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="ece21-166">The Sequencer optimizes the package for streaming by rebuilding the primary feature block.</span></span>

   <span data-ttu-id="ece21-167">Se você não quiser configurar os aplicativos, clique em **ignorar esta etapa**e vá para a etapa 9 deste procedimento e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-167">If you do not want to configure the applications, click **Skip this step**, and to go to step 9 of this procedure, and then click **Next**.</span></span>

9. <span data-ttu-id="ece21-168">Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativo virtual** , clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="ece21-168">On the **Completion** page, after you have reviewed the information displayed in the **Virtual Application Package Report** pane, click **Close**.</span></span>

   <span data-ttu-id="ece21-169">O pacote agora está disponível no sequenciador.</span><span class="sxs-lookup"><span data-stu-id="ece21-169">The package is now available in the Sequencer.</span></span> <span data-ttu-id="ece21-170">Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**.</span><span class="sxs-lookup"><span data-stu-id="ece21-170">To edit the package properties, click **Edit \[Package Name\]**.</span></span> <span data-ttu-id="ece21-171">Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="ece21-171">For more information about modifying a package, see [How to Modify an Existing Virtual Application Package (App-V 4.6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).</span></span>

## <span data-ttu-id="ece21-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ece21-172">Related topics</span></span>


[<span data-ttu-id="ece21-173">Configuração do Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="ece21-173">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="ece21-174">Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="ece21-174">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









