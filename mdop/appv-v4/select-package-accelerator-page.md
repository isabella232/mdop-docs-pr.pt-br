---
title: Selecione a página Acelerador de pacote
description: Selecione a página Acelerador de pacote
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796756"
---
# <span data-ttu-id="e6caf-103">Selecione a página Acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="e6caf-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="e6caf-104">Use a página **selecionar acelerador de pacote** para selecionar o acelerador de pacote que será usado para criar o novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="e6caf-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="e6caf-105">Você deve copiar o acelerador de pacote para uma pasta no computador que executa o sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="e6caf-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="e6caf-106">Para obter mais informações, consulte sobre o app [-v Package Accelerators (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="e6caf-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="e6caf-107">Só execute aceleradores de pacote de editores nos quais você confia.</span><span class="sxs-lookup"><span data-stu-id="e6caf-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="e6caf-108">Os aceleradores de pacote geralmente incluem uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="e6caf-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="e6caf-109">Uma assinatura digital é uma marca de segurança eletrônica que pode ajudar a indicar o fornecedor do software e se o pacote foi adulterado após a transformação ter sido assinada originalmente.</span><span class="sxs-lookup"><span data-stu-id="e6caf-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="e6caf-110">Se você usar uma transformação que foi assinada digitalmente por um fornecedor e o fornecedor tiver verificado sua identidade com uma autoridade de certificação, você poderá ter mais certeza de que a transformação vem desse fornecedor específico e não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="e6caf-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="e6caf-111">O sequenciador App-V informa se qualquer uma das seguintes condições é verdadeira:</span><span class="sxs-lookup"><span data-stu-id="e6caf-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="e6caf-112">A transformação selecionada não foi assinada digitalmente.</span><span class="sxs-lookup"><span data-stu-id="e6caf-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="e6caf-113">A transformação selecionada é assinada por um fornecedor que não verificou sua identidade com uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="e6caf-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="e6caf-114">A transformação selecionada foi alterada após ter sido assinada e liberada digitalmente.</span><span class="sxs-lookup"><span data-stu-id="e6caf-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="e6caf-115">Se qualquer uma dessas mensagens for exibida ao usar aceleradores de pacote, acesse o site do Publisher aceleradores de pacote para obter uma versão assinada digitalmente da transformação.</span><span class="sxs-lookup"><span data-stu-id="e6caf-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="e6caf-116">Esta página contém os seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="e6caf-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="e6caf-117">Procurar</span><span class="sxs-lookup"><span data-stu-id="e6caf-117">Browse</span></span>**  
<span data-ttu-id="e6caf-118">Clique em **procurar** para especificar o acelerador de pacote que será usado para criar o pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="e6caf-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="e6caf-119">Salve o acelerador de pacote especificado localmente no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="e6caf-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="e6caf-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6caf-120">Related topics</span></span>


[<span data-ttu-id="e6caf-121">Assistente do Sequencer - Acelerador de Pacote (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="e6caf-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





