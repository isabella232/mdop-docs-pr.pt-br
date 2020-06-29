---
title: Alterando a frequência das tarefas agendadas do UE-V
description: Alterando a frequência das tarefas agendadas do UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799122"
---
# <span data-ttu-id="1ebf5-103">Alterando a frequência das tarefas agendadas do UE-V</span><span class="sxs-lookup"><span data-stu-id="1ebf5-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="1ebf5-104">O instalador do agente do Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, cria duas tarefas agendadas durante a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="1ebf5-105">As duas tarefas são a tarefa de **atualização automática do modelo** e a tarefa **configuração de status do local de armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="1ebf5-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="1ebf5-106">Essas tarefas agendadas não são configuráveis com as ferramentas do UE-V.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="1ebf5-107">Os administradores que quiserem alterar a tarefa agendada desses itens poderão criar um script que use as opções de linha de comando do Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="1ebf5-108">Para obter mais informações sobre Schtasks.exe, consulte [como usar Schtasks, exe para agendar tarefas no Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="1ebf5-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="1ebf5-109">Atualização automática de modelo</span><span class="sxs-lookup"><span data-stu-id="1ebf5-109">Template Auto-Update</span></span>


<span data-ttu-id="1ebf5-110">A tarefa de **atualização automática do modelo** verifica o catálogo de modelos de configurações para modelos novos, atualizados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="1ebf5-111">Essa tarefa só é executada se a SettingsTemplateCatalog estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="1ebf5-112">A tarefa de **atualização automática do modelo** executa o arquivo ApplySettingsCatalog.exe, localizado no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ebf5-113">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="1ebf5-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="1ebf5-114">Gatilho padrão</span><span class="sxs-lookup"><span data-stu-id="1ebf5-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ebf5-115">Atualização automática do \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="1ebf5-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ebf5-116">3:30 AM todos os dias</span><span class="sxs-lookup"><span data-stu-id="1ebf5-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1ebf5-117">**Exemplo:** O comando a seguir configura o agente para verificar a lista de catálogos de modelos de configurações a cada hora.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="1ebf5-118">Status do local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="1ebf5-118">Settings Storage Location Status</span></span>


<span data-ttu-id="1ebf5-119">A tarefa **configuração de status do local de armazenamento** executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="1ebf5-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="1ebf5-120">Verifica se as pastas do UE-V ainda estão fixadas ou registradas com o recurso arquivos offline.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="1ebf5-121">Verifica se o local de armazenamento de configurações está offline ou online.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="1ebf5-122">Força uma sincronização no intervalo especificado em vez do intervalo padrão para arquivos offline.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="1ebf5-123">Sincroniza qualquer pacote de configurações que está configurado para ser previamente buscado.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="1ebf5-124">Verifica se o caminho da pasta base do Active Directory foi alterado.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="1ebf5-125">Grava a configuração de armazenamento de configurações atuais no seguinte local</span><span class="sxs-lookup"><span data-stu-id="1ebf5-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="1ebf5-126">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="1ebf5-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="1ebf5-127">Gatilho padrão</span><span class="sxs-lookup"><span data-stu-id="1ebf5-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1ebf5-128">Status do local de armazenamento do \Microsoft\UE-V\Settings</span><span class="sxs-lookup"><span data-stu-id="1ebf5-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1ebf5-129">Ao fazer logon de qualquer usuário – após o disparo, repita a cada 30 minutos indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="1ebf5-130">**Exemplo:** O comando a seguir configura o agente para executar a ação acima de cada hora.</span><span class="sxs-lookup"><span data-stu-id="1ebf5-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="1ebf5-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ebf5-131">Related topics</span></span>


[<span data-ttu-id="1ebf5-132">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1ebf5-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="1ebf5-133">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1ebf5-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





