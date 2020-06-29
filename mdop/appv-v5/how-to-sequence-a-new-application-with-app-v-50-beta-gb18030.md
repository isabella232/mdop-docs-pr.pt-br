---
title: Como sequenciar um novo aplicativo com o App-V 5.0
description: Como sequenciar um novo aplicativo com o App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796320"
---
# <span data-ttu-id="811af-103">Como sequenciar um novo aplicativo com o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="811af-103">How to Sequence a New Application with App-V 5.0</span></span>


**<span data-ttu-id="811af-104">Para revisar ou fazer antes de iniciar o sequenciamento</span><span class="sxs-lookup"><span data-stu-id="811af-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="811af-105">Determine o tipo de pacote de aplicativo virtualizado que você deseja criar:</span><span class="sxs-lookup"><span data-stu-id="811af-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="811af-106">Tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="811af-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="811af-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="811af-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="811af-108">Standard</span><span class="sxs-lookup"><span data-stu-id="811af-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="811af-109">Cria um pacote que contém um aplicativo ou um pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="811af-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="811af-110">Esta é a opção preferida para a maioria dos tipos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811af-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="811af-111">Complemento ou plug-in</span><span class="sxs-lookup"><span data-stu-id="811af-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="811af-112">Cria um pacote que estende a funcionalidade de um aplicativo padrão, por exemplo, um plug-in para o Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="811af-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="811af-113">Além disso, você pode usar plug-ins para aplicativos instalados nativamente ou para outro pacote vinculado por meio de grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="811af-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="811af-114">Middleware</span><span class="sxs-lookup"><span data-stu-id="811af-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="811af-115">Cria um pacote que é necessário para um aplicativo padrão, por exemplo, Java.</span><span class="sxs-lookup"><span data-stu-id="811af-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="811af-116">Os pacotes middleware são usados para a vinculação a outros pacotes usando grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="811af-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="811af-117">Copie todos os arquivos de instalação necessários para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="811af-118">Crie uma imagem de backup do seu ambiente virtual antes de sequenciar um aplicativo e, em seguida, reverta para essa imagem a cada vez após concluir o sequenciamento de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811af-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="811af-119">Revise os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="811af-119">Review the following items:</span></span>

    -   <span data-ttu-id="811af-120">Se um instalador do aplicativo alterar o acesso de segurança para um arquivo ou diretório novo ou existente, essas alterações não serão capturadas no pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="811af-121">Se demarcadores curtos forem desabilitados para o volume de destino do pacote virtualizado, você também deverá sequenciar o pacote para um volume que tenha sido criado e ainda ter caminhos curtos desativados.</span><span class="sxs-lookup"><span data-stu-id="811af-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="811af-122">Ele não pode ser o volume do sistema.</span><span class="sxs-lookup"><span data-stu-id="811af-122">It cannot be the system volume.</span></span>

    -   <span data-ttu-id="811af-123">A partir do App-V 5,0 SP3, o diretório de aplicativos virtual primário (PVAD) está oculto, mas você pode ativá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="811af-123">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="811af-124">Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="811af-124">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>

