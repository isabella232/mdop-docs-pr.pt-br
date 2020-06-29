---
title: Introdução ao MBAM 1.0
description: Introdução ao MBAM 1.0
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799639"
---
# <span data-ttu-id="be2d6-103">Introdução ao MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="be2d6-104">**Importante** MBAM 1,0 entrará em contato com o fim do suporte em 14 de setembro de 2021.</span><span class="sxs-lookup"><span data-stu-id="be2d6-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="be2d6-105">Consulte nossa [página do ciclo de vida](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="be2d6-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="be2d6-106">Recomendamos [migrar para o MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) ou outra versão suportada do MBAM ou migrar o gerenciamento do BitLocker para o [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span><span class="sxs-lookup"><span data-stu-id="be2d6-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="be2d6-107">A administração e o monitoramento do Microsoft BitLocker (MBAM) exigem planejamento completo antes de você implantá-lo ou usar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="be2d6-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="be2d6-108">Como este produto pode afetar cada computador da sua organização, você pode interromper toda a sua rede se não planejar a implantação com cuidado.</span><span class="sxs-lookup"><span data-stu-id="be2d6-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="be2d6-109">No entanto, se você planejar a implantação com cuidado e gerenciá-la para que ela atenda às suas necessidades de negócios, a MBAM pode ajudar a reduzir a sobrecarga administrativa e o custo total de propriedade.</span><span class="sxs-lookup"><span data-stu-id="be2d6-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="be2d6-110">Se você for novo para este produto, recomendamos que leia a documentação completamente.</span><span class="sxs-lookup"><span data-stu-id="be2d6-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="be2d6-111">Antes de implantá-lo em um ambiente de produção, também recomendamos que você valide seu plano de implantação em um ambiente de rede de teste.</span><span class="sxs-lookup"><span data-stu-id="be2d6-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="be2d6-112">Você também pode considerar a criação de uma classe sobre tecnologias pertinentes.</span><span class="sxs-lookup"><span data-stu-id="be2d6-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="be2d6-113">Para obter mais informações sobre oportunidades de treinamento da Microsoft, consulte a visão geral de treinamento da Microsoft em <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="be2d6-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="be2d6-114">**Observação**  Você pode encontrar uma versão para download desta documentação e o guia de avaliação do MBAM em <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="be2d6-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="be2d6-115">Esta seção do guia do administrador do MBAM inclui informações de alto nível sobre o MBAM para fornecer a você uma compreensão básica do produto antes de começar a planejar a implantação.</span><span class="sxs-lookup"><span data-stu-id="be2d6-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="be2d6-116">A documentação adicional do MBAM pode ser encontrada na página de download recursos da documentação do MBAM em <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="be2d6-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="be2d6-117">Introdução ao MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="be2d6-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="be2d6-118">Sobre o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="be2d6-119">Fornece uma visão geral de alto nível do MBAM e como ele pode ser usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="be2d6-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="be2d6-120">Avaliação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="be2d6-121">Fornece informações sobre como você pode avaliar melhor o MBAM para usar em sua organização.</span><span class="sxs-lookup"><span data-stu-id="be2d6-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="be2d6-122">Arquitetura de alto nível para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="be2d6-123">Fornece uma descrição dos recursos do MBAM e como eles funcionam juntos.</span><span class="sxs-lookup"><span data-stu-id="be2d6-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="be2d6-124">Acessibilidade para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="be2d6-125">Fornece informações sobre recursos e serviços que tornam esse produto e sua documentação correspondente mais acessível para pessoas com deficiências.</span><span class="sxs-lookup"><span data-stu-id="be2d6-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="be2d6-126">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="be2d6-126">Other resources for this product</span></span>


-   [<span data-ttu-id="be2d6-127">Guia do administrador do Microsoft BitLocker Administration and Monitoring 1</span><span class="sxs-lookup"><span data-stu-id="be2d6-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="be2d6-128">Planejamento para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="be2d6-129">Implantando o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="be2d6-130">Operações do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="be2d6-131">Solução de problemas do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="be2d6-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





