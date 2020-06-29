---
title: Como determinar o estado de criptografia BitLocker de computadores perdidos
description: Como determinar o estado de criptografia BitLocker de computadores perdidos
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799479"
---
# <span data-ttu-id="57f0f-103">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="57f0f-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="57f0f-104">Use esse procedimento com o site de administração e monitoramento para determinar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="57f0f-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="57f0f-105">O último status de criptografia BitLocker conhecido de computadores perdidos ou roubados</span><span class="sxs-lookup"><span data-stu-id="57f0f-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="57f0f-106">Se os volumes em um computador perdido ou roubado foram criptografados</span><span class="sxs-lookup"><span data-stu-id="57f0f-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="57f0f-107">Para concluir essa tarefa, você precisa ter acesso à área **relatórios** do site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="57f0f-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="57f0f-108">Para obter acesso a essa área, você deve receber a função de usuários de relatório MBAM.</span><span class="sxs-lookup"><span data-stu-id="57f0f-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="57f0f-109">Você pode ter atribuído a essas funções nomes diferentes quando você as criou.</span><span class="sxs-lookup"><span data-stu-id="57f0f-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="57f0f-110">Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="57f0f-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="57f0f-111">**Observação**  A conformidade do dispositivo é determinada pelas políticas do BitLocker que sua empresa implantou.</span><span class="sxs-lookup"><span data-stu-id="57f0f-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="57f0f-112">Você pode querer verificar suas políticas implantadas antes de tentar determinar o estado de criptografia do BitLocker de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57f0f-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="57f0f-113">Para determinar o último estado de criptografia do BitLocker conhecido de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="57f0f-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="57f0f-114">Abra um navegador da Web e navegue até o **site de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="57f0f-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="57f0f-115">No painel esquerdo, selecione **relatórios** para abrir a página relatórios.</span><span class="sxs-lookup"><span data-stu-id="57f0f-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="57f0f-116">Selecione o **relatório de conformidade do computador**.</span><span class="sxs-lookup"><span data-stu-id="57f0f-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="57f0f-117">Use os campos de filtro no painel à direita para restringir os resultados da pesquisa e, em seguida, clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="57f0f-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="57f0f-118">Os resultados são mostrados na sua consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="57f0f-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="57f0f-119">Execute a ação apropriada, conforme determinado pela política de dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="57f0f-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="57f0f-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57f0f-120">Related topics</span></span>


[<span data-ttu-id="57f0f-121">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="57f0f-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="57f0f-122">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="57f0f-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="57f0f-123">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="57f0f-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="57f0f-124">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="57f0f-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





