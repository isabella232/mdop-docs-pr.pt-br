---
title: Atualização do MBAM 2,5 para o MBAM 2,5 SP1 atualização da versão de manutenção
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796082"
---
# <span data-ttu-id="e7671-102">Atualização do MBAM 2,5 para o MBAM 2,5 SP1 atualização da versão de manutenção</span><span class="sxs-lookup"><span data-stu-id="e7671-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="e7671-103">Este artigo fornece instruções passo a passo para fazer a atualização do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para MBAM 2,5 Service Pack 1 (SP1) junto com o [Microsoft Desktop Optimization Pack (MDOP) pode 2019 atualização de serviço](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) em uma configuração autônoma.</span><span class="sxs-lookup"><span data-stu-id="e7671-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="e7671-104">Neste guia, usaremos uma configuração de dois servidores.</span><span class="sxs-lookup"><span data-stu-id="e7671-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="e7671-105">Um servidor será um servidor de banco de dados que está executando o Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e7671-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="e7671-106">Este servidor hospedará os bancos de dados e relatórios do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7671-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="e7671-107">O outro servidor será um servidor Web do Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e7671-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="e7671-108">Este servidor irá hospedar "administração e monitoramento" e "portal de autoatendimento".</span><span class="sxs-lookup"><span data-stu-id="e7671-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="e7671-109">Preparar-se para atualizar o MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="e7671-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="e7671-110">Conheça os servidores do MBAM em seu ambiente</span><span class="sxs-lookup"><span data-stu-id="e7671-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="e7671-111">Mecanismo de banco de dados do SQL Server: Server que hospeda os bancos de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7671-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="e7671-112">SQL Server Reporting Services: Server que hospeda os relatórios do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7671-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="e7671-113">Servidores Web dos serviços de informações da Internet (IIS): servidor que hospeda aplicativos Web do MBAM e serviços do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7671-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="e7671-114">Adicionais Servidor de site primário do Microsoft System Center Configuration Manager: o aplicativo de configuração do MBAM é executado neste servidor para integrar relatórios do MBAM com o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e7671-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="e7671-115">Esses relatórios são mesclados com os relatórios do Configuration Manager existentes na instância do SQL Server Reporting Services (SSRS) do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e7671-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="e7671-116">Identificar contas de serviço, grupos, nome do servidor e URL de relatórios</span><span class="sxs-lookup"><span data-stu-id="e7671-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="e7671-117">Identifique a conta de serviço do pool de aplicativos do MBAM que é usada pelos servidores Web do IIS para ler e gravar dados em bancos de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7671-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="e7671-118">Identifique os grupos que são usados durante a configuração de recursos da Web do MBAM e a URL do serviço Web relatórios.</span><span class="sxs-lookup"><span data-stu-id="e7671-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="e7671-119">Identifique o nome do SQL Server e o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="e7671-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="e7671-120">Assista a este vídeo para saber mais.</span><span class="sxs-lookup"><span data-stu-id="e7671-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="e7671-121">Identifique a conta do SQL Server Reporting Services que é usada para ler dados de conformidade do banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="e7671-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="e7671-122">Assista a este vídeo para saber mais.</span><span class="sxs-lookup"><span data-stu-id="e7671-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="e7671-123">Atualize a infraestrutura do MBAM para a versão mais recente disponível</span><span class="sxs-lookup"><span data-stu-id="e7671-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="e7671-124">A instalação ou atualização da infraestrutura do servidor MBAM é sempre executada na ordem listada abaixo:</span><span class="sxs-lookup"><span data-stu-id="e7671-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="e7671-125">Mecanismo de banco de dados do SQL Server: bancos de dados</span><span class="sxs-lookup"><span data-stu-id="e7671-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="e7671-126">SQL Server Reporting Services: relatórios</span><span class="sxs-lookup"><span data-stu-id="e7671-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="e7671-127">Servidor Web: aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="e7671-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="e7671-128">Servidor SCCM: relatórios integrados do SCCM, se aplicável</span><span class="sxs-lookup"><span data-stu-id="e7671-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="e7671-129">Clientes: agente do MBAM ou atualização do cliente</span><span class="sxs-lookup"><span data-stu-id="e7671-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="e7671-130">Modelos de política de Grupo: atualizar a política de grupo existente com novos modelos e habilitar novas configurações em uma política de grupo MBAM existente</span><span class="sxs-lookup"><span data-stu-id="e7671-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="e7671-131">Recomendamos que você crie um backup completo do banco de dados dos bancos de dados do MBAM antes de executar as atualizações.</span><span class="sxs-lookup"><span data-stu-id="e7671-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="e7671-132">Atualizar o MBAM SQL Server</span><span class="sxs-lookup"><span data-stu-id="e7671-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="e7671-133">Assista a este vídeo para saber como atualizar o MBAM SQL Server:</span><span class="sxs-lookup"><span data-stu-id="e7671-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="e7671-134">Atualizar o servidor Web do MBAM</span><span class="sxs-lookup"><span data-stu-id="e7671-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="e7671-135">Assista a este vídeo para saber como atualizar o servidor Web do MBAM:</span><span class="sxs-lookup"><span data-stu-id="e7671-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="e7671-136">Mais informações</span><span class="sxs-lookup"><span data-stu-id="e7671-136">More information</span></span>

<span data-ttu-id="e7671-137">Para obter mais informações sobre problemas conhecidos no MBAM 2,5 SP1, consulte [notas de versão para MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span><span class="sxs-lookup"><span data-stu-id="e7671-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>
