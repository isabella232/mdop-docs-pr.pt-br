---
title: Como sequenciar um pacote usando o PowerShell
description: Como sequenciar um pacote usando o PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796315"
---
# <span data-ttu-id="3144b-103">Como sequenciar um pacote usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="3144b-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="3144b-104">Use o procedimento a seguir para criar um novo pacote App-V 5,0 usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3144b-104">Use the following procedure to create a new App-V 5.0 package using PowerShell.</span></span>

<span data-ttu-id="3144b-105">**Observação**  Antes de usar este procedimento, você deve copiar os arquivos de instalação associados para o computador que executa o sequenciador e ler e entender a seção Sequencer de [planejamento para o App-V 5,0 Sequencer e para a implantação do cliente](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3144b-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="3144b-106">Para criar um novo aplicativo virtual usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="3144b-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="3144b-107">Instale o sequenciador do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3144b-107">Install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="3144b-108">Para obter mais informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="3144b-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="3144b-109">Para abrir um console do PowerShell, clique em **Iniciar** e digite **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="3144b-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="3144b-110">Clique com o botão direito do mouse em **Windows PowerShell** e selecione **Executar como Administrador**.</span><span class="sxs-lookup"><span data-stu-id="3144b-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="3144b-111">Usando o console do PowerShell, digite o seguinte: **Import-Module appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="3144b-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="3144b-112">Para criar um pacote, use o cmdlet **New-AppvSequencerPackage** .</span><span class="sxs-lookup"><span data-stu-id="3144b-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="3144b-113">Os parâmetros a seguir são necessários para criar um pacote:</span><span class="sxs-lookup"><span data-stu-id="3144b-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="3144b-114">**Name** -especifica o nome do pacote.</span><span class="sxs-lookup"><span data-stu-id="3144b-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="3144b-115">**PrimaryVirtualApplicationDirectory** -especifica o caminho para o diretório que será usado para instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3144b-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="3144b-116">Esse caminho deve existir.</span><span class="sxs-lookup"><span data-stu-id="3144b-116">This path must exist.</span></span>

    -   <span data-ttu-id="3144b-117">**Installer** – especifica o caminho para o instalador do aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="3144b-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="3144b-118">**Path** -especifica o diretório de saída do pacote.</span><span class="sxs-lookup"><span data-stu-id="3144b-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="3144b-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3144b-119">For example:</span></span>

    **<span data-ttu-id="3144b-120">New-AppvSequencerPackage – nome &lt; do caminho do pacote &gt; -PrimaryVirtualApplicationDirectory &lt; para o caminho do instalador raiz do pacote &gt; &lt; para o &gt; diretório executável do instalador-OutputPath &lt; do caminho de saída&gt;</span><span class="sxs-lookup"><span data-stu-id="3144b-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="3144b-121">Aguarde até que o sequenciador crie o pacote.</span><span class="sxs-lookup"><span data-stu-id="3144b-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="3144b-122">A criação de um pacote usando o PowerShell pode levar tempo.</span><span class="sxs-lookup"><span data-stu-id="3144b-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="3144b-123">Se o pacote não foi criado com êxito, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="3144b-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="3144b-124">A lista a seguir exibe parâmetros opcionais adicionais que podem ser usados com o cmdlet **New-AppvSequencerPackage** :</span><span class="sxs-lookup"><span data-stu-id="3144b-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="3144b-125">AcceleratorFilePath – especifica o caminho para o arquivo Accelerator. cab para gerar um pacote.</span><span class="sxs-lookup"><span data-stu-id="3144b-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="3144b-126">InstalledFilesPath-especifica o caminho para o local onde os arquivos locais instalados do aplicativo são salvos.</span><span class="sxs-lookup"><span data-stu-id="3144b-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="3144b-127">InstallMediaPath-especifica o caminho para o local onde a mídia de instalação está</span><span class="sxs-lookup"><span data-stu-id="3144b-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="3144b-128">TemplateFilePath-especifica o caminho para um arquivo de modelo se você quiser personalizar o processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="3144b-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="3144b-129">FullLoad-especifica que o pacote deve ser totalmente baixado para o computador que está executando o App-V 5,0 antes de poder ser aberto.</span><span class="sxs-lookup"><span data-stu-id="3144b-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.0 before it can be opened.</span></span>

    <span data-ttu-id="3144b-130">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="3144b-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3144b-131">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="3144b-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3144b-132">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="3144b-132">Got an App-V issue?</span></span>** <span data-ttu-id="3144b-133">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3144b-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3144b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3144b-134">Related topics</span></span>


[<span data-ttu-id="3144b-135">Administração do App-V usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="3144b-135">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





