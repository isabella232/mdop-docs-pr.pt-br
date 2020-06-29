---
title: Implantação da Atualização da Versão de Idioma do MBAM 1.0
description: Implantação da Atualização da Versão de Idioma do MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796096"
---
# <span data-ttu-id="77240-103">Implantação da Atualização da Versão de Idioma do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="77240-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="77240-104">O lançamento do idioma do Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 é uma atualização do MBAM e inclui o suporte de novos idiomas.</span><span class="sxs-lookup"><span data-stu-id="77240-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="77240-105">Os novos idiomas são:</span><span class="sxs-lookup"><span data-stu-id="77240-105">The new languages are:</span></span>

-   <span data-ttu-id="77240-106">Inglês (en-US)</span><span class="sxs-lookup"><span data-stu-id="77240-106">English (en-us)</span></span>

-   <span data-ttu-id="77240-107">Francês (FR)</span><span class="sxs-lookup"><span data-stu-id="77240-107">French (fr)</span></span>

-   <span data-ttu-id="77240-108">Italiano (TI)</span><span class="sxs-lookup"><span data-stu-id="77240-108">Italian (it)</span></span>

-   <span data-ttu-id="77240-109">Alemão (de)</span><span class="sxs-lookup"><span data-stu-id="77240-109">German (de)</span></span>

-   <span data-ttu-id="77240-110">Espanhol (es)</span><span class="sxs-lookup"><span data-stu-id="77240-110">Spanish (es)</span></span>

-   <span data-ttu-id="77240-111">Coreano (KO)</span><span class="sxs-lookup"><span data-stu-id="77240-111">Korean (ko)</span></span>

-   <span data-ttu-id="77240-112">Japonês (ja)</span><span class="sxs-lookup"><span data-stu-id="77240-112">Japanese (ja)</span></span>

-   <span data-ttu-id="77240-113">Português (Brasil) Português (Portugal-br)</span><span class="sxs-lookup"><span data-stu-id="77240-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="77240-114">Russo (ru)</span><span class="sxs-lookup"><span data-stu-id="77240-114">Russian (ru)</span></span>

-   <span data-ttu-id="77240-115">Chinês tradicional (zh-TW)</span><span class="sxs-lookup"><span data-stu-id="77240-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="77240-116">Chinês simplificado (ZH-CN)</span><span class="sxs-lookup"><span data-stu-id="77240-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="77240-117">A atualização de idioma do MBAM 1.0 alterará o número de versão de MBAM 1.0.1237.1 para MBAM 1.0.2001.</span><span class="sxs-lookup"><span data-stu-id="77240-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="77240-118">Você não precisa reinstalar todos os recursos MBAM para adicionar esses idiomas adicionais.</span><span class="sxs-lookup"><span data-stu-id="77240-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="77240-119">Este tópico define as etapas necessárias para adicionar os idiomas recentemente aceitos.</span><span class="sxs-lookup"><span data-stu-id="77240-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="77240-120">Implantar o MBAM International Release to MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="77240-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="77240-121">Para começar, você deve atualizar os seguintes recursos do MBAM Server:</span><span class="sxs-lookup"><span data-stu-id="77240-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="77240-122">Relatório de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="77240-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="77240-123">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="77240-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="77240-124">Modelos de política</span><span class="sxs-lookup"><span data-stu-id="77240-124">Policy Templates</span></span>

<span data-ttu-id="77240-125">Em seguida, você deve executar o **MbamSetup.exe** para atualizar os recursos do MBAM que são executados no mesmo servidor ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="77240-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="77240-126">Como instalar a atualização de idiomas do MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="77240-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="77240-127">Como instalar a atualização de idioma do MBAM em servidores distribuídos</span><span class="sxs-lookup"><span data-stu-id="77240-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="77240-128">Instalar a atualização de idioma do MBAM para políticas de grupo</span><span class="sxs-lookup"><span data-stu-id="77240-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="77240-129">Os modelos de política de grupo do MBAM podem ser instalados em cada estação de trabalho de gerenciamento ou podem ser copiados para o repositório central de política de grupo, a fim de disponibilizar os modelos para todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="77240-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="77240-130">Os modelos de política não podem ser instalados diretamente em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="77240-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="77240-131">Se você não usar um repositório central de políticas de grupo, deverá copiar as políticas manualmente para cada controlador de domínio que gerencia a política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="77240-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="77240-132">Para adicionar os modelos de diretivas de idioma do MBAM, copie os arquivos de idioma da política de grupo do%SystemRoot%\\PolicyDefinitions no computador em que a função "modelos de política" foi instalada no mesmo local no computador da estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77240-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="77240-133">Veja alguns exemplos de arquivos de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="77240-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="77240-134">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="77240-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="77240-135">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="77240-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="77240-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="77240-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="77240-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="77240-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="77240-138">fr-fr\\ BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="77240-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="77240-139">fr-fr\\ BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="77240-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="77240-140">(e, da mesma forma, para cada idioma com suporte)</span><span class="sxs-lookup"><span data-stu-id="77240-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="77240-141">Problemas conhecidos do lançamento do MBAM International</span><span class="sxs-lookup"><span data-stu-id="77240-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="77240-142">Este tópico contém problemas conhecidos para a atualização do Microsoft BitLocker Administration and Monitoring International.</span><span class="sxs-lookup"><span data-stu-id="77240-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="77240-143">Problemas Conhecidos na Versão Internacional do MBAM</span><span class="sxs-lookup"><span data-stu-id="77240-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="77240-144">Outros recursos para implantar a atualização de idioma do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="77240-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="77240-145">Implantando o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="77240-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





