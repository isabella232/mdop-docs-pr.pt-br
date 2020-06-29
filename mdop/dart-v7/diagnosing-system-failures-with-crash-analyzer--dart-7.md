---
title: Como diagnosticar falhas de sistema com o Crash Analyzer
description: Como diagnosticar falhas de sistema com o Crash Analyzer
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799278"
---
# <span data-ttu-id="c55cf-103">Como diagnosticar falhas de sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="c55cf-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="c55cf-104">O Crash Analyzer no Microsoft Diagnostics and Recovery Toolset (DaRT) 7 permite que você depure um arquivo de despejo de falha em um computador baseado no Windows e, em seguida, diagnostique qualquer erro de computador relacionado.</span><span class="sxs-lookup"><span data-stu-id="c55cf-104">The Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (DaRT)7 lets you debug a crash dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="c55cf-105">O analisador de falha usa as ferramentas de depuração da Microsoft para Windows para examinar um arquivo de despejo de falha para o driver que causou a falha do computador.</span><span class="sxs-lookup"><span data-stu-id="c55cf-105">The Crash Analyzer uses the Microsoft Debugging Tools for Windows to examine a crash dump file for the driver that caused the computer to fail.</span></span>

## <span data-ttu-id="c55cf-106">Executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="c55cf-106">Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="c55cf-107">Normalmente, você executa o Crash Analyzer na janela diagnóstico e recuperação de conjunto de ferramentas em um computador de usuário final com problemas.</span><span class="sxs-lookup"><span data-stu-id="c55cf-107">Typically, you run Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="c55cf-108">O analisador de falha tenta localizar as ferramentas de depuração para Windows no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="c55cf-108">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="c55cf-109">Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="c55cf-109">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="c55cf-110">Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.</span><span class="sxs-lookup"><span data-stu-id="c55cf-110">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="c55cf-111">Se você incluiu as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo ao criar a imagem de recuperação do DaRT, elas deverão estar disponíveis quando você executar o Crash Analyzer no computador com problema.</span><span class="sxs-lookup"><span data-stu-id="c55cf-111">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, they should be available when you run the Crash Analyzer on the problem computer.</span></span>

[<span data-ttu-id="c55cf-112">Como executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="c55cf-112">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## <span data-ttu-id="c55cf-113">Executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="c55cf-113">Run the Crash Analyzer in stand-alone mode on a computer other than an end-user computer</span></span>


<span data-ttu-id="c55cf-114">O analisador de falha tenta localizar as ferramentas de depuração para Windows no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="c55cf-114">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="c55cf-115">Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="c55cf-115">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="c55cf-116">Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.</span><span class="sxs-lookup"><span data-stu-id="c55cf-116">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="c55cf-117">Se você não incluiu as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo ao criar a imagem de recuperação do DaRT, ou se os problemas de conectividade de rede ou tamanho de disco impedirem você de obtê-los, poderá copiar o arquivo de despejo do computador com problema e analisá-lo em um computador que tenha a versão autônoma do Crash Analyzer instalada , como um computador administrador da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="c55cf-117">If you did not include the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, then you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

[<span data-ttu-id="c55cf-118">Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="c55cf-118">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## <span data-ttu-id="c55cf-119">Verifique se o Crash Analyzer pode acessar arquivos de símbolo</span><span class="sxs-lookup"><span data-stu-id="c55cf-119">Ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="c55cf-120">Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável.</span><span class="sxs-lookup"><span data-stu-id="c55cf-120">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="c55cf-121">Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele travou.</span><span class="sxs-lookup"><span data-stu-id="c55cf-121">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span>

<span data-ttu-id="c55cf-122">Os arquivos de símbolo são baixados automaticamente quando você executa o Crash Analyzer.</span><span class="sxs-lookup"><span data-stu-id="c55cf-122">Symbol files are automatically downloaded when you run Crash Analyzer.</span></span> <span data-ttu-id="c55cf-123">Se o computador não tiver uma conexão com a Internet ou a rede exigir que o computador acesse um servidor proxy HTTP, os arquivos de símbolo não poderão ser baixados.</span><span class="sxs-lookup"><span data-stu-id="c55cf-123">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

[<span data-ttu-id="c55cf-124">Como garantir que o Crash Analyzer possa acessar arquivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="c55cf-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## <span data-ttu-id="c55cf-125">Outros recursos para diagnosticar falhas do sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="c55cf-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="c55cf-126">Operações do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="c55cf-126">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





