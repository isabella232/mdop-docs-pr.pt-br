---
title: Cenário de planejamento de ponta a ponta para a MED-V 2.0
description: Cenário de planejamento de ponta a ponta para a MED-V 2.0
author: dansimp
ms.assetid: e7833883-be93-4b42-9fa3-5c4d9a919058
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f34dcccade7987b8b01269caa667018a74d020c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800020"
---
# <span data-ttu-id="12d26-103">Cenário de planejamento de ponta a ponta para a MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="12d26-103">End-to-End Planning Scenario for MED-V 2.0</span></span>


<span data-ttu-id="12d26-104">Este cenário de exemplo para a virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 ajuda você a atingir o objetivo de planejar a implantação do MED-V usando vários cenários de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="12d26-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you achieve your goal of planning your MED-V deployment by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="12d26-105">Você pode pensar nesse exemplo de cenário como um estudo de caso que ajuda a colocar os cenários e procedimentos individuais em contexto.</span><span class="sxs-lookup"><span data-stu-id="12d26-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="12d26-106">Esta seção fornece informações básicas e instruções para planejar a implantação do MED-V como uma solução completa na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="12d26-106">This section provides basic information and directions for planning you MED-V deployment as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="12d26-107">Cenário passo a passo do planejamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="12d26-107">MED-V Planning Step-by-Step Scenario</span></span>


<span data-ttu-id="12d26-108">Os tópicos deste cenário passo a passo incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="12d26-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="12d26-109">A [arquitetura de alto nível](high-level-architecturemedv2.md) discute a arquitetura do sistema de alto nível e o design de componentes do MED-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="12d26-109">[High-Level Architecture](high-level-architecturemedv2.md) discusses the high-level system architecture and component design of MED-V 2.0.</span></span> <span data-ttu-id="12d26-110">O MED-V aprimora o Windows Virtual PC para executar dois sistemas operacionais em um dispositivo, adicionando entrega de imagem virtual, provisionamento baseado em política de grupo e gerenciamento centralizado.</span><span class="sxs-lookup"><span data-stu-id="12d26-110">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="12d26-111">Ao usar o MED-V, você pode facilmente configurar, implantar e gerenciar imagens do Windows Virtual PC corporativo em qualquer área de trabalho baseada no Windows com o Windows 7 Professional, Enterprise ou Windows 7 Ultimate.</span><span class="sxs-lookup"><span data-stu-id="12d26-111">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span>

-   <span data-ttu-id="12d26-112">[Defina e planeje a implantação do MED-v](define-and-plan-your-med-v-deployment.md) discute as considerações para planejar a implantação do MED-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="12d26-112">[Define and Plan your MED-V Deployment](define-and-plan-your-med-v-deployment.md) discusses the considerations for planning your MED-V 2.0 deployment.</span></span> <span data-ttu-id="12d26-113">Este tópico fornece a direção sobre como identificar os sistemas em sua empresa que recebem o MED-V e calculando os requisitos de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="12d26-113">This topic provides direction about identifying the systems in your enterprise that receive MED-V and calculating disk space requirements.</span></span> <span data-ttu-id="12d26-114">Este tópico também ajuda a avaliar sua infraestrutura existente e determina como ela pode ser usada para a implantação do MED-V.</span><span class="sxs-lookup"><span data-stu-id="12d26-114">This topic also helps evaluate your existing infrastructure and determines how it can be used for MED-V deployment.</span></span>

-   <span data-ttu-id="12d26-115">As [práticas recomendadas do MED-V 2,0](med-v-20-best-practices.md) discutem as práticas recomendadas recomendadas para planejamento, instalação, implantação e gerenciamento do MED-V 2,0 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="12d26-115">[MED-V 2.0 Best Practices](med-v-20-best-practices.md) discusses the recommended best practices for planning, installing, deploying, and managing MED-V 2.0 in your environment.</span></span> <span data-ttu-id="12d26-116">Essas práticas recomendadas incluem recomendações que produzem tempos de execução mais rápidos, melhor operabilidade durante a configuração inicial, maior desempenho e melhor gerenciamento de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="12d26-116">These best practices include recommendations that produce faster run times, better operability during first time setup, increased performance, and better virtual machine management.</span></span>

## <span data-ttu-id="12d26-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12d26-117">Related topics</span></span>


[<span data-ttu-id="12d26-118">Planejamento para o MED-V</span><span class="sxs-lookup"><span data-stu-id="12d26-118">Planning for MED-V</span></span>](planning-for-med-v.md)

[<span data-ttu-id="12d26-119">Cenário de implantação de ponta a ponta para a MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="12d26-119">End-to-End Deployment Scenario for MED-V 2.0</span></span>](end-to-end-deployment-scenario-for-med-v-20.md)

[<span data-ttu-id="12d26-120">Cenário de operações de ponta a ponta para a MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="12d26-120">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





