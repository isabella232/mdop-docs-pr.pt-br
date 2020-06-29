---
title: Parâmetros de linha de comando
description: Parâmetros de linha de comando
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797518"
---
# <span data-ttu-id="3c4ce-103">Parâmetros de linha de comando</span><span class="sxs-lookup"><span data-stu-id="3c4ce-103">Command-Line Parameters</span></span>


<span data-ttu-id="3c4ce-104">Use os seguintes parâmetros do sequenciador do Application Virtualization para sequenciar um aplicativo e para atualizar um pacote de aplicativo sequenciado no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="3c4ce-105">No diretório Microsoft Application Virtualization Sequencer, você digitaria **SFTSequencer**, seguido do parâmetro apropriado.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="3c4ce-106">*/Help* ou */?*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="3c4ce-107">Use para exibir a lista de parâmetros disponíveis para o sequenciamento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="3c4ce-108">*/INSTALLPACKAGE* ou */i*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="3c4ce-109">Use para especificar o instalador ou um arquivo em lotes para o aplicativo ser sequenciado.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="3c4ce-110">*/InstallPath* ou */p*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="3c4ce-111">Use para especificar o diretório raiz do pacote.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="3c4ce-112">*/OutputFile* ou */o*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="3c4ce-113">Use para especificar o caminho e o nome do arquivo SPRJ que será gerado.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="3c4ce-114">**Importante**  O parâmetro */OutputFile* não está disponível ao abrir um pacote que você não pretende atualizar.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="3c4ce-115">*/FULLLOAD* ou */f*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="3c4ce-116">Use para especificar se deseja colocar tudo no bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="3c4ce-117">*/PackageName* ou */k*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="3c4ce-118">Use para especificar o nome do pacote do aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="3c4ce-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="3c4ce-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="3c4ce-120">Especifica o tamanho do bloco de arquivos SFT que será usado para transmitir o pacote para os computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="3c4ce-121">Você pode selecionar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3c4ce-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="3c4ce-122">4 KB</span><span class="sxs-lookup"><span data-stu-id="3c4ce-122">4 KB</span></span>

-   <span data-ttu-id="3c4ce-123">16 KB</span><span class="sxs-lookup"><span data-stu-id="3c4ce-123">16 KB</span></span>

-   <span data-ttu-id="3c4ce-124">32 KB</span><span class="sxs-lookup"><span data-stu-id="3c4ce-124">32 KB</span></span>

-   <span data-ttu-id="3c4ce-125">64 KB</span><span class="sxs-lookup"><span data-stu-id="3c4ce-125">64 KB</span></span>

<span data-ttu-id="3c4ce-126">Você deve considerar o tamanho do arquivo SFT ao especificar o tamanho do bloco.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="3c4ce-127">Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda e consome menos largura de banda.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="3c4ce-128">Arquivos com tamanhos de blocos maiores usam mais largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="3c4ce-129">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="3c4ce-129">/COMPRESSION</span></span>*  
<span data-ttu-id="3c4ce-130">Use para especificar o método para compactar o arquivo SFT conforme ele é transmitido para o cliente.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="3c4ce-131">*/MSI* ou */m*</span><span class="sxs-lookup"><span data-stu-id="3c4ce-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="3c4ce-132">Use para especificar a geração de um pacote do Microsoft Windows Installer para o aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="3c4ce-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3c4ce-133">/DEFAULT</span></span>*  
<span data-ttu-id="3c4ce-134">Especifica o arquivo SPRJ padrão que será usado ao criar um pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="3c4ce-135">Esse arquivo é usado como o modelo. sprj quando o aplicativo é sequenciado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="3c4ce-136">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="3c4ce-136">/UPGRADE</span></span>*  
<span data-ttu-id="3c4ce-137">Especifica o caminho e o nome do arquivo SPRJ que será atualizado.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="3c4ce-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="3c4ce-138">/DECODEPATH</span></span>*  
<span data-ttu-id="3c4ce-139">Especifica o diretório no computador de sequenciamento em que os arquivos associados ao pacote de aplicativo sequenciado são instalados.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="3c4ce-140">Use um dos seguintes formatos ao especificar o diretório:</span><span class="sxs-lookup"><span data-stu-id="3c4ce-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="3c4ce-141">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="3c4ce-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="3c4ce-142">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="3c4ce-143">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="3c4ce-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="3c4ce-144">/DECODEPATH: "p:"</span><span class="sxs-lookup"><span data-stu-id="3c4ce-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="3c4ce-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c4ce-145">Related topics</span></span>


[<span data-ttu-id="3c4ce-146">Sobre como usar a linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="3c4ce-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="3c4ce-147">Como abrir um aplicativo sequenciado usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="3c4ce-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="3c4ce-148">Como fazer upgrade de um pacote usando o comando Abrir Pacote</span><span class="sxs-lookup"><span data-stu-id="3c4ce-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





