---
title: Criação e gerenciamento de aplicativos virtualizados App-V 5.0
description: Criação e gerenciamento de aplicativos virtualizados App-V 5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796565"
---
# <span data-ttu-id="f123d-103">Criação e gerenciamento de aplicativos virtualizados App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f123d-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="f123d-104">Depois de implantar corretamente o sequenciador do Microsoft Application Virtualization (App-V) 5,0, você pode usá-lo para monitorar e gravar o processo de instalação e configuração para que um aplicativo seja executado como um aplicativo virtualizado.</span><span class="sxs-lookup"><span data-stu-id="f123d-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="f123d-105">**Observação**  Para obter mais informações sobre como configurar o sequenciador do Microsoft Application Virtualization (App-V) 5,0, as práticas recomendadas de sequenciamento e um exemplo de como criar e atualizar um aplicativo virtual, consulte o [Guia de sequenciamento do Microsoft Application Virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 sequenciating Guide.docx).</span><span class="sxs-lookup"><span data-stu-id="f123d-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="f123d-106">Sequenciando um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f123d-106">Sequencing an application</span></span>


<span data-ttu-id="f123d-107">Você pode usar o sequenciador do App-V 5,0 para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f123d-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="f123d-108">Crie pacotes virtuais que podem ser implantados em computadores que executam o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f123d-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="f123d-109">Atualize os pacotes existentes.</span><span class="sxs-lookup"><span data-stu-id="f123d-109">Upgrade existing packages.</span></span> <span data-ttu-id="f123d-110">Você pode expandir um pacote existente no computador executando o sequenciador e, em seguida, atualizar o aplicativo para criar uma versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="f123d-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="f123d-111">Edite informações de configuração associadas a um pacote existente.</span><span class="sxs-lookup"><span data-stu-id="f123d-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="f123d-112">Por exemplo, você pode adicionar um atalho ou modificar uma associação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f123d-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="f123d-113">**Observação**  Você deve criar atalhos e salvá-los em um local de rede disponível para permitir o roaming.</span><span class="sxs-lookup"><span data-stu-id="f123d-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="f123d-114">Se um atalho é criado e salvo em um local privado, o pacote deve ser publicado localmente no computador executando o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f123d-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="f123d-115">Converter pacotes virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="f123d-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="f123d-116">O sequenciador usa o diretório **% tmp% \ \ Scratch** ou **% Temp% \ \ Scratch** e o diretório **Temp** para armazenar arquivos temporários durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="f123d-117">No computador que executa o sequenciador, você deve configurar esses diretórios com espaço livre em disco equivalente aos requisitos de instalação de aplicativo estimados.</span><span class="sxs-lookup"><span data-stu-id="f123d-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="f123d-118">Configurar os diretórios temporários e o diretório Temp em partições de disco rígido diferentes podem ajudar a melhorar o desempenho durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="f123d-119">Quando você usa o sequenciador para criar um novo aplicativo virtual, os seguintes arquivos listados são criados.</span><span class="sxs-lookup"><span data-stu-id="f123d-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="f123d-120">Esses arquivos compreendem o pacote App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f123d-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="f123d-121">arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="f123d-121">.msi file.</span></span> <span data-ttu-id="f123d-122">Este arquivo do Windows Installer (. msi) é criado pelo sequenciador e é usado para instalar o pacote virtual em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="f123d-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="f123d-123">Arquivo Report.xml.</span><span class="sxs-lookup"><span data-stu-id="f123d-123">Report.xml file.</span></span> <span data-ttu-id="f123d-124">Nesse arquivo, o sequenciador salva todos os problemas, avisos e erros que foram descobertos durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="f123d-125">Ele exibe as informações após a criação do pacote.</span><span class="sxs-lookup"><span data-stu-id="f123d-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="f123d-126">Você pode nos reenviar para o diagnóstico e a solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f123d-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="f123d-127">arquivo. AppV.</span><span class="sxs-lookup"><span data-stu-id="f123d-127">.appv file.</span></span> <span data-ttu-id="f123d-128">Este é o arquivo de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="f123d-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="f123d-129">Arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f123d-129">Deployment configuration file.</span></span> <span data-ttu-id="f123d-130">O arquivo de configuração de implantação determina como o aplicativo virtual será implantado nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="f123d-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="f123d-131">Arquivo de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="f123d-131">User configuration file.</span></span> <span data-ttu-id="f123d-132">O arquivo de configuração do usuário determina como o aplicativo virtual será executado em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="f123d-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="f123d-133">**Importante**  Você deve configurar as pastas% TMP% e% TEMP% que o conversor de pacote usa para ser um local seguro e um diretório.</span><span class="sxs-lookup"><span data-stu-id="f123d-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="f123d-134">Um local seguro está acessível somente por um administrador.</span><span class="sxs-lookup"><span data-stu-id="f123d-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="f123d-135">Além disso, quando você sequenciar o pacote, salve o pacote em um local seguro ou certifique-se de que nenhum outro usuário tenha permissão para estar conectado durante o processo de conversão e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f123d-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="f123d-136">A caixa de diálogo **Opções** no console do sequenciador contém as seguintes guias:</span><span class="sxs-lookup"><span data-stu-id="f123d-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="f123d-137">**Geral**.</span><span class="sxs-lookup"><span data-stu-id="f123d-137">**General**.</span></span> <span data-ttu-id="f123d-138">Use esta guia para habilitar as atualizações da Microsoft para serem executadas durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="f123d-139">Selecione **acrescentar versão do pacote ao nome do arquivo** para configurar a sequência para adicionar um número de versão ao pacote virtualizado que está sendo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="f123d-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="f123d-140">Selecione **sempre confiar na fonte dos aceleradores de pacote** para criar pacotes virtualizados usando um acelerador de pacote sem precisar de autorização.</span><span class="sxs-lookup"><span data-stu-id="f123d-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="f123d-141">**Importante**  Aceleradores de pacote criados usando o App-V 4.6 não são compatíveis com o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f123d-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="f123d-142">**Analisar itens**.</span><span class="sxs-lookup"><span data-stu-id="f123d-142">**Parse Items**.</span></span> <span data-ttu-id="f123d-143">Esta guia exibe os locais de caminho de arquivo associados que serão analisados ou emsinaláveis no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="f123d-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="f123d-144">Os tokens são úteis para adicionar arquivos usando a guia **arquivos de pacote** em **edição avançada**.</span><span class="sxs-lookup"><span data-stu-id="f123d-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="f123d-145">**Itens de exclusão**.</span><span class="sxs-lookup"><span data-stu-id="f123d-145">**Exclusion Items**.</span></span> <span data-ttu-id="f123d-146">Use esta guia para especificar quais pastas e diretórios não devem ser monitorados durante a sequenciagem.</span><span class="sxs-lookup"><span data-stu-id="f123d-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="f123d-147">Para adicionar dados de aplicativo locais salvos na pasta dados do aplicativo local no pacote, clique em **novo** e especifique o local e o tipo de **mapeamento**associado.</span><span class="sxs-lookup"><span data-stu-id="f123d-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="f123d-148">Essa opção é necessária para alguns pacotes.</span><span class="sxs-lookup"><span data-stu-id="f123d-148">This option is required for some packages.</span></span>

