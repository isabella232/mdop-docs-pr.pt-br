---
title: Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)
description: Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797165"
---
# <span data-ttu-id="267ae-103">Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="267ae-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="267ae-104">Você pode usar aceleradores de pacotes do App-V para gerar automaticamente um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="267ae-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="267ae-105">Depois de criar um acelerador de pacote com êxito, você poderá reutilizar e compartilhar o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="267ae-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="267ae-106">Para obter mais informações sobre aceleradores de pacote, consulte [sobre o app-v Package Accelerators (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="267ae-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="267ae-107">A criação de aceleradores de pacotes do App-V é uma tarefa avançada.</span><span class="sxs-lookup"><span data-stu-id="267ae-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="267ae-108">Os aceleradores de pacote podem conter informações específicas de senha e usuário.</span><span class="sxs-lookup"><span data-stu-id="267ae-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="267ae-109">Portanto, você deve salvar aceleradores de pacotes e a mídia de instalação associada em um local seguro e deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o fornecedor possa ser verificado quando o acelerador de pacotes do App-V for aplicado.</span><span class="sxs-lookup"><span data-stu-id="267ae-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="267ae-110">Em algumas situações, para criar o acelerador de pacote, talvez seja necessário instalar o aplicativo localmente no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="267ae-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="267ae-111">Primeiro, tente criar o acelerador de pacote usando a mídia de instalação e, se houver vários arquivos ausentes necessários, instale o aplicativo localmente no computador que executa o sequenciador e crie o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="267ae-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="267ae-112">Importante</span><span class="sxs-lookup"><span data-stu-id="267ae-112">Important</span></span>**  
<span data-ttu-id="267ae-113">Antes de começar o procedimento a seguir, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="267ae-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="267ae-114">Copie o pacote de aplicativo virtual que você deve usar para criar o acelerador de pacote localmente para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="267ae-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="267ae-115">Copie todos os arquivos de instalação necessários associados ao pacote de aplicativo virtual para o computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="267ae-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="267ae-116">Importante</span><span class="sxs-lookup"><span data-stu-id="267ae-116">Important</span></span>**  
<span data-ttu-id="267ae-117">Aviso de isenção de responsabilidade: o Microsoft Application Virtualization Sequencer não lhe concede nenhum direito de licença para o aplicativo de software que você está usando para criar um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="267ae-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="267ae-118">Você deve obedecer a todos os termos de licença de usuário final para tal aplicativo.</span><span class="sxs-lookup"><span data-stu-id="267ae-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="267ae-119">É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="267ae-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="267ae-120">Para criar um acelerador de pacote App-V</span><span class="sxs-lookup"><span data-stu-id="267ae-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="267ae-121">Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.</span><span class="sxs-lookup"><span data-stu-id="267ae-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="267ae-122">Para iniciar o assistente app-v **Create Package Accelerator** na App-v Sequencer, clique em **ferramentas**  /  **Create Package Accelerator**.</span><span class="sxs-lookup"><span data-stu-id="267ae-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="267ae-123">Na página **selecionar pacote** , para especificar um pacote de aplicativo virtual existente a ser usado para criar o acelerador de pacote, clique em **procurar**e localize o pacote de aplicativo virtual existente (arquivo. sprj).</span><span class="sxs-lookup"><span data-stu-id="267ae-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="267ae-124">Dica</span><span class="sxs-lookup"><span data-stu-id="267ae-124">Tip</span></span>**  
    <span data-ttu-id="267ae-125">Copie os arquivos associados ao pacote de aplicativo virtual que você planeja usar localmente para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="267ae-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="267ae-126">Na página **arquivos de instalação** , para especificar a pasta que contém os arquivos de instalação que você usou para criar o pacote de aplicativo virtual original, clique em **procurar**e selecione o diretório que contém os arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="267ae-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="267ae-127">Dica</span><span class="sxs-lookup"><span data-stu-id="267ae-127">Tip</span></span>**  
   <span data-ttu-id="267ae-128">Copie a pasta que contém os arquivos de instalação necessários para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="267ae-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="267ae-129">Na página **coletando informações** , examine os arquivos que não foram encontrados no local especificado na página **arquivos de instalação** deste assistente.</span><span class="sxs-lookup"><span data-stu-id="267ae-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="267ae-130">Se os arquivos exibidos não forem necessários, selecione **remover estes arquivos**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="267ae-131">Se os arquivos forem necessários, clique em **anterior** e copie os arquivos necessários para o diretório especificado na página **arquivos de instalação** .</span><span class="sxs-lookup"><span data-stu-id="267ae-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="267ae-132">Observação</span><span class="sxs-lookup"><span data-stu-id="267ae-132">Note</span></span>**  
   <span data-ttu-id="267ae-133">Você deve remover os arquivos desnecessários ou clicar em **anterior** e localizar os arquivos necessários para avançar para a próxima página deste assistente.</span><span class="sxs-lookup"><span data-stu-id="267ae-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="267ae-134">Na página **selecionar arquivos** , examine atentamente os arquivos detectados e desmarque todos os arquivos que devem ser removidos do acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="267ae-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="267ae-135">Selecione apenas os arquivos necessários para que o aplicativo seja executado com êxito e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="267ae-136">Na página **verificar aplicativos** , confirme se todos os arquivos de instalação necessários para compilar o pacote são exibidos.</span><span class="sxs-lookup"><span data-stu-id="267ae-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="267ae-137">Quando o acelerador de pacote é usado para criar um novo pacote, todos os arquivos de instalação exibidos no painel **aplicativos** são necessários para criar o pacote.</span><span class="sxs-lookup"><span data-stu-id="267ae-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="267ae-138">Se necessário, para adicionar outros arquivos do instalador, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="267ae-139">Para remover arquivos de instalação desnecessários, selecione o arquivo de instalação e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="267ae-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="267ae-140">Para editar as propriedades associadas a um instalador, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="267ae-141">Os arquivos de instalação especificados nesta etapa serão obrigatórios quando o acelerador de pacote for usado para criar um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="267ae-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="267ae-142">Depois de confirmar as informações exibidas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="267ae-143">Na página **selecionar orientação** , para especificar um arquivo que contenha informações sobre como o acelerador de pacote, clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="267ae-144">Por exemplo, esse arquivo pode conter informações sobre como o computador que executa o sequenciador deve ser configurado, informações de pré-requisito do aplicativo para computadores de destino e anotações gerais.</span><span class="sxs-lookup"><span data-stu-id="267ae-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="267ae-145">Você deve fornecer todas as informações necessárias para que o acelerador de pacote seja aplicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="267ae-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="267ae-146">O arquivo que você selecionar deve estar no formato Rich Text (. rtf) ou arquivo de texto (. txt).</span><span class="sxs-lookup"><span data-stu-id="267ae-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="267ae-147">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-147">Click **Next**.</span></span>

9. <span data-ttu-id="267ae-148">Na página **Create Package Accelerator** , para especificar onde salvar o acelerador de pacote, clique em **procurar** e selecione o diretório.</span><span class="sxs-lookup"><span data-stu-id="267ae-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="267ae-149">Na página **conclusão** , para fechar o assistente **criar acelerador de pacote** , clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="267ae-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="267ae-150">Importante</span><span class="sxs-lookup"><span data-stu-id="267ae-150">Important</span></span>**  
   <span data-ttu-id="267ae-151">Para ajudar a garantir que o acelerador do pacote seja o mais seguro possível e para que o fornecedor possa ser verificado quando o acelerador de pacote é aplicado, você sempre deve assinar digitalmente o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="267ae-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="267ae-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="267ae-152">Related topics</span></span>


<span data-ttu-id="267ae-153">Configurando o Application Virtualization Sequencer (App-V 4,6 SP1) [como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="267ae-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>









