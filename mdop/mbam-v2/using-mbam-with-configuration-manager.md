---
title: Usando o MBAM com o Configuration Manager
description: Usando o MBAM com o Configuration Manager
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799342"
---
# <span data-ttu-id="448ee-103">Usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="448ee-104">Ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode escolher uma instalação que integre a administração e o monitoramento do Microsoft BitLocker com o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="448ee-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="448ee-105">Para obter uma lista das versões com suporte do Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="448ee-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="448ee-106">Essa integração move a infraestrutura de conformidade e a conformidade do Microsoft BitLocker e o monitoramento de relatórios para o ambiente nativo do Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="448ee-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="448ee-107">Com a topologia do Configuration Manager, os administradores de ti podem ver relatórios e o status de conformidade da empresa no console de gerenciamento do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="448ee-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="448ee-108">**Importante**  Não há suporte para o Windows to go ao instalar a topologia integrada do MBAM com o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="448ee-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="448ee-109">Introdução – usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="448ee-110">Esta seção descreve como o MBAM funciona com o Configuration Manager e explica a arquitetura recomendada para implantar o MBAM com a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="448ee-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="448ee-111">Introdução – Como usar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="448ee-112">Como planejar a implantação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="448ee-113">Esta seção descreve os pré-requisitos de instalação, configurações com suporte e requisitos de hardware e software que você precisa considerar antes de instalar o MBAM com a topologia do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="448ee-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="448ee-114">Como planejar a implantação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="448ee-115">Como implantar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="448ee-116">Esta seção descreve como implantar o MBAM com o Configuration Manager e inclui instruções para instalar e configurar o MBAM no servidor de administração e monitoramento e no servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="448ee-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="448ee-117">Como implantar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="448ee-118">Noções básicas sobre relatórios do MBAM no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="448ee-119">Esta seção descreve os relatórios do MBAM que você pode executar a partir do Configuration Manager para mostrar a conformidade da sua empresa e a conformidade de computadores individuais na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="448ee-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="448ee-120">Noções básicas sobre relatórios do MBAM no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="448ee-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="448ee-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="448ee-121">Related topics</span></span>


[<span data-ttu-id="448ee-122">Operações do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="448ee-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





