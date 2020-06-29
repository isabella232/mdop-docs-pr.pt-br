---
title: Como implantar uma imagem de espaço de trabalho
description: Como implantar uma imagem de espaço de trabalho
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799987"
---
# <span data-ttu-id="a6cdf-103">Como implantar uma imagem de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a6cdf-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="a6cdf-104">Ao usar um pacote de implantação, uma nova imagem pode ser implantada em computadores cliente de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="a6cdf-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="a6cdf-105">Download da Web</span><span class="sxs-lookup"><span data-stu-id="a6cdf-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="a6cdf-106">Pré-preparação de imagem</span><span class="sxs-lookup"><span data-stu-id="a6cdf-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="a6cdf-107">Implantando a imagem dentro do pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="a6cdf-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="a6cdf-108">Como implantar uma imagem de espaço de trabalho via Web</span><span class="sxs-lookup"><span data-stu-id="a6cdf-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="a6cdf-109">Para implantar uma imagem de espaço de trabalho via Web</span><span class="sxs-lookup"><span data-stu-id="a6cdf-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="a6cdf-110">Carregue a imagem do MED-V para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="a6cdf-111">Para obter informações sobre como carregar a imagem, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="a6cdf-112">Crie um pacote de implantação e inclua o caminho do servidor para o local da imagem.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="a6cdf-113">Para obter informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="a6cdf-114">Implante o pacote para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="a6cdf-115">Para obter informações sobre a implantação do pacote, consulte [como instalar o cliente do MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="a6cdf-116">O cliente MED-V está instalado e iniciado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="a6cdf-117">Na primeira inicialização, o cliente baixa a imagem do endereço do servidor especificado na instalação do cliente.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="a6cdf-118">Como implantar uma imagem de espaço de trabalho usando a pré-preparação de imagem</span><span class="sxs-lookup"><span data-stu-id="a6cdf-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="a6cdf-119">Para implantar uma imagem de espaço de trabalho usando a transferência prévia de imagem</span><span class="sxs-lookup"><span data-stu-id="a6cdf-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="a6cdf-120">Crie uma pasta pré-teste de imagem e empurre a imagem para a pasta.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="a6cdf-121">Para obter informações sobre como configurar o pré-teste de imagem, consulte [como configurar o pré-teste de imagem](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="a6cdf-122">Crie um pacote de implantação e inclua o caminho para a pasta anterior ao pré-teste da imagem.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="a6cdf-123">Para obter informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="a6cdf-124">Implante o pacote para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="a6cdf-125">Para obter informações sobre a implantação do pacote, consulte [como instalar o cliente do MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="a6cdf-126">O cliente MED-V está instalado e iniciado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="a6cdf-127">Na primeira inicialização, o cliente busca a imagem da pasta de pré-teste especificada na instalação do cliente.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="a6cdf-128">Como implantar uma imagem de espaço de trabalho usando um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="a6cdf-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="a6cdf-129">Para implantar uma imagem de espaço de trabalho usando um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="a6cdf-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="a6cdf-130">Crie um pacote de implantação e inclua a imagem no pacote.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="a6cdf-131">Para obter informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="a6cdf-132">Implante o pacote para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="a6cdf-133">Para obter informações sobre a implantação do pacote, consulte [como instalar o cliente do MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="a6cdf-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="a6cdf-134">A imagem é importada para o host como parte da instalação do pacote.</span><span class="sxs-lookup"><span data-stu-id="a6cdf-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="a6cdf-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6cdf-135">Related topics</span></span>


[<span data-ttu-id="a6cdf-136">Como configurar o servidor de distribuição na Web de imagem</span><span class="sxs-lookup"><span data-stu-id="a6cdf-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="a6cdf-137">Como configurar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="a6cdf-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