**<span data-ttu-id="811af-125">Para sequenciar um novo aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="811af-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="811af-126">No computador que executa o sequenciador, clique em **todos os programas**e, em seguida, clique em **Microsoft Application Virtualization**e, em seguida, clique em **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="811af-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="811af-127">No sequenciador, clique em **criar um novo pacote de aplicativo virtual**.</span><span class="sxs-lookup"><span data-stu-id="811af-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="811af-128">Selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="811af-129">Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou fazer com que o pacote contenha dados desnecessários.</span><span class="sxs-lookup"><span data-stu-id="811af-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="811af-130">Você deve resolver todos os possíveis problemas antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="811af-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="811af-131">Depois de fazer qualquer correção, clique em **Atualizar** para exibir as informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="811af-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="811af-132">Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-132">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="811af-133">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-133">Important</span></span>**  
    <span data-ttu-id="811af-134">Se for necessário desativar o software de verificação de vírus, você deve primeiro verificar o computador que executa o sequenciador para garantir que não seja possível adicionar arquivos indesejados ou mal-intencionados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-134">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="811af-135">Na página **tipo de aplicativo** , clique na caixa de seleção **aplicativo padrão (padrão)** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-135">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5.  <span data-ttu-id="811af-136">Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811af-136">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

    **<span data-ttu-id="811af-137">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-137">Note</span></span>**  
    <span data-ttu-id="811af-138">Se o instalador do aplicativo especificado modificar o acesso de segurança a um arquivo ou diretório, existente ou novo, as alterações associadas não serão capturadas no pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-138">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="811af-139">Na página **nome do pacote** , digite um nome que será associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-139">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="811af-140">Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-140">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="811af-141">O nome do pacote é exibido no console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="811af-141">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="811af-142">O **diretório de aplicativos virtual primário** exibe o caminho onde o aplicativo será instalado nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="811af-142">The **Primary Virtual Application Directory** displays the path where the application will be installed on target computers.</span></span> <span data-ttu-id="811af-143">Para especificar esse local, selecione **procurar**.</span><span class="sxs-lookup"><span data-stu-id="811af-143">To specify this location, select **Browse**.</span></span>

   **<span data-ttu-id="811af-144">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-144">Note</span></span>**  
   <span data-ttu-id="811af-145">A partir do App-V 5,0 SP3, o diretório de aplicativos virtual primário (PVAD) está oculto, mas você pode ativá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="811af-145">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="811af-146">Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="811af-146">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. <span data-ttu-id="811af-147">Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, você poderá continuar a instalar o aplicativo para que o sequenciador possa monitorar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="811af-147">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   **<span data-ttu-id="811af-148">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-148">Important</span></span>**  
   <span data-ttu-id="811af-149">Você sempre deve instalar aplicativos em um local seguro e verificar se nenhum outro usuário está conectado ao computador executando o sequenciador durante o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="811af-149">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="811af-150">Na página **instalação** , aguarde enquanto o sequenciador configura o pacote de aplicativo virtualizado.</span><span class="sxs-lookup"><span data-stu-id="811af-150">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="811af-151">Na página **configurar software** , execute a opção executar os programas contidos no pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-151">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="811af-152">Esta etapa permite concluir todas as tarefas necessárias de licença ou configuração antes de você implantar e executar o pacote em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="811af-152">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="811af-153">Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**.</span><span class="sxs-lookup"><span data-stu-id="811af-153">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="811af-154">Para executar programas específicos, selecione o programa ou programas e, em seguida, clique em **executar selecionado**.</span><span class="sxs-lookup"><span data-stu-id="811af-154">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="811af-155">Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="811af-155">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="811af-156">Talvez seja necessário aguardar alguns minutos para que todos os programas sejam executados.</span><span class="sxs-lookup"><span data-stu-id="811af-156">You may need to wait several minutes for all programs to run.</span></span>

   **<span data-ttu-id="811af-157">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-157">Note</span></span>**  
   <span data-ttu-id="811af-158">Para executar as tarefas de primeira utilização para qualquer aplicativo que não esteja disponível na lista, abra o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811af-158">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="811af-159">As informações associadas serão capturadas durante esta etapa.</span><span class="sxs-lookup"><span data-stu-id="811af-159">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="811af-160">Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativos virtualizados que você acabou de sequenciar.</span><span class="sxs-lookup"><span data-stu-id="811af-160">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="811af-161">Em **informações adicionais**, clique duas vezes em um evento para obter informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="811af-161">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="811af-162">Para continuar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-162">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="811af-163">A página **Personalizar** será exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-163">The **Customize** page is displayed.</span></span> <span data-ttu-id="811af-164">Se você tiver terminado de instalar e configurar o aplicativo virtual, selecione **parar agora** e pule para a etapa 14 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="811af-164">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="811af-165">Para executar qualquer uma das seguintes personalizações, selecione **Personalizar**.</span><span class="sxs-lookup"><span data-stu-id="811af-165">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="811af-166">Prepare o pacote virtual para streaming.</span><span class="sxs-lookup"><span data-stu-id="811af-166">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="811af-167">A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="811af-167">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="811af-168">Especifique os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-168">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="811af-169">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-169">Click **Next**.</span></span>

