---
title: Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0
description: Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800009"
---
# <span data-ttu-id="7ba30-103">Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7ba30-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="7ba30-104">O Microsoft User Experience Virtualization (UE-V) usa modelos de local de configurações (arquivos XML) que definem as configurações que são capturadas e aplicadas pela virtualização da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ba30-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="7ba30-105">O UE-V inclui um conjunto de modelos padrão, bem como uma ferramenta, o UE-V Generator, que permite criar modelos de localização de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7ba30-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="7ba30-106">Depois de criar um modelo de local de configurações, você deve testá-lo para garantir que as configurações do aplicativo sejam referidas corretamente em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="7ba30-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="7ba30-107">Em seguida, você pode implantar com segurança o modelo de local de configurações em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="7ba30-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="7ba30-108">Os modelos de locais de configurações podem ser implantados usando ESD (Enterprise Software Distribution), preferências de política de grupo ou configurando um catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ba30-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="7ba30-109">Os modelos implantados usando um ESD ou uma política de grupo devem ser registrados pelo UE-V WMI ou pelo PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ba30-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="7ba30-110">Os modelos armazenados na localização do catálogo de modelos de configurações são automaticamente registrados pelo UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="7ba30-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="7ba30-111">Implantar os modelos de local de configurações com um caminho de catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="7ba30-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="7ba30-112">O caminho do catálogo de modelos de local de configurações do UE-V pode ser definido usando os seguintes métodos: política de grupo, parâmetros de linha de comando de instalação de agente, WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ba30-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="7ba30-113">Após a definição do caminho do catálogo de modelos, o UE-V Agent recupera os modelos novos ou atualizados deste local.</span><span class="sxs-lookup"><span data-stu-id="7ba30-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="7ba30-114">O UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos encontrados nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="7ba30-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="7ba30-115">Os modelos que foram adicionados ou atualizados nesta pasta desde a última verificação são registrados pelo UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="7ba30-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="7ba30-116">O UE-V Agent também cancela o registro de modelos que foram removidos desta pasta.</span><span class="sxs-lookup"><span data-stu-id="7ba30-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="7ba30-117">Os modelos são registrados e não registrados uma vez por dia pelo Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7ba30-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="7ba30-118">Para usar o caminho do catálogo de modelos de configurações para implantar os modelos de local das configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="7ba30-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="7ba30-119">Navegue até a pasta de compartilhamento de rede que é definida como o catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="7ba30-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="7ba30-120">Adicione, remova ou atualize os modelos de local de configurações no catálogo de modelos de configurações para refletir a configuração de modelo de agente do UE-V desejada para computadores UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ba30-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="7ba30-121">Os modelos em computadores são atualizados diariamente com base nas alterações do catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="7ba30-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="7ba30-122">Abra um prompt de comando elevado e navegue até \*\*% Program Files%\\Microsoft de experiência do usuário \ \ agente \ \ &lt; x86 &gt; ou x64 \*\*e, em seguida, execute **ApplySettingsTemplateCatalog.exe** para atualizar manualmente os modelos em um computador que executa o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="7ba30-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="7ba30-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ba30-123">Related topics</span></span>


[<span data-ttu-id="7ba30-124">Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="7ba30-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="7ba30-125">Implantação da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7ba30-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="7ba30-126">Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7ba30-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





