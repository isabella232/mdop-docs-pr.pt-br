---
title: Como executar o Crash Analyzer em um computador de usuário final
description: Como executar o Crash Analyzer em um computador de usuário final
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799352"
---
# <span data-ttu-id="502fc-103">Como executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="502fc-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="502fc-104">Normalmente, você executa o Microsoft Diagnostics and Recovery Toolset (DaRT) 7 Crash Analyzer da janela Diagnostics and Recovery Toolset em um computador de usuário final com problemas.</span><span class="sxs-lookup"><span data-stu-id="502fc-104">Typically, you run Microsoft Diagnostics and Recovery Toolset (DaRT)7 Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="502fc-105">O analisador de falha tenta localizar as ferramentas de depuração para Windows no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="502fc-105">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="502fc-106">Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="502fc-106">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="502fc-107">Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.</span><span class="sxs-lookup"><span data-stu-id="502fc-107">You must also provide a path to where the symbol files are located.</span></span>

**<span data-ttu-id="502fc-108">Para abrir e executar o Crash Analyzer em um computador de usuário final</span><span class="sxs-lookup"><span data-stu-id="502fc-108">To open and run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="502fc-109">Na janela **diagnóstico e Recovery Toolset** em um computador usuário final, clique em **Crash Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="502fc-109">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="502fc-110">Forneça as informações necessárias para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="502fc-110">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="502fc-111">Ferramentas de depuração da Microsoft para Windows</span><span class="sxs-lookup"><span data-stu-id="502fc-111">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="502fc-112">Arquivos de símbolo</span><span class="sxs-lookup"><span data-stu-id="502fc-112">Symbol files</span></span>

        <span data-ttu-id="502fc-113">Para obter mais informações sobre arquivos de símbolos, consulte [como garantir que o Crash Analyzer possa acessar arquivos de símbolo](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="502fc-113">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="502fc-114">Um arquivo de despejo de falha</span><span class="sxs-lookup"><span data-stu-id="502fc-114">A crash dump file</span></span>

        <span data-ttu-id="502fc-115">Siga estas etapas para determinar o local do arquivo de despejo de falha:</span><span class="sxs-lookup"><span data-stu-id="502fc-115">Follow these steps to determine the location of the crash dump file:</span></span>

        1.  <span data-ttu-id="502fc-116">Abra a janela **Propriedades do sistema** .</span><span class="sxs-lookup"><span data-stu-id="502fc-116">Open the **System Properties** window.</span></span>

            <span data-ttu-id="502fc-117">Clique em **Iniciar**, digite sysdm.cpl e, em seguida, pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="502fc-117">Click **Start**, type sysdm.cpl, and then press Enter.</span></span>

        2.  <span data-ttu-id="502fc-118">Clique na guia **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="502fc-118">Click the **Advanced** tab.</span></span>

        3.  <span data-ttu-id="502fc-119">Na área **inicialização e recuperação** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="502fc-119">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="502fc-120">**Observação**  Se você não tiver acesso à janela **Propriedades do sistema** , poderá pesquisar arquivos de despejo no computador do usuário final usando a ferramenta de **pesquisa** no DART.</span><span class="sxs-lookup"><span data-stu-id="502fc-120">**Note** If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in DaRT.</span></span>

         

3.  <span data-ttu-id="502fc-121">O **Crash Analyzer** verifica o arquivo de despejo de falha e relata uma provável causa da falha.</span><span class="sxs-lookup"><span data-stu-id="502fc-121">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="502fc-122">Você pode ver mais informações sobre a falha, como a mensagem de erro e a descrição específicas, os drivers carregados no momento da falha e a saída completa da análise.</span><span class="sxs-lookup"><span data-stu-id="502fc-122">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="502fc-123">Decidir sobre uma estratégia apropriada para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="502fc-123">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="502fc-124">Isso pode exigir a desativação ou atualização do driver de dispositivo que causou a falha com o uso do nó **serviços e drivers** da ferramenta de **Gerenciamento de computador** no DART.</span><span class="sxs-lookup"><span data-stu-id="502fc-124">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="502fc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="502fc-125">Related topics</span></span>


[<span data-ttu-id="502fc-126">Como diagnosticar falhas de sistema com o Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="502fc-126">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





