---
title: Como criar um acelerador de pacote
description: Como criar um acelerador de pacote
author: dansimp
ms.assetid: dfe305e5-7cf8-498f-9581-4805ffc722bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0710bff5e5ea420119ac3c395c2e8917f7c582dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796459"
---
# <span data-ttu-id="e883d-103">Como criar um acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="e883d-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="e883d-104">Aceleradores de pacotes do App-V 5,0 geram automaticamente novos pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="e883d-104">App-V 5.0 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="e883d-105">Observação</span><span class="sxs-lookup"><span data-stu-id="e883d-105">Note</span></span>**  
<span data-ttu-id="e883d-106">Você pode usar o PowerShell para criar um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="e883d-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="e883d-107">Para obter mais informações [, consulte como criar um acelerador de pacote usando o PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="e883d-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span></span>



<span data-ttu-id="e883d-108">Use o procedimento a seguir para criar um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="e883d-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="e883d-109">Importante</span><span class="sxs-lookup"><span data-stu-id="e883d-109">Important</span></span>**  
<span data-ttu-id="e883d-110">Os aceleradores de pacote podem conter informações específicas de senha e usuário.</span><span class="sxs-lookup"><span data-stu-id="e883d-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="e883d-111">Portanto, você deve salvar aceleradores de pacote e a mídia de instalação associada em um local seguro, e deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o fornecedor possa ser verificado quando o acelerador de pacotes do App-V 5,0 for aplicado.</span><span class="sxs-lookup"><span data-stu-id="e883d-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>



**<span data-ttu-id="e883d-112">Importante</span><span class="sxs-lookup"><span data-stu-id="e883d-112">Important</span></span>**  
<span data-ttu-id="e883d-113">Antes de começar o procedimento a seguir, você deve executar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e883d-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="e883d-114">Copie o pacote de aplicativo virtual que você usará para criar o acelerador de pacote localmente para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="e883d-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="e883d-115">Copie todos os arquivos de instalação necessários associados ao pacote de aplicativo virtual para o computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="e883d-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="e883d-116">Para criar um acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="e883d-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="e883d-117">Importante</span><span class="sxs-lookup"><span data-stu-id="e883d-117">Important</span></span>**  
    <span data-ttu-id="e883d-118">O sequenciador do App-V 5,0 não concede direitos de licença para o aplicativo de software que você está usando para criar o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="e883d-118">The App-V 5.0 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="e883d-119">Você deve obedecer a todos os termos de licença de usuário final para o aplicativo que você está usando.</span><span class="sxs-lookup"><span data-stu-id="e883d-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="e883d-120">É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o sequenciador do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e883d-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.0 Sequencer.</span></span>



