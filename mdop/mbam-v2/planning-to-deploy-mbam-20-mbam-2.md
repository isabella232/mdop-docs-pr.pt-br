---
title: Planejar a implantação do MBAM 2.0
description: Planejar a implantação do MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799711"
---
# <span data-ttu-id="2d31e-103">Planejar a implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d31e-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="2d31e-104">Você deve considerar várias configurações de implantação e pré-requisitos diferentes antes de criar seu plano de implantação do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="2d31e-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="2d31e-105">Esta seção inclui informações que podem ajudá-lo a coletar as informações necessárias para formular um plano de implantação que melhor atenda às suas necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="2d31e-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="2d31e-106">Se você estiver instalando o MBAM com a topologia do Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) para obter informações adicionais sobre o planejamento.</span><span class="sxs-lookup"><span data-stu-id="2d31e-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="2d31e-107">Examine as configurações compatíveis do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="2d31e-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="2d31e-108">Depois de preparar seu ambiente de computação para a instalação de recursos do cliente e do servidor do MBAM, verifique se você revisar as configurações compatíveis para confirmar se os computadores nos quais está instalando o MBAM atendem aos requisitos mínimos de hardware e sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2d31e-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="2d31e-109">Para obter mais informações sobre os pré-requisitos de implantação do MBAM, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="2d31e-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="2d31e-110">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d31e-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="2d31e-111">Plano para a implantação do servidor e do cliente do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="2d31e-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="2d31e-112">A infraestrutura do MBAM Server depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa.</span><span class="sxs-lookup"><span data-stu-id="2d31e-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="2d31e-113">Esses recursos podem ser instalados em uma configuração distribuída em vários servidores.</span><span class="sxs-lookup"><span data-stu-id="2d31e-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="2d31e-114">**Observação**  Uma instalação do MBAM em um único servidor é recomendada apenas para ambientes de laboratório.</span><span class="sxs-lookup"><span data-stu-id="2d31e-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="2d31e-115">O cliente MBAM permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="2d31e-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="2d31e-116">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software corporativo ou instalando o agente do cliente em computadores cliente como parte do processo de imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="2d31e-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="2d31e-117">Com o MBAM, você pode criptografar um computador em sua organização antes de o usuário final receber o computador ou depois de usar a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="2d31e-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="2d31e-118">Planejar implantação de servidor MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d31e-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="2d31e-119">Planejar implantação de cliente MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d31e-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="2d31e-120">Outros recursos para o planejamento do MBAM</span><span class="sxs-lookup"><span data-stu-id="2d31e-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="2d31e-121">Planejamento para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d31e-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





