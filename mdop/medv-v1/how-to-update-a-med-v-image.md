---
title: Como atualizar uma imagem do MED-V
description: Como atualizar uma imagem do MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796014"
---
# <span data-ttu-id="f03c4-103">Como atualizar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="f03c4-104">Como atualizar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="f03c4-105">Uma imagem do MED-V existente pode ser atualizada, criando, portanto, uma nova versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="f03c4-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="f03c4-106">A nova versão pode ser implantada em computadores cliente, substituindo a imagem existente.</span><span class="sxs-lookup"><span data-stu-id="f03c4-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="f03c4-107">**Observação**  Quando uma nova versão é implantada no cliente, ela substitui a imagem existente.</span><span class="sxs-lookup"><span data-stu-id="f03c4-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="f03c4-108">Ao atualizar uma imagem, certifique-se de que não seja necessário salvar dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="f03c4-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="f03c4-109">Para atualizar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="f03c4-110">Abra a imagem existente no PC2007 virtual.</span><span class="sxs-lookup"><span data-stu-id="f03c4-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="f03c4-111">Faça as alterações necessárias na imagem, atualizando a imagem (como instalar o novo software).</span><span class="sxs-lookup"><span data-stu-id="f03c4-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="f03c4-112">Feche o PC2007 virtual.</span><span class="sxs-lookup"><span data-stu-id="f03c4-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="f03c4-113">Testar a imagem.</span><span class="sxs-lookup"><span data-stu-id="f03c4-113">Test the image.</span></span>

5.  <span data-ttu-id="f03c4-114">Depois que a imagem for testada, compacte-a no repositório local, usando o mesmo nome da imagem existente.</span><span class="sxs-lookup"><span data-stu-id="f03c4-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="f03c4-115">**Observação**  Se você nomear a imagem como um nome diferente da versão existente, uma nova imagem será criada em vez de uma nova versão da imagem existente.</span><span class="sxs-lookup"><span data-stu-id="f03c4-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="f03c4-116">Carregue a nova versão para o servidor ou distribua-a por meio de um pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="f03c4-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="f03c4-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f03c4-117">Related topics</span></span>


[<span data-ttu-id="f03c4-118">Criando uma imagem do Virtual PC para o MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="f03c4-119">Como criar e testar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="f03c4-120">Como empacotar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="f03c4-121">Como carregar uma imagem do MED-V no servidor</span><span class="sxs-lookup"><span data-stu-id="f03c4-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="f03c4-122">Atualizando uma imagem de espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="f03c4-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





