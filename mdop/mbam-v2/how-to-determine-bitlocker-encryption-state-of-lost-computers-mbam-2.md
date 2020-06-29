---
title: Como determinar o estado de criptografia BitLocker de computadores perdidos
description: Como determinar o estado de criptografia BitLocker de computadores perdidos
author: dansimp
ms.assetid: dbd23b64-dff3-4913-9acd-affe67b9462e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9ea4afd6dd08f2040b9e2bd1e1a8998181d1e60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799507"
---
# <span data-ttu-id="66a1b-103">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="66a1b-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="66a1b-104">Você pode usar o Microsoft BitLocker Administration and Monitoring (MBAM) para determinar o último status de criptografia do BitLocker conhecido de computadores que foram perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="66a1b-104">You can use Microsoft BitLocker Administration and Monitoring (MBAM) to determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span> <span data-ttu-id="66a1b-105">O procedimento a seguir explica como determinar se os volumes em um computador são criptografados se houver perda ou roubo.</span><span class="sxs-lookup"><span data-stu-id="66a1b-105">The following procedure explains how to determine whether the volumes on a computer are encrypted if there is a loss or theft.</span></span>

**<span data-ttu-id="66a1b-106">Para determinar o último estado de criptografia do BitLocker conhecido de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="66a1b-106">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="66a1b-107">Abra um navegador da Web e navegue até o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="66a1b-107">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

    <span data-ttu-id="66a1b-108">**Observação**  Observação: o endereço padrão para o site de administração e monitoramento é http://\* &lt; nome_do_computador &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="66a1b-108">**Note** Note: The default address for the Administration and Monitoring website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="66a1b-109">Usar o nome de servidor totalmente qualificado gerará resultados de navegação mais rápidos.</span><span class="sxs-lookup"><span data-stu-id="66a1b-109">Using the fully qualified server name will yield faster browsing results.</span></span>

     

2.  <span data-ttu-id="66a1b-110">Seleciona o nó do **relatório** no painel de navegação e seleciona o **relatório de conformidade do computador**.</span><span class="sxs-lookup"><span data-stu-id="66a1b-110">Selects the **Report** node from the navigation pane, and select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="66a1b-111">Use os campos de filtro no painel à direita para restringir os resultados da pesquisa e, em seguida, clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="66a1b-111">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="66a1b-112">Os resultados são mostrados abaixo da sua consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="66a1b-112">Results are shown below your search query.</span></span>

4.  <span data-ttu-id="66a1b-113">Execute a ação apropriada, conforme determinado pela política de dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="66a1b-113">Take the appropriate action, as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="66a1b-114">**Observação**  A conformidade do dispositivo é determinada pelas políticas do BitLocker que sua empresa implantou.</span><span class="sxs-lookup"><span data-stu-id="66a1b-114">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="66a1b-115">Você pode querer verificar suas políticas implantadas antes de tentar determinar o estado de criptografia do BitLocker de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66a1b-115">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="66a1b-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="66a1b-116">Related topics</span></span>


[<span data-ttu-id="66a1b-117">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="66a1b-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





