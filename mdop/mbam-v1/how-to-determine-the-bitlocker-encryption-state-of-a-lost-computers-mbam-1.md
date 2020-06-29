---
title: Como determinar o estado de criptografia BitLocker de computadores perdidos
description: Como determinar o estado de criptografia BitLocker de computadores perdidos
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799443"
---
# <span data-ttu-id="5c91d-103">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="5c91d-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="5c91d-104">O Microsoft BitLocker Administration and Monitoring (MBAM) permite que você determine o último status de criptografia do BitLocker conhecido de computadores perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="5c91d-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="5c91d-105">Use o procedimento a seguir para determinar se os volumes foram criptografados em computadores que não estão mais em sua posse.</span><span class="sxs-lookup"><span data-stu-id="5c91d-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="5c91d-106">Determinar o último estado de criptografia do BitLocker conhecido do computador</span><span class="sxs-lookup"><span data-stu-id="5c91d-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="5c91d-107">Abra o site do MBAM.</span><span class="sxs-lookup"><span data-stu-id="5c91d-107">Open the MBAM website.</span></span>

    <span data-ttu-id="5c91d-108">**Observação**  O endereço padrão do site MBAM é http://\* &lt; ComputerName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="5c91d-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="5c91d-109">Use o nome de servidor totalmente qualificado para obter resultados de navegação mais rápidos.</span><span class="sxs-lookup"><span data-stu-id="5c91d-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="5c91d-110">Selecione o nó do **relatório** no painel de navegação e selecione o **relatório de conformidade do computador**.</span><span class="sxs-lookup"><span data-stu-id="5c91d-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="5c91d-111">Use os campos de filtro no painel à direita para restringir os resultados da pesquisa e, em seguida, clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="5c91d-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="5c91d-112">Os resultados serão mostrados abaixo da sua consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5c91d-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="5c91d-113">Execute a ação adequada conforme determinado pela política para os dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="5c91d-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="5c91d-114">**Observação**  A conformidade do dispositivo é determinada pelas políticas do BitLocker implantadas.</span><span class="sxs-lookup"><span data-stu-id="5c91d-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="5c91d-115">Você deve verificar essas políticas implantadas quando está tentando determinar o estado de criptografia do BitLocker de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c91d-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="5c91d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c91d-116">Related topics</span></span>


[<span data-ttu-id="5c91d-117">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="5c91d-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





