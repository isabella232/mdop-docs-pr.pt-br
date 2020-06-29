---
title: Planejar a implantação de modelo personalizado para a UE-V 1.0
description: Planejar a implantação de modelo personalizado para a UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797876"
---
# <span data-ttu-id="8b26f-103">Planejar a implantação de modelo personalizado para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8b26f-103">Planning for Custom Template Deployment for UE-V 1.0</span></span>


<span data-ttu-id="8b26f-104">O Microsoft User Experience Virtualization (UE-V) usa modelos de local de configurações (arquivos XML) que definem as configurações que são capturadas e aplicadas pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="8b26f-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="8b26f-105">Você pode usar o UE-V Generator para criar modelos de local de configurações personalizadas que permitem aos usuários fazer roaming das configurações de aplicativos diferentes daqueles incluídos nos modelos UE-V padrão.</span><span class="sxs-lookup"><span data-stu-id="8b26f-105">You can use the UE-V Generator to create custom settings location templates that let users roam the settings of applications other than those that are included in the default UE-V templates.</span></span> <span data-ttu-id="8b26f-106">Depois de testar o modelo personalizado para garantir que as configurações do aplicativo sejam referidas corretamente em um ambiente de teste, você pode implantar esses modelos de local de configurações em computadores na empresa.</span><span class="sxs-lookup"><span data-stu-id="8b26f-106">After you test the custom template to ensure that the application settings roam correctly in a test environment, you can deploy these settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="8b26f-107">Você pode implantar seus modelos de local de configurações personalizadas com uma infraestrutura de implantação existente, como o ESD (Enterprise Software Distribution), com preferências de política de grupo ou configurando um catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="8b26f-107">You can deploy your custom settings location templates with an existing deployment infrastructure, such as Enterprise Software Distribution (ESD), with Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="8b26f-108">Os modelos implantados usando ESD ou a política de grupo devem ser registrados com o UE-V WMI ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b26f-108">Templates that are deployed by using ESD or Group Policy must be registered with UE-V WMI or PowerShell.</span></span>

## <span data-ttu-id="8b26f-109">Catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="8b26f-109">Settings template catalog</span></span>


