---
title: Implantação da infraestrutura de servidor do MBAM 2.0
description: Implantação da infraestrutura de servidor do MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799536"
---
# <span data-ttu-id="5e992-103">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5e992-103">Deploying the MBAM 2.0 Server Infrastructure</span></span>


<span data-ttu-id="5e992-104">Os recursos de servidor de administração e monitoramento do Microsoft BitLocker (MBAM) para a topologia autônoma podem ser instalados em diferentes configurações em dois ou mais servidores em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="5e992-104">Microsoft BitLocker Administration and Monitoring (MBAM) Server features for the Stand-alone topology can be installed in different configurations on two or more servers in a production environment.</span></span> <span data-ttu-id="5e992-105">A configuração recomendada é de dois servidores para um ambiente de produção, dependendo dos requisitos de escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="5e992-105">The recommended configuration is two servers for a production environment, depending on your scalability requirements.</span></span> <span data-ttu-id="5e992-106">Use um único servidor para uma instalação do MBAM somente em ambientes de teste.</span><span class="sxs-lookup"><span data-stu-id="5e992-106">Use a single server for an MBAM installation only in test environments.</span></span> <span data-ttu-id="5e992-107">Para obter mais informações sobre como planejar a implantação de recursos do servidor MBAM, consulte [planejando a implantação do MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="5e992-107">For more information about planning for the MBAM Server feature deployment, see [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span></span>

<span data-ttu-id="5e992-108">O diagrama a seguir mostra um exemplo de como você pode configurar a implantação de MBAM de dois servidores recomendada.</span><span class="sxs-lookup"><span data-stu-id="5e992-108">The following diagram shows an example of how you can configure the recommended two-server MBAM deployment.</span></span> <span data-ttu-id="5e992-109">Essa configuração oferece suporte a até 200.000 clientes do MBAM em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="5e992-109">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span> <span data-ttu-id="5e992-110">Os recursos do servidor e os bancos de dados na imagem da arquitetura são descritos na seção a seguir e estão listados no computador ou servidor onde recomendamos que você os instale.</span><span class="sxs-lookup"><span data-stu-id="5e992-110">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

![MBAM 2 2-topologia de implantação do servidor](images/mbam2-3-servers.gif)

## <span data-ttu-id="5e992-112">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="5e992-112">Administration and Monitoring Server</span></span>


<span data-ttu-id="5e992-113">Os recursos a seguir estão instalados neste servidor:</span><span class="sxs-lookup"><span data-stu-id="5e992-113">The following features are installed on this server:</span></span>

-   <span data-ttu-id="5e992-114">**Servidor de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="5e992-114">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="5e992-115">O recurso do servidor de administração e monitoramento é instalado em um servidor Windows e consiste no site de suporte técnico e nos serviços Web de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="5e992-115">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Help Desk website and the monitoring web services.</span></span>

-   <span data-ttu-id="5e992-116">**Portal de autoatendimento**.</span><span class="sxs-lookup"><span data-stu-id="5e992-116">**Self-Service Portal**.</span></span> <span data-ttu-id="5e992-117">O portal de autoatendimento está instalado em um servidor Windows.</span><span class="sxs-lookup"><span data-stu-id="5e992-117">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="5e992-118">O portal de autoatendimento permite que os usuários finais em computadores cliente façam logon independentemente em um site, onde eles podem obter uma chave de recuperação para recuperar um volume do BitLocker bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5e992-118">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="5e992-119">Servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="5e992-119">Database Server</span></span>


<span data-ttu-id="5e992-120">Os recursos a seguir estão instalados neste servidor:</span><span class="sxs-lookup"><span data-stu-id="5e992-120">The following features are installed on this server:</span></span>

-   <span data-ttu-id="5e992-121">**Banco de dados de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="5e992-121">**Recovery Database**.</span></span> <span data-ttu-id="5e992-122">O banco de dados de recuperação está instalado em um servidor Windows e uma instância com suporte do Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="5e992-122">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="5e992-123">Esse banco de dados armazena dados de recuperação coletados de computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="5e992-123">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="5e992-124">**Banco de dados de auditoria e conformidade**.</span><span class="sxs-lookup"><span data-stu-id="5e992-124">**Compliance and Audit Database**.</span></span> <span data-ttu-id="5e992-125">O banco de dados de conformidade e auditoria está instalado em um servidor Windows e uma instância com suporte do SQLServer.</span><span class="sxs-lookup"><span data-stu-id="5e992-125">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="5e992-126">Esse banco de dados armazena dados de conformidade para computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="5e992-126">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="5e992-127">Esses dados são usados principalmente para relatórios que os SQL Server Reporting Services (SSRS) hospedam.</span><span class="sxs-lookup"><span data-stu-id="5e992-127">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="5e992-128">**Relatórios de conformidade e auditoria**.</span><span class="sxs-lookup"><span data-stu-id="5e992-128">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="5e992-129">Os relatórios de conformidade e auditoria são instalados em um servidor Windows e uma instância com suporte do SQLServer que tem o recurso do SQL Server Reporting Services (SSRS) instalado.</span><span class="sxs-lookup"><span data-stu-id="5e992-129">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="5e992-130">Esses relatórios fornecem relatórios do MBAM que você pode acessar a partir do site do suporte técnico ou diretamente do servidor do SSRS.</span><span class="sxs-lookup"><span data-stu-id="5e992-130">These reports provide MBAM reports that you can access from the Help Desk website or directly from the SSRS server.</span></span>

## <span data-ttu-id="5e992-131">Estação de trabalho de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5e992-131">Management Workstation</span></span>


<span data-ttu-id="5e992-132">O recurso a seguir está instalado na estação de trabalho de gerenciamento, que pode ser um servidor Windows ou um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="5e992-132">The following feature is installed on the Management Workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="5e992-133">**Modelo de política**.</span><span class="sxs-lookup"><span data-stu-id="5e992-133">**Policy Template**.</span></span> <span data-ttu-id="5e992-134">O modelo de política consiste em políticas de grupo que definem as configurações de implementação de MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e992-134">The Policy Template consists of Group Policies that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="5e992-135">Você pode instalar o modelo de política em qualquer servidor ou estação de trabalho, mas ele geralmente está instalado em uma estação de trabalho de gerenciamento, que é um computador cliente ou servidor com suporte.</span><span class="sxs-lookup"><span data-stu-id="5e992-135">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="5e992-136">A estação de trabalho não precisa ser um computador dedicado.</span><span class="sxs-lookup"><span data-stu-id="5e992-136">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="5e992-137">Cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="5e992-137">MBAM Client</span></span>


<span data-ttu-id="5e992-138">O cliente do MBAM está instalado em um computador com Windows e tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="5e992-138">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="5e992-139">Usa a política de grupo para impor a criptografia de unidade de disco BitLocker dos computadores cliente da empresa.</span><span class="sxs-lookup"><span data-stu-id="5e992-139">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="5e992-140">Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).</span><span class="sxs-lookup"><span data-stu-id="5e992-140">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="5e992-141">Coleta dados de conformidade do computador e passa os dados para o sistema de relatórios.</span><span class="sxs-lookup"><span data-stu-id="5e992-141">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="5e992-142">Outros recursos para a implantação de recursos do MBAM 2,0 Server</span><span class="sxs-lookup"><span data-stu-id="5e992-142">Other Resources for Deploying MBAM 2.0 Server Features</span></span>


[<span data-ttu-id="5e992-143">Implantando o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5e992-143">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





