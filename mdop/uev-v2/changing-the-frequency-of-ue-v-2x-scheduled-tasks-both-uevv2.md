---
title: Alterar a frequência das tarefas agendadas do UE-V 2. x
description: Alterar a frequência das tarefas agendadas do UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799470"
---
# <span data-ttu-id="d6a7d-103">Alterar a frequência das tarefas agendadas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="d6a7d-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="d6a7d-104">O instalador do agente do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, AgentSetup.exe, cria as seguintes tarefas agendadas durante a instalação do agente do UE-V:</span><span class="sxs-lookup"><span data-stu-id="d6a7d-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="d6a7d-105">Monitorar configurações de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d6a7d-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="d6a7d-106">Aplicativo de controlador de sincronização</span><span class="sxs-lookup"><span data-stu-id="d6a7d-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="d6a7d-107">Sincronizar configurações durante logoff</span><span class="sxs-lookup"><span data-stu-id="d6a7d-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="d6a7d-108">Atualização automática de modelo</span><span class="sxs-lookup"><span data-stu-id="d6a7d-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="d6a7d-109">Coletar dados do CEIP</span><span class="sxs-lookup"><span data-stu-id="d6a7d-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="d6a7d-110">Carregar dados CEIP</span><span class="sxs-lookup"><span data-stu-id="d6a7d-110">Upload CEIP Data</span></span>**