12. <span data-ttu-id="811af-170">Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="811af-170">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="811af-171">Pode levar alguns minutos para que todos os aplicativos sejam executados.</span><span class="sxs-lookup"><span data-stu-id="811af-171">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="811af-172">Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-172">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="811af-173">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-173">Note</span></span>**  
   <span data-ttu-id="811af-174">Se você não abrir nenhum aplicativo durante esta etapa, o método de streaming padrão será a entrega de streaming sob demanda.</span><span class="sxs-lookup"><span data-stu-id="811af-174">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="811af-175">Isso significa que os aplicativos serão baixados por bit até que possam ser abertos e, em seguida, dependendo de como o carregamento em segundo plano está configurado, carregará o restante do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811af-175">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="811af-176">Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-176">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="811af-177">Para permitir que todos os sistemas operacionais com suporte em seu ambiente executem este pacote, selecione **permitir que este pacote seja executado em qualquer sistema operacional**.</span><span class="sxs-lookup"><span data-stu-id="811af-177">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="811af-178">Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, selecione **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e selecione os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-178">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="811af-179">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-179">Click **Next**.</span></span>

   **<span data-ttu-id="811af-180">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-180">Important</span></span>**  
   <span data-ttu-id="811af-181">Verifique se os sistemas operacionais especificados aqui são suportados pelo aplicativo que você está sequenciando.</span><span class="sxs-lookup"><span data-stu-id="811af-181">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="811af-182">A página **criar pacote** será exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-182">The **Create Package** page is displayed.</span></span> <span data-ttu-id="811af-183">Para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvá-lo usando o editor de pacote**.</span><span class="sxs-lookup"><span data-stu-id="811af-183">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="811af-184">Essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="811af-184">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="811af-185">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-185">Click **Next**.</span></span>

   <span data-ttu-id="811af-186">Para salvar o pacote imediatamente, selecione **salvar o pacote agora** (padrão).</span><span class="sxs-lookup"><span data-stu-id="811af-186">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="811af-187">Adicione **comentários** opcionais a serem associados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-187">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="811af-188">Os comentários são úteis para identificar a versão do programa e outras informações sobre o pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-188">Comments are useful for identifying the program version and other information about the package.</span></span>

   **<span data-ttu-id="811af-189">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-189">Important</span></span>**  
   <span data-ttu-id="811af-190">O sistema não oferece suporte a caracteres que não podem ser impressos em **comentários** e **descrições**.</span><span class="sxs-lookup"><span data-stu-id="811af-190">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="811af-191">A página de **conclusão** será exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-191">The **Completion** page is displayed.</span></span> <span data-ttu-id="811af-192">Examine as informações no painel **relatório do pacote do aplicativo virtual** conforme necessário e clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="811af-192">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="811af-193">Essas informações também estão disponíveis no arquivo **Report.xml** localizado no diretório em que o pacote foi criado.</span><span class="sxs-lookup"><span data-stu-id="811af-193">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="811af-194">O pacote agora está disponível no sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-194">The package is now available in the sequencer.</span></span>

   **<span data-ttu-id="811af-195">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-195">Important</span></span>**  
   <span data-ttu-id="811af-196">Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-196">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="811af-197">Para sequenciar um complemento ou aplicativo de plug-in</span><span class="sxs-lookup"><span data-stu-id="811af-197">To sequence an add-on or plug-in application</span></span>**