<span data-ttu-id="f123d-149">O App-V 5,0 dá suporte a aplicativos que incluem serviços do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f123d-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="f123d-150">Se um aplicativo incluir um serviço do Windows, o serviço será incluído no pacote virtual sequenciado desde que seja instalado enquanto estiver sendo monitorado pelo sequenciador.</span><span class="sxs-lookup"><span data-stu-id="f123d-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="f123d-151">Se um aplicativo virtual criar um serviço do Windows quando ele for executado inicialmente, depois, posteriormente, após a instalação, o aplicativo deverá ser executado enquanto o sequenciador estiver sendo monitorado para que o serviço do Windows seja adicionado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="f123d-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="f123d-152">Só há suporte para serviços que são executados na conta do sistema local.</span><span class="sxs-lookup"><span data-stu-id="f123d-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="f123d-153">Os serviços que são configurados para o AutoStart ou o AutoStart atrasar são iniciados antes do primeiro aplicativo virtual em um pacote ser executado dentro do ambiente virtual do pacote.</span><span class="sxs-lookup"><span data-stu-id="f123d-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="f123d-154">Os serviços do Windows que estão configurados para serem iniciados sob demanda por um aplicativo são iniciados quando o aplicativo virtual dentro do pacote inicia o serviço por meio da chamada de API.</span><span class="sxs-lookup"><span data-stu-id="f123d-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="f123d-155">Como sequenciar um novo aplicativo com o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f123d-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="f123d-156">Suporte à extensão do shell do App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f123d-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="f123d-157">O App-V 5.0 SP2 oferece suporte a extensões do Shell.</span><span class="sxs-lookup"><span data-stu-id="f123d-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="f123d-158">As extensões do Shell serão detectadas e inseridas no pacote durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="f123d-159">Extensões do shell são incorporadas ao pacote automaticamente durante o processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="f123d-160">Quando o pacote for publicado, a extensão do Shell fornecerá aos usuários a mesma funcionalidade do que se o aplicativo fosse instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="f123d-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="f123d-161">Requisitos para usar extensões do Shell:</span><span class="sxs-lookup"><span data-stu-id="f123d-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="f123d-162">Os pacotes que contêm extensões de shell inseridas devem ser publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="f123d-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="f123d-163">O aplicativo não requer configuração adicional ou configuração no cliente para habilitar a funcionalidade de extensão do Shell.</span><span class="sxs-lookup"><span data-stu-id="f123d-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="f123d-164">O "" bits "do aplicativo, o Sequencer e o cliente App-V devem corresponder ou as extensões do shell não funcionarão.</span><span class="sxs-lookup"><span data-stu-id="f123d-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="f123d-165">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f123d-165">For example:</span></span>

    -   <span data-ttu-id="f123d-166">A versão do aplicativo é de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f123d-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="f123d-167">O sequenciador está em execução em um computador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f123d-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="f123d-168">O pacote está sendo entregue a um computador cliente do App-V do 64-bit.</span><span class="sxs-lookup"><span data-stu-id="f123d-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="f123d-169">A tabela a seguir lista as extensões do shell com suporte:</span><span class="sxs-lookup"><span data-stu-id="f123d-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f123d-170">Manipulação</span><span class="sxs-lookup"><span data-stu-id="f123d-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="f123d-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="f123d-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f123d-172">Manipulador de menu de contexto</span><span class="sxs-lookup"><span data-stu-id="f123d-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-173">Adiciona itens de menu ao menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="f123d-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="f123d-174">Ele é chamado antes de o menu de contexto ser exibido.</span><span class="sxs-lookup"><span data-stu-id="f123d-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f123d-175">Manipulador de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="f123d-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-176">Controla a ação na qual clique com o botão direito do mouse, arraste e solte e modifique o menu de contexto exibido.</span><span class="sxs-lookup"><span data-stu-id="f123d-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f123d-177">Manipulador de destino soltar</span><span class="sxs-lookup"><span data-stu-id="f123d-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-178">Controla a ação após a arrastar e soltar um objeto de dados em um destino de soltura, como um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f123d-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f123d-179">Manipulador de objeto de dados</span><span class="sxs-lookup"><span data-stu-id="f123d-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-180">Controla a ação após um arquivo ser copiado para a área de transferência ou arrastado e solto em um destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="f123d-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="f123d-181">Ele pode fornecer formatos de área de transferência adicionais para o destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="f123d-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f123d-182">Manipulador de folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="f123d-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-183">Substitui ou adiciona páginas à caixa de diálogo folha de propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="f123d-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f123d-184">Manipulador InfoTip</span><span class="sxs-lookup"><span data-stu-id="f123d-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-185">Permite a recuperação de sinalizadores e informações de infotip de um item e a exibição dentro de uma dica de ferramenta pop-up durante o foco do mouse.</span><span class="sxs-lookup"><span data-stu-id="f123d-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f123d-186">Manipulador de colunas</span><span class="sxs-lookup"><span data-stu-id="f123d-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-187">Permite criar e exibir colunas personalizadas no <strong> modo de exibição de detalhes do Windows Explorer </strong> .</span><span class="sxs-lookup"><span data-stu-id="f123d-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="f123d-188">Ele pode ser usado para estender a classificação e o agrupamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f123d-189">Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="f123d-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f123d-190">Permite que uma visualização de um arquivo seja exibida no painel de visualização do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f123d-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f123d-191">Suporte à extensão de arquivo Copy on Write (vaca)</span><span class="sxs-lookup"><span data-stu-id="f123d-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="f123d-192">As extensões de arquivo Copy on Write (vaca) permitem que o App-V 5,0 grave dinamicamente em locais específicos contidos no pacote virtual enquanto ele está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="f123d-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="f123d-193">A tabela a seguir exibe os tipos de arquivo que podem existir em um pacote virtual no diretório VFS, mas não pode ser atualizado no computador que executa o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f123d-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="f123d-194">Todos os outros arquivos e diretórios podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="f123d-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="f123d-195">. ACM</span><span class="sxs-lookup"><span data-stu-id="f123d-195">.acm</span></span>

