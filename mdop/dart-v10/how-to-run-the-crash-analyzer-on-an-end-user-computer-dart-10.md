---
title: Como executar o Crash Analyzer em um computador de usuário final
description: Como executar o Crash Analyzer em um computador de usuário final
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799118"
---
# <span data-ttu-id="2ef40-103">Como executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="2ef40-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="2ef40-104">Para executar o **Crash Analyzer** na janela **diagnóstico e recuperação do conjunto de ferramentas** em um computador de usuário final com problemas, você deve ter as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo instalados.</span><span class="sxs-lookup"><span data-stu-id="2ef40-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="2ef40-105">Para baixar as ferramentas de depuração do Windows, consulte [ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="2ef40-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="2ef40-106">Para executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="2ef40-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="2ef40-107">Na janela **diagnóstico e Recovery Toolset** em um computador usuário final, clique em **Crash Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="2ef40-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="2ef40-108">Forneça as informações necessárias para as ferramentas de depuração da Microsoft para Windows.</span><span class="sxs-lookup"><span data-stu-id="2ef40-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="2ef40-109">Forneça as informações necessárias para os arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="2ef40-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="2ef40-110">Para obter mais informações sobre arquivos de símbolos, consulte [como garantir que o Crash Analyzer possa acessar arquivos de símbolo](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="2ef40-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span></span>

4.  <span data-ttu-id="2ef40-111">Forneça as informações necessárias para um arquivo de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="2ef40-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="2ef40-112">Para determinar a localização do arquivo de despejo de memória:</span><span class="sxs-lookup"><span data-stu-id="2ef40-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="2ef40-113">Abra a janela **Propriedades do sistema** .</span><span class="sxs-lookup"><span data-stu-id="2ef40-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="2ef40-114">Clique em **Iniciar**, digite **sysdm.cpl**e, em seguida, pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="2ef40-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="2ef40-115">Clique na guia **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="2ef40-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="2ef40-116">Na área **inicialização e recuperação** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="2ef40-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="2ef40-117">Se você não tiver acesso à janela **Propriedades do sistema** , poderá pesquisar arquivos de despejo no computador do usuário final usando a ferramenta **Pesquisar** no Microsoft Diagnostics e o conjunto de ferramentas de recuperação (DART) 10.</span><span class="sxs-lookup"><span data-stu-id="2ef40-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

    <span data-ttu-id="2ef40-118">O **Crash Analyzer** verifica o arquivo de despejo de memória e relata uma provável causa do problema.</span><span class="sxs-lookup"><span data-stu-id="2ef40-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="2ef40-119">Você pode ver mais informações sobre a falha, como a mensagem de despejo de memória específica e a descrição, os drivers carregados no momento da falha e a saída completa da análise.</span><span class="sxs-lookup"><span data-stu-id="2ef40-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="2ef40-120">Identifique a estratégia apropriada para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="2ef40-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="2ef40-121">A estratégia pode exigir a desativação ou atualização do driver de dispositivo que causou a falha com o uso do nó **serviços e drivers** da ferramenta de **Gerenciamento do computador** no DART 10.</span><span class="sxs-lookup"><span data-stu-id="2ef40-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 10.</span></span>

## <span data-ttu-id="2ef40-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ef40-122">Related topics</span></span>


[<span data-ttu-id="2ef40-123">Como diagnosticar falhas de sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="2ef40-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[<span data-ttu-id="2ef40-124">Operações do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="2ef40-124">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





