---
title: Implantação da imagem de recuperação do DaRT 7.0
description: Implantação da imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796054"
---
# <span data-ttu-id="26c5b-103">Implantação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="26c5b-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="26c5b-104">Depois de criar o arquivo ISO (organização internacional de normalização) que contém a imagem de recuperação do Microsoft diagnóstico e recuperação do conjunto de ferramentas de recuperação (DaRT) 7, você pode implantar a imagem de recuperação do DaRT em toda a sua empresa para que ela fique disponível para os usuários finais e agentes da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="26c5b-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="26c5b-105">Há quatro métodos compatíveis que você pode usar para implantar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="26c5b-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="26c5b-106">Gravar o arquivo de imagem ISO em um CD ou DVD</span><span class="sxs-lookup"><span data-stu-id="26c5b-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="26c5b-107">Salvar o conteúdo do arquivo de imagem ISO em uma unidade flash USB (UFD)</span><span class="sxs-lookup"><span data-stu-id="26c5b-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="26c5b-108">Extrair o arquivo boot. wim da imagem ISO e implantá-lo como uma partição remota disponível para os computadores dos usuários finais</span><span class="sxs-lookup"><span data-stu-id="26c5b-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="26c5b-109">Extrair o arquivo boot. wim da imagem ISO e implantá-lo na partição de recuperação de uma nova instalação do Windows 7</span><span class="sxs-lookup"><span data-stu-id="26c5b-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="26c5b-110">**Importante**  O **Assistente de imagem de recuperação DART** oferece apenas a opção de gravar um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="26c5b-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="26c5b-111">Todos os outros métodos de salvar e implantar a imagem de recuperação exigem etapas adicionais que envolvem ferramentas que não estão incluídas no DaRT.</span><span class="sxs-lookup"><span data-stu-id="26c5b-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="26c5b-112">Algumas diretrizes e links para esses outros métodos são fornecidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="26c5b-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="26c5b-113">Implantar a imagem de recuperação do DaRT usando uma unidade flash USB</span><span class="sxs-lookup"><span data-stu-id="26c5b-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="26c5b-114">Após concluir a execução do assistente de imagem de recuperação DaRT, você pode usar a ferramenta em <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar o arquivo de imagem ISO para uma unidade flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="26c5b-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="26c5b-115">Como implantar a imagem de recuperação do DaRT usando um pen drive</span><span class="sxs-lookup"><span data-stu-id="26c5b-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="26c5b-116">Implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="26c5b-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="26c5b-117">Depois de terminar de executar o assistente de recuperação de imagem do DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="26c5b-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="26c5b-118">Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="26c5b-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="26c5b-119">Implantar a imagem de recuperação do DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="26c5b-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="26c5b-120">Depois de terminar de executar o assistente de imagem de recuperação DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="26c5b-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="26c5b-121">Como implantar a imagem de recuperação do DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="26c5b-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="26c5b-122">Outros recursos para manter a implantação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="26c5b-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="26c5b-123">Implantação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="26c5b-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