<span data-ttu-id="f123d-196">. asa</span><span class="sxs-lookup"><span data-stu-id="f123d-196">.asa</span></span>

<span data-ttu-id="f123d-197">.asp</span><span class="sxs-lookup"><span data-stu-id="f123d-197">.asp</span></span>

<span data-ttu-id="f123d-198">. aspx</span><span class="sxs-lookup"><span data-stu-id="f123d-198">.aspx</span></span>

<span data-ttu-id="f123d-199">. AX</span><span class="sxs-lookup"><span data-stu-id="f123d-199">.ax</span></span>

<span data-ttu-id="f123d-200">.bat</span><span class="sxs-lookup"><span data-stu-id="f123d-200">.bat</span></span>

<span data-ttu-id="f123d-201">.cer</span><span class="sxs-lookup"><span data-stu-id="f123d-201">.cer</span></span>

<span data-ttu-id="f123d-202">.chm</span><span class="sxs-lookup"><span data-stu-id="f123d-202">.chm</span></span>

<span data-ttu-id="f123d-203">. CLB</span><span class="sxs-lookup"><span data-stu-id="f123d-203">.clb</span></span>

<span data-ttu-id="f123d-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="f123d-204">.cmd</span></span>

<span data-ttu-id="f123d-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="f123d-205">.cnt</span></span>

