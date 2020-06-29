---
title: Configurando os recursos de servidor do MBAM 2.5
description: Configurando os recursos de servidor do MBAM 2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799196"
---
# <span data-ttu-id="ed01d-103">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="ed01d-104">Use estas informações como um local inicial para configurar os recursos do servidor do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 após [a instalação do software do MBAM 2,5 Server](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="ed01d-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="ed01d-105">Há dois métodos que você pode usar para configurar o MBAM:</span><span class="sxs-lookup"><span data-stu-id="ed01d-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="ed01d-106">Assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="ed01d-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="ed01d-107">Cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed01d-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="ed01d-108">Antes de começar a configurar os recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ed01d-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="ed01d-109">Examine e conclua as etapas a seguir antes de começar a configurar os recursos do servidor do MBAM:</span><span class="sxs-lookup"><span data-stu-id="ed01d-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ed01d-110">Etapa</span><span class="sxs-lookup"><span data-stu-id="ed01d-110">Step</span></span></th>
<th align="left"><span data-ttu-id="ed01d-111">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="ed01d-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed01d-112">Examine a arquitetura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed01d-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="ed01d-113">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed01d-114">Examine as configurações com suporte para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed01d-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="ed01d-115">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed01d-116">Complete os pré-requisitos obrigatórios em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="ed01d-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="ed01d-117">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ed01d-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="ed01d-118">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ed01d-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed01d-119">Instale o software do servidor MBAM em cada servidor em que você irá configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed01d-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="ed01d-120">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed01d-121">Examine os pré-requisitos para usar o Windows PowerShell para configurar os recursos do MBAM Server (se você estiver usando esse método para configurar os recursos do MBAM Server).</span><span class="sxs-lookup"><span data-stu-id="ed01d-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="ed01d-122">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed01d-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ed01d-123">Etapas para configurar os recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ed01d-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="ed01d-124">Cada linha na tabela a seguir descreve os recursos que você irá configurar em um servidor separado, de acordo com a [arquitetura de alto nível recomendada para o MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="ed01d-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ed01d-125">Recursos para instalar</span><span class="sxs-lookup"><span data-stu-id="ed01d-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="ed01d-126">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="ed01d-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed01d-127">Configurar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="ed01d-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="ed01d-128">Como configurar os bancos de dados do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed01d-129">Configurar os relatórios.</span><span class="sxs-lookup"><span data-stu-id="ed01d-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="ed01d-130">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed01d-131">Configurar os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="ed01d-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="ed01d-132">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed01d-133">Configurar a integração do System Center Configuration Manager (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="ed01d-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="ed01d-134">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ed01d-135">Para obter uma lista de eventos sobre a configuração de recursos do servidor do MBAM, consulte [logs de eventos do servidor](server-event-logs.md).</span><span class="sxs-lookup"><span data-stu-id="ed01d-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="ed01d-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed01d-136">Related topics</span></span>


<span data-ttu-id="ed01d-137">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed01d-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="ed01d-138">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="ed01d-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ed01d-139">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ed01d-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ed01d-140">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ed01d-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




