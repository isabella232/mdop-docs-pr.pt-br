---
title: Como converter um pacote criado em uma versão anterior do App-V
description: Como converter um pacote criado em uma versão anterior do App-V
author: dansimp
ms.assetid: 3366d399-2891-491d-8de1-f8cfdf39bbab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 402e64e3bdbc55eea1edb91d070bb7ebb11c912b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796479"
---
# <span data-ttu-id="ca0e7-103">Como converter um pacote criado em uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="ca0e7-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="ca0e7-104">Você pode usar o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais que foram criados com versões anteriores do App-V.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="ca0e7-105">Observação</span><span class="sxs-lookup"><span data-stu-id="ca0e7-105">Note</span></span>**  
<span data-ttu-id="ca0e7-106">Se estiver executando um computador com uma arquitetura de 64 bits, você deve usar a versão x86 do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="ca0e7-107">O conversor de pacote só pode converter diretamente pacotes que foram criados usando o sequenciador do App-V 4,5 ou uma versão subsequente.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="ca0e7-108">Os pacotes que foram criados usando uma versão anterior ao App-V 4,5 devem ser atualizados para o formato App-V 4,5 ou App-V 4,6 antes da conversão.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="ca0e7-109">As informações a seguir fornecem a direção para converter pacotes de aplicativos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="ca0e7-110">Importante</span><span class="sxs-lookup"><span data-stu-id="ca0e7-110">Important</span></span>**  
<span data-ttu-id="ca0e7-111">Você deve configurar o conversor de pacote para sempre salvar o arquivo ingredientes do pacote em um local seguro e diretório.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="ca0e7-112">Um local seguro pode ser acessado apenas por um administrador.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="ca0e7-113">Além disso, ao implantar o pacote, salve-o em um local seguro ou certifique-se de que nenhum outro usuário tenha permissão para ser conectado durante o processo de conversão.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="ca0e7-114">A pasta de instalação do App-V 4,6 é redirecionada para a raiz do sistema de arquivos virtual</span><span class="sxs-lookup"><span data-stu-id="ca0e7-114">App-V 4.6 installation folder is redirected to virtual file system root</span></span>**

<span data-ttu-id="ca0e7-115">Quando você converte pacotes do App-V 4,6 para o 5,1, o pacote App-V 5,1 pode acessar a unidade codificada que você era obrigado a usar quando criou pacotes do 4,6.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-115">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="ca0e7-116">A letra da unidade será a unidade que você selecionou como a unidade de instalação na máquina de sequenciamento de 4,6.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-116">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="ca0e7-117">(A letra da unidade padrão é Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="ca0e7-117">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="ca0e7-118">Antes do App-V 5,1, a pasta raiz do 4,6 não era reconhecida e não pôde ser acessada pelos pacotes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-118">Prior to App-V 5.1, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="ca0e7-119">Agora, os pacotes do App-V 5,1 podem acessar arquivos codificados por seu caminho completo ou podem enumerar arquivos de forma programática na raiz de instalação do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-119">Now, App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="ca0e7-120">**Detalhes técnicos:** O conversor de pacotes do App-V 5,1 salvará a pasta raiz de instalação do App-V 4,6 e nomes de pastas curtas no arquivo FilesystemMetadata.xml do elemento FileSystem.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-120">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="ca0e7-121">Quando o cliente App-V 5,1 cria o processo virtual, ele mapeará solicitações da raiz de instalação do App-V 4,6 para a raiz do sistema de arquivos virtual.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-121">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

**<span data-ttu-id="ca0e7-122">Introdução</span><span class="sxs-lookup"><span data-stu-id="ca0e7-122">Getting started</span></span>**

1.  <span data-ttu-id="ca0e7-123">Instale o sequenciador do App-V em um computador no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-123">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="ca0e7-124">Para obter informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="ca0e7-124">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  

    <span data-ttu-id="ca0e7-125">Os seguintes cmdlets estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ca0e7-125">The following cmdlets are available:</span></span>

    -   <span data-ttu-id="ca0e7-126">Test-AppvLegacyPackage – este cmdlet foi projetado para verificar pacotes.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-126">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="ca0e7-127">Ele retornará informações sobre qualquer falha com o pacote, como arquivos **. sft** ausentes, uma fonte inválida, erros de arquivo **. OSD** ou uma versão de pacote inválida.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-127">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="ca0e7-128">Esse cmdlet não analisará o arquivo **. sft** nem fará nenhuma validação em profundidade.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-128">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="ca0e7-129">Para obter informações sobre opções e funcionalidade básica para esse cmdlet, usando o PowerShell cmdline, digite `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="ca0e7-129">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

    -   <span data-ttu-id="ca0e7-130">ConvertFrom-AppvLegacyPackage – para converter um pacote existente, digite-o `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="ca0e7-130">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="ca0e7-131">Nesse comando, `c:\contentStore` representa a localização do pacote existente e `c:\convertedPackages` é o diretório de saída no qual o arquivo do pacote de aplicativo virtual do App-5,1 V resultante será salvo.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-131">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.1 virtual application package file will be saved.</span></span> <span data-ttu-id="ca0e7-132">Por padrão, se você não especificar um novo nome, o nome do pacote antigo será usado para o nome do arquivo App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-132">By default, if you do not specify a new name, the old package name will be used for the App-V 5.1 filename.</span></span>

        <span data-ttu-id="ca0e7-133">Além disso, o conversor de pacote otimiza o desempenho de pacotes no App-V 5,1 definindo o pacote para transmitir a falha do pacote App-V.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-133">Additionally, the package converter optimizes performance of packages in App-V 5.1 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="ca0e7-134">Isso é mais performativo do que o bloco de recursos principal e baixando completamente o pacote.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-134">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="ca0e7-135">O sinalizador **DownloadFullPackageOnFirstLaunch** permite que você converta o pacote e defina o pacote para ser totalmente baixado por padrão.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-135">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

        **<span data-ttu-id="ca0e7-136">Observação</span><span class="sxs-lookup"><span data-stu-id="ca0e7-136">Note</span></span>**  
        <span data-ttu-id="ca0e7-137">Antes de especificar o diretório de saída, você deve criar o diretório de saída.</span><span class="sxs-lookup"><span data-stu-id="ca0e7-137">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.1 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="ca0e7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca0e7-138">Related topics</span></span>


[<span data-ttu-id="ca0e7-139">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ca0e7-139">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









