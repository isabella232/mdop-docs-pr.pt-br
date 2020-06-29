---
title: Como gerenciar o cache do cliente do App-V usando contadores de desempenho
description: Como gerenciar o cache do cliente do App-V usando contadores de desempenho
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797064"
---
# <span data-ttu-id="a4918-103">Como gerenciar o cache do cliente do App-V usando contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="a4918-103">How to Manage the App-V Client Cache Using Performance Counters</span></span>


<span data-ttu-id="a4918-104">Você pode usar o procedimento a seguir para determinar a quantidade de espaço livre disponível no cache do cliente do Application Virtualization (App-V) usando o monitor de desempenho para exibir as informações graficamente.</span><span class="sxs-lookup"><span data-stu-id="a4918-104">You can use the following procedure to determine how much free space is available in the Application Virtualization (App-V) client cache by using Performance Monitor to display the information graphically.</span></span> <span data-ttu-id="a4918-105">Essas informações são capturadas no computador cliente por um contador de desempenho chamado "cache do cliente do aplicativo virt" e inclui os seguintes contadores: "tamanho do cache (MB)," "espaço livre em cache (MB)" e "% espaço livre".</span><span class="sxs-lookup"><span data-stu-id="a4918-105">This information is captured on the client computer by a performance counter called “App Virt Client Cache,” and it includes the following counters: “Cache size (MB),” “Cache free space (MB),” and “% free space.”</span></span>

**<span data-ttu-id="a4918-106">Para determinar o uso do espaço em cache do cliente</span><span class="sxs-lookup"><span data-stu-id="a4918-106">To determine client cache space usage</span></span>**

1.  <span data-ttu-id="a4918-107">Abra um prompt de comando como administrador ou clique em **Iniciar**, **executar**, digite **perfmon.exe**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4918-107">Open a command prompt as administrator, or click **Start**, **Run**, type **perfmon.exe**, and click **OK**.</span></span>

2.  <span data-ttu-id="a4918-108">Dependendo do sistema operacional Windows sendo usado, clique na ferramenta Monitor de desempenho ou monitor do sistema após a abertura da janela do MMC.</span><span class="sxs-lookup"><span data-stu-id="a4918-108">Depending on the Windows operating system being used, click the Performance Monitor or System Monitor tool after the MMC window opens.</span></span>

3.  <span data-ttu-id="a4918-109">Para adicionar contadores, clique com o botão direito do mouse na área do gráfico e selecione **Adicionar contadores**.</span><span class="sxs-lookup"><span data-stu-id="a4918-109">To add counters, right-click the graph area and select **Add Counters**.</span></span>

4.  <span data-ttu-id="a4918-110">Clique na lista suspensa para exibir a lista de contadores disponíveis, role para localizar o **App Virt o cache do cliente**e, em seguida, adicione os três contadores.</span><span class="sxs-lookup"><span data-stu-id="a4918-110">Click the drop-down to display the list of available counters, scroll to find **App Virt Client Cache**, and then add the three counters.</span></span>

    <span data-ttu-id="a4918-111">**Importante**  Os contadores de desempenho do App-V são implementados em uma DLL de 32 bits, portanto, para vê-los, você deve usar o seguinte comando para iniciar a versão de 32 bits do monitor de desempenho: **MMC/32 perfmon. msc**.</span><span class="sxs-lookup"><span data-stu-id="a4918-111">**Important** The App-V performance counters are implemented in a 32-bit DLL, so to see them, you must use the following command to start the 32-bit version of Performance Monitor: **mmc /32 perfmon.msc**.</span></span> <span data-ttu-id="a4918-112">Esse comando deve ser executado diretamente no computador que está sendo monitorado e não pode ser usado para monitorar um computador remoto que executa um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a4918-112">This command must be run directly on the computer being monitored and cannot be used to monitor a remote computer running a 64-bit operating system.</span></span>

     

## <span data-ttu-id="a4918-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4918-113">Related topics</span></span>


[<span data-ttu-id="a4918-114">Como gerenciar aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="a4918-114">How to Manage Virtual Applications by Using the Command Line</span></span>](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