<span data-ttu-id="8b26f-110">O catálogo de modelos de configurações de experiência de usuário da experiência do usuário é um caminho de pasta em computadores UE-V ou um compartilhamento de rede de servidor de mensagens (SMB) que armazena todos os modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8b26f-110">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="8b26f-111">O UE-V Agent recupera modelos novos ou atualizados deste local.</span><span class="sxs-lookup"><span data-stu-id="8b26f-111">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="8b26f-112">O UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos desta pasta.</span><span class="sxs-lookup"><span data-stu-id="8b26f-112">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="8b26f-113">Os modelos que foram adicionados ou atualizados nesta pasta desde a última vez que a pasta foi verificada são registrados pelo UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="8b26f-113">Templates that were added or updated in this folder since the last time that the folder was checked are registered by the UE-V agent.</span></span> <span data-ttu-id="8b26f-114">O UE-V Agent cancela o registro de modelos que são removidos desta pasta.</span><span class="sxs-lookup"><span data-stu-id="8b26f-114">The UE-V agent deregisters templates that are removed from this folder.</span></span> <span data-ttu-id="8b26f-115">Por padrão, os modelos são registrados e não registrados uma vez por dia em 3:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="8b26f-115">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="8b26f-116">Hora local pelo Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b26f-116">local time by the task scheduler.</span></span> <span data-ttu-id="8b26f-117">Para obter mais informações sobre as tarefas do UE-V, consulte [alterando a frequência de tarefas agendadas de UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="8b26f-117">For more information about the UE-V tasks, see [Changing the Frequency of UE-V Scheduled Tasks](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span></span>

<span data-ttu-id="8b26f-118">Você pode configurar o caminho do catálogo de modelos de configurações usando as opções de linha de comando de instalação, a política de grupo, o WMI ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b26f-118">You can configure the settings template catalog path by using the install command-line options, Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="8b26f-119">Os modelos armazenados no caminho do catálogo de modelos de configurações são automaticamente registrados e não são registrados por uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="8b26f-119">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span> <span data-ttu-id="8b26f-120">Você pode personalizar essa tarefa agendada conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="8b26f-120">You can customize this scheduled task as needed.</span></span>

## <span data-ttu-id="8b26f-121">Substituir os modelos padrão da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b26f-121">Replace the default Microsoft templates</span></span>


<span data-ttu-id="8b26f-122">O UE-V Agent instala um grupo padrão de modelos de local de configurações para aplicativos comuns da Microsoft e configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b26f-122">The UE-V agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="8b26f-123">Se a sua empresa precisa de versões personalizadas desses modelos, o UE-V Agent pode ser configurado para usar um catálogo de modelos de configurações e, em seguida, substituir os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b26f-123">If your enterprise needs customized versions of these templates, the UE-V agent can be configured to use a settings template catalog and you should then replace the default Microsoft templates.</span></span>

<span data-ttu-id="8b26f-124">Durante a instalação do UE-V Agent, o parâmetro de linha de comando, `RegisterMSTemplates` pode ser usado para desabilitar o registro dos modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b26f-124">During the installation of the UE-V agent, the command-line parameter, `RegisterMSTemplates`, can be used to disable the registration of the default Microsoft templates.</span></span> <span data-ttu-id="8b26f-125">Para obter mais informações sobre como definir os parâmetros do UE-V, consulte [planejando métodos de configuração do UE-v](planning-for-ue-v-configuration-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8b26f-125">For more information about how to set the UE-V parameters, see [Planning for UE-V Configuration Methods](planning-for-ue-v-configuration-methods.md).</span></span>

<span data-ttu-id="8b26f-126">Ao usar a política de grupo para definir o caminho do catálogo de modelos de configurações, você pode optar por substituir os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b26f-126">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="8b26f-127">Se você definir as configurações de política para substituir os modelos padrão da Microsoft, todos os modelos padrão da Microsoft instalados pelo UE-V Agent serão excluídos do computador e somente os modelos localizados no catálogo de modelos de configurações serão usados.</span><span class="sxs-lookup"><span data-stu-id="8b26f-127">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V agent will be deleted from the computer, and only the templates that are located in the settings template catalog will be used.</span></span> <span data-ttu-id="8b26f-128">A configuração do UE-V Agent `RegisterMSTemplates` deve ser definida como true para substituir o modelo padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b26f-128">The UE-V Agent configuration setting `RegisterMSTemplates` must be set to true in order to override the default Microsoft template.</span></span>

<span data-ttu-id="8b26f-129">**Observação**  Se você desabilitar essa configuração de política depois que ela for habilitada, o UE-V Agent não restaurará os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b26f-129">**Note** If you disable this policy setting after it has been enabled, the UE-V agent will not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="8b26f-130">Se houver modelos personalizados no catálogo de modelos de configurações que usam a mesma ID que os modelos padrão da Microsoft, e o UE-V Agent não estiver configurado para substituir os modelos padrão da Microsoft, os modelos da Microsoft no catálogo serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="8b26f-130">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V agent is not configured to replace the default Microsoft templates, the Microsoft templates in the catalog will be ignored.</span></span>

<span data-ttu-id="8b26f-131">Você também pode substituir os modelos padrão usando os recursos do PowerShell do UE-V.</span><span class="sxs-lookup"><span data-stu-id="8b26f-131">You can also replace the default templates by using the UE-V PowerShell features.</span></span> <span data-ttu-id="8b26f-132">Para substituir o modelo padrão da Microsoft pelo PowerShell, cancele o registro de todos os modelos padrão da Microsoft e registre os modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="8b26f-132">To replace the default Microsoft Template with PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="8b26f-133">**Observação**  Os pacotes de configurações antigas permanecem no local de armazenamento configurações, mesmo que novos modelos de configurações sejam implantados para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b26f-133">**Note** Old settings packages remain in the settings storage location even if new settings templates are deployed for an application.</span></span> <span data-ttu-id="8b26f-134">Esses pacotes não são lidos pelo agente, mas nenhum deles é excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8b26f-134">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <span data-ttu-id="8b26f-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b26f-135">Related topics</span></span>


[<span data-ttu-id="8b26f-136">Planejamento para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8b26f-136">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="8b26f-137">Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8b26f-137">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="8b26f-138">Planejamento para os métodos de configuração da UE-V</span><span class="sxs-lookup"><span data-stu-id="8b26f-138">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

<span data-ttu-id="8b26f-139">Planejando a implantação de modelos personalizados</span><span class="sxs-lookup"><span data-stu-id="8b26f-139">Planning for Custom Template Deployment</span></span>
 

 





