---
title: Como alterar as propriedades do pacote
description: Como alterar as propriedades do pacote
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797246"
---
# <span data-ttu-id="27b7a-103">Como alterar as propriedades do pacote</span><span class="sxs-lookup"><span data-stu-id="27b7a-103">How to Change Package Properties</span></span>


<span data-ttu-id="27b7a-104">Você pode usar os procedimentos a seguir para modificar o nome de um pacote de virtualização de aplicativo e seus comentários associados.</span><span class="sxs-lookup"><span data-stu-id="27b7a-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="27b7a-105">Se essa for a primeira vez que o pacote foi criado, você também pode alterar o tamanho do bloco de parâmetro de sequenciamento, que determina como um pacote de aplicativo sequenciado é transmitido de um servidor de virtualização de aplicativos para um cliente de desktop do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="27b7a-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="27b7a-106">**Observação**  Ao selecionar um tamanho de bloco, considere o tamanho do arquivo SFT e a largura de banda da rede.</span><span class="sxs-lookup"><span data-stu-id="27b7a-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="27b7a-107">Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda.</span><span class="sxs-lookup"><span data-stu-id="27b7a-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="27b7a-108">Arquivos com tamanhos de blocos maiores podem ser usados com mais rapidez, mas usam mais largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="27b7a-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="27b7a-109">Por meio da experimentação, você pode descobrir o tamanho de bloco ideal para aplicativos de streaming na sua rede.</span><span class="sxs-lookup"><span data-stu-id="27b7a-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="27b7a-110">O restante das propriedades do pacote na guia **Propriedades** é gerado automaticamente e não pode ser modificado nessa guia.</span><span class="sxs-lookup"><span data-stu-id="27b7a-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="27b7a-111">Para alterar o nome ou os comentários do pacote</span><span class="sxs-lookup"><span data-stu-id="27b7a-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="27b7a-112">Clique na guia **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="27b7a-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="27b7a-113">Na caixa de texto **nome do pacote** , digite ou edite o nome único usado para o pacote, que pode conter vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="27b7a-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="27b7a-114">Na caixa de texto **comentários** , opcionalmente, digite ou edite os comentários.</span><span class="sxs-lookup"><span data-stu-id="27b7a-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="27b7a-115">A prática recomendada sugerida é fornecer informações detalhadas sobre o pacote e o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="27b7a-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="27b7a-116">No menu **arquivo** , selecione **salvar**.</span><span class="sxs-lookup"><span data-stu-id="27b7a-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="27b7a-117">Para alterar o tamanho do bloco</span><span class="sxs-lookup"><span data-stu-id="27b7a-117">To change the block size</span></span>**

1.  <span data-ttu-id="27b7a-118">Clique na guia **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="27b7a-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="27b7a-119">Na lista suspensa **tamanho do bloco** , selecione **4 KB**, **16 kb**, **32 KB**ou **64 KB**.</span><span class="sxs-lookup"><span data-stu-id="27b7a-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="27b7a-120">No menu **arquivo** , selecione **salvar**.</span><span class="sxs-lookup"><span data-stu-id="27b7a-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="27b7a-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27b7a-121">Related topics</span></span>


[<span data-ttu-id="27b7a-122">Sobre a guia Propriedades</span><span class="sxs-lookup"><span data-stu-id="27b7a-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="27b7a-123">Console do Sequencer</span><span class="sxs-lookup"><span data-stu-id="27b7a-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





