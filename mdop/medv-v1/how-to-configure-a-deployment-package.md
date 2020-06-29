---
title: Como configurar um pacote de implantação
description: Como configurar um pacote de implantação
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799774"
---
# <span data-ttu-id="2ecbc-103">Como configurar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="2ecbc-104">O assistente de empacotamento percorre a criação de um pacote criando uma pasta em seu computador local e transferindo todos os arquivos de instalação necessários para a pasta única.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="2ecbc-105">O conteúdo da pasta pode ser movido para várias unidades de mídia removível para distribuição.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="2ecbc-106">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-106">Note</span></span>**  
<span data-ttu-id="2ecbc-107">Um único pacote não pode conter arquivos de instalação para sistemas x86 e x64.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="2ecbc-108">Como criar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="2ecbc-109">Para criar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-109">To create a deployment package</span></span>**

1. <span data-ttu-id="2ecbc-110">Verifique no módulo **imagens** que você criou pelo menos uma imagem empacotada local.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="2ecbc-111">No menu **ferramentas** , selecione **Assistente de empacotamento**.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="2ecbc-112">Na página Bem-vindo ao **Assistente de empacotamento** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="2ecbc-113">Na página **imagem do espaço de trabalho** , marque a caixa de seleção **incluir imagem no pacote** para incluir uma imagem no pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="2ecbc-114">O campo de **imagem** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="2ecbc-115">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-115">Note</span></span>**  
   <span data-ttu-id="2ecbc-116">Uma imagem não é necessária em um pacote do MED-V; o pacote pode ser criado sem uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="2ecbc-117">Nesse caso, a imagem deve ser carregada no servidor para que possa ser descarregada posteriormente pela rede para o cliente ou enviada para uma pasta pré-estágio de imagem.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="2ecbc-118">Clique na lista de **imagens** para ver todas as imagens disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="2ecbc-119">Selecione a imagem a ser copiada para o pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="2ecbc-120">Clique em **Atualizar** para atualizar a lista de imagens disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="2ecbc-121">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-121">Click **Next**.</span></span>

7. <span data-ttu-id="2ecbc-122">Na página **configurações de instalação do MED-v** , selecione o arquivo de instalação do MED-v seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="2ecbc-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="2ecbc-123">No campo **arquivo de instalação do MED-V** , digite o caminho completo do diretório onde o arquivo de instalação está localizado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="2ecbc-124">Clique em **..** . para navegar até o diretório onde o arquivo de instalação está localizado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="2ecbc-125">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-125">Note</span></span>**  
   <span data-ttu-id="2ecbc-126">Este campo é obrigatório, e o assistente não continuará sem um nome de arquivo válido.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="2ecbc-127">No campo **endereço do servidor** , digite o nome ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="2ecbc-128">No campo **porta do servidor** , digite a porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="2ecbc-129">Selecione a caixa de seleção o **servidor é acessado usando HTTPS** para exigir uma conexão HTTPS para se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="2ecbc-130">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="2ecbc-130">Do one of the following:</span></span>

    -   <span data-ttu-id="2ecbc-131">Clique em **configurações de instalação padrão**e, em seguida, clique em **Avançar** para continuar e deixar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="2ecbc-132">Clique em **configurações de instalação personalizadas**e, em seguida, clique em **Avançar** para personalizar as configurações de instalação.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="2ecbc-133">Na página **configurações personalizadas da instalação do MED-V** , no campo **pasta de instalação** , digite o caminho da pasta na qual os arquivos MED-V serão instalados no computador host.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="2ecbc-134">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-134">Note</span></span>**  
            <span data-ttu-id="2ecbc-135">É recomendável usar variáveis no caminho, em vez de constantes, que podem variar de um computador para o computador.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="2ecbc-136">Por exemplo, use *%ProgramFiles%\\MED-V* em vez de *c:\\MED-V*.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="2ecbc-137">Na página **instalações adicionais** , marque a caixa de seleção **incluir a instalação da software de virtualização** para incluir a instalação do Virtual PC no pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="2ecbc-138">O campo **arquivo de instalação** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="2ecbc-139">Digite o caminho completo do arquivo de instalação do software de virtualização ou clique em **...** para navegar até o diretório.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="2ecbc-140">Marque a caixa de seleção **incluir a instalação do Virtual PC QFE** para incluir a instalação da atualização do Virtual PC no pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="2ecbc-141">O campo **arquivo de instalação** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="2ecbc-142">Digite o caminho completo do arquivo de instalação da atualização do Virtual PC ou clique em **..** . para navegar até o diretório.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="2ecbc-143">Marque a caixa de seleção **incluir a instalação do Microsoft .NET framework 2,0** para incluir a instalação do Microsoft .net Framework 2,0 no pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="2ecbc-144">O campo **arquivo de instalação** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="2ecbc-145">Digite o caminho completo do arquivo de instalação do Microsoft .NET Framework 2,0 ou clique em **...** para navegar até o diretório.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="2ecbc-146">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-146">Click **Next**.</span></span>

16. <span data-ttu-id="2ecbc-147">Na página **finalizar** , selecione o local onde o pacote deve ser salvo seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="2ecbc-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="2ecbc-148">No campo **destino do pacote** , digite o caminho completo do diretório em que o pacote deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="2ecbc-149">Clique em **..** . para navegar até o diretório em que os arquivos de instalação devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="2ecbc-150">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-150">Note</span></span>**  
    <span data-ttu-id="2ecbc-151">A criação do pacote pode consumir mais espaço do que o tamanho real do pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="2ecbc-152">Portanto, é recomendável construir o pacote no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="2ecbc-153">Após a criação do pacote, ele pode ser copiado para o USB.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="2ecbc-154">No campo **nome do pacote** , insira um nome para o pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="2ecbc-155">Clique em **concluir** para criar o pacote.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="2ecbc-156">O pacote será criado.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-156">The package is created.</span></span> <span data-ttu-id="2ecbc-157">Isso pode levar alguns minutos.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-157">This might take several minutes.</span></span>

    <span data-ttu-id="2ecbc-158">Após a criação do pacote, será exibida uma mensagem informando que ele foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="2ecbc-159">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-159">Note</span></span>**  
<span data-ttu-id="2ecbc-160">Se você salvou todos os arquivos localmente, e não diretamente na mídia removível, certifique-se de copiar somente o conteúdo da pasta e não a própria pasta para a mídia removível.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="2ecbc-161">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-161">Note</span></span>**  
<span data-ttu-id="2ecbc-162">A mídia removível deve ser grande o suficiente para que o conteúdo do pacote consuma um máximo de apenas três trimestres da memória da mídia removível.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="2ecbc-163">Observação</span><span class="sxs-lookup"><span data-stu-id="2ecbc-163">Note</span></span>**  
<span data-ttu-id="2ecbc-164">Ao criar o pacote, até o dobro do tamanho do pacote real pode ser necessário quando a compilação é concluída.</span><span class="sxs-lookup"><span data-stu-id="2ecbc-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="2ecbc-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ecbc-165">Related topics</span></span>


[<span data-ttu-id="2ecbc-166">Criando uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="2ecbc-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









