---
title: Atualizando uma imagem de espaço de trabalho do MED-V
description: Atualizando uma imagem de espaço de trabalho do MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799755"
---
# <span data-ttu-id="a1729-103">Atualizando uma imagem de espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="a1729-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="a1729-104">Uma imagem pode ser atualizada de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="a1729-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="a1729-105">A atualização pode ser enviada para o sistema operacional convidado usando o sistema de distribuição de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="a1729-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="a1729-106">A atualização pode ser carregada para o servidor de distribuição de imagens da Web e, em seguida, baixada pelo cliente e aplicada à imagem do MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1729-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="a1729-107">A imagem base do MED-V pode ser atualizada e reimplantada.</span><span class="sxs-lookup"><span data-stu-id="a1729-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="a1729-108">Como atualizar uma imagem do MED-V usando um sistema de distribuição de software corporativo</span><span class="sxs-lookup"><span data-stu-id="a1729-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="a1729-109">Para atualizar uma imagem do MED-V usando um sistema de distribuição de software corporativo</span><span class="sxs-lookup"><span data-stu-id="a1729-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="a1729-110">Consulte a documentação do sistema que você está usando.</span><span class="sxs-lookup"><span data-stu-id="a1729-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="a1729-111">Como atualizar uma imagem do MED-V usando o download da Web</span><span class="sxs-lookup"><span data-stu-id="a1729-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="a1729-112">Para atualizar uma imagem do MED-V usando o download da Web</span><span class="sxs-lookup"><span data-stu-id="a1729-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="a1729-113">No gerenciamento do MED-V, na guia **máquina virtual** , verifique se as configurações a seguir são aplicadas às políticas do espaço de trabalho do MED-v associadas à imagem do MED-v que está sendo atualizada:</span><span class="sxs-lookup"><span data-stu-id="a1729-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="a1729-114">A caixa de seleção **sugerir atualização quando uma nova versão estiver disponível** estará marcada.</span><span class="sxs-lookup"><span data-stu-id="a1729-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="a1729-115">Opcionalmente, a caixa de seleção **clientes devem usar a transferência de corte ao baixar imagens para este espaço de trabalho** está marcada.</span><span class="sxs-lookup"><span data-stu-id="a1729-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="a1729-116">Para obter mais informações, consulte [como aplicar as configurações da máquina virtual a um espaço de trabalho do MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="a1729-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="a1729-117">Carregue a atualização de imagem para o servidor Web de distribuição de imagens.</span><span class="sxs-lookup"><span data-stu-id="a1729-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="a1729-118">Todos os clientes com imagens que precisam ser atualizadas baixam automaticamente a atualização e a aplicam à imagem.</span><span class="sxs-lookup"><span data-stu-id="a1729-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="a1729-119">Como atualizar uma imagem base do MED-V</span><span class="sxs-lookup"><span data-stu-id="a1729-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="a1729-120">Para atualizar uma imagem base do MED-V</span><span class="sxs-lookup"><span data-stu-id="a1729-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="a1729-121">Abra a imagem existente no PC2007 virtual.</span><span class="sxs-lookup"><span data-stu-id="a1729-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="a1729-122">Faça as alterações necessárias na imagem, atualizando a imagem (como instalar o novo software).</span><span class="sxs-lookup"><span data-stu-id="a1729-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="a1729-123">Feche o PC2007 virtual.</span><span class="sxs-lookup"><span data-stu-id="a1729-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="a1729-124">Testar a imagem.</span><span class="sxs-lookup"><span data-stu-id="a1729-124">Test the image.</span></span>

5.  <span data-ttu-id="a1729-125">Depois que a imagem for testada, compacte-a no repositório local, usando o mesmo nome da imagem existente.</span><span class="sxs-lookup"><span data-stu-id="a1729-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="a1729-126">**Observação**  Se você nomear a imagem como um nome diferente da versão existente, uma nova imagem será criada em vez de uma nova versão da imagem existente.</span><span class="sxs-lookup"><span data-stu-id="a1729-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="a1729-127">Carregue a nova versão para o servidor, empurre-a para a pasta pre-Stage de imagem ou distribua-a por meio de um pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="a1729-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="a1729-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1729-128">Related topics</span></span>


[<span data-ttu-id="a1729-129">Criando uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="a1729-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="a1729-130">Como atualizar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="a1729-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="a1729-131">Configurando políticas de espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="a1729-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="a1729-132">Como configurar o servidor de distribuição na Web de imagem</span><span class="sxs-lookup"><span data-stu-id="a1729-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





