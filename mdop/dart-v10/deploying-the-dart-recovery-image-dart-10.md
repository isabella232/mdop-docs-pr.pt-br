---
title: Implantação da imagem de recuperação do DaRT
description: Implantação da imagem de recuperação do DaRT
author: dansimp
ms.assetid: 2b859da6-e31a-4240-8868-93a754328cf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de3ed9c01a1808364158124c4f2dcab835823a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796169"
---
# <span data-ttu-id="ec551-103">Implantação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="ec551-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="ec551-104">Depois de criar o arquivo ISO (organização internacional de normalização) que contém a imagem de recuperação do Microsoft (Microsoft Diagnostics and Recovery Toolset) 10, você pode implantar a imagem de recuperação do DaRT 10 em toda a sua empresa, para que ela fique disponível para usuários finais e trabalhadores de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="ec551-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image, you can deploy the DaRT 10 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="ec551-105">Há quatro métodos compatíveis que você pode usar para implantar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="ec551-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="ec551-106">Para revisar as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="ec551-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="ec551-107">Gravar o arquivo de imagem ISO em um CD ou DVD usando o assistente de imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="ec551-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="ec551-108">Salvar o conteúdo do arquivo de imagem ISO em uma unidade flash USB (UFD) usando o assistente de imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="ec551-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="ec551-109">Extrair o arquivo boot. wim da imagem ISO e implantá-lo como uma partição remota disponível para os computadores dos usuários finais</span><span class="sxs-lookup"><span data-stu-id="ec551-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="ec551-110">Extrair o arquivo boot. wim da imagem ISO e implantá-lo na partição de recuperação de uma nova instalação do Windows 10</span><span class="sxs-lookup"><span data-stu-id="ec551-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 10 installation</span></span>

<span data-ttu-id="ec551-111">**Importante**  O **Assistente de imagem de recuperação do DART** fornece a opção de gravar a imagem em um CD, DVD ou UFD, mas os outros métodos de salvar e implantar a imagem de recuperação exigem etapas adicionais que envolvem ferramentas que não estão incluídas no DART.</span><span class="sxs-lookup"><span data-stu-id="ec551-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="ec551-112">Algumas diretrizes e links para esses outros métodos são fornecidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="ec551-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="ec551-113">Implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="ec551-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="ec551-114">Depois de terminar de executar o assistente de recuperação de imagem do DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ec551-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 10 image.</span></span>

[<span data-ttu-id="ec551-115">Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="ec551-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-10.md)

## <span data-ttu-id="ec551-116">Implantar a imagem de recuperação do DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="ec551-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="ec551-117">Você pode hospedar a imagem de recuperação em um servidor de inicialização de rede central, como os serviços de implantação do Windows, e permitir que os usuários ou a equipe de suporte transmitam a imagem para os computadores sob demanda.</span><span class="sxs-lookup"><span data-stu-id="ec551-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="ec551-118">Como implantar a imagem de recuperação do DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="ec551-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-10.md)

## <span data-ttu-id="ec551-119">Outros recursos para a implantação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="ec551-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="ec551-120">Implantação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ec551-120">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





