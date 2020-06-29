---
title: Parâmetros de linha de comando do Sequencer
description: Parâmetros de linha de comando do Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796748"
---
# <span data-ttu-id="fdd1d-103">Parâmetros de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="fdd1d-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="fdd1d-104">Você pode usar os seguintes parâmetros do sequenciador do Application Virtualization (App-V) para sequenciar um aplicativo e atualizar um aplicativo virtual existente usando uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="fdd1d-105">Para obter mais informações sobre como sequenciar um aplicativo usando uma linha de comando, consulte [como sequenciar um novo aplicativo usando a linha de comando](how-to-sequence-a-new-application-by-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="fdd1d-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="fdd1d-106">Parâmetros de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="fdd1d-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="fdd1d-107">/HELP ou/?</span><span class="sxs-lookup"><span data-stu-id="fdd1d-107">/HELP or /?</span></span>**  
<span data-ttu-id="fdd1d-108">Exibe informações sobre os parâmetros que estão disponíveis para usar uma linha de comando para sequenciar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="fdd1d-109">/INSTALLPACKAGE ou/I</span><span class="sxs-lookup"><span data-stu-id="fdd1d-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="fdd1d-110">Especifica o Windows Installer ou um arquivo em lotes que será usado para instalar um aplicativo para que ele possa ser sequenciado.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="fdd1d-111">/INSTALLPATH ou/P</span><span class="sxs-lookup"><span data-stu-id="fdd1d-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="fdd1d-112">Especifica o diretório raiz do pacote para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="fdd1d-113">/OUTPUTFILE ou/O</span><span class="sxs-lookup"><span data-stu-id="fdd1d-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="fdd1d-114">Especifica o caminho e o nome do arquivo SPRJ que será gerado.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="fdd1d-115">/FULLLOAD ou/F</span><span class="sxs-lookup"><span data-stu-id="fdd1d-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="fdd1d-116">Especifica se todos os arquivos estarão contidos no bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="fdd1d-117">Se o parâmetro **/FULLLOAD** for especificado na linha de comando, todos os dados de aplicativo associados serão adicionados ao bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="fdd1d-118">Se o parâmetro **/FULLLOAD** não for especificado na linha de comando, nenhum dos dados do aplicativo associado será adicionado ao bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="fdd1d-119">/PACKAGENAME ou/K</span><span class="sxs-lookup"><span data-stu-id="fdd1d-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="fdd1d-120">Especifica o nome do pacote que será atribuído ao aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="fdd1d-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="fdd1d-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="fdd1d-122">Especifica o tamanho do bloco de arquivos SFT que será usado para transmitir o pacote para os computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="fdd1d-123">Você pode selecionar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fdd1d-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="fdd1d-124">4 KB</span><span class="sxs-lookup"><span data-stu-id="fdd1d-124">4 KB</span></span>

-   <span data-ttu-id="fdd1d-125">16 KB</span><span class="sxs-lookup"><span data-stu-id="fdd1d-125">16 KB</span></span>

-   <span data-ttu-id="fdd1d-126">32 KB</span><span class="sxs-lookup"><span data-stu-id="fdd1d-126">32 KB</span></span>

-   <span data-ttu-id="fdd1d-127">64 KB</span><span class="sxs-lookup"><span data-stu-id="fdd1d-127">64 KB</span></span>

<span data-ttu-id="fdd1d-128">Você deve considerar o tamanho do arquivo SFT ao especificar o tamanho do bloco.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="fdd1d-129">Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda e consome menos largura de banda.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="fdd1d-130">Arquivos com tamanhos de blocos maiores usam mais largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="fdd1d-131">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="fdd1d-131">/COMPRESSION</span></span>**  
<span data-ttu-id="fdd1d-132">Especifica o método para compactar o arquivo SFT que será transmitido ao cliente.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="fdd1d-133">/MSI ou/M</span><span class="sxs-lookup"><span data-stu-id="fdd1d-133">/MSI or /M</span></span>**  
<span data-ttu-id="fdd1d-134">Especifica se um instalador do Windows para o aplicativo sequenciado deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="fdd1d-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="fdd1d-135">/DEFAULT</span></span>**  
<span data-ttu-id="fdd1d-136">Especifica o arquivo SPRJ padrão que será usado ao criar um pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="fdd1d-137">Esse arquivo é usado como o modelo. sprj quando o aplicativo é sequenciado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="fdd1d-138">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="fdd1d-138">/UPGRADE</span></span>**  
<span data-ttu-id="fdd1d-139">Especifica o caminho e o nome do arquivo SPRJ que será atualizado.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="fdd1d-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="fdd1d-140">/DECODEPATH</span></span>**  
<span data-ttu-id="fdd1d-141">Especifica o diretório no computador de sequenciamento em que os arquivos associados ao pacote de aplicativo sequenciado são instalados.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="fdd1d-142">Use um dos seguintes formatos ao especificar o diretório:</span><span class="sxs-lookup"><span data-stu-id="fdd1d-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="fdd1d-143">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="fdd1d-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="fdd1d-144">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="fdd1d-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="fdd1d-145">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="fdd1d-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="fdd1d-146">/DECODEPATH: "p:"</span><span class="sxs-lookup"><span data-stu-id="fdd1d-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="fdd1d-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdd1d-147">Related topics</span></span>


[<span data-ttu-id="fdd1d-148">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fdd1d-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="fdd1d-149">Códigos de erro de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="fdd1d-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