1.  

    **<span data-ttu-id="811af-198">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-198">Note</span></span>**  
    <span data-ttu-id="811af-199">Antes de executar o procedimento a seguir, instale o aplicativo pai localmente no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-199">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="811af-200">Ou, se você tiver o aplicativo pai virtualizado, poderá seguir as etapas no complemento ou no fluxo de trabalho de plug-in para descompactar o aplicativo pai no computador.</span><span class="sxs-lookup"><span data-stu-id="811af-200">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>

    <span data-ttu-id="811af-201">Por exemplo, se você estiver sequenciando um plug-in do Microsoft Excel, instale o Microsoft Excel localmente no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-201">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="811af-202">Além disso, instale o aplicativo pai no mesmo diretório em que o aplicativo está instalado nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="811af-202">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="811af-203">Se o plug-in ou complemento for usado com um pacote de aplicativo virtual existente, instale o aplicativo na mesma unidade de aplicativo virtual que foi usada quando você criou o pacote de aplicativo virtual pai.</span><span class="sxs-lookup"><span data-stu-id="811af-203">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="811af-204">\*<strong><em>No sequenciador, clique em \* </em> criar um novo pacote de aplicativo virtual </strong> .</span><span class="sxs-lookup"><span data-stu-id="811af-204">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="811af-205">Selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-205">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="811af-206">Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou fazer com que o pacote contenha dados desnecessários.</span><span class="sxs-lookup"><span data-stu-id="811af-206">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="811af-207">Você deve resolver todos os possíveis problemas antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="811af-207">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="811af-208">Depois de fazer qualquer correção, clique em **Atualizar** para exibir as informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="811af-208">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="811af-209">Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-209">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="811af-210">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-210">Important</span></span>**  
   <span data-ttu-id="811af-211">Se for necessário desativar o software de verificação de vírus, você deve primeiro verificar o computador que executa o sequenciador para garantir que não seja possível adicionar arquivos indesejados ou mal-intencionados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-211">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="811af-212">Na página **tipo de aplicativo** , selecione **complemento ou plug-in**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-212">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="811af-213">Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação para o complemento ou plug-in.</span><span class="sxs-lookup"><span data-stu-id="811af-213">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="811af-214">Se o complemento ou o plug-in não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-214">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="811af-215">Na página **instalar primário** , verifique se o aplicativo principal está instalado no computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-215">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="811af-216">Você também pode expandir um pacote existente que tenha sido salvo localmente no computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-216">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="811af-217">Para fazer isso, clique em **expandir pacote**e, em seguida, selecione o pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-217">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="811af-218">Depois de expandir ou instalar o programa pai, selecione **eu instalei o programa pai primário**.</span><span class="sxs-lookup"><span data-stu-id="811af-218">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="811af-219">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-219">Click **Next**.</span></span>

7. <span data-ttu-id="811af-220">Na página **nome do pacote** , digite um nome que será associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-220">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="811af-221">Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-221">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="811af-222">O nome do pacote será exibido no console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="811af-222">The package name will be displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="811af-223">O **diretório de aplicativos virtual primário** exibe o caminho onde o aplicativo será instalado.</span><span class="sxs-lookup"><span data-stu-id="811af-223">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="811af-224">Para especificar esse local, digite o caminho ou clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="811af-224">To specify this location, type the path, or click **Browse**.</span></span>

   **<span data-ttu-id="811af-225">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-225">Note</span></span>**  
   <span data-ttu-id="811af-226">A partir do App-V 5,0 SP3, o diretório de aplicativos virtual primário (PVAD) está oculto, mas você pode ativá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="811af-226">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="811af-227">Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="811af-227">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="811af-228">Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estão prontos, você pode prosseguir para instalar o plug-in ou o aplicativo de suplemento para que o sequenciador possa monitorar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="811af-228">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="811af-229">Use o processo de instalação do aplicativo para executar a instalação.</span><span class="sxs-lookup"><span data-stu-id="811af-229">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="811af-230">Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar** e localize e execute os arquivos de instalação adicionais.</span><span class="sxs-lookup"><span data-stu-id="811af-230">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="811af-231">Quando tiver terminado a instalação, selecione concluído a **instalação**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-231">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="811af-232">Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativo virtual que você acabou de sequenciar.</span><span class="sxs-lookup"><span data-stu-id="811af-232">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="811af-233">Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento.</span><span class="sxs-lookup"><span data-stu-id="811af-233">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="811af-234">Depois de revisar as informações, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-234">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="811af-235">A página **Personalizar** será exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-235">The **Customize** page is displayed.</span></span> <span data-ttu-id="811af-236">Se você tiver terminado de instalar e configurar o aplicativo virtual, selecione **parar agora** e pule para a etapa 12 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="811af-236">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="811af-237">Para executar qualquer uma das seguintes personalizações, selecione **Personalizar**.</span><span class="sxs-lookup"><span data-stu-id="811af-237">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="811af-238">Otimize como o pacote será executado em uma rede lenta ou não confiável.</span><span class="sxs-lookup"><span data-stu-id="811af-238">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="811af-239">Especifique os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-239">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="811af-240">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-240">Click **Next**.</span></span>

