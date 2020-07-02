---
title: Microsoft BitLocker Administration and Monitoring 2.5
description: Microsoft BitLocker Administration and Monitoring 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795350"
---
# <span data-ttu-id="86326-103">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="86326-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) 2,5 fornecem uma interface administrativa simplificada que você pode usar para gerenciar a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="86326-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="86326-105">Você configura os modelos de política de grupo do MBAM que permitem definir as opções de política de criptografia de unidade de disco BitLocker adequadas para a sua empresa e usá-las para monitorar a compatibilidade do cliente com essas políticas.</span><span class="sxs-lookup"><span data-stu-id="86326-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="86326-106">Você também pode relatar o status de criptografia de um computador individual e na empresa como um todo.</span><span class="sxs-lookup"><span data-stu-id="86326-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="86326-107">Além disso, você pode acessar informações da chave de recuperação quando os usuários esquecem seu PIN ou senha ou quando o BIOS ou o registro de inicialização muda.</span><span class="sxs-lookup"><span data-stu-id="86326-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="86326-108">Para obter uma descrição mais detalhada do MBAM, consulte [sobre o MBAM 2,5](about-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="86326-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="86326-109">Para obter o MBAM, confira [como faço para obter o MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span><span class="sxs-lookup"><span data-stu-id="86326-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="86326-110">Vários</span><span class="sxs-lookup"><span data-stu-id="86326-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="86326-111">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="86326-112">Sobre o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="86326-113">Notas de versão do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="86326-114">Sobre o MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="86326-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="86326-115">Notas de versão do MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="86326-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="86326-116">Avaliando o MBAM 2.5 em um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="86326-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="86326-117">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="86326-118">Acessibilidade do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="86326-119">Planejamento do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="86326-120">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="86326-121">Pré-requisitos para implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="86326-122">Planejamento para os requisitos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="86326-123">Planejamento para contas e grupos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="86326-124">Planejamento de formas para proteger os sites do MBAM</span><span class="sxs-lookup"><span data-stu-id="86326-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="86326-125">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="86326-126">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="86326-127">Planejando a alta disponibilidade do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="86326-128">Considerações sobre segurança do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="86326-129">Lista de verificação de planejamento para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="86326-130">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="86326-131">Implantando a infraestrutura de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="86326-132">Implantando objetos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="86326-133">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="86326-134">Lista de verificação para implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="86326-135">Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores</span><span class="sxs-lookup"><span data-stu-id="86326-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="86326-136">Removendo os recursos de servidor ou o software do MBAM</span><span class="sxs-lookup"><span data-stu-id="86326-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="86326-137">Operações do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="86326-138">Administrando os recursos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="86326-139">Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="86326-140">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="86326-141">Manutenção do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="86326-142">Usando o Windows PowerShell para administrar o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="86326-143">Solução de problemas do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="86326-144">Referência técnica do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="86326-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="86326-145">Logs de eventos do cliente</span><span class="sxs-lookup"><span data-stu-id="86326-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="86326-146">Logs de eventos do servidor</span><span class="sxs-lookup"><span data-stu-id="86326-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="86326-147">Mais informações</span><span class="sxs-lookup"><span data-stu-id="86326-147">More Information</span></span>

- [<span data-ttu-id="86326-148">Experiência de informações do MDOP</span><span class="sxs-lookup"><span data-stu-id="86326-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="86326-149">Encontre documentação, vídeos e outros recursos para tecnologias do MDOP.</span><span class="sxs-lookup"><span data-stu-id="86326-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="86326-150">Guia de implantação do MBAM</span><span class="sxs-lookup"><span data-stu-id="86326-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="86326-151">Obtenha ajuda para escolher um método de implantação para MBAM, incluindo instruções passo a passo para cada método.</span><span class="sxs-lookup"><span data-stu-id="86326-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="86326-152">Aplicar hotfixes no servidor do MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="86326-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="86326-153">Guia de como aplicar hotfixes do servidor do MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="86326-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
