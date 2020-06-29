---
title: Como implantar uma imagem de espaço de trabalho
description: Como implantar uma imagem de espaço de trabalho
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799985"
---
# <span data-ttu-id="87117-103">Como implantar uma imagem de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="87117-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="87117-104">Ao usar um sistema de distribuição de software corporativo, uma nova imagem pode ser implantada em computadores cliente de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="87117-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="87117-105">Download da Web</span><span class="sxs-lookup"><span data-stu-id="87117-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="87117-106">Pré-preparação de imagem</span><span class="sxs-lookup"><span data-stu-id="87117-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="87117-107">Como implantar uma imagem de espaço de trabalho via Web</span><span class="sxs-lookup"><span data-stu-id="87117-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="87117-108">Para implantar uma imagem de espaço de trabalho via Web</span><span class="sxs-lookup"><span data-stu-id="87117-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="87117-109">Carregue a imagem do MED-V para o servidor.</span><span class="sxs-lookup"><span data-stu-id="87117-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="87117-110">Para obter informações sobre como carregar a imagem, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="87117-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="87117-111">Usando o sistema de distribuição de software corporativo, instale o pacote. msi do cliente MED-V nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="87117-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="87117-112">Para obter informações sobre como instalar o pacote do cliente. msi do MED-V, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="87117-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="87117-113">O cliente MED-V está instalado e iniciado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="87117-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="87117-114">Na primeira inicialização, o cliente baixa a imagem do endereço do servidor especificado na instalação do cliente.</span><span class="sxs-lookup"><span data-stu-id="87117-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="87117-115">Como implantar uma imagem de espaço de trabalho usando a pré-preparação de imagem</span><span class="sxs-lookup"><span data-stu-id="87117-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="87117-116">Para implantar uma imagem de espaço de trabalho usando a transferência prévia de imagem</span><span class="sxs-lookup"><span data-stu-id="87117-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="87117-117">Crie uma pasta pré-teste de imagem e empurre a imagem para a pasta.</span><span class="sxs-lookup"><span data-stu-id="87117-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="87117-118">Para obter informações sobre como configurar o pré-teste de imagem, consulte [como configurar o pré-teste de imagem](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="87117-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="87117-119">Usando o sistema de distribuição de software corporativo, instale o pacote. msi do cliente MED-V nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="87117-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="87117-120">Para obter informações sobre como instalar o pacote do cliente. msi do MED-V, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="87117-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="87117-121">O cliente MED-V está instalado e iniciado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="87117-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="87117-122">Na primeira inicialização, o cliente busca a imagem da pasta de pré-teste especificada na instalação do cliente.</span><span class="sxs-lookup"><span data-stu-id="87117-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="87117-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87117-123">Related topics</span></span>


[<span data-ttu-id="87117-124">Como configurar o servidor de distribuição na Web de imagem</span><span class="sxs-lookup"><span data-stu-id="87117-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





