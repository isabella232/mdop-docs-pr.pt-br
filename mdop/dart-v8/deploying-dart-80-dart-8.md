---
title: Implantação do DaRT 8.0
description: Implantação do DaRT 8.0
author: dansimp
ms.assetid: 5a976d4e-3372-4ef6-9095-1b48e99af21b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7cc847836587abb0eaa22c009c8fd18d0ba0899b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799417"
---
# <span data-ttu-id="7167f-103">Implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-103">Deploying DaRT 8.0</span></span>


<span data-ttu-id="7167f-104">O Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 oferece suporte a várias configurações de implantação diferentes.</span><span class="sxs-lookup"><span data-stu-id="7167f-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 supports a number of different deployment configurations.</span></span> <span data-ttu-id="7167f-105">Esta seção inclui informações que você deve considerar sobre a implantação do DaRT 8,0 e procedimentos passo a passo para ajudar você a executar com êxito as tarefas que devem ser concluídas em diferentes estágios da implantação.</span><span class="sxs-lookup"><span data-stu-id="7167f-105">This section includes information you should consider about the deployment of DaRT 8.0 and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="7167f-106">Informações de implantação</span><span class="sxs-lookup"><span data-stu-id="7167f-106">Deployment Information</span></span>


-   [<span data-ttu-id="7167f-107">Implantar o DaRT 8.0 em computadores de administrador</span><span class="sxs-lookup"><span data-stu-id="7167f-107">Deploying DaRT 8.0 to Administrator Computers</span></span>](deploying-dart-80-to-administrator-computers-dart-8.md)

    <span data-ttu-id="7167f-108">Esta seção descreve as diferentes opções de implantação do DaRT para seus requisitos e explica como implementá-las.</span><span class="sxs-lookup"><span data-stu-id="7167f-108">This section describes the different DaRT deployment options for your requirements and explains how to deploy them.</span></span>

-   [<span data-ttu-id="7167f-109">Criação da imagem de recuperação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-109">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

    <span data-ttu-id="7167f-110">Esta seção descreve os métodos que você pode usar para criar a imagem de recuperação do DaRT e fornece instruções para criar a imagem de recuperação usando o assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="7167f-110">This section describes the methods you can use to create the DaRT recovery image and provides instructions to create the recovery image by using the DaRT Recovery Image wizard.</span></span>

-   [<span data-ttu-id="7167f-111">Implantação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="7167f-111">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

    <span data-ttu-id="7167f-112">Esta seção fornece informações para ajudá-lo a decidir sobre a melhor opção de implantação de imagem de recuperação do DaRT para seus requisitos e fornece instruções sobre como implantar a imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7167f-112">This section provides information to help you decide on the best DaRT recovery image deployment option for your requirements and provides instructions on how to deploy the recovery image.</span></span>

-   [<span data-ttu-id="7167f-113">Lista de verificação de implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-113">DaRT 8.0 Deployment Checklist</span></span>](dart-80-deployment-checklist-dart-8.md)

    <span data-ttu-id="7167f-114">Esta seção contém uma lista de verificação de implantação que pode ajudá-lo a implantar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="7167f-114">This section contains a deployment checklist that can help you to deploy DaRT.</span></span>

### <span data-ttu-id="7167f-115">Como obter o DaRT</span><span class="sxs-lookup"><span data-stu-id="7167f-115">How to get DaRT</span></span>

<span data-ttu-id="7167f-116">Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="7167f-116">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="7167f-117">Os clientes empresariais podem obter o MDOP com o Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="7167f-117">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="7167f-118">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="7167f-118">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

## <span data-ttu-id="7167f-119">Outros recursos para a implantação do DaRT</span><span class="sxs-lookup"><span data-stu-id="7167f-119">Other Resources for deploying DaRT</span></span>


[<span data-ttu-id="7167f-120">Ferramentas de administrador e conjunto de ferramentas de diagnóstico e recuperação 8</span><span class="sxs-lookup"><span data-stu-id="7167f-120">Diagnostics and Recovery Toolset 8 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="7167f-121">Introdução ao DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-121">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="7167f-122">Planejamento para o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-122">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

[<span data-ttu-id="7167f-123">Operações do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-123">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="7167f-124">Solução de problemas do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="7167f-124">Troubleshooting DaRT 8.0</span></span>](troubleshooting-dart-80-dart-8.md)

 

 





