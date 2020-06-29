---
title: Administração do UE-V 2. x
description: Administração do UE-V 2. x
author: dansimp
ms.assetid: 996e4797-8383-4627-b714-24a84c907798
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2674f6ace80672c1e89bb4f9c765b56f260c3bc0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799719"
---
# <span data-ttu-id="fc3f9-103">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-103">Administering UE-V 2.x</span></span>


<span data-ttu-id="fc3f9-104">Depois de implantar o Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 ou o 2,1 SP1, você deve ser capaz de executar várias tarefas administrativas em andamento, como o gerenciamento da configuração do UE-V Agent e a recuperação de configurações perdidas.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-104">After you have deployed Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you must be able to perform various ongoing administrative tasks, such as managing the configuration of the UE-V Agent and recovering lost settings.</span></span> <span data-ttu-id="fc3f9-105">Estas tarefas pós-instalação estão descritas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="fc3f9-106">Gerenciando configurações do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-106">Managing UE-V 2.x configurations</span></span>


<span data-ttu-id="fc3f9-107">No curso do ciclo de vida do UE-V, você precisa gerenciar a configuração do UE-V Agent e também gerenciar locais de armazenamento para recursos como arquivos de pacote de configurações.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-107">In the course of the UE-V lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span>

[<span data-ttu-id="fc3f9-108">Gerenciar as configurações da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-108">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

## <span data-ttu-id="fc3f9-109">Trabalhando com modelos personalizados do UE-V e do UE-V 2. x Generator</span><span class="sxs-lookup"><span data-stu-id="fc3f9-109">Working with custom UE-V templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="fc3f9-110">Este tópico fornece instruções sobre como usar o UE-V Generator e gerenciar modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-110">This topic provides instructions for how to use the UE-V Generator and manage custom settings location templates.</span></span>

[<span data-ttu-id="fc3f9-111">Trabalhando com os modelos personalizados do UE-V 2. x e do UE-V 2. x Generator</span><span class="sxs-lookup"><span data-stu-id="fc3f9-111">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

## <span data-ttu-id="fc3f9-112">Aplicativos de backup e restauração e configurações do Windows que são sincronizadas com o UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-112">Backup and restore application and Windows settings that are synchronized with UE-V 2.x</span></span>


<span data-ttu-id="fc3f9-113">Os recursos de instrumentação de gerenciamento do Windows (WMI) e do Windows PowerShell da UE-V oferecem a capacidade de restaurar pacotes de configurações.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-113">Windows Management Instrumentation (WMI) and Windows PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="fc3f9-114">Ao usar os comandos WMI e Windows PowerShell, você pode restaurar as configurações do aplicativo e do Windows ao estado original e restaurar configurações adicionais quando um usuário adotar um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-114">By using WMI and Windows PowerShell commands, you can restore application and Windows settings to their original state and restore additional settings when a user adopts a new device.</span></span>

[<span data-ttu-id="fc3f9-115">Gerenciar o backup e a restauração administrativos no UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-115">Manage Administrative Backup and Restore in UE-V 2.x</span></span>](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

## <span data-ttu-id="fc3f9-116">Alterar a frequência das tarefas agendadas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-116">Changing the frequency of UE-V 2.x scheduled tasks</span></span>


<span data-ttu-id="fc3f9-117">Você pode configurar as tarefas agendadas que gerenciam quando a UE-V Verifica se há configurações novas ou atualizadas ou para modelos de localização de configurações personalizadas atualizadas no catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-117">You can configure the scheduled tasks that manage when UE-V checks for new or updated settings or for updated custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="fc3f9-118">Alterar a frequência das tarefas agendadas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-118">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

## <span data-ttu-id="fc3f9-119">Migrando pacotes de configurações do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-119">Migrating UE-V 2.x settings packages</span></span>


<span data-ttu-id="fc3f9-120">Você pode realocar os pacotes de configurações do usuário quando migrar para um novo servidor ou para fins de backup.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-120">You can relocate the user settings packages either when they migrate to a new server or for backup purposes.</span></span>

[<span data-ttu-id="fc3f9-121">Migrando pacotes de configurações do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-121">Migrating UE-V 2.x Settings Packages</span></span>](migrating-ue-v-2x-settings-packages-both-uevv2.md)

## <span data-ttu-id="fc3f9-122">Usar o UE-V 2. x com aplicativos do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fc3f9-122">Using UE-V 2.x with Application Virtualization applications</span></span>


<span data-ttu-id="fc3f9-123">Você pode usar o UE-V com o Microsoft Application Virtualization (App-V) para compartilhar configurações entre aplicativos virtuais e aplicativos instalados em vários computadores.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-123">You can use UE-V with Microsoft Application Virtualization (App-V) to share settings between virtual applications and installed applications across multiple computers.</span></span>

[<span data-ttu-id="fc3f9-124">Usar o UE-V 2. x com aplicativos do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fc3f9-124">Using UE-V 2.x with Application Virtualization Applications</span></span>](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)

## <span data-ttu-id="fc3f9-125">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="fc3f9-125">Other resources for this product</span></span>


-   [<span data-ttu-id="fc3f9-126">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-126">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="fc3f9-127">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-127">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="fc3f9-128">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-128">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="fc3f9-129">Solução de problemas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-129">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="fc3f9-130">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="fc3f9-130">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





