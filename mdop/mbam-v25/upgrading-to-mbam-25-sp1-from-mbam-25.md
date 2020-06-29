---
title: Atualizando do MBAM 2.5 para o MBAM 2.5 SP1
description: Atualizando do MBAM 2.5 para o MBAM 2.5 SP1
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796076"
---
# <span data-ttu-id="e0274-103">Atualizando do MBAM 2.5 para o MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="e0274-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="e0274-104">Este tópico descreve o processo de atualização do servidor de administração e monitoramento do Microsoft BitLocker (MBAM) 2,5 e do cliente MBAM do 2,5 para o MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="e0274-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="e0274-105">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="e0274-105">Before you begin</span></span>
#### <span data-ttu-id="e0274-106">Baixe o lançamento de manutenção de maio de 2019</span><span class="sxs-lookup"><span data-stu-id="e0274-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="e0274-107">Desktop Optimization Pack</span><span class="sxs-lookup"><span data-stu-id="e0274-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="e0274-108">Verificar a instalação do documentaion</span><span class="sxs-lookup"><span data-stu-id="e0274-108">Verify the installation documentaion</span></span>
<span data-ttu-id="e0274-109">Verifique se você tem uma documentação atual do seu ambiente MBAM, incluindo todos os nomes de servidor, nomes de banco de dados, contas de serviço e suas senhas.</span><span class="sxs-lookup"><span data-stu-id="e0274-109">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="e0274-110">Etapas de atualização</span><span class="sxs-lookup"><span data-stu-id="e0274-110">Upgrade steps</span></span>
#### <span data-ttu-id="e0274-111">Etapas para atualizar o banco de dados do MBAM (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="e0274-111">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="e0274-112">Usando o configurador MBAM; Remova a função relatórios do SQL Server ou onde o banco de dados do SSRS estiver hospedado.</span><span class="sxs-lookup"><span data-stu-id="e0274-112">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="e0274-113">Dependendo do seu ambiente, ele pode ser o mesmo servidor ou um separado.</span><span class="sxs-lookup"><span data-stu-id="e0274-113">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="e0274-114">Você não verá uma opção para remover os bancos de dados; Isso é esperado.</span><span class="sxs-lookup"><span data-stu-id="e0274-114">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="e0274-115">Instale o 2,5 SP1 (localizado com o MDOP-Microsoft Desktop Optimization Pack 2015 do site do centro de serviços de licenciamento por volume:</span><span class="sxs-lookup"><span data-stu-id="e0274-115">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="e0274-116">Não configurar no momento</span><span class="sxs-lookup"><span data-stu-id="e0274-116">Do not configure it at this time</span></span> 
4. <span data-ttu-id="e0274-117">Usando o configurador MBAM; Adicionar novamente a função relatórios</span><span class="sxs-lookup"><span data-stu-id="e0274-117">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="e0274-118">Usando o configurador MBAM; Adicionar novamente a função de banco de dados SQL ao SQL Server</span><span class="sxs-lookup"><span data-stu-id="e0274-118">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="e0274-119">No final, você será avisado de que os bancos de bancos já existem e não foram criados, mas isso é esperado</span><span class="sxs-lookup"><span data-stu-id="e0274-119">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="e0274-120">Esse processo atualiza os bancos de dados existentes para a versão atual que está sendo instalada.</span><span class="sxs-lookup"><span data-stu-id="e0274-120">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="e0274-121">Etapas para atualizar o servidor MBAM (executando MBAM e IIS)</span><span class="sxs-lookup"><span data-stu-id="e0274-121">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="e0274-122">Usando o configurador MBAM; remover os portais de administração e de autoatendimento do servidor IIS</span><span class="sxs-lookup"><span data-stu-id="e0274-122">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="e0274-123">Instalar o MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="e0274-123">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="e0274-124">Não configurar no momento</span><span class="sxs-lookup"><span data-stu-id="e0274-124">Do not configure it at this time</span></span>  
4. <span data-ttu-id="e0274-125">Usando o configurador MBAM; Adicionar novamente os portais de administração e de autoatendimento ao servidor IIS</span><span class="sxs-lookup"><span data-stu-id="e0274-125">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="e0274-126">Abra um prompt de comando elevado, digite **iisreset**e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="e0274-126">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="e0274-127">Etapas para atualizar os clientes do MBAM/pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="e0274-127">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="e0274-128">Desinstalar o agente do 2,5 dos pontos de extremidade do cliente</span><span class="sxs-lookup"><span data-stu-id="e0274-128">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="e0274-129">Instalar o agente do 2,5 SP1 nos pontos de extremidade do cliente</span><span class="sxs-lookup"><span data-stu-id="e0274-129">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="e0274-130">Empurre a atualização de cliente de pacote de maio de 2019 para clientes que executam o agente do 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="e0274-130">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="e0274-131">Não é necessário desinstalar o cliente existente antes de instalar o pacote de maio de 2019.</span><span class="sxs-lookup"><span data-stu-id="e0274-131">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