<span data-ttu-id="f123d-206">.cnv</span><span class="sxs-lookup"><span data-stu-id="f123d-206">.cnv</span></span>

<span data-ttu-id="f123d-207">.com</span><span class="sxs-lookup"><span data-stu-id="f123d-207">.com</span></span>

<span data-ttu-id="f123d-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="f123d-208">.cpl</span></span>

<span data-ttu-id="f123d-209">.cpx</span><span class="sxs-lookup"><span data-stu-id="f123d-209">.cpx</span></span>

<span data-ttu-id="f123d-210">.crt</span><span class="sxs-lookup"><span data-stu-id="f123d-210">.crt</span></span>

<span data-ttu-id="f123d-211">.dll</span><span class="sxs-lookup"><span data-stu-id="f123d-211">.dll</span></span>

<span data-ttu-id="f123d-212">.drv</span><span class="sxs-lookup"><span data-stu-id="f123d-212">.drv</span></span>

<span data-ttu-id="f123d-213">.exe</span><span class="sxs-lookup"><span data-stu-id="f123d-213">.exe</span></span>

<span data-ttu-id="f123d-214">.fon</span><span class="sxs-lookup"><span data-stu-id="f123d-214">.fon</span></span>

<span data-ttu-id="f123d-215">.grp</span><span class="sxs-lookup"><span data-stu-id="f123d-215">.grp</span></span>

<span data-ttu-id="f123d-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="f123d-216">.hlp</span></span>

<span data-ttu-id="f123d-217">.hta</span><span class="sxs-lookup"><span data-stu-id="f123d-217">.hta</span></span>

<span data-ttu-id="f123d-218">. IME</span><span class="sxs-lookup"><span data-stu-id="f123d-218">.ime</span></span>

<span data-ttu-id="f123d-219">.inf</span><span class="sxs-lookup"><span data-stu-id="f123d-219">.inf</span></span>

<span data-ttu-id="f123d-220">.ins</span><span class="sxs-lookup"><span data-stu-id="f123d-220">.ins</span></span>

<span data-ttu-id="f123d-221">.isp</span><span class="sxs-lookup"><span data-stu-id="f123d-221">.isp</span></span>

<span data-ttu-id="f123d-222">. seu</span><span class="sxs-lookup"><span data-stu-id="f123d-222">.its</span></span>

<span data-ttu-id="f123d-223">.js</span><span class="sxs-lookup"><span data-stu-id="f123d-223">.js</span></span>

<span data-ttu-id="f123d-224">.jse</span><span class="sxs-lookup"><span data-stu-id="f123d-224">.jse</span></span>

<span data-ttu-id="f123d-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="f123d-225">.lnk</span></span>

<span data-ttu-id="f123d-226">.msc</span><span class="sxs-lookup"><span data-stu-id="f123d-226">.msc</span></span>

