---
title: Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final
description: Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799142"
---
# <span data-ttu-id="143ba-103">Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="143ba-103">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>


<span data-ttu-id="143ba-104">Se não for possível acessar as ferramentas de depuração da Microsoft para Windows ou os arquivos de símbolo no computador do usuário final, você poderá copiar o arquivo de despejo do computador com problema e analisá-lo em um computador que tenha a versão autônoma do Crash Analyzer instalada, como um computador do administrador da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="143ba-104">If you cannot access the Microsoft Debugging Tools for Windows or the symbol files on the end-user computer, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

**<span data-ttu-id="143ba-105">Para executar o Crash Analyzer no modo autônomo</span><span class="sxs-lookup"><span data-stu-id="143ba-105">To run the Crash Analyzer in stand-alone mode</span></span>**

1.  <span data-ttu-id="143ba-106">Em um computador com o DaRT7 instalado, clique em **Iniciar**  /  **todos os programas**  /  **Microsoft DART 7**.</span><span class="sxs-lookup"><span data-stu-id="143ba-106">On a computer with DaRT7 installed, click **Start** / **All Programs** / **Microsoft DaRT 7**.</span></span>

2.  <span data-ttu-id="143ba-107">Forneça as informações necessárias para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="143ba-107">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="143ba-108">Ferramentas de depuração da Microsoft para Windows</span><span class="sxs-lookup"><span data-stu-id="143ba-108">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="143ba-109">Arquivos de símbolo</span><span class="sxs-lookup"><span data-stu-id="143ba-109">Symbol files</span></span>

        <span data-ttu-id="143ba-110">Para obter mais informações sobre arquivos de símbolos, consulte [como garantir que o Crash Analyzer possa acessar arquivos de símbolo](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="143ba-110">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="143ba-111">Um arquivo de despejo de falha</span><span class="sxs-lookup"><span data-stu-id="143ba-111">A crash dump file</span></span>

        <span data-ttu-id="143ba-112">**Observação**  Use a ferramenta de pesquisa no DaRT7 para localizar o arquivo de despejo de falha copiado.</span><span class="sxs-lookup"><span data-stu-id="143ba-112">**Note** Use the Search tool in DaRT7 to locate the copied crash dump file.</span></span>

         

3.  <span data-ttu-id="143ba-113">O **Crash Analyzer** verifica o arquivo de despejo de falha e relata uma provável causa da falha.</span><span class="sxs-lookup"><span data-stu-id="143ba-113">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="143ba-114">Você pode ver mais informações sobre a falha, como a mensagem de erro e a descrição específicas, os drivers carregados no momento da falha e a saída completa da análise.</span><span class="sxs-lookup"><span data-stu-id="143ba-114">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="143ba-115">Decidir sobre uma estratégia apropriada para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="143ba-115">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="143ba-116">Isso pode exigir a desativação ou atualização do driver de dispositivo que causou a falha com o uso do nó **serviços e drivers** da ferramenta de **Gerenciamento de computador** no DART.</span><span class="sxs-lookup"><span data-stu-id="143ba-116">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="143ba-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="143ba-117">Related topics</span></span>


[<span data-ttu-id="143ba-118">Como diagnosticar falhas de sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="143ba-118">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





