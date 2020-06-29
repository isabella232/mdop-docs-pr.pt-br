---
title: Arquitetura de alto nível
description: Arquitetura de alto nível
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800043"
---
# <span data-ttu-id="075c8-103">Arquitetura de alto nível</span><span class="sxs-lookup"><span data-stu-id="075c8-103">High-Level Architecture</span></span>


<span data-ttu-id="075c8-104">Esta seção descreve a arquitetura do sistema de alto nível e o design de componentes da virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="075c8-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="075c8-105">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="075c8-105">System Architecture</span></span>


<span data-ttu-id="075c8-106">O MED-V aprimora o Windows Virtual PC para executar dois sistemas operacionais em um dispositivo, adicionando entrega de imagem virtual, provisionamento baseado em política de grupo e gerenciamento centralizado.</span><span class="sxs-lookup"><span data-stu-id="075c8-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="075c8-107">Ao usar o MED-V, você pode facilmente configurar, implantar e gerenciar imagens do Windows Virtual PC corporativo em qualquer área de trabalho baseada no Windows com o Windows 7 Professional, Enterprise ou Windows 7 Ultimate.</span><span class="sxs-lookup"><span data-stu-id="075c8-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="075c8-108">A solução MED-V inclui os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="075c8-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="075c8-109">Host MED-V</span><span class="sxs-lookup"><span data-stu-id="075c8-109">MED-V Host</span></span>**  
<span data-ttu-id="075c8-110">Um ambiente do Windows 7 que inclui um agente de host do MED-V, um sistema ESD (distribuição de software eletrônico), um sistema de gerenciamento de registro e um convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="075c8-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="075c8-111">O host do MED-V interage com o MED-V Guest para que determinadas funções de configuração e informações do sistema possam ser processadas.</span><span class="sxs-lookup"><span data-stu-id="075c8-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="075c8-112">Agente de host do MED-V</span><span class="sxs-lookup"><span data-stu-id="075c8-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="075c8-113">O software MED-V contido no host MED-V que fornece um canal para se comunicar com o convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="075c8-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="075c8-114">Ele também fornece funcionalidade como a configuração pela primeira vez e a publicação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="075c8-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="075c8-115">**Observação**  Após a instalação do MED-V e dos componentes obrigatórios, o MED-V deve ser configurado.</span><span class="sxs-lookup"><span data-stu-id="075c8-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="075c8-116">A configuração do MED-V é chamada de configuração pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="075c8-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="075c8-117">Sistema ESD</span><span class="sxs-lookup"><span data-stu-id="075c8-117">ESD System</span></span>**  
<span data-ttu-id="075c8-118">Seu método de distribuição de software existente que permite implantar e instalar os arquivos de pacote do espaço de trabalho do MED-V que o MED-V cria.</span><span class="sxs-lookup"><span data-stu-id="075c8-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="075c8-119">Sistema de gerenciamento de registros</span><span class="sxs-lookup"><span data-stu-id="075c8-119">Registry Management System</span></span>**  
<span data-ttu-id="075c8-120">Seu método existente de gerenciamento de preferências e configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="075c8-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="075c8-121">Imagem do PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="075c8-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="075c8-122">Uma máquina virtual definida pelo administrador que contém os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="075c8-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="075c8-123">Sistema operacional corporativo</span><span class="sxs-lookup"><span data-stu-id="075c8-123">Corporate Operating System</span></span>**  
<span data-ttu-id="075c8-124">Seu sistema operacional corporativo padrão.</span><span class="sxs-lookup"><span data-stu-id="075c8-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="075c8-125">Ferramentas de gerenciamento e segurança</span><span class="sxs-lookup"><span data-stu-id="075c8-125">Management and Security Tools</span></span>**  
<span data-ttu-id="075c8-126">Suas ferramentas de gerenciamento e segurança padrão, como proteção contra vírus.</span><span class="sxs-lookup"><span data-stu-id="075c8-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="075c8-127">Convidado do MED-V</span><span class="sxs-lookup"><span data-stu-id="075c8-127">MED-V Guest</span></span>**  
<span data-ttu-id="075c8-128">Um ambiente do Windows XP SP3, como parte de um PC virtual do Windows em execução no Windows 7 que contém os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="075c8-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="075c8-129">Agente de convidado do MED-V</span><span class="sxs-lookup"><span data-stu-id="075c8-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="075c8-130">O software MED-V contido no convidado do MED-V que fornece um canal para se comunicar com o host do MED-V.</span><span class="sxs-lookup"><span data-stu-id="075c8-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="075c8-131">Ele também dá suporte ao agente de host do MED-V com funções como executar a configuração inicial.</span><span class="sxs-lookup"><span data-stu-id="075c8-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="075c8-132">**Observação**  O agente de convidado do MED-V é instalado automaticamente durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="075c8-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="075c8-133">Cliente ESD</span><span class="sxs-lookup"><span data-stu-id="075c8-133">ESD Client</span></span>**  
<span data-ttu-id="075c8-134">Uma parte opcional do seu sistema ESD que instala pacotes de software e o status dos relatórios para o sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="075c8-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="075c8-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="075c8-135">Related topics</span></span>


[<span data-ttu-id="075c8-136">Planejamento da compatibilidade do sistema operacional para aplicativos</span><span class="sxs-lookup"><span data-stu-id="075c8-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="075c8-137">Preparar o ambiente de implantação para a MED-V</span><span class="sxs-lookup"><span data-stu-id="075c8-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





