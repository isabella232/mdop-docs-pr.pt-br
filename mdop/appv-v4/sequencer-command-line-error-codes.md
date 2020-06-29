---
title: Códigos de erro de linha de comando do Sequencer
description: Códigos de erro de linha de comando do Sequencer
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796749"
---
# <span data-ttu-id="35470-103">Códigos de erro de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="35470-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="35470-104">Use a lista a seguir para ajudar a identificar erros relacionados a aplicativos de sequenciamento usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="35470-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="35470-105">Você também pode ver essas informações exibindo o arquivo de log associado ao App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="35470-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="35470-106">**Observação**  Vários erros podem ocorrer durante o sequenciamento e, se isso acontecer, o código de erro exibido pode ser a soma de dois códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="35470-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="35470-107">Por exemplo, se os parâmetros */InstallPath* e */OutputFile* estiverem ausentes, o sequenciador do App-V retornará **96**— a soma dos dois códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="35470-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="35470-108">Dezembro</span><span class="sxs-lookup"><span data-stu-id="35470-108">01</span></span>  
<span data-ttu-id="35470-109">Há um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="35470-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="35470-110">02</span><span class="sxs-lookup"><span data-stu-id="35470-110">02</span></span>  
<span data-ttu-id="35470-111">O diretório de instalação especificado (/INSTALLPACKAGE) não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="35470-112">04</span><span class="sxs-lookup"><span data-stu-id="35470-112">04</span></span>  
<span data-ttu-id="35470-113">O diretório raiz do pacote especificado (/INSTALLPATH) não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="35470-114">08</span><span class="sxs-lookup"><span data-stu-id="35470-114">08</span></span>  
<span data-ttu-id="35470-115">O parâmetro */OutputFile* especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="35470-116">16</span><span class="sxs-lookup"><span data-stu-id="35470-116">16</span></span>  
<span data-ttu-id="35470-117">O diretório de instalação (/INSTALLPACKAGE) não está especificado.</span><span class="sxs-lookup"><span data-stu-id="35470-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="35470-118">32</span><span class="sxs-lookup"><span data-stu-id="35470-118">32</span></span>  
<span data-ttu-id="35470-119">O diretório raiz do pacote (/INSTALLPATH) não está especificado.</span><span class="sxs-lookup"><span data-stu-id="35470-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="35470-120">64</span><span class="sxs-lookup"><span data-stu-id="35470-120">64</span></span>  
<span data-ttu-id="35470-121">O parâmetro */OutputFile* não está especificado.</span><span class="sxs-lookup"><span data-stu-id="35470-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="35470-122">128</span><span class="sxs-lookup"><span data-stu-id="35470-122">128</span></span>  
<span data-ttu-id="35470-123">A unidade de virtualização do aplicativo especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="35470-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="35470-124">256</span><span class="sxs-lookup"><span data-stu-id="35470-124">256</span></span>  
<span data-ttu-id="35470-125">Falha no instalador.</span><span class="sxs-lookup"><span data-stu-id="35470-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="35470-126">512</span><span class="sxs-lookup"><span data-stu-id="35470-126">512</span></span>  
<span data-ttu-id="35470-127">Falha no sequenciamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35470-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="35470-128">1024</span><span class="sxs-lookup"><span data-stu-id="35470-128">1024</span></span>  
<span data-ttu-id="35470-129">Falha na avaliação dos atalhos instalados.</span><span class="sxs-lookup"><span data-stu-id="35470-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="35470-130">2048</span><span class="sxs-lookup"><span data-stu-id="35470-130">2048</span></span>  
<span data-ttu-id="35470-131">O pacote do aplicativo sequenciado não pode ser salvo.</span><span class="sxs-lookup"><span data-stu-id="35470-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="35470-132">4096</span><span class="sxs-lookup"><span data-stu-id="35470-132">4096</span></span>  
<span data-ttu-id="35470-133">O nome do pacote especificado (/PACKAGENAME) não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="35470-134">8192</span><span class="sxs-lookup"><span data-stu-id="35470-134">8192</span></span>  
<span data-ttu-id="35470-135">O tamanho de bloco especificado (/BLOCKSIZE) não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="35470-136">16384</span><span class="sxs-lookup"><span data-stu-id="35470-136">16384</span></span>  
<span data-ttu-id="35470-137">O tipo de compactação especificado (/COMPRESSION) não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="35470-138">32768</span><span class="sxs-lookup"><span data-stu-id="35470-138">32768</span></span>  
<span data-ttu-id="35470-139">O caminho do projeto especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="35470-140">65536</span><span class="sxs-lookup"><span data-stu-id="35470-140">65536</span></span>  
<span data-ttu-id="35470-141">O parâmetro de atualização especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="35470-142">131072</span><span class="sxs-lookup"><span data-stu-id="35470-142">131072</span></span>  
<span data-ttu-id="35470-143">O parâmetro projeto de atualização especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="35470-144">262144</span><span class="sxs-lookup"><span data-stu-id="35470-144">262144</span></span>  
<span data-ttu-id="35470-145">O parâmetro de caminho de decodificação especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="35470-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="35470-146">525288</span><span class="sxs-lookup"><span data-stu-id="35470-146">525288</span></span>  
<span data-ttu-id="35470-147">O nome do pacote não está especificado.</span><span class="sxs-lookup"><span data-stu-id="35470-147">The package name is not specified.</span></span>

## <span data-ttu-id="35470-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35470-148">Related topics</span></span>


[<span data-ttu-id="35470-149">Referência do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="35470-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="35470-150">Parâmetros de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="35470-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





