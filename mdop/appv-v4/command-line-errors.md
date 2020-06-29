---
title: Erros de linha de comando
description: Erros de linha de comando
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797519"
---
# <span data-ttu-id="de07b-103">Erros de linha de comando</span><span class="sxs-lookup"><span data-stu-id="de07b-103">Command-Line Errors</span></span>


<span data-ttu-id="de07b-104">Use a seguinte lista de erros para identificar os motivos pelos quais o sequenciamento de linha de comando não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="de07b-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="de07b-105">Você também pode ver esses erros exibindo o arquivo de log do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="de07b-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="de07b-106">**Observação**  Mais de um erro pode ser exibido durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="de07b-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="de07b-107">Além disso, o código de erro exibido pode ser a soma de dois códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="de07b-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="de07b-108">Por exemplo, se os parâmetros */InstallPath* e */OutputFile* estiverem ausentes, o Microsoft System Center Application Virtualization Sequencer retornará 96 — a soma dos dois códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="de07b-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="de07b-109">Dezembro</span><span class="sxs-lookup"><span data-stu-id="de07b-109">01</span></span>  
<span data-ttu-id="de07b-110">Há um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="de07b-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="de07b-111">02</span><span class="sxs-lookup"><span data-stu-id="de07b-111">02</span></span>  
<span data-ttu-id="de07b-112">O diretório de instalação especificado (/INSTALLPACKAGE) especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="de07b-113">04</span><span class="sxs-lookup"><span data-stu-id="de07b-113">04</span></span>  
<span data-ttu-id="de07b-114">O diretório raiz do pacote especificado (/INSTALLPATH) não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="de07b-115">08</span><span class="sxs-lookup"><span data-stu-id="de07b-115">08</span></span>  
<span data-ttu-id="de07b-116">O parâmetro */OutputFile* especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="de07b-117">16</span><span class="sxs-lookup"><span data-stu-id="de07b-117">16</span></span>  
<span data-ttu-id="de07b-118">O diretório de instalação (/INSTALLPACKAGE) não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="de07b-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="de07b-119">32</span><span class="sxs-lookup"><span data-stu-id="de07b-119">32</span></span>  
<span data-ttu-id="de07b-120">O diretório raiz do pacote (/INSTALLPATH) não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="de07b-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="de07b-121">64</span><span class="sxs-lookup"><span data-stu-id="de07b-121">64</span></span>  
<span data-ttu-id="de07b-122">O parâmetro */OutputFile* não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="de07b-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="de07b-123">128</span><span class="sxs-lookup"><span data-stu-id="de07b-123">128</span></span>  
<span data-ttu-id="de07b-124">A unidade de virtualização do aplicativo especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="de07b-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="de07b-125">256</span><span class="sxs-lookup"><span data-stu-id="de07b-125">256</span></span>  
<span data-ttu-id="de07b-126">Falha no instalador.</span><span class="sxs-lookup"><span data-stu-id="de07b-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="de07b-127">512</span><span class="sxs-lookup"><span data-stu-id="de07b-127">512</span></span>  
<span data-ttu-id="de07b-128">Falha no sequenciamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de07b-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="de07b-129">1024</span><span class="sxs-lookup"><span data-stu-id="de07b-129">1024</span></span>  
<span data-ttu-id="de07b-130">Falha na avaliação dos atalhos instalados.</span><span class="sxs-lookup"><span data-stu-id="de07b-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="de07b-131">2048</span><span class="sxs-lookup"><span data-stu-id="de07b-131">2048</span></span>  
<span data-ttu-id="de07b-132">O pacote do aplicativo sequenciado não pode ser salvo.</span><span class="sxs-lookup"><span data-stu-id="de07b-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="de07b-133">4096</span><span class="sxs-lookup"><span data-stu-id="de07b-133">4096</span></span>  
<span data-ttu-id="de07b-134">O nome do pacote especificado (/PACKAGENAME) não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="de07b-135">8192</span><span class="sxs-lookup"><span data-stu-id="de07b-135">8192</span></span>  
<span data-ttu-id="de07b-136">O tamanho de bloco especificado (/BLOCKSIZE <em> ) </em> não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="de07b-137">16384</span><span class="sxs-lookup"><span data-stu-id="de07b-137">16384</span></span>  
<span data-ttu-id="de07b-138">O tipo de compactação especificado (/COMPRESSION) não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="de07b-139">32768</span><span class="sxs-lookup"><span data-stu-id="de07b-139">32768</span></span>  
<span data-ttu-id="de07b-140">O caminho do projeto especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="de07b-141">65536</span><span class="sxs-lookup"><span data-stu-id="de07b-141">65536</span></span>  
<span data-ttu-id="de07b-142">O parâmetro de atualização especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="de07b-143">131072</span><span class="sxs-lookup"><span data-stu-id="de07b-143">131072</span></span>  
<span data-ttu-id="de07b-144">O parâmetro projeto de atualização especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="de07b-145">262144</span><span class="sxs-lookup"><span data-stu-id="de07b-145">262144</span></span>  
<span data-ttu-id="de07b-146">O parâmetro de caminho de decodificação especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="de07b-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="de07b-147">525288</span><span class="sxs-lookup"><span data-stu-id="de07b-147">525288</span></span>  
<span data-ttu-id="de07b-148">O nome do pacote não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="de07b-148">The package name was not specified.</span></span>

## <span data-ttu-id="de07b-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de07b-149">Related topics</span></span>


[<span data-ttu-id="de07b-150">Sobre como usar a linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="de07b-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="de07b-151">Parâmetros de linha de comando</span><span class="sxs-lookup"><span data-stu-id="de07b-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





