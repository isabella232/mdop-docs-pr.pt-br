---
title: Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial
description: Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799310"
---
# <span data-ttu-id="28819-103">Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial</span><span class="sxs-lookup"><span data-stu-id="28819-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="28819-104">O cliente MED-V pode ser distribuído usando um sistema de distribuição de software corporativo, como o Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="28819-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="28819-105">**Observação**  Se o MED-V estiver instalado usando o Microsoft System Center Configuration Manager, ao criar um pacote para MED-V, defina o modo de execução como direitos administrativos.</span><span class="sxs-lookup"><span data-stu-id="28819-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="28819-106">Antes de implantar o MED-V usando um sistema de distribuição de software corporativo, certifique-se de ter criado uma imagem do MED-V pronto para implantação.</span><span class="sxs-lookup"><span data-stu-id="28819-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="28819-107">Para obter mais informações sobre como criar uma imagem do MED-V, consulte [criando uma imagem do MED-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="28819-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="28819-108">Depois que a imagem do MED-V estiver preparada, considere o melhor método para distribuir a imagem no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="28819-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="28819-109">A imagem pode ser distribuída de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="28819-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="28819-110">Carregado na Web e distribuído via download da Web, opcionalmente, utilizando a tecnologia de transferência de corte.</span><span class="sxs-lookup"><span data-stu-id="28819-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="28819-111">Distribuído usando pré-preparação de imagem.</span><span class="sxs-lookup"><span data-stu-id="28819-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="28819-112">Implantando a imagem pela Web</span><span class="sxs-lookup"><span data-stu-id="28819-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="28819-113">Se você estiver implantando a imagem pela Web, carregue a imagem do MED-V em um servidor de distribuição da Web de imagem.</span><span class="sxs-lookup"><span data-stu-id="28819-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="28819-114">Para obter informações sobre como configurar um servidor de distribuição da Web Image, consulte [como configurar o servidor de distribuição da Web de imagem](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="28819-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="28819-115">Para obter informações sobre como carregar uma imagem no servidor, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="28819-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="28819-116">Implantando a imagem via pré-preparação</span><span class="sxs-lookup"><span data-stu-id="28819-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="28819-117">Se você estiver implantando a imagem via pré-teste de imagem, configure a pasta de pré-teste e empurre a imagem do MED-V para a pasta.</span><span class="sxs-lookup"><span data-stu-id="28819-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="28819-118">Para obter mais informações sobre como configurar o pré-teste de imagem, consulte [como configurar o pré-teste de imagem](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="28819-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="28819-119">**Observação**  Se você estiver usando pré-preparação de imagem, é importante configurar a pasta de pré-estágio de imagem antes de colocar o pacote. msi do cliente.</span><span class="sxs-lookup"><span data-stu-id="28819-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="28819-120">O caminho da pasta precisa ser incluído no pacote Client. msi.</span><span class="sxs-lookup"><span data-stu-id="28819-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="28819-121">Por fim, empurre o pacote Client. msi usando o centro de distribuição de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="28819-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="28819-122">Em seguida, o MED-V pode ser instalado e a imagem implantada.</span><span class="sxs-lookup"><span data-stu-id="28819-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="28819-123">Para obter mais informações sobre como instalar o MED-V Client, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="28819-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="28819-124">Para obter mais informações sobre a implantação da imagem, consulte [como implantar uma imagem de espaço de trabalho](how-to-deploy-a-workspace-imageesds.md).</span><span class="sxs-lookup"><span data-stu-id="28819-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