11. <span data-ttu-id="811af-241">Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="811af-241">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="811af-242">A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino em redes de alta latência.</span><span class="sxs-lookup"><span data-stu-id="811af-242">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="811af-243">Pode levar alguns minutos para que todos os aplicativos sejam executados.</span><span class="sxs-lookup"><span data-stu-id="811af-243">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="811af-244">Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="811af-244">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="811af-245">Você também pode configurar o pacote para ser totalmente baixado antes de abrir marcando a caixa de seleção **forçar aplicativos a serem baixados** .</span><span class="sxs-lookup"><span data-stu-id="811af-245">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="811af-246">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-246">Click **Next**.</span></span>

   **<span data-ttu-id="811af-247">Observação</span><span class="sxs-lookup"><span data-stu-id="811af-247">Note</span></span>**  
   <span data-ttu-id="811af-248">Se necessário, você pode interromper o carregamento de um aplicativo durante esta etapa.</span><span class="sxs-lookup"><span data-stu-id="811af-248">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="811af-249">Na caixa de diálogo **Iniciar aplicativo** , clique em **parar** e marque uma das caixas de seleção: **interromper todos os aplicativos** ou **interromper somente este aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="811af-249">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="811af-250">Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-250">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="811af-251">Para permitir que todos os sistemas operacionais com suporte em seu ambiente executem este pacote, marque a caixa de seleção **permitir que este pacote seja executado em qualquer sistema operacional** .</span><span class="sxs-lookup"><span data-stu-id="811af-251">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="811af-252">Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, marque a caixa de seleção **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e, em seguida, selecione os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-252">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="811af-253">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-253">Click **Next**.</span></span>

13. <span data-ttu-id="811af-254">A página **criar pacote** será exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-254">The **Create Package** page is displayed.</span></span> <span data-ttu-id="811af-255">Para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvar usando a caixa de seleção do editor de pacote** .</span><span class="sxs-lookup"><span data-stu-id="811af-255">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="811af-256">Essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="811af-256">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="811af-257">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-257">Click **Next**.</span></span>

   <span data-ttu-id="811af-258">Para salvar o pacote imediatamente, selecione **salvar o pacote agora**.</span><span class="sxs-lookup"><span data-stu-id="811af-258">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="811af-259">Opcionalmente, adicione uma **Descrição** que será associada ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-259">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="811af-260">Descrições são úteis para identificar a versão e outras informações sobre o pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-260">Descriptions are useful for identifying the version and other information about the package.</span></span>

   **<span data-ttu-id="811af-261">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-261">Important</span></span>**  
   <span data-ttu-id="811af-262">O sistema não oferece suporte a caracteres que não podem ser impressos em comentários e descrições.</span><span class="sxs-lookup"><span data-stu-id="811af-262">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="811af-263">Para sequenciar um aplicativo de middleware</span><span class="sxs-lookup"><span data-stu-id="811af-263">To sequence a middleware application</span></span>**

1. <span data-ttu-id="811af-264">No computador que executa o sequenciador, clique em **todos os programas**e, em seguida, clique em **Microsoft Application Virtualization**e, em seguida, clique em **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="811af-264">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="811af-265">\*<strong><em>No sequenciador, clique em \* </em> criar um novo pacote de aplicativo virtual </strong> .</span><span class="sxs-lookup"><span data-stu-id="811af-265">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="811af-266">Selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-266">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="811af-267">Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou fazer com que o pacote contenha dados desnecessários.</span><span class="sxs-lookup"><span data-stu-id="811af-267">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="811af-268">Você deve resolver todos os possíveis problemas antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="811af-268">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="811af-269">Depois de fazer qualquer correção, clique em **Atualizar** para exibir as informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="811af-269">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="811af-270">Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-270">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="811af-271">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-271">Important</span></span>**  
   <span data-ttu-id="811af-272">Se for necessário desativar o software de verificação de vírus, você deve primeiro examinar o computador que executa o sequenciador do App-V 5,0 para garantir que arquivos indesejados ou mal-intencionados possam ser adicionados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-272">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="811af-273">Na página **tipo de aplicativo** , selecione **middlewaree**, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-273">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="811af-274">Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="811af-274">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="811af-275">Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-275">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="811af-276">Na página **nome do pacote** , digite um nome que será associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-276">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="811af-277">Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-277">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="811af-278">O nome do pacote é exibido no console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="811af-278">The package name is displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="811af-279">O **diretório de aplicativos virtual primário** exibe o caminho onde o aplicativo será instalado.</span><span class="sxs-lookup"><span data-stu-id="811af-279">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="811af-280">Para especificar esse local, digite o caminho ou clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="811af-280">To specify this location, type the path or click **Browse**.</span></span>

   <span data-ttu-id="811af-281">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-281">Click **Next**.</span></span>

