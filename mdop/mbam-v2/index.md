---
title: Guia do administrador do Microsoft BitLocker Administration and Monitoring 2
description: Guia do administrador do Microsoft BitLocker Administration and Monitoring 2
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795364"
---
# <span data-ttu-id="48fa5-103">Guia do administrador do Microsoft BitLocker Administration and Monitoring 2</span><span class="sxs-lookup"><span data-stu-id="48fa5-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="48fa5-104">O Microsoft BitLockerAdministration e o Monitoring (MBAM) 2.0 fornecem uma interface administrativa simplificada que você pode usar para gerenciar a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="48fa5-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="48fa5-105">No BitLockerAdministration e no Monitoring 2.0, você pode selecionar as opções de política de criptografia de unidade de disco BitLocker adequadas para a sua empresa e usá-las para monitorar a conformidade do cliente com essas políticas.</span><span class="sxs-lookup"><span data-stu-id="48fa5-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="48fa5-106">Você também pode relatar o status de criptografia de um computador individual e na empresa como um todo.</span><span class="sxs-lookup"><span data-stu-id="48fa5-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="48fa5-107">Além disso, você pode acessar informações da chave de recuperação quando os usuários esquecem seu PIN ou senha ou quando o BIOS ou o registro de inicialização muda.</span><span class="sxs-lookup"><span data-stu-id="48fa5-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="48fa5-108">Vários</span><span class="sxs-lookup"><span data-stu-id="48fa5-108">Outline</span></span>

- [<span data-ttu-id="48fa5-109">Introdução ao MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-110">Sobre o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-111">Notas de Versão do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-112">Sobre o MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="48fa5-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="48fa5-113">Notas de versão do MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="48fa5-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="48fa5-114">Avaliação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-115">Arquitetura de alto nível para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-116">Acessibilidade para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="48fa5-117">Planejamento para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-118">Como preparar seu ambiente para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-119">Pré-requisitos para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="48fa5-120">Planejar a implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-121">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="48fa5-122">Lista de Verificação de Planejamento do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="48fa5-123">Implantando o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-124">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="48fa5-125">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="48fa5-126">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="48fa5-127">Lista de verificação para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="48fa5-128">Atualizando de versões anteriores do MBAM</span><span class="sxs-lookup"><span data-stu-id="48fa5-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="48fa5-129">Operações do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-130">Usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="48fa5-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="48fa5-131">Administrando os Recursos do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="48fa5-132">Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-133">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="48fa5-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="48fa5-134">Manutenção do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-135">Segurança e privacidade para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="48fa5-136">Administrar o MBAM 2.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="48fa5-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="48fa5-137">Solução de problemas do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="48fa5-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="48fa5-138">Mais informações</span><span class="sxs-lookup"><span data-stu-id="48fa5-138">More Information</span></span>

- [<span data-ttu-id="48fa5-139">Experiência de informações do MDOP</span><span class="sxs-lookup"><span data-stu-id="48fa5-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="48fa5-140">Encontre documentação, vídeos e outros recursos para tecnologias do MDOP.</span><span class="sxs-lookup"><span data-stu-id="48fa5-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





