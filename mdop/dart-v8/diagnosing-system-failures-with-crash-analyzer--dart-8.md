---
title: Como diagnosticar falhas de sistema com o Crash Analyzer
description: Como diagnosticar falhas de sistema com o Crash Analyzer
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799493"
---
# <span data-ttu-id="de7e2-103">Como diagnosticar falhas de sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="de7e2-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="de7e2-104">O **Crash Analyzer** no Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 permite que você depure um arquivo de despejo de memória em um computador baseado no Windows e, em seguida, diagnostique qualquer erro de computador relacionado.</span><span class="sxs-lookup"><span data-stu-id="de7e2-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="de7e2-105">O **analisador de falha** usa as ferramentas de depuração da Microsoft para Windows para examinar um arquivo de despejo de memória para o driver que causou a falha do computador.</span><span class="sxs-lookup"><span data-stu-id="de7e2-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="de7e2-106">Você pode executar o Crash Analyzer em um computador de usuário final ou no modo autônomo em um computador que não seja um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="de7e2-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="de7e2-107">Executar o Crash Analyzer em um computador usuário final</span><span class="sxs-lookup"><span data-stu-id="de7e2-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="de7e2-108">Normalmente, você executa o **Crash Analyzer** na janela **diagnóstico e recuperação de conjunto de ferramentas** em um computador de usuário final que está apresentando o problema.</span><span class="sxs-lookup"><span data-stu-id="de7e2-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="de7e2-109">O **analisador de falha** tenta localizar as ferramentas de depuração para Windows no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="de7e2-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="de7e2-110">Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="de7e2-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="de7e2-111">Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.</span><span class="sxs-lookup"><span data-stu-id="de7e2-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="de7e2-112">Se você incluiu as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo ao criar a imagem de recuperação do DaRT 8,0, as ferramentas e os arquivos de símbolo devem estar disponíveis quando você executa o **Crash Analyzer** no computador com problema.</span><span class="sxs-lookup"><span data-stu-id="de7e2-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 8.0 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="de7e2-113">Se você não os tiver incluído na imagem de recuperação do DaRT, ou se o tamanho do disco ou problemas de conectividade de rede estiverem impedindo que você os receba, é possível executar o Crash Analyzer no modo autônomo em um computador diferente do computador do usuário final, conforme descrito na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="de7e2-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="de7e2-114">Como executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="de7e2-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="de7e2-115">Executar o Crash Analyzer no modo autônomo em um computador diferente do computador de um usuário final</span><span class="sxs-lookup"><span data-stu-id="de7e2-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="de7e2-116">Embora você normalmente execute o **Crash Analyzer** no computador do usuário final que está apresentando o problema, você também pode executar o Crash Analyzer no modo autônomo, em um computador que não seja um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="de7e2-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="de7e2-117">Você pode escolher essa opção se não incluíu as ferramentas de depuração do Windows na imagem de recuperação do DaRT ou se os problemas de conectividade de rede ou tamanho de disco impedem que você obtenha as ferramentas de depuração.</span><span class="sxs-lookup"><span data-stu-id="de7e2-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="de7e2-118">Nesse caso, você pode copiar o arquivo de despejo do computador problemático e analisá-lo em um computador que tenha a versão autônoma do **Crash Analyzer** instalada, como em um computador do agente de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="de7e2-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="de7e2-119">Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="de7e2-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## <span data-ttu-id="de7e2-120">Como garantir que o Crash Analyzer possa acessar arquivos de símbolo</span><span class="sxs-lookup"><span data-stu-id="de7e2-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="de7e2-121">Para depurar aplicativos que parou de responder, você precisa ter acesso ao arquivo de símbolo, que é separado do programa.</span><span class="sxs-lookup"><span data-stu-id="de7e2-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="de7e2-122">Embora os arquivos de símbolo sejam baixados automaticamente quando você executa o Crash Analyzer, pode haver ocasiões em que o computador com problema não tenha acesso à Internet.</span><span class="sxs-lookup"><span data-stu-id="de7e2-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="de7e2-123">Há várias maneiras de garantir o acesso garantido a arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="de7e2-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="de7e2-124">Como garantir que o Crash Analyzer possa acessar arquivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="de7e2-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## <span data-ttu-id="de7e2-125">Outros recursos para diagnosticar falhas do sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="de7e2-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="de7e2-126">Operações do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="de7e2-126">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





