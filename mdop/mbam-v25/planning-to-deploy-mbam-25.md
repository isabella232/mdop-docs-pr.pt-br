---
title: Planejando a implantação do MBAM 2.5
description: Planejando a implantação do MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799923"
---
# <span data-ttu-id="784c1-103">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="784c1-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="784c1-104">Você deve considerar várias configurações de implantação e pré-requisitos diferentes antes de criar seu plano de implantação do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="784c1-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="784c1-105">Esta seção inclui informações que podem ajudá-lo a coletar as informações necessárias para formular um plano de implantação que melhor atenda às suas necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="784c1-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="784c1-106">Examine as configurações compatíveis do MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="784c1-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="784c1-107">Depois de preparar seu ambiente de computação para a implantação de recursos do cliente e do servidor do MBAM, verifique se você revisar as configurações compatíveis para confirmar se os computadores nos quais está instalando o MBAM atendem aos requisitos mínimos de hardware e sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="784c1-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="784c1-108">Para obter mais informações sobre os pré-requisitos de implantação do MBAM, consulte [pré-requisitos de implantação do MBAM 2,5](mbam-25-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="784c1-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="784c1-109">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="784c1-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="784c1-110">Plano para a implantação do servidor e do cliente do MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="784c1-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="784c1-111">A infraestrutura do MBAM Server depende de um conjunto de recursos do servidor que podem ser configurados em um ou mais computadores servidor, de acordo com os requisitos da empresa.</span><span class="sxs-lookup"><span data-stu-id="784c1-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="784c1-112">Esses recursos podem ser configurados em uma configuração distribuída em vários servidores.</span><span class="sxs-lookup"><span data-stu-id="784c1-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="784c1-113">**Observação**  Uma instalação do MBAM em um único servidor é recomendada apenas para ambientes de laboratório.</span><span class="sxs-lookup"><span data-stu-id="784c1-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="784c1-114">O cliente MBAM permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="784c1-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="784c1-115">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software corporativo ou instalando o cliente em computadores cliente como parte do processo de imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="784c1-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="784c1-116">Com o MBAM, você pode criptografar um computador em sua organização antes de o usuário final receber o computador ou depois de usar a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="784c1-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="784c1-117">Planejando a implantação de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="784c1-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="784c1-118">Planejando a implantação do cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="784c1-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="784c1-119">Outros recursos para o planejamento do MBAM</span><span class="sxs-lookup"><span data-stu-id="784c1-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="784c1-120">Planejamento do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="784c1-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="784c1-121">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="784c1-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="784c1-122">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="784c1-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="784c1-123">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="784c1-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





