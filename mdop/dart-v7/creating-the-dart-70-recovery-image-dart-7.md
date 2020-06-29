---
title: Criação da imagem de recuperação do DaRT 7.0
description: Criação da imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799241"
---
# <span data-ttu-id="9969e-103">Criação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9969e-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="9969e-104">O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 inclui o **Assistente de imagem de recuperação do DART** que é usado no Windows para criar uma imagem ISO (organização internacional) inicializável (ISO).</span><span class="sxs-lookup"><span data-stu-id="9969e-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="9969e-105">Uma imagem ISO é um arquivo que representa o conteúdo bruto de um CD.</span><span class="sxs-lookup"><span data-stu-id="9969e-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="9969e-106">Usar o assistente de imagem de recuperação do DaRT para criar a imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="9969e-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="9969e-107">O ISO criado pelo assistente de imagem de recuperação DaRT contém a imagem de recuperação do DaRT que permite que você inicialize em um computador com problema, mesmo que ele não seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="9969e-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="9969e-108">Após inicializar o computador no DaRT, você pode executar as diferentes ferramentas do DaRT para tentar diagnosticar e reparar o computador.</span><span class="sxs-lookup"><span data-stu-id="9969e-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="9969e-109">Você pode escrever o ISO em um CD ou DVD gravável, salvá-lo em uma unidade flash USB ou salvá-lo em um formato que você pode usar para inicializar o DaRT a partir de uma partição remota ou de uma partição de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9969e-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="9969e-110">Para obter mais informações, consulte [implantando a imagem de recuperação do DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="9969e-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="9969e-111">**Observação**  Se o seu computador inclui uma unidade de CD-RW, o assistente oferece para gravar a imagem ISO em um CD ou DVD em branco.</span><span class="sxs-lookup"><span data-stu-id="9969e-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="9969e-112">Se o seu computador não incluir uma unidade compatível com o assistente, você poderá gravar a imagem ISO em um CD ou DVD usando a maioria dos programas que podem gravar um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="9969e-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="9969e-113">Para criar um CD ou DVD inicializável a partir da imagem ISO, você deve ter:</span><span class="sxs-lookup"><span data-stu-id="9969e-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="9969e-114">Uma unidade de CD-RW.</span><span class="sxs-lookup"><span data-stu-id="9969e-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="9969e-115">Um CD ou DVD gravável (em um formato compatível com a unidade gravável).</span><span class="sxs-lookup"><span data-stu-id="9969e-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="9969e-116">Software que dá suporte à unidade gravável e suporta a gravação de uma imagem ISO diretamente em um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="9969e-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="9969e-117">**Importante**  Teste o CD ou DVD que você cria em todos os diferentes tipos de computadores que você pretende dar suporte, porque alguns computadores não podem iniciar de todos os tipos de mídias graváveis.</span><span class="sxs-lookup"><span data-stu-id="9969e-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="9969e-118">Para salvar a imagem ISO em uma unidade flash USB (UFD), você deve ter:</span><span class="sxs-lookup"><span data-stu-id="9969e-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="9969e-119">Uma unidade UFD formatada corretamente.</span><span class="sxs-lookup"><span data-stu-id="9969e-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="9969e-120">Um programa que você pode usar para montar a imagem ISO.</span><span class="sxs-lookup"><span data-stu-id="9969e-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="9969e-121">Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="9969e-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="9969e-122">Criar uma imagem de recuperação limitada por tempo</span><span class="sxs-lookup"><span data-stu-id="9969e-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="9969e-123">Você pode criar uma imagem de recuperação do DaRT que só pode ser usada por um determinado número de dias após a geração.</span><span class="sxs-lookup"><span data-stu-id="9969e-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="9969e-124">Para fazer isso, você deve executar o **Assistente de imagem de recuperação do DART** em um prompt de comando e especificar o número de dias.</span><span class="sxs-lookup"><span data-stu-id="9969e-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="9969e-125">Como criar uma imagem de recuperação por tempo limitado</span><span class="sxs-lookup"><span data-stu-id="9969e-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="9969e-126">Outros recursos para criar a imagem de recuperação do DaRT7</span><span class="sxs-lookup"><span data-stu-id="9969e-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="9969e-127">Implantação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9969e-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





