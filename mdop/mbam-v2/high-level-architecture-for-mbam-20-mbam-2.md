---
title: Arquitetura de alto nível para o MBAM 2.0
description: Arquitetura de alto nível para o MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799525"
---
# <span data-ttu-id="ba19c-103">Arquitetura de alto nível para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ba19c-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="ba19c-104">O Microsoft BitLocker Administration and Monitoring (MBAM) é uma solução cliente/servidor que pode ajudá-lo a simplificar o provisionamento e a implantação do BitLocker, melhorar a conformidade e os relatórios sobre o BitLocker e reduzir os custos de suporte.</span><span class="sxs-lookup"><span data-stu-id="ba19c-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="ba19c-105">A administração e o monitoramento do Microsoft BitLocker incluem os recursos descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ba19c-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="ba19c-106">A administração e o monitoramento do Microsoft BitLocker podem ser implantados na topologia autônoma ou em uma topologia integrada ao Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="ba19c-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="ba19c-107">Este tópico descreve a arquitetura para a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="ba19c-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="ba19c-108">Para obter informações sobre a implantação na topologia do Gerenciador de configurações integradas, consulte [usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="ba19c-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="ba19c-109">O diagrama a seguir mostra a arquitetura recomendada MBAM para um ambiente de produção, que consiste em dois servidores e uma estação de trabalho de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ba19c-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="ba19c-110">Essa arquitetura dá suporte a até 200.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="ba19c-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="ba19c-111">Os recursos do servidor e os bancos de dados na imagem da arquitetura são descritos na seção a seguir e estão listados no computador ou servidor onde recomendamos que você os instale.</span><span class="sxs-lookup"><span data-stu-id="ba19c-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="ba19c-112">**Observação**  Uma arquitetura de servidor único deve ser usada somente em ambientes de teste.</span><span class="sxs-lookup"><span data-stu-id="ba19c-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![MBAM 2 2-topologia de implantação do servidor](images/mbam2-3-servers.gif)

## <span data-ttu-id="ba19c-114">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="ba19c-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="ba19c-115">Os recursos a seguir estão instalados neste servidor:</span><span class="sxs-lookup"><span data-stu-id="ba19c-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="ba19c-116">**Servidor de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="ba19c-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="ba19c-117">O recurso servidor de administração e monitoramento é instalado em um servidor Windows e consiste no site de administração e monitoramento, que inclui os relatórios e o portal de suporte técnico e os serviços Web de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="ba19c-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="ba19c-118">**Portal de autoatendimento**.</span><span class="sxs-lookup"><span data-stu-id="ba19c-118">**Self-Service Portal**.</span></span> <span data-ttu-id="ba19c-119">O portal de autoatendimento está instalado em um servidor Windows.</span><span class="sxs-lookup"><span data-stu-id="ba19c-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="ba19c-120">O portal de autoatendimento permite que os usuários finais em computadores cliente façam logon independentemente em um site, onde eles podem obter uma chave de recuperação para recuperar um volume do BitLocker bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ba19c-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="ba19c-121">Servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="ba19c-121">Database Server</span></span>


<span data-ttu-id="ba19c-122">Os recursos a seguir estão instalados neste servidor:</span><span class="sxs-lookup"><span data-stu-id="ba19c-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="ba19c-123">**Banco de dados de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="ba19c-123">**Recovery Database**.</span></span> <span data-ttu-id="ba19c-124">O banco de dados de recuperação está instalado em um servidor Windows e uma instância com suporte do Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="ba19c-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="ba19c-125">Esse banco de dados armazena dados de recuperação coletados de computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ba19c-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="ba19c-126">**Banco de dados de auditoria e conformidade**.</span><span class="sxs-lookup"><span data-stu-id="ba19c-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="ba19c-127">O banco de dados de conformidade e auditoria está instalado em um servidor Windows e uma instância com suporte do SQLServer.</span><span class="sxs-lookup"><span data-stu-id="ba19c-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="ba19c-128">Esse banco de dados armazena dados de conformidade para computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ba19c-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="ba19c-129">Esses dados são usados principalmente para relatórios que os SQL Server Reporting Services (SSRS) hospedam.</span><span class="sxs-lookup"><span data-stu-id="ba19c-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="ba19c-130">**Relatórios de conformidade e auditoria**.</span><span class="sxs-lookup"><span data-stu-id="ba19c-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="ba19c-131">Os relatórios de conformidade e auditoria são instalados em um servidor Windows e uma instância com suporte do SQLServer que tem o recurso do SQL Server Reporting Services (SSRS) instalado.</span><span class="sxs-lookup"><span data-stu-id="ba19c-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="ba19c-132">Esses relatórios fornecem relatórios do MBAM que você pode acessar a partir do site de administração e monitoramento ou diretamente do servidor SSRS.</span><span class="sxs-lookup"><span data-stu-id="ba19c-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="ba19c-133">Estação de trabalho de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ba19c-133">Management Workstation</span></span>


<span data-ttu-id="ba19c-134">O recurso a seguir está instalado na estação de trabalho de gerenciamento, que pode ser um servidor Windows ou um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="ba19c-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="ba19c-135">**Modelo de política**.</span><span class="sxs-lookup"><span data-stu-id="ba19c-135">**Policy Template**.</span></span> <span data-ttu-id="ba19c-136">O modelo de política consiste em configurações de política de grupo que definem as configurações de implementação MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ba19c-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="ba19c-137">Você pode instalar o modelo de política em qualquer servidor ou estação de trabalho, mas ele geralmente está instalado em uma estação de trabalho de gerenciamento, que é um computador cliente ou servidor com suporte.</span><span class="sxs-lookup"><span data-stu-id="ba19c-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="ba19c-138">A estação de trabalho não precisa ser um computador dedicado.</span><span class="sxs-lookup"><span data-stu-id="ba19c-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="ba19c-139">Cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="ba19c-139">MBAM Client</span></span>


<span data-ttu-id="ba19c-140">O cliente do MBAM está instalado em um computador com Windows e tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="ba19c-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="ba19c-141">Usa a política de grupo para impor a criptografia de unidade de disco BitLocker dos computadores cliente da empresa.</span><span class="sxs-lookup"><span data-stu-id="ba19c-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="ba19c-142">Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).</span><span class="sxs-lookup"><span data-stu-id="ba19c-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="ba19c-143">Coleta dados de conformidade do computador e passa os dados para o sistema de relatórios.</span><span class="sxs-lookup"><span data-stu-id="ba19c-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="ba19c-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba19c-144">Related topics</span></span>


[<span data-ttu-id="ba19c-145">Introdução ao MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ba19c-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