<span data-ttu-id="f123d-227">.msi</span><span class="sxs-lookup"><span data-stu-id="f123d-227">.msi</span></span>

<span data-ttu-id="f123d-228">.msp</span><span class="sxs-lookup"><span data-stu-id="f123d-228">.msp</span></span>

<span data-ttu-id="f123d-229">.mst</span><span class="sxs-lookup"><span data-stu-id="f123d-229">.mst</span></span>

<span data-ttu-id="f123d-230">. mui</span><span class="sxs-lookup"><span data-stu-id="f123d-230">.mui</span></span>

<span data-ttu-id="f123d-231">. NLS</span><span class="sxs-lookup"><span data-stu-id="f123d-231">.nls</span></span>

<span data-ttu-id="f123d-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="f123d-232">.ocx</span></span>

<span data-ttu-id="f123d-233">. PAL</span><span class="sxs-lookup"><span data-stu-id="f123d-233">.pal</span></span>

<span data-ttu-id="f123d-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="f123d-234">.pcd</span></span>

<span data-ttu-id="f123d-235">.pif</span><span class="sxs-lookup"><span data-stu-id="f123d-235">.pif</span></span>

<span data-ttu-id="f123d-236">.reg</span><span class="sxs-lookup"><span data-stu-id="f123d-236">.reg</span></span>

<span data-ttu-id="f123d-237">.scf</span><span class="sxs-lookup"><span data-stu-id="f123d-237">.scf</span></span>

<span data-ttu-id="f123d-238">.scr</span><span class="sxs-lookup"><span data-stu-id="f123d-238">.scr</span></span>

<span data-ttu-id="f123d-239">. SCT</span><span class="sxs-lookup"><span data-stu-id="f123d-239">.sct</span></span>

<span data-ttu-id="f123d-240">.shb</span><span class="sxs-lookup"><span data-stu-id="f123d-240">.shb</span></span>

<span data-ttu-id="f123d-241">.shs</span><span class="sxs-lookup"><span data-stu-id="f123d-241">.shs</span></span>

<span data-ttu-id="f123d-242">.sys</span><span class="sxs-lookup"><span data-stu-id="f123d-242">.sys</span></span>

<span data-ttu-id="f123d-243">. tlb</span><span class="sxs-lookup"><span data-stu-id="f123d-243">.tlb</span></span>

<span data-ttu-id="f123d-244">. tsp</span><span class="sxs-lookup"><span data-stu-id="f123d-244">.tsp</span></span>

<span data-ttu-id="f123d-245">.url</span><span class="sxs-lookup"><span data-stu-id="f123d-245">.url</span></span>

<span data-ttu-id="f123d-246">.vb</span><span class="sxs-lookup"><span data-stu-id="f123d-246">.vb</span></span>

<span data-ttu-id="f123d-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="f123d-247">.vbe</span></span>

<span data-ttu-id="f123d-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="f123d-248">.vbs</span></span>

<span data-ttu-id="f123d-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="f123d-249">.vsmacros</span></span>

<span data-ttu-id="f123d-250">.ws</span><span class="sxs-lookup"><span data-stu-id="f123d-250">.ws</span></span>

<span data-ttu-id="f123d-251">. ESC</span><span class="sxs-lookup"><span data-stu-id="f123d-251">.esc</span></span>

<span data-ttu-id="f123d-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="f123d-252">.wsf</span></span>

<span data-ttu-id="f123d-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="f123d-253">.wsh</span></span>

 

## <span data-ttu-id="f123d-254">Modificando um pacote de aplicativo virtual existente</span><span class="sxs-lookup"><span data-stu-id="f123d-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="f123d-255">Você pode usar o sequenciador para modificar um pacote existente.</span><span class="sxs-lookup"><span data-stu-id="f123d-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="f123d-256">O computador no qual você faz isso deve corresponder à arquitetura de chip do computador usado para criar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f123d-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="f123d-257">Por exemplo, se você inicialmente sequenciava um pacote usando um computador que executa um sistema operacional de 64 bits, deve modificá-lo usando um computador que esteja executando um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f123d-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="f123d-258">Como modificar um pacote de aplicativo virtual existente</span><span class="sxs-lookup"><span data-stu-id="f123d-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="f123d-259">Criando um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="f123d-259">Creating a project template</span></span>


