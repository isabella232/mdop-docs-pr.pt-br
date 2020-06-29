---
title: Como criar um acelerador de pacotes usando o PowerShell
description: Como criar um acelerador de pacotes usando o PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796460"
---
# <span data-ttu-id="1d0ad-103">Como criar um acelerador de pacotes usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="1d0ad-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="1d0ad-104">Os aceleradores de pacotes do App-V 5,1 seqüenciam automaticamente aplicativos grandes e complexos.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-104">App-V 5.1 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="1d0ad-105">Além disso, ao aplicar um acelerador de pacotes do App-V 5,1, você nem sempre é obrigado a instalar manualmente um aplicativo para criar o pacote virtualizado.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-105">Additionally, when you apply an App-V 5.1 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="1d0ad-106">Para criar um acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="1d0ad-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="1d0ad-107">Instale o sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="1d0ad-108">Para obter mais informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="1d0ad-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="1d0ad-109">Para abrir um console do PowerShell, clique em **Iniciar** e digite **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="1d0ad-110">Clique com o botão direito do mouse em **Windows PowerShell** e selecione **Executar como Administrador**.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="1d0ad-111">Use o cmdlet **New-AppvPackageAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="1d0ad-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="1d0ad-112">Para criar um acelerador de pacote, certifique-se de que você tenha o pacote. AppV para criar um acelerador a partir da mídia de instalação ou arquivos de instalação e, opcionalmente, um arquivo Leia-me para que os consumidores do acelerador usem.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="1d0ad-113">Os parâmetros a seguir são necessários para usar o cmdlet do acelerador de pacote:</span><span class="sxs-lookup"><span data-stu-id="1d0ad-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="1d0ad-114">**InstalledFilesPath** -especifica o caminho de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="1d0ad-115">**Instalador** – especifica o caminho para a mídia do instalador do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1d0ad-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="1d0ad-116">**InputPackagePath** – especifica o caminho para o pacote. AppV</span><span class="sxs-lookup"><span data-stu-id="1d0ad-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="1d0ad-117">**Path** – especifica o diretório de saída do pacote.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="1d0ad-118">O exemplo a seguir mostra como você pode criar um acelerador de pacote com um pacote. AppV e a mídia de instalação:</span><span class="sxs-lookup"><span data-stu-id="1d0ad-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="1d0ad-119">Caminho New-AppvPackageAccelerator-InputPackagePath &lt; para o caminho do instalador de arquivo. AppV &gt; &lt; para o &gt; diretório do instalador executável-caminho &lt; do caminho de saída&gt;</span><span class="sxs-lookup"><span data-stu-id="1d0ad-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="1d0ad-120">Parâmetros opcionais adicionais que podem ser usados com o cmdlet **New-AppvPackageAccelerator** são exibidos na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="1d0ad-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="1d0ad-121">**AcceleratorDescriptionFile** -especifica o caminho para instruções do acelerador do pacote criado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="1d0ad-122">As instruções do pacote acelerador são arquivos de descrição **. txt** ou **. rtf** que serão empacotados com o pacote criado usando o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="1d0ad-123">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="1d0ad-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="1d0ad-124">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="1d0ad-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="1d0ad-125">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="1d0ad-125">Got an App-V issue?</span></span>** <span data-ttu-id="1d0ad-126">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="1d0ad-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="1d0ad-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d0ad-127">Related topics</span></span>


[<span data-ttu-id="1d0ad-128">Administração do App-V 5.1 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="1d0ad-128">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