7. <span data-ttu-id="811af-282">Na página de **instalação** , quando o instalador do aplicativo de sequenciador e middleware estiver pronto, você pode continuar a instalar o aplicativo para que o sequenciador possa monitorar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="811af-282">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="811af-283">Use o processo de instalação do aplicativo para executar a instalação.</span><span class="sxs-lookup"><span data-stu-id="811af-283">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="811af-284">Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar**, para localizar e executar os arquivos de instalação adicionais.</span><span class="sxs-lookup"><span data-stu-id="811af-284">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="811af-285">Quando terminar a instalação, marque a caixa de seleção **já terminei de instalar** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-285">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="811af-286">Na página de **instalação** , aguarde enquanto o sequenciador configura o pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="811af-286">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="811af-287">Na página **relatório de instalação** , você pode revisar as informações sobre o pacote de aplicativo virtual que você acabou de sequenciar.</span><span class="sxs-lookup"><span data-stu-id="811af-287">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="811af-288">Em **informações adicionais**, clique duas vezes em um evento para obter informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="811af-288">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="811af-289">Para continuar, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-289">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="811af-290">Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-290">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="811af-291">Para habilitar todos os sistemas operacionais com suporte em seu ambiente para executar este pacote, marque a caixa de seleção **permitir que este pacote seja executado em qualquer sistema operacional** .</span><span class="sxs-lookup"><span data-stu-id="811af-291">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="811af-292">Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, marque a caixa de seleção **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e selecione os sistemas operacionais que podem executar este pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-292">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="811af-293">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-293">Click **Next**.</span></span>

11. <span data-ttu-id="811af-294">Na página **criar pacote** é exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-294">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="811af-295">Para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvá-lo usando o editor de pacote**.</span><span class="sxs-lookup"><span data-stu-id="811af-295">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="811af-296">Essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="811af-296">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="811af-297">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="811af-297">Click **Next**.</span></span>

    <span data-ttu-id="811af-298">Para salvar o pacote imediatamente, selecione **salvar o pacote agora**.</span><span class="sxs-lookup"><span data-stu-id="811af-298">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="811af-299">Opcionalmente, adicione uma **Descrição** para estar associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-299">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="811af-300">Descrições são úteis para identificar a versão do programa e outras informações sobre o pacote.</span><span class="sxs-lookup"><span data-stu-id="811af-300">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    **<span data-ttu-id="811af-301">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-301">Important</span></span>**  
    <span data-ttu-id="811af-302">O sistema não oferece suporte a caracteres que não podem ser impressos em comentários e descrições.</span><span class="sxs-lookup"><span data-stu-id="811af-302">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="811af-303">A página de **conclusão** será exibida.</span><span class="sxs-lookup"><span data-stu-id="811af-303">The **Completion** page is displayed.</span></span> <span data-ttu-id="811af-304">Examine as informações no painel **relatório do pacote do aplicativo virtual** conforme necessário e clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="811af-304">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="811af-305">Essas informações também estão disponíveis no arquivo **Report.xml** localizado no diretório especificado na etapa 11 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="811af-305">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="811af-306">O pacote agora está disponível no sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-306">The package is now available in the sequencer.</span></span> <span data-ttu-id="811af-307">Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**.</span><span class="sxs-lookup"><span data-stu-id="811af-307">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   **<span data-ttu-id="811af-308">Importante</span><span class="sxs-lookup"><span data-stu-id="811af-308">Important</span></span>**  
   <span data-ttu-id="811af-309">Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="811af-309">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="811af-310">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="811af-310">Related topics</span></span>


[<span data-ttu-id="811af-311">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="811af-311">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









