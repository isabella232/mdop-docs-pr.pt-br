---
title: Implantação da UE-V 1.0
description: Implantação da UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800014"
---
# <span data-ttu-id="2cc51-103">Implantação da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="2cc51-104">Há várias configurações de implantação diferentes que o Microsoft User Experience Virtualization (UE-V) suporta.</span><span class="sxs-lookup"><span data-stu-id="2cc51-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="2cc51-105">Esta seção inclui informações gerais e procedimentos passo a passo para ajudar você a executar com êxito as tarefas que devem ser concluídas em diferentes estágios da implantação.</span><span class="sxs-lookup"><span data-stu-id="2cc51-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="2cc51-106">Informações de implantação para UE-V</span><span class="sxs-lookup"><span data-stu-id="2cc51-106">Deployment information for UE-V</span></span>


<span data-ttu-id="2cc51-107">Uma implantação do UE-V exige um local de armazenamento de configurações em um compartilhamento de rede e um agente do UE-V instalado em cada computador que sincroniza as configurações.</span><span class="sxs-lookup"><span data-stu-id="2cc51-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="2cc51-108">Os modelos de política de grupo UE-V podem ser usados para gerenciar as configurações de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2cc51-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="2cc51-109">Os tópicos a seguir descrevem como implantar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="2cc51-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="2cc51-110">Implantação da localização do armazenamento de configurações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="2cc51-111">Todas as implantações de UE-V exigem um local de armazenamento de configurações onde os pacotes de configurações que contêm os valores de configuração sincronizados estão localizados.</span><span class="sxs-lookup"><span data-stu-id="2cc51-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="2cc51-112">Implantação do agente da UE-V</span><span class="sxs-lookup"><span data-stu-id="2cc51-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="2cc51-113">Para sincronizar as configurações usando o UE-V, um computador deve ter o UE-V Agent instalado e em execução.</span><span class="sxs-lookup"><span data-stu-id="2cc51-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="2cc51-114">Instalação dos modelos ADMX da Política de Grupo da UE-V</span><span class="sxs-lookup"><span data-stu-id="2cc51-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="2cc51-115">Você pode usar a política de grupo para pré-configurar as configurações de UE-V antes de implantar o UE-V Agent, bem como a configuração padrão de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2cc51-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="2cc51-116">Informações de implantação para a implantação de modelos personalizados</span><span class="sxs-lookup"><span data-stu-id="2cc51-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="2cc51-117">Se você planeja criar modelos de localização de configurações personalizadas para aplicativos que não sejam os aplicativos Microsoft incluídos na UE-V, como aplicativos de linha de negócios, poderá implantar um catálogo de modelos de configurações e instalar o UE-V Generator para criar esses modelos.</span><span class="sxs-lookup"><span data-stu-id="2cc51-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="2cc51-118">Para obter mais informações, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="2cc51-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="2cc51-119">Instalação do gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="2cc51-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="2cc51-120">Use o UE-V Generator para criar, editar e validar modelos de local de configurações personalizadas que ajudam a sincronizar as configurações de aplicativos diferentes dos aplicativos padrão.</span><span class="sxs-lookup"><span data-stu-id="2cc51-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="2cc51-121">Implantação do catálogo de modelos de configurações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="2cc51-122">Se você precisar implantar modelos de localização de configurações personalizadas para dar suporte a aplicativos diferentes dos aplicativos padrão no UE-V Agent, será preciso configurar um catálogo de modelos de configurações para armazená-los.</span><span class="sxs-lookup"><span data-stu-id="2cc51-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="2cc51-123">Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="2cc51-124">Se você precisar sincronizar aplicativos diferentes dos aplicativos padrão no UE-V Agent, os modelos de local de configuração personalizada criados com o UE-V Generator podem ser distribuídos para o catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="2cc51-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="2cc51-125">**Observação**  A implantação de modelos personalizados exige um catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="2cc51-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="2cc51-126">Os modelos de aplicativos padrão da Microsoft são implantados com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2cc51-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="2cc51-127">Tópicos para este produto</span><span class="sxs-lookup"><span data-stu-id="2cc51-127">Topics for this product</span></span>


[<span data-ttu-id="2cc51-128">Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="2cc51-129">Introdução à User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="2cc51-130">Planejamento para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="2cc51-131">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="2cc51-132">Solução de problemas da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc51-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