<span data-ttu-id="d6a7d-111">**Observação**  Com exceção da coleta de dados CEIP, essas tarefas devem permanecer habilitadas, pois o UE-V não pode funcionar sem elas.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="d6a7d-112">Essas tarefas agendadas não são configuráveis com as ferramentas do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="d6a7d-113">Os administradores que desejam alterar a tarefa agendada desses itens podem criar um script que use as opções de linha de comando do Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="d6a7d-114">Para obter mais informações sobre Schtasks.exe, consulte [como usar Schtasks, exe para agendar tarefas no Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="d6a7d-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="d6a7d-115">Para obter mais informações sobre</span><span class="sxs-lookup"><span data-stu-id="d6a7d-115">For more information about</span></span>

## <span data-ttu-id="d6a7d-116">Tarefas agendadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="d6a7d-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="d6a7d-117">As seguintes tarefas agendadas estão incluídas no UE-V 2 com comandos de configuração agendada de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="d6a7d-118">Coletar dados do CEIP</span><span class="sxs-lookup"><span data-stu-id="d6a7d-118">Collect CEIP Data</span></span>

<span data-ttu-id="d6a7d-119">Se, durante a instalação, o usuário ou o administrador tiver optado por participar do programa de aperfeiçoamento da experiência do usuário (CEIP), o UE-V coleta dados para ajudar a melhorar o produto em lançamentos futuros.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="d6a7d-120">Esta tarefa agendada só é executada no logon.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="d6a7d-121">A tarefa **coletar dados CEIP** executa a UevSqmSession.exe, localizada no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6a7d-122">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d6a7d-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="d6a7d-123">Evento padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6a7d-124">Dados do CEIP do \Microsoft\UE-V\Collect</span><span class="sxs-lookup"><span data-stu-id="d6a7d-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-125">Sessão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d6a7d-126">Monitorar configurações de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d6a7d-126">Monitor Application Settings</span></span>

<span data-ttu-id="d6a7d-127">A tarefa **monitorar configurações do aplicativo** é usada para sincronizar as configurações para aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="d6a7d-128">Ele é executado no momento do logon, mas atrasado em 30 segundos para não afetar o logon de acordo.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="d6a7d-129">A tarefa monitorar status do aplicativo executa o arquivo UevAppMonitor.exe, localizado no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6a7d-130">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d6a7d-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="d6a7d-131">Evento padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6a7d-132">Status do aplicativo \Microsoft\UE-V\Monitor</span><span class="sxs-lookup"><span data-stu-id="d6a7d-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-133">Sessão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d6a7d-134">Aplicativo de controlador de sincronização</span><span class="sxs-lookup"><span data-stu-id="d6a7d-134">Sync Controller Application</span></span>

<span data-ttu-id="d6a7d-135">A tarefa de **aplicativo do controlador de sincronização** é usada para iniciar o controlador de sincronização para sincronizar as configurações do computador com o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="d6a7d-136">Por padrão, a tarefa é executada a cada 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="d6a7d-137">Nesse momento, as configurações locais são sincronizadas com o local de armazenamento de configurações e as configurações atualizadas no local de armazenamento de configurações são sincronizadas com o computador.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="d6a7d-138">O aplicativo de controlador de sincronização executa o Microsoft.Uev.SyncController.exe, localizado no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="d6a7d-139">**Observação:** De acordo com a tarefa **monitorar configurações do aplicativo** , essa tarefa é executada no momento do logon, mas demora 30 segundos para não afetar o logon de forma prejudicial.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6a7d-140">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d6a7d-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="d6a7d-141">Evento padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6a7d-142">Aplicativo de controlador \Microsoft\UE-V\Sync</span><span class="sxs-lookup"><span data-stu-id="d6a7d-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-143">Faça logon e a cada 30 minutos depois</span><span class="sxs-lookup"><span data-stu-id="d6a7d-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d6a7d-144">Por exemplo, o comando a seguir configura o agente para sincronizar as configurações a cada 15 minutos, em vez do padrão de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="d6a7d-145">Sincronizar configurações durante logoff</span><span class="sxs-lookup"><span data-stu-id="d6a7d-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="d6a7d-146">A tarefa **sincronizar configurações em logoff** é usada para iniciar um aplicativo no logon que controla a sincronização de aplicativos durante o logoff para UE-V.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="d6a7d-147">A tarefa sincronizar configurações em logoff executa o arquivo Microsoft.Uev.SyncController.exe, localizado no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6a7d-148">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d6a7d-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="d6a7d-149">Evento padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6a7d-150">Configurações do \Microsoft\UE-V\Synchronize ao fazer logoff</span><span class="sxs-lookup"><span data-stu-id="d6a7d-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-151">Sessão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d6a7d-152">Atualização automática de modelo</span><span class="sxs-lookup"><span data-stu-id="d6a7d-152">Template Auto Update</span></span>

<span data-ttu-id="d6a7d-153">A tarefa de **atualização automática do modelo** verifica o catálogo de modelos de configurações para modelos novos, atualizados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="d6a7d-154">Essa tarefa só é executada se a SettingsTemplateCatalog estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="d6a7d-155">A tarefa de **atualização automática do modelo** executa o arquivo ApplySettingsCatalog.exe, localizado no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6a7d-156">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d6a7d-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="d6a7d-157">Evento padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6a7d-158">Atualização automática do \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="d6a7d-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-159">Inicialização do sistema e em 3:30 AM todos os dias, em um tempo aleatório em uma janela de 1 hora</span><span class="sxs-lookup"><span data-stu-id="d6a7d-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d6a7d-160">**Exemplo:** O comando a seguir configura o UE-V Agent para verificar a lista de catálogos de modelos de configurações a cada hora.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="d6a7d-161">Carregar dados CEIP</span><span class="sxs-lookup"><span data-stu-id="d6a7d-161">Upload CEIP Data</span></span>

<span data-ttu-id="d6a7d-162">A tarefa **carregar dados do CEIP** será executada durante a instalação se o usuário ou o administrador optar por participar do programa de aperfeiçoamento da experiência do usuário (CEIP).</span><span class="sxs-lookup"><span data-stu-id="d6a7d-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="d6a7d-163">Essa tarefa carrega os dados nos servidores CEIP nos quais os dados são usados para ajudar a melhorar o produto para futuras versões do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="d6a7d-164">Esta tarefa agendada é executada no momento do logon e a cada 4 horas depois.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="d6a7d-165">A tarefa **carregar dados do CEIP** executa o arquivo UevSqmUploader.exe, localizado no diretório de instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6a7d-166">Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="d6a7d-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="d6a7d-167">Evento padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6a7d-168">Dados do CEIP do \Microsoft\UE-V\Upload</span><span class="sxs-lookup"><span data-stu-id="d6a7d-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-169">Durante o logon e a cada 4 horas</span><span class="sxs-lookup"><span data-stu-id="d6a7d-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d6a7d-170">Detalhes da tarefa agendada do UE-V 2</span><span class="sxs-lookup"><span data-stu-id="d6a7d-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="d6a7d-171">O gráfico a seguir fornece informações adicionais sobre as tarefas agendadas para o UE-V 2:</span><span class="sxs-lookup"><span data-stu-id="d6a7d-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d6a7d-172">Nome da tarefa </strong> (nome do arquivo)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d6a7d-173">Frequência padrão</span><span class="sxs-lookup"><span data-stu-id="d6a7d-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d6a7d-174">Alternância de energia</span><span class="sxs-lookup"><span data-stu-id="d6a7d-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d6a7d-175">Somente ocioso</span><span class="sxs-lookup"><span data-stu-id="d6a7d-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d6a7d-176">Conexão de rede</span><span class="sxs-lookup"><span data-stu-id="d6a7d-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d6a7d-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6a7d-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d6a7d-178">Monitorar configurações </strong> do aplicativo (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-179">Inicia 30 segundos após o logon e continua até que o logoff seja efetuado.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-180">Não</span><span class="sxs-lookup"><span data-stu-id="d6a7d-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-181">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-182">N/A</span><span class="sxs-lookup"><span data-stu-id="d6a7d-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-183">Sincroniza as configurações para aplicativos do Windows (AppX).</span><span class="sxs-lookup"><span data-stu-id="d6a7d-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d6a7d-184">Aplicativo de controlador </strong> de sincronização (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-185">Durante o logon e a cada 30 min em diante.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-186">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-187">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-188">Somente se a rede estiver conectada</span><span class="sxs-lookup"><span data-stu-id="d6a7d-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-189">Inicia o controlador de sincronização que sincroniza as configurações locais com o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d6a7d-190">Sincronizar configurações ao fazer logoff </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-191">Executa no logon e, em seguida, aguarda o logoff para sincronizar as configurações.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-192">Não</span><span class="sxs-lookup"><span data-stu-id="d6a7d-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-193">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-194">N/A</span><span class="sxs-lookup"><span data-stu-id="d6a7d-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-195">Inicie um aplicativo no logon que controla a sincronização de aplicativos durante o logoff.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d6a7d-196">Atualização automática </strong> de modelo (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-197">É executado no logon inicial e em 3:30 AM todos os dias daí em diante.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-198">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-199">Não</span><span class="sxs-lookup"><span data-stu-id="d6a7d-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-200">N/A</span><span class="sxs-lookup"><span data-stu-id="d6a7d-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-201">Verifica o catálogo de modelos de configurações para modelos novos, atualizados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="d6a7d-202">Esta tarefa só será executada se SettingsTemplateCatalog estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d6a7d-203">Coletar dados CEIP </strong> (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-204">No logon iniciado pelo serviço</span><span class="sxs-lookup"><span data-stu-id="d6a7d-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-205">Não</span><span class="sxs-lookup"><span data-stu-id="d6a7d-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-206">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-207">N/A</span><span class="sxs-lookup"><span data-stu-id="d6a7d-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-208">Se o usuário ou o administrador optar pelo programa de aperfeiçoamento da experiência do usuário (CEIP), essa tarefa coletará dados que ajudarão a aprimorar futuras versões do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d6a7d-209">Carregar dados CEIP </strong> (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-210">É executado no momento da conexão e às 4:00 fica todos os dias depois disso.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-211">Não</span><span class="sxs-lookup"><span data-stu-id="d6a7d-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-212">Sim</span><span class="sxs-lookup"><span data-stu-id="d6a7d-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-213">Somente se a rede estiver conectada</span><span class="sxs-lookup"><span data-stu-id="d6a7d-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6a7d-214">Se o usuário ou o administrador optar pelo programa de aperfeiçoamento da experiência do usuário (CEIP), essa tarefa carregará os dados nos servidores CEIP.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d6a7d-215">Da</span><span class="sxs-lookup"><span data-stu-id="d6a7d-215">Legend</span></span>**

-   <span data-ttu-id="d6a7d-216">Botão de **alternância de energia** – o Agendador de tarefas otimizará o consumo de energia quando não estiver conectado à alimentação de CA.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="d6a7d-217">A tarefa pode parar de funcionar se o computador mudar para energia da bateria.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="d6a7d-218">**Somente ocioso** – a tarefa será interrompida se o computador deixar de ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="d6a7d-219">Por padrão, a tarefa não será reiniciada quando o computador ficar ocioso novamente.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="d6a7d-220">Em vez disso, a tarefa será iniciada novamente no próximo gatilho de tarefa.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="d6a7d-221">**Conexão de rede** – tarefas marcadas como "Sim" só são executadas se o computador tiver uma conexão de rede disponível.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="d6a7d-222">As tarefas marcadas como "N/d" são executadas independentemente da conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="d6a7d-223">Como gerenciar tarefas agendadas</span><span class="sxs-lookup"><span data-stu-id="d6a7d-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="d6a7d-224">Para localizar tarefas agendadas, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d6a7d-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="d6a7d-225">Abra "agendar tarefas" no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="d6a7d-226">Navegue até: Agendador de tarefas – &gt; biblioteca do Agendador de tarefas- &gt; Microsoft- &gt; UE-V</span><span class="sxs-lookup"><span data-stu-id="d6a7d-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="d6a7d-227">Selecione a tarefa agendada que você deseja gerenciar e configurar no painel detalhes.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="d6a7d-228">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="d6a7d-228">Additional information</span></span>

<span data-ttu-id="d6a7d-229">As seguintes informações adicionais se aplicam às tarefas agendadas do UE-V:</span><span class="sxs-lookup"><span data-stu-id="d6a7d-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="d6a7d-230">ll a sequência de tarefas programas estão localizados na pasta de instalação do UE-V Agent, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` por padrão.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="d6a7d-231">A tarefa agendada do aplicativo de controlador de sincronização é o componente crucial quando o UE-V SyncMethod é definido como "SyncProvider" (a configuração padrão do UE-V 2).</span><span class="sxs-lookup"><span data-stu-id="d6a7d-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="d6a7d-232">Esta tarefa agendada mantém o SettingsSToragePath sincronizado com as versões armazenadas em cache localmente dos arquivos de pacote de configurações.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="d6a7d-233">Se os usuários reclamarem de que as configurações não sincronizam com frequência suficiente, você poderá reduzir a configuração de tarefa agendada para apenas 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="d6a7d-234">Você também pode aumentar o padrão de 30 min para um valor mais alto, se necessário.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="d6a7d-235">Se os usuários reclamarem de que as configurações não sincronizam rápido o suficiente no logon, você poderá remover a configuração de atraso para a tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="d6a7d-236">(Você pode encontrar a configuração atraso na caixa de diálogo **Editar gatilho** )</span><span class="sxs-lookup"><span data-stu-id="d6a7d-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="d6a7d-237">Você não precisa desabilitar a tarefa agendada de atualização automática de modelo se usar outro método para manter os modelos dos clientes em sincronia (ou seja, política de grupo ou linhas de base do Configuration Manager).</span><span class="sxs-lookup"><span data-stu-id="d6a7d-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="d6a7d-238">Deixar o valor da propriedade SettingsTemplateCatalog em branco impede que o UE-V Verifique o catálogo de configurações para ver os modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="d6a7d-239">Esta tarefa agendada executa ApplySettingsCatalog.exe e, essencialmente, retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="d6a7d-240">A tarefa monitorar configurações do aplicativo agendada atualizará as configurações do aplicativo do Windows (AppX) em tempo real, com base nos gatilhos de configuração do programa de aplicativos do Windows, criados em cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6a7d-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="d6a7d-241">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6a7d-241">Related topics</span></span>


[<span data-ttu-id="d6a7d-242">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="d6a7d-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="d6a7d-243">Implantar o UE-V 2. x para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="d6a7d-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





