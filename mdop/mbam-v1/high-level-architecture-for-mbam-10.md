---
title: Arquitetura de alto nível para o MBAM 1.0
description: Arquitetura de alto nível para o MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799632"
---
# <span data-ttu-id="8df37-103">Arquitetura de alto nível para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8df37-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="8df37-104">O Microsoft BitLocker Administration and Monitoring (MBAM) é uma solução de criptografia de dados cliente/servidor que pode ajudá-lo a simplificar a implantação e o provisionamento de BitLocker, melhorar a conformidade e os relatórios do BitLocker, além de reduzir os custos de suporte.</span><span class="sxs-lookup"><span data-stu-id="8df37-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="8df37-105">O MBAM inclui os recursos descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8df37-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="8df37-106">Além disso, há um vídeo que fornece uma visão geral da arquitetura MBAM e da configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="8df37-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="8df37-107">Para obter mais informações, consulte [visão geral da arquitetura e implantação do MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span><span class="sxs-lookup"><span data-stu-id="8df37-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="8df37-108">Visão geral da arquitetura</span><span class="sxs-lookup"><span data-stu-id="8df37-108">Architecture Overview</span></span>


<span data-ttu-id="8df37-109">O diagrama a seguir exibe a arquitetura MBAM.</span><span class="sxs-lookup"><span data-stu-id="8df37-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="8df37-110">A topologia de implantação do MBAM do servidor único é mostrada para apresentar os recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="8df37-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="8df37-111">No entanto, essa topologia de implantação do MBAM é recomendada apenas para ambientes de laboratório.</span><span class="sxs-lookup"><span data-stu-id="8df37-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="8df37-112">**Observação**  Pelo menos uma topologia de implantação do MBAM de três computadores é recomendada para uma implantação de produção.</span><span class="sxs-lookup"><span data-stu-id="8df37-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="8df37-113">Para obter mais informações sobre topologias de implantação do MBAM, consulte [implantando a infraestrutura de servidor do MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="8df37-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![topologia de implantação de servidor único do MBAM](images/mbam-1-server.jpg)

1.  <span data-ttu-id="8df37-115">**Servidor de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="8df37-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="8df37-116">O servidor de administração e monitoramento do MBAM é instalado em um servidor Windows e hospeda o site de administração e gerenciamento do MBAM e os serviços Web de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="8df37-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="8df37-117">O site de administração e gerenciamento do MBAM é usado para determinar o status de conformidade empresarial, para a atividade de auditoria, para gerenciar o recurso de hardware e para acessar dados de recuperação, como as chaves de recuperação do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8df37-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="8df37-118">O servidor de administração e monitoramento se conecta aos seguintes bancos de dados e serviços:</span><span class="sxs-lookup"><span data-stu-id="8df37-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="8df37-119">Recuperação e banco de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="8df37-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="8df37-120">O banco de dados de recuperação e de hardware é instalado em um servidor baseado no Windows e na instância do SQLServer com suporte.</span><span class="sxs-lookup"><span data-stu-id="8df37-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="8df37-121">Esse banco de dados armazena dados de recuperação e informações de hardware coletados de computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="8df37-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="8df37-122">Banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="8df37-122">Compliance and Audit Database.</span></span> <span data-ttu-id="8df37-123">O banco de dados de conformidade e auditoria está instalado em um servidor Windows e na instância do SQLServer com suporte.</span><span class="sxs-lookup"><span data-stu-id="8df37-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="8df37-124">Esse banco de dados armazena dados de conformidade para computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="8df37-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="8df37-125">Esses dados são usados principalmente para relatórios que são hospedados pelo SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="8df37-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="8df37-126">Relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="8df37-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="8df37-127">Os relatórios de conformidade e auditoria são instalados em um servidor baseado no Windows e na instância do SQLServer com suporte que tem o recurso SSRS instalado.</span><span class="sxs-lookup"><span data-stu-id="8df37-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="8df37-128">Esses relatórios fornecem relatórios de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8df37-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="8df37-129">Esses relatórios podem ser acessados a partir do site de administração e gerenciamento do MBAM ou diretamente do servidor SSRS.</span><span class="sxs-lookup"><span data-stu-id="8df37-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="8df37-130">**Cliente MBAM**.</span><span class="sxs-lookup"><span data-stu-id="8df37-130">**MBAM Client**.</span></span> <span data-ttu-id="8df37-131">O cliente de administração e monitoramento do Microsoft BitLocker executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="8df37-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="8df37-132">Usa a política de grupo para impor a criptografia do BitLocker dos computadores cliente da empresa.</span><span class="sxs-lookup"><span data-stu-id="8df37-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="8df37-133">Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).</span><span class="sxs-lookup"><span data-stu-id="8df37-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="8df37-134">Coleta informações de recuperação e informações de hardware sobre os computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="8df37-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="8df37-135">Coleta dados de conformidade do computador e passa os dados para o sistema de relatórios.</span><span class="sxs-lookup"><span data-stu-id="8df37-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="8df37-136">**Modelo de política**.</span><span class="sxs-lookup"><span data-stu-id="8df37-136">**Policy Template**.</span></span> <span data-ttu-id="8df37-137">O modelo de política de grupo do MBAM é instalado em um servidor ou computador cliente compatível com Windows.</span><span class="sxs-lookup"><span data-stu-id="8df37-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="8df37-138">Este modelo é usado para especificar as configurações de implementação do MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8df37-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="8df37-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8df37-139">Related topics</span></span>


[<span data-ttu-id="8df37-140">Introdução ao MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8df37-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





