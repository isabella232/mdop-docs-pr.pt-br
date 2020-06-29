---
title: Implantando o MBAM 2.0
description: Implantando o MBAM 2.0
author: dansimp
ms.assetid: 4b0eaf10-81b4-427e-9d43-eb833de935a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba4423de5306e1ca204ef3b9fd31424bb8f2630f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799279"
---
# <span data-ttu-id="ab0ad-103">Implantando o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-103">Deploying MBAM 2.0</span></span>


<span data-ttu-id="ab0ad-104">O monitoramento e administração do Microsoft BitLocker (MBAM) oferece suporte a várias configurações de implantação diferentes.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-104">Microsoft BitLocker Administration and Monitoring (MBAM) supports a number of different deployment configurations.</span></span> <span data-ttu-id="ab0ad-105">Esta seção inclui informações que você deve considerar sobre a implantação de MBAM e procedimentos passo a passo para ajudar você a executar com êxito as tarefas que devem ser concluídas em diferentes estágios da implantação.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-105">This section includes information that you should consider about the deployment of MBAM and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

<span data-ttu-id="ab0ad-106">Você pode implantar o MBAM em uma topologia autônoma ou em uma topologia que integre o MBAM com o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-106">You can deploy MBAM either in a Stand-alone topology, or with a topology that integrates MBAM with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="ab0ad-107">Para obter informações sobre como instalar o MBAM com a topologia integrada do Configuration Manager, consulte [usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="ab0ad-107">For information about installing MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

## <span data-ttu-id="ab0ad-108">Informações de implantação</span><span class="sxs-lookup"><span data-stu-id="ab0ad-108">Deployment Information</span></span>


-   [<span data-ttu-id="ab0ad-109">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-109">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

    <span data-ttu-id="ab0ad-110">Esta seção descreve as diferentes opções de topologia de implantação do MBAM e como usar a configuração do MBAM para implantar recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-110">This section describes the different MBAM deployment topology options and how to use MBAM Setup to deploy MBAM Server features.</span></span>

-   [<span data-ttu-id="ab0ad-111">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-111">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

    <span data-ttu-id="ab0ad-112">Esta seção descreve como criar e implantar objetos de política de grupo do MBAM que são necessários para gerenciar clientes do MBAM e políticas de criptografia do BitLocker em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-112">This section describes how to create and deploy MBAM Group Policy Objects that are required for managing MBAM Clients and BitLocker encryption policies throughout the enterprise.</span></span>

-   [<span data-ttu-id="ab0ad-113">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-113">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

    <span data-ttu-id="ab0ad-114">Esta seção descreve como usar os arquivos do instalador do cliente do MBAM para implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-114">This section describes how to use the MBAM Client Installer files to deploy the MBAM Client software.</span></span>

-   [<span data-ttu-id="ab0ad-115">Lista de verificação para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-115">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)

    <span data-ttu-id="ab0ad-116">Esta seção fornece uma lista de verificação de implantação que pode ser usada para auxiliar no recurso MBAM Server e na implantação de cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-116">This section provides a deployment checklist that can be used to assist in MBAM Server feature and MBAM Client deployment.</span></span>

-   [<span data-ttu-id="ab0ad-117">Atualizando de versões anteriores do MBAM</span><span class="sxs-lookup"><span data-stu-id="ab0ad-117">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)

    <span data-ttu-id="ab0ad-118">Esta seção fornece instruções para a atualização do MBAM de versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="ab0ad-118">This section provides instructions for upgrading MBAM from previous versions.</span></span>

## <span data-ttu-id="ab0ad-119">Outros recursos para a implantação do MBAM</span><span class="sxs-lookup"><span data-stu-id="ab0ad-119">Other Resources for Deploying MBAM</span></span>


[<span data-ttu-id="ab0ad-120">Guia do administrador do Microsoft BitLocker Administration and Monitoring 2</span><span class="sxs-lookup"><span data-stu-id="ab0ad-120">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="ab0ad-121">Introdução ao MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-121">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

[<span data-ttu-id="ab0ad-122">Planejamento para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-122">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="ab0ad-123">Operações do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-123">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="ab0ad-124">Solução de problemas do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ab0ad-124">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