~~~
To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="e883d-121">Para iniciar o assistente do Gerenciador de **aceleração de criação** do App-v 5,0, no console app-v 5,0 Sequencer, clique em **ferramentas**  /  **criar acelerador**.</span><span class="sxs-lookup"><span data-stu-id="e883d-121">To start the App-V 5.0 **Create Package Accelerator** wizard, in the App-V 5.0 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="e883d-122">Na página **selecionar pacote** , para especificar um pacote de aplicativo virtual existente a ser usado para criar o acelerador de pacote, clique em **procurar**e localize o pacote de aplicativo virtual existente (arquivo. AppV).</span><span class="sxs-lookup"><span data-stu-id="e883d-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="e883d-123">Dica</span><span class="sxs-lookup"><span data-stu-id="e883d-123">Tip</span></span>**  
   <span data-ttu-id="e883d-124">Copie os arquivos associados ao pacote de aplicativo virtual que você planeja usar localmente para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="e883d-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="e883d-125">Na página **arquivos de instalação** , para especificar a pasta que contém os arquivos de instalação que você usou para criar o pacote de aplicativo virtual original, clique em **procurar**e selecione o diretório que contém os arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="e883d-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="e883d-126">Dica</span><span class="sxs-lookup"><span data-stu-id="e883d-126">Tip</span></span>**  
   <span data-ttu-id="e883d-127">Copie a pasta que contém os arquivos de instalação necessários para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="e883d-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="e883d-128">Se o aplicativo já estiver instalado no computador que executa o sequenciador, para especificar o arquivo de instalação, selecione os **arquivos instalados no sistema local**.</span><span class="sxs-lookup"><span data-stu-id="e883d-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="e883d-129">Para usar essa opção, o aplicativo já deve estar instalado no local de instalação padrão.</span><span class="sxs-lookup"><span data-stu-id="e883d-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="e883d-130">Na página **coletando informações** , examine os arquivos que não foram encontrados no local especificado na página **arquivos de instalação** deste assistente.</span><span class="sxs-lookup"><span data-stu-id="e883d-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="e883d-131">Se os arquivos exibidos não forem necessários, selecione **remover estes arquivos**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="e883d-132">Se os arquivos forem necessários, clique em **anterior** e copie os arquivos necessários para o diretório especificado na página **arquivos de instalação** .</span><span class="sxs-lookup"><span data-stu-id="e883d-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="e883d-133">Observação</span><span class="sxs-lookup"><span data-stu-id="e883d-133">Note</span></span>**  
   <span data-ttu-id="e883d-134">Você deve remover os arquivos desnecessários ou clicar em **anterior** e localizar os arquivos necessários para avançar para a próxima página deste assistente.</span><span class="sxs-lookup"><span data-stu-id="e883d-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="e883d-135">Na página **selecionar arquivos** , examine atentamente os arquivos detectados e desmarque todos os arquivos que devem ser removidos do acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="e883d-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="e883d-136">Selecione apenas os arquivos necessários para que o aplicativo seja executado com êxito e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="e883d-137">Na página **verificar aplicativos** , confirme se todos os arquivos de instalação necessários para compilar o pacote são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e883d-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="e883d-138">Quando o acelerador de pacote é usado para criar um novo pacote, todos os arquivos de instalação exibidos no painel **aplicativos** são necessários para criar o pacote.</span><span class="sxs-lookup"><span data-stu-id="e883d-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="e883d-139">Se necessário, para adicionar outros arquivos do instalador, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="e883d-140">Para remover arquivos de instalação desnecessários, selecione o arquivo de instalação e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="e883d-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="e883d-141">Para editar as propriedades associadas a um instalador, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="e883d-142">Os arquivos de instalação especificados nesta etapa serão obrigatórios quando o acelerador de pacote for usado para criar um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="e883d-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="e883d-143">Depois de confirmar as informações exibidas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="e883d-144">Na página **selecionar orientação** , para especificar um arquivo que contenha informações sobre como o acelerador de pacote, clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="e883d-145">Por exemplo, esse arquivo pode conter informações sobre como o computador que executa o sequenciador deve ser configurado, informações de pré-requisito do aplicativo para computadores de destino e anotações gerais.</span><span class="sxs-lookup"><span data-stu-id="e883d-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="e883d-146">Você deve fornecer todas as informações necessárias para que o acelerador de pacote seja aplicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e883d-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="e883d-147">O arquivo que você selecionar deve estar no formato Rich Text (. rtf) ou arquivo de texto (. txt).</span><span class="sxs-lookup"><span data-stu-id="e883d-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="e883d-148">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-148">Click **Next**.</span></span>

10. <span data-ttu-id="e883d-149">Na página **Create Package Accelerator** , para especificar onde salvar o acelerador de pacote, clique em **procurar** e selecione o diretório.</span><span class="sxs-lookup"><span data-stu-id="e883d-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="e883d-150">Na página **conclusão** , para fechar o assistente **criar acelerador de pacote** , clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="e883d-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="e883d-151">Importante</span><span class="sxs-lookup"><span data-stu-id="e883d-151">Important</span></span>**  
   <span data-ttu-id="e883d-152">Para ajudar a garantir que o acelerador do pacote seja o mais seguro possível e para que o fornecedor possa ser verificado quando o acelerador de pacote é aplicado, você sempre deve assinar digitalmente o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="e883d-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="e883d-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e883d-153">Related topics</span></span>


[<span data-ttu-id="e883d-154">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e883d-154">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="e883d-155">Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="e883d-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)









