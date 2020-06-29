---
title: Implantando um espaço de trabalho do MED-V usando um pacote de implantação
description: Implantando um espaço de trabalho do MED-V usando um pacote de implantação
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799311"
---
# <span data-ttu-id="c5a1a-103">Implantando um espaço de trabalho do MED-V usando um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="c5a1a-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="c5a1a-104">A instalação do pacote de implantação fornece um método de instalação do MED-V cliente juntamente com todos os pré-requisitos obrigatórios, bem como as configurações predefinidas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="c5a1a-105">Ao usar um pacote de implantação, o pacote é distribuído por meio de uma rede compartilhada ou mídia removível.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="c5a1a-106">A imagem pode ser incluída no pacote ou pode ser distribuída separadamente.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="c5a1a-107">Antes de criar um pacote de implantação, certifique-se de que você criou uma imagem do MED-V Ready para implantação.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="c5a1a-108">Para obter mais informações sobre como criar uma imagem do MED-V, consulte [criando uma imagem do MED-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="c5a1a-109">Depois que a imagem do MED-V estiver preparada, considere o melhor método para distribuir a imagem no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="c5a1a-110">A imagem pode ser distribuída de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="c5a1a-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="c5a1a-111">Carregado na Web e distribuído via download da Web, opcionalmente, usando a tecnologia de transferência de corte.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="c5a1a-112">Distribuído usando pré-preparação de imagem.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="c5a1a-113">Incluído no pacote de implantação e distribuído em conjunto com todos os outros componentes do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="c5a1a-114">Se a imagem for incluída no pacote, nenhuma outra configuração será necessária para a imagem.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="c5a1a-115">Se a imagem não for incluída no pacote de implantação, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="c5a1a-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="c5a1a-116">Se você estiver implantando a imagem pela Web, carregue a imagem do MED-V para o servidor de distribuição da Web de imagem.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="c5a1a-117">Para obter informações sobre como configurar um servidor de distribuição da Web Image, consulte [como configurar o servidor de distribuição da Web de imagem](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="c5a1a-118">Para obter informações sobre como carregar uma imagem no servidor, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="c5a1a-119">Se você estiver implantando a imagem via pré-teste de imagem, configure a pasta de pré-teste e empurre a imagem do MED-V para a pasta.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="c5a1a-120">Para obter mais informações sobre como configurar o pré-teste da imagem, consulte [como configurar o pré-teste da imagem](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="c5a1a-121">**Observação**  Se você estiver usando pré-preparação de imagem, é importante configurar a pasta de pré-estágio de imagem antes de criar o pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="c5a1a-122">O caminho da pasta precisa ser incluído no pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="c5a1a-123">Por fim, crie o pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-123">Finally, create the deployment package.</span></span> <span data-ttu-id="c5a1a-124">Para obter mais informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="c5a1a-125">Após a conclusão do pacote, distribua-o para implantação.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="c5a1a-126">Depois que o pacote de implantação for distribuído, o cliente MED-V pode ser instalado e a imagem implantada.</span><span class="sxs-lookup"><span data-stu-id="c5a1a-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="c5a1a-127">Para obter mais informações sobre como instalar o MED-V Client, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="c5a1a-128">Para obter mais informações sobre a implantação da imagem, consulte [como implantar uma imagem de espaço de trabalho](how-to-deploy-a-workspace-imagedeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="c5a1a-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





