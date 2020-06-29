---
title: Planejar a implantação do MBAM 1.0
description: Planejar a implantação do MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799222"
---
# <span data-ttu-id="e22a3-103">Planejar a implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e22a3-103">Planning to Deploy MBAM 1.0</span></span>


<span data-ttu-id="e22a3-104">Você deve considerar várias configurações e pré-requisitos de implantação diferentes antes de criar seu plano de implantação do Microsoft BitLocker Administration and Monitoring (MBAM) 1,0.</span><span class="sxs-lookup"><span data-stu-id="e22a3-104">You should consider a number of different deployment configurations and prerequisites before you create your Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 deployment plan.</span></span> <span data-ttu-id="e22a3-105">Esta seção inclui informações que podem ajudá-lo a obter as informações que você precisa ter para formular um plano de implantação que melhor atenda às suas necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="e22a3-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="e22a3-106">Examine as configurações compatíveis do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="e22a3-106">Review the MBAM 1.0 supported configurations</span></span>


<span data-ttu-id="e22a3-107">Depois de preparar o ambiente de computação para a instalação de recursos cliente e servidor do MBAM, verifique se você revisar as informações de configuração com suporte para o MBAM para confirmar se os computadores nos quais você instala MBAM atendem aos requisitos mínimos de hardware e sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e22a3-107">After you prepare your computing environment for the MBAM Client and Server feature installation, make sure that you review the Supported Configurations information for MBAM to confirm that the computers on which you install MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="e22a3-108">Para obter mais informações sobre os pré-requisitos de implantação do MBAM, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="e22a3-108">For more information about MBAM deployment prerequisites, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="e22a3-109">Configurações com suporte no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e22a3-109">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

## <span data-ttu-id="e22a3-110">Plano para a implantação do servidor e do cliente do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="e22a3-110">Plan for MBAM 1.0 Server and Client deployment</span></span>


<span data-ttu-id="e22a3-111">A infraestrutura do MBAM Server depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa.</span><span class="sxs-lookup"><span data-stu-id="e22a3-111">The MBAM server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="e22a3-112">Esses recursos podem ser instalados em um único servidor ou distribuídos entre vários servidores.</span><span class="sxs-lookup"><span data-stu-id="e22a3-112">These features can be installed on a single server or distributed across multiple servers.</span></span>

<span data-ttu-id="e22a3-113">O cliente MBAM permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="e22a3-113">The MBAM Client enables administrators to enforce and monitor the BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="e22a3-114">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de ferramentas como os serviços de domínio do Active Directory ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="e22a3-114">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="e22a3-115">Com o MBAM, você pode criptografar um computador em sua organização antes de o usuário final receber o computador ou depois, usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="e22a3-115">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer or afterwards, by using Group Policy.</span></span> <span data-ttu-id="e22a3-116">Você pode usar um ou os dois métodos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="e22a3-116">You can use one or both methods in your organization.</span></span> <span data-ttu-id="e22a3-117">Se optar por usar os dois métodos, você poderá melhorar a conformidade, o relatório e o suporte à recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="e22a3-117">If you choose to use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

[<span data-ttu-id="e22a3-118">Planejar implantação de servidor MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e22a3-118">Planning for MBAM 1.0 Server Deployment</span></span>](planning-for-mbam-10-server-deployment.md)

[<span data-ttu-id="e22a3-119">Planejar implantação de cliente MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e22a3-119">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="e22a3-120">Outros recursos para o planejamento do MBAM</span><span class="sxs-lookup"><span data-stu-id="e22a3-120">Other resources for MBAM planning</span></span>


-   [<span data-ttu-id="e22a3-121">Planejamento para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e22a3-121">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





