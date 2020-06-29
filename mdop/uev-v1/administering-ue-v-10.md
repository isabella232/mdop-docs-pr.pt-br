---
title: Administração da UE-V 1.0
description: Administração da UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799124"
---
# <span data-ttu-id="7d903-103">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7d903-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="7d903-104">Depois de implantar o Microsoft User Experience Virtualization (UE-V), você deve ser capaz de executar várias tarefas administrativas em andamento.</span><span class="sxs-lookup"><span data-stu-id="7d903-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="7d903-105">Estas tarefas pós-instalação estão descritas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d903-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="7d903-106">Gerenciando recursos do UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-106">Managing UE-V resources</span></span>


<span data-ttu-id="7d903-107">No curso do ciclo de vida de UE-V, você precisará gerenciar a configuração do UE-V Agent e também gerenciar locais de armazenamento para recursos como pacotes de configurações.</span><span class="sxs-lookup"><span data-stu-id="7d903-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="7d903-108">Talvez seja necessário executar outras tarefas, como restaurar as configurações de um usuário ao estado original antes de o UE-V ter sido instalado para recuperar as configurações perdidas.</span><span class="sxs-lookup"><span data-stu-id="7d903-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="7d903-109">Os tópicos a seguir fornecem orientação para o gerenciamento de recursos do UE-V.</span><span class="sxs-lookup"><span data-stu-id="7d903-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="7d903-110">Alterando a frequência das tarefas agendadas do UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="7d903-111">Você pode configurar as tarefas agendadas que gerenciam quando o UE-V Verifica se há modelos de localização de configurações personalizadas novas, atualizadas ou removidas no catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="7d903-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="7d903-112">Alterando a frequência das tarefas agendadas do UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="7d903-113">Compartilhamento de modelos de localização de configurações com a galeria de modelos da UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="7d903-114">A Galeria de modelos UE-V facilita o compartilhamento de modelos de local de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="7d903-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="7d903-115">A Galeria permite carregar modelos de local de configurações para compartilhar com outras pessoas e baixar modelos que outras pessoas criaram.</span><span class="sxs-lookup"><span data-stu-id="7d903-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="7d903-116">Compartilhamento de modelos de localização de configurações com a galeria de modelos da UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="7d903-117">Restaurando configurações do aplicativo e do Windows sincronizadas com o UE-V 1,0</span><span class="sxs-lookup"><span data-stu-id="7d903-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="7d903-118">Os recursos do WMI e do PowerShell da UE-V fornecem a capacidade de restaurar pacotes de configurações.</span><span class="sxs-lookup"><span data-stu-id="7d903-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="7d903-119">Os comandos do WMI e do PowerShell permitem restaurar configurações do aplicativo e configurações do Windows para os valores de configurações que estavam no computador na primeira vez em que o aplicativo foi iniciado após o início do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="7d903-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="7d903-120">Restauração de configurações de aplicativos e do Windows com a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7d903-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="7d903-121">Configuração da UE-V com objetos de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="7d903-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="7d903-122">Você pode usar a política de grupo para modificar as configurações que definem como o UE-V sincroniza as configurações em computadores.</span><span class="sxs-lookup"><span data-stu-id="7d903-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="7d903-123">Configurando o UE-V com objetos de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="7d903-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="7d903-124">Administração da UE-V com o PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="7d903-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="7d903-125">Você pode usar o PowerShell e o WMI para modificar as configurações que definem como o UE-V sincroniza as configurações em computadores.</span><span class="sxs-lookup"><span data-stu-id="7d903-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="7d903-126">Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="7d903-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="7d903-127">Migrando pacotes de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="7d903-128">Você pode realocar os pacotes de configurações de usuário ao migrar para um novo servidor ou para fins de backup.</span><span class="sxs-lookup"><span data-stu-id="7d903-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="7d903-129">Migrando pacotes de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="7d903-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="7d903-130">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="7d903-130">Other resources for this product</span></span>


[<span data-ttu-id="7d903-131">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7d903-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





