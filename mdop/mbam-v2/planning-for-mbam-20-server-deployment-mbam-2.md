---
title: Planejar implantação de servidor MBAM 2.0
description: Planejar implantação de servidor MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796043"
---
# <span data-ttu-id="79d01-103">Planejar implantação de servidor MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="79d01-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="79d01-104">A infraestrutura de servidor de administração e monitoramento do Microsoft BitLocker (MBAM) depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa.</span><span class="sxs-lookup"><span data-stu-id="79d01-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="79d01-105">Se você estiver instalando a administração e o monitoramento do Microsoft BitLocker com a topologia do Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="79d01-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="79d01-106">**Observação**  As instalações do Microsoft BitLocker Administration and Monitoring em um único servidor são recomendadas apenas para ambientes de teste.</span><span class="sxs-lookup"><span data-stu-id="79d01-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="79d01-107">Planejando a implantação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="79d01-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="79d01-108">A infraestrutura para uma implantação do MBAM Server inclui os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="79d01-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="79d01-109">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="79d01-109">Recovery Database</span></span>

-   <span data-ttu-id="79d01-110">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="79d01-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="79d01-111">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="79d01-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="79d01-112">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="79d01-112">Self-Service Portal</span></span>

-   <span data-ttu-id="79d01-113">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="79d01-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="79d01-114">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="79d01-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="79d01-115">Os bancos de dados e recursos do MBAM Server podem ser instalados em configurações diferentes, dependendo dos requisitos de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="79d01-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="79d01-116">Todos os recursos do MBAM Server podem ser instalados em um único servidor ou distribuídos entre vários servidores.</span><span class="sxs-lookup"><span data-stu-id="79d01-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="79d01-117">Recomendamos que você use uma configuração de dois servidores para ambientes de produção, embora configurações de dois a quatro servidores também possam ser usadas, dependendo de suas necessidades de computação.</span><span class="sxs-lookup"><span data-stu-id="79d01-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="79d01-118">Cada recurso MBAM tem pré-requisitos específicos.</span><span class="sxs-lookup"><span data-stu-id="79d01-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="79d01-119">Para obter uma lista completa de pré-requisitos de recursos de servidor e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="79d01-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="79d01-120">Além dos recursos do MBAM relacionados ao servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="79d01-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="79d01-121">O modelo contém configurações de objeto de política de grupo (GPO) que você configura para gerenciar a criptografia de unidade de disco BitLocker na empresa.</span><span class="sxs-lookup"><span data-stu-id="79d01-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="79d01-122">Você pode instalar esse modelo em qualquer computador que possa executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="79d01-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="79d01-123">Ao planejar a implantação do MBAM Server, considere que as chaves de recuperação do BitLocker no MBAM devem ser somente para uso único, após o vencimento das chaves de recuperação.</span><span class="sxs-lookup"><span data-stu-id="79d01-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="79d01-124">Para que as chaves expirem após o uso, elas devem ser recuperadas por meio do portal de suporte técnico ou do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="79d01-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="79d01-125">Ordem de implantação de recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="79d01-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="79d01-126">Para implantar recursos do MBAM em vários servidores, você precisa instalar os recursos na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="79d01-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="79d01-127">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="79d01-127">Recovery Database</span></span>

2.  <span data-ttu-id="79d01-128">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="79d01-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="79d01-129">Auditoria e relatórios de conformidade</span><span class="sxs-lookup"><span data-stu-id="79d01-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="79d01-130">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="79d01-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="79d01-131">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="79d01-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="79d01-132">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="79d01-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="79d01-133">**Observação**  Mantenha o controle dos nomes dos computadores nos quais você instala cada recurso.</span><span class="sxs-lookup"><span data-stu-id="79d01-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="79d01-134">Você precisa usar essas informações em todo o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="79d01-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="79d01-135">Você pode imprimir e usar uma lista de verificação de implantação para ajudar nesse esforço.</span><span class="sxs-lookup"><span data-stu-id="79d01-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="79d01-136">Para obter mais informações sobre a lista de verificação de implantação do MBAM, consulte [lista de verificação de implantação do MBAM 2,0](mbam-20-deployment-checklist-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="79d01-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="79d01-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79d01-137">Related topics</span></span>


[<span data-ttu-id="79d01-138">Planejar a implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="79d01-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="79d01-139">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="79d01-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





