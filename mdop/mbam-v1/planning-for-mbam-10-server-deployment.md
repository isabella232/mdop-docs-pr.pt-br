---
title: Planejar implantação de servidor MBAM 1.0
description: Planejar implantação de servidor MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795997"
---
# <span data-ttu-id="46bae-103">Planejar implantação de servidor MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="46bae-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="46bae-104">A infraestrutura de servidor de administração e monitoramento do Microsoft BitLocker (MBAM) depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="46bae-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="46bae-105">Planejando a implantação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="46bae-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="46bae-106">Os seguintes recursos de MBAM representam a infraestrutura de servidor para a implantação de servidor MBAM:</span><span class="sxs-lookup"><span data-stu-id="46bae-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="46bae-107">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="46bae-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="46bae-108">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="46bae-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="46bae-109">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="46bae-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="46bae-110">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="46bae-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="46bae-111">Os bancos de dados e recursos do MBAM Server podem ser instalados em configurações diferentes, dependendo das suas necessidades de escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="46bae-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="46bae-112">Todos os recursos do MBAM Server podem ser instalados em um único servidor ou distribuídos entre vários servidores.</span><span class="sxs-lookup"><span data-stu-id="46bae-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="46bae-113">Geralmente, recomendamos que você use uma configuração de três servidores ou cinco servidores para ambientes de produção, embora configurações de dois ou quatro servidores também possam ser usadas, dependendo das suas necessidades de computação.</span><span class="sxs-lookup"><span data-stu-id="46bae-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="46bae-114">**Observação**  Para obter mais informações sobre a escalabilidade de desempenho de MBAM e as topologias de implantação recomendadas, consulte o White Paper MBAM redimensionation and High-Availability Guide at <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="46bae-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="46bae-115">Cada recurso MBAM tem pré-requisitos específicos.</span><span class="sxs-lookup"><span data-stu-id="46bae-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="46bae-116">Para obter uma lista completa de pré-requisitos de recursos de servidor e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="46bae-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="46bae-117">Além dos recursos do MBAM relacionados ao servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="46bae-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="46bae-118">Este modelo pode ser instalado em qualquer computador que possa executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="46bae-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="46bae-119">Ordem de implantação de recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="46bae-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="46bae-120">Ao implantar os recursos do MBAM Server, instale os recursos na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="46bae-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="46bae-121">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="46bae-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="46bae-122">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="46bae-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="46bae-123">Auditoria e relatórios de conformidade</span><span class="sxs-lookup"><span data-stu-id="46bae-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="46bae-124">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="46bae-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="46bae-125">Modelo de política</span><span class="sxs-lookup"><span data-stu-id="46bae-125">Policy Template</span></span>

<span data-ttu-id="46bae-126">**Observação**  Mantenha o controle dos nomes dos computadores nos quais você instala cada recurso.</span><span class="sxs-lookup"><span data-stu-id="46bae-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="46bae-127">Você usará essas informações durante todo o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="46bae-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="46bae-128">Você pode imprimir e usar uma lista de verificação de implantação para ajudá-lo no processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="46bae-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="46bae-129">Para obter mais informações sobre a lista de verificação de implantação do MBAM, consulte [lista de verificação de implantação do MBAM 1,0](mbam-10-deployment-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="46bae-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="46bae-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46bae-130">Related topics</span></span>


[<span data-ttu-id="46bae-131">Planejar a implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="46bae-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="46bae-132">Implantando a infraestrutura do Servidor do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="46bae-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





