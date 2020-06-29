---
title: Implantando a infraestrutura do Servidor do MBAM 1.0
description: Implantando a infraestrutura do Servidor do MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799620"
---
# <span data-ttu-id="1653b-103">Implantando a infraestrutura do Servidor do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1653b-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="1653b-104">Você pode instalar os recursos do servidor de administração e monitoramento do Microsoft BitLocker (MBAM) em diferentes configurações usando um a cinco servidores.</span><span class="sxs-lookup"><span data-stu-id="1653b-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="1653b-105">Geralmente, você deve usar uma configuração de três a cinco servidores para ambientes de produção, dependendo de suas necessidades de escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="1653b-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="1653b-106">Para obter mais informações sobre a escalabilidade de desempenho de MBAM e topologias de implantação recomendadas, consulte o [White Paper MBAM Redimensionation and High-Availability Guide](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span><span class="sxs-lookup"><span data-stu-id="1653b-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="1653b-107">Implantar todas as MBAM 1,0 em um único servidor</span><span class="sxs-lookup"><span data-stu-id="1653b-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="1653b-108">Nesta configuração, todos os recursos do MBAM são instalados em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="1653b-109">Esta topologia de implantação para a infraestrutura do MBAM Server dará suporte a até 21.000 MBAM computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="1653b-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="1653b-110">**Importante**  Essa configuração tem suporte, mas recomendamos que ela seja testada apenas.</span><span class="sxs-lookup"><span data-stu-id="1653b-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="1653b-111">Os procedimentos desta seção descrevem a instalação completa dos recursos do MBAM em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="1653b-112">Como instalar e configurar o MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="1653b-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="1653b-113">Implantar o MBAM 1,0 em servidores distribuídos</span><span class="sxs-lookup"><span data-stu-id="1653b-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="1653b-114">Os recursos do MBAM podem ser instalados em configurações diferentes, dependendo de suas necessidades de escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="1653b-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="1653b-115">Para obter mais informações sobre como planejar a implantação de recursos do MBAM Server, consulte [planejando a implantação do MBAM 1,0 Server](planning-for-mbam-10-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="1653b-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="1653b-116">Os procedimentos desta seção descrevem a instalação completa dos recursos do MBAM em servidores distribuídos.</span><span class="sxs-lookup"><span data-stu-id="1653b-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="1653b-117">Configuração de três computadores</span><span class="sxs-lookup"><span data-stu-id="1653b-117">Three-computer configuration</span></span>

<span data-ttu-id="1653b-118">O diagrama a seguir exibe a topologia de implantação de três computadores para MBAM.</span><span class="sxs-lookup"><span data-stu-id="1653b-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1653b-119">Recomendamos Esta topologia para ambientes de produção que dão suporte a até 55.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="1653b-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![MBAM a topologia de implantação do computador](images/mbam-3-server.jpg)

<span data-ttu-id="1653b-121">Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="1653b-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1653b-122">Bancos de dados de recuperação e de hardware, conformidade e auditoria, e conformidade e relatórios de auditoria são instalados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="1653b-123">O recurso de servidor de administração e monitoramento está instalado em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="1653b-124">MBAM modelo de política de grupo está instalado em um computador que é capaz de modificar objetos de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="1653b-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="1653b-125">Configuração de quatro computadores</span><span class="sxs-lookup"><span data-stu-id="1653b-125">Four-computer configuration</span></span>

<span data-ttu-id="1653b-126">O diagrama a seguir exibe a topologia de implantação de quatro computadores para MBAM.</span><span class="sxs-lookup"><span data-stu-id="1653b-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1653b-127">Recomendamos Esta topologia para ambientes de produção que dão suporte a até 110.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="1653b-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![MBAM 4 topologia de implantação do computador.](images/mbam-4-computer.jpg)

<span data-ttu-id="1653b-129">Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="1653b-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1653b-130">Bancos de dados de recuperação e de hardware, conformidade e auditoria, e conformidade e relatórios de auditoria são instalados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="1653b-131">O recurso de administração e administração do servidor está instalado em um servidor configurado em um cluster de servidor de balanceamento de carga de rede (NLB).</span><span class="sxs-lookup"><span data-stu-id="1653b-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="1653b-132">MBAM modelo de política de grupo está instalado em um computador que é capaz de modificar os objetos de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="1653b-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="1653b-133">Configuração de cinco computadores</span><span class="sxs-lookup"><span data-stu-id="1653b-133">Five-computer configuration</span></span>

<span data-ttu-id="1653b-134">O diagrama a seguir exibe a topologia de implantação de cinco computadores para MBAM.</span><span class="sxs-lookup"><span data-stu-id="1653b-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1653b-135">Recomendamos Esta topologia para ambientes de produção que dão suporte a até 135.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="1653b-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![MBAM cinco topologia de implantação do computador.](images/mbam-5-computer.jpg)

<span data-ttu-id="1653b-137">Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="1653b-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1653b-138">Recuperação e banco de dados de hardware instalado em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="1653b-139">O banco de dados de conformidade e auditoria e a conformidade e os relatórios de auditoria são instalados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1653b-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="1653b-140">O recurso de administração e administração do servidor está instalado em um servidor configurado em um cluster de servidor de balanceamento de carga de rede (NLB).</span><span class="sxs-lookup"><span data-stu-id="1653b-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="1653b-141">MBAM modelo de política de grupo está instalado em um computador que é capaz de modificar objetos de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="1653b-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="1653b-142">Como instalar e configurar o MBAM em servidores distribuídos</span><span class="sxs-lookup"><span data-stu-id="1653b-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="1653b-143">Como configurar os Balanceamento de Carga de Rede para o MBAM</span><span class="sxs-lookup"><span data-stu-id="1653b-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="1653b-144">Outros recursos para a implantação de recursos do MBAM 1,0 Server</span><span class="sxs-lookup"><span data-stu-id="1653b-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="1653b-145">Implantando o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1653b-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





