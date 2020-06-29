---
title: Criando uma imagem do MED-V
description: Criando uma imagem do MED-V
author: dansimp
ms.assetid: 7cbbcd22-83f5-4b60-825f-781b4c6a2d36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de1c2cd87d85bbe2fc40b9007eba8f86d2ed6f60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796015"
---
# <span data-ttu-id="ffe33-103">Criando uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ffe33-103">Creating a MED-V Image</span></span>


## <span data-ttu-id="ffe33-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ffe33-104">In This Section</span></span>


<span data-ttu-id="ffe33-105">Esta seção descreve como configurar uma imagem do MED-V em um computador no qual o cliente MED-V e o aplicativo de gerenciamento do MED-V estão instalados e explica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ffe33-105">This section describes how to configure a MED-V image on a computer on which the MED-V client and MED-V management application are installed, and explains the following:</span></span>

<a href="" id="how-to-create-and-test-a-med-v-image"></a>[<span data-ttu-id="ffe33-106">Como criar e testar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ffe33-106">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)  
<span data-ttu-id="ffe33-107">Descreve como criar uma imagem do MED-V e, em seguida, testar a imagem localmente.</span><span class="sxs-lookup"><span data-stu-id="ffe33-107">Describes how to create a MED-V image, and then test the image locally.</span></span>

<a href="" id="how-to-pack-a-med-v-image"></a>[<span data-ttu-id="ffe33-108">Como empacotar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ffe33-108">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)  
<span data-ttu-id="ffe33-109">Descreve como compactar uma imagem do MED-V para que ela possa ser adicionada a um pacote de implantação ou carregada no servidor.</span><span class="sxs-lookup"><span data-stu-id="ffe33-109">Describes how to pack a MED-V image so that it can be added to a deployment package or uploaded to the server.</span></span>

<a href="" id="how-to-upload-a-med-v-image-to-the-server"></a>[<span data-ttu-id="ffe33-110">Como carregar uma imagem do MED-V no servidor</span><span class="sxs-lookup"><span data-stu-id="ffe33-110">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)  
<span data-ttu-id="ffe33-111">Descreve como carregar uma imagem do MED-V para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ffe33-111">Describes how to upload a MED-V image to the server.</span></span>

<a href="" id="how-to-localize-a-med-v-image"></a>[<span data-ttu-id="ffe33-112">Como localizar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ffe33-112">How to Localize a MED-V Image</span></span>](how-to-localize-a-med-v-image.md)  
<span data-ttu-id="ffe33-113">Descreve como localizar uma imagem do MED-V por meio da extração ou do download da imagem.</span><span class="sxs-lookup"><span data-stu-id="ffe33-113">Describes how to localize a MED-V image either through extracting or downloading the image.</span></span>

<a href="" id="how-to-update-a-med-v-image"></a>[<span data-ttu-id="ffe33-114">Como atualizar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ffe33-114">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)  
<span data-ttu-id="ffe33-115">Descreve como atualizar uma imagem do MED-V para criar uma nova versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="ffe33-115">Describes how to update a MED-V image to create a new version of the image.</span></span>

<a href="" id="how-to-delete-a-med-v-image"></a>[<span data-ttu-id="ffe33-116">Como excluir uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ffe33-116">How to Delete a MED-V Image</span></span>](how-to-delete-a-med-v-image.md)  
<span data-ttu-id="ffe33-117">Descreve como excluir uma imagem do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ffe33-117">Describes how to delete a MED-V image.</span></span>

<span data-ttu-id="ffe33-118">**Observação**  Depois que a imagem do MED-V é configurada, o computador não deve fazer parte de um domínio porque o procedimento de ingresso no domínio deve ser executado no cliente após a implantação, como parte da configuração do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ffe33-118">**Note** After the MED-V image is configured, the computer should not be part of a domain because the join domain procedure should be performed on the client after the deployment, as part of the MED-V workspace setup.</span></span>

 

 

 