<span data-ttu-id="f123d-260">Um arquivo. appvt é um modelo de projeto que pode ser usado para salvar configurações personalizadas e comumente aplicadas.</span><span class="sxs-lookup"><span data-stu-id="f123d-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="f123d-261">Você pode usar mais facilmente essas configurações para sequenciais futuros.</span><span class="sxs-lookup"><span data-stu-id="f123d-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="f123d-262">Os modelos de projeto do App-V 5,0 diferem dos aceleradores de aplicativos do App-V 5,0 porque o App-V 5,0 Application Accelerators são específicos do aplicativo e os modelos de projeto do App-V 5,0 podem ser aplicados a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f123d-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="f123d-263">Além disso, você não pode usar um modelo de projeto quando usa um acelerador de pacote para criar um pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="f123d-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="f123d-264">As seguintes configurações gerais são salvas com um modelo de projeto App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="f123d-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="f123d-265">Um modelo pode especificar e armazenar várias configurações da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f123d-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="f123d-266">**Opções avançadas de monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="f123d-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="f123d-267">Permite que o Microsoft Update seja executado durante o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f123d-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="f123d-268">Salva as configurações da opção permitir interação local</span><span class="sxs-lookup"><span data-stu-id="f123d-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="f123d-269">**Opções gerais**.</span><span class="sxs-lookup"><span data-stu-id="f123d-269">**General Options**.</span></span> <span data-ttu-id="f123d-270">Habilita o uso do **Windows Installer**, **acrescenta a versão do pacote ao nome do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="f123d-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="f123d-271">Itens de exclusão.</span><span class="sxs-lookup"><span data-stu-id="f123d-271">Exclusion Items.</span></span>** <span data-ttu-id="f123d-272">Contém a lista de padrões de exclusão.</span><span class="sxs-lookup"><span data-stu-id="f123d-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="f123d-273">Como criar e usar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="f123d-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="f123d-274">Criando um acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="f123d-274">Creating a package accelerator</span></span>


<span data-ttu-id="f123d-275">**Observação**  Os aceleradores de pacote criados usando uma versão anterior do App-V devem ser recriados usando o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f123d-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="f123d-276">Você pode usar aceleradores de pacotes do App-V 5,0 para gerar automaticamente novos pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="f123d-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="f123d-277">Depois de criar um acelerador de pacote com êxito, você poderá reutilizar e compartilhar o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="f123d-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="f123d-278">Em algumas situações, para criar o acelerador de pacote, talvez seja necessário instalar o aplicativo localmente no computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="f123d-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="f123d-279">Nesses casos, você deve primeiro tentar criar o acelerador de pacote com a mídia de instalação.</span><span class="sxs-lookup"><span data-stu-id="f123d-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="f123d-280">Se vários arquivos ausentes forem necessários, instale o aplicativo localmente no computador que executa o sequenciador e, em seguida, crie o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="f123d-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="f123d-281">Depois de criar um acelerador de pacote com êxito, você poderá reutilizar e compartilhar o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="f123d-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="f123d-282">A criação de aceleradores de pacotes do App-V 5,0 é uma tarefa avançada.</span><span class="sxs-lookup"><span data-stu-id="f123d-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="f123d-283">Os aceleradores de pacote podem conter informações específicas de senha e usuário.</span><span class="sxs-lookup"><span data-stu-id="f123d-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="f123d-284">Portanto, você deve salvar aceleradores de pacote e a mídia de instalação associada em um local seguro, e deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o fornecedor possa ser verificado quando o acelerador de pacotes do App-V 5,0 for aplicado.</span><span class="sxs-lookup"><span data-stu-id="f123d-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="f123d-285">Como criar um acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="f123d-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="f123d-286">Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="f123d-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="f123d-287">Relatório de erros do sequenciador</span><span class="sxs-lookup"><span data-stu-id="f123d-287">Sequencer error reporting</span></span>


<span data-ttu-id="f123d-288">O sequenciador do App-V 5,0 pode detectar problemas de sequenciamento comuns durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f123d-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="f123d-289">A página **relatório de instalação** no final do assistente de sequenciamento exibe as mensagens de diagnóstico categorizadas em **erros**, **avisos**e **informações** dependendo da gravidade do problema.</span><span class="sxs-lookup"><span data-stu-id="f123d-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="f123d-290">Você também pode encontrar informações adicionais sobre o sequenciamento de erros usando o Visualizador de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="f123d-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="f123d-291">Outros recursos para o sequenciador do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f123d-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="f123d-292">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f123d-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





