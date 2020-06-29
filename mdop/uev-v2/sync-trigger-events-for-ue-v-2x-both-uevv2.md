---
title: Sincronizar eventos de disparo para a UE-V 2.x
description: Sincronizar eventos de disparo para a UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799944"
---
# <span data-ttu-id="12867-103">Sincronizar eventos de disparo para a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="12867-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="12867-104">O Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 permite sincronizar seu aplicativo e as configurações do Windows em todos os seus dispositivos ingressados no domínio.</span><span class="sxs-lookup"><span data-stu-id="12867-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="12867-105">Os *eventos de gatilho de sincronização* definem quando o UE-V Agent sincroniza essas configurações com o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="12867-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="12867-106">O UE-V 2 introduz um novo *método de sincronização* chamado *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="12867-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="12867-107">Para obter mais informações sobre a configuração do método de sincronização, consulte [métodos de sincronização para UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="12867-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="12867-108">Eventos do gatilho de sincronização do UE-V 2</span><span class="sxs-lookup"><span data-stu-id="12867-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="12867-109">A tabela a seguir explica os eventos de gatilho para aplicativos clássicos e configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="12867-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12867-110">Evento de gatilho UE-V 2</span><span class="sxs-lookup"><span data-stu-id="12867-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="12867-111">SyncMethod = SyncProvider</span><span class="sxs-lookup"><span data-stu-id="12867-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="12867-112">SyncMethod = nenhum</span><span class="sxs-lookup"><span data-stu-id="12867-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12867-113">Logon do Windows</span><span class="sxs-lookup"><span data-stu-id="12867-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="12867-114">As configurações do aplicativo e do Windows são importadas para o cache local do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="12867-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="12867-115">As configurações assíncronas do Windows </a> são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="12867-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="12867-116">As configurações síncronas do Windows serão aplicadas durante o próximo logon do Windows.</span><span class="sxs-lookup"><span data-stu-id="12867-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="12867-117">As configurações do aplicativo serão aplicadas quando o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="12867-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="12867-118">As configurações do aplicativo e do Windows são lidas diretamente do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="12867-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="12867-119">As configurações assíncronas e assíncronas do Windows são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="12867-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="12867-120">As configurações do aplicativo serão aplicadas quando o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="12867-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12867-121">Logoff do Windows</span><span class="sxs-lookup"><span data-stu-id="12867-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12867-122">Armazenar alterações localmente e armazenar em cache e copiar configurações assíncronas e assíncronas do Windows para o servidor de localização de armazenamento de configurações, se disponível</span><span class="sxs-lookup"><span data-stu-id="12867-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="12867-123">Armazenar alterações no local de armazenamento de configurações assíncronas e assíncronas do Windows</span><span class="sxs-lookup"><span data-stu-id="12867-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12867-124">Windows Connect (RDP)/desbloquear</span><span class="sxs-lookup"><span data-stu-id="12867-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12867-125">Sincronize as configurações assíncronas do Windows do local de armazenamento de configurações para o cache local, se disponível.</span><span class="sxs-lookup"><span data-stu-id="12867-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="12867-126">Aplicar configurações do Windows armazenadas em cache</span><span class="sxs-lookup"><span data-stu-id="12867-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="12867-127">Baixar e aplicar configurações assíncronas do Windows do local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="12867-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12867-128">Desconexão do Windows (RDP)/bloqueio</span><span class="sxs-lookup"><span data-stu-id="12867-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12867-129">Armazene as alterações de configurações assíncronas do Windows no cache local.</span><span class="sxs-lookup"><span data-stu-id="12867-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="12867-130">Sincronizar qualquer configuração assíncrona do Windows do cache local para o local de armazenamento configurações, se disponível</span><span class="sxs-lookup"><span data-stu-id="12867-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="12867-131">Armazenar alterações de configurações assíncronas do Windows no local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="12867-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12867-132">Início do aplicativo</span><span class="sxs-lookup"><span data-stu-id="12867-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12867-133">Aplicar configurações de aplicativo do cache local conforme o aplicativo é iniciado</span><span class="sxs-lookup"><span data-stu-id="12867-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="12867-134">Aplicar configurações do aplicativo do local de armazenamento de configurações à medida que o aplicativo for iniciado</span><span class="sxs-lookup"><span data-stu-id="12867-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12867-135">Aplicativo é fechado</span><span class="sxs-lookup"><span data-stu-id="12867-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12867-136">Armazenar as alterações de configurações do aplicativo nas configurações de cache local e copiar para o local de armazenamento de configurações, se disponíveis</span><span class="sxs-lookup"><span data-stu-id="12867-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="12867-137">Armazenar as alterações de configurações do aplicativo em local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="12867-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12867-138">A tarefa agendada do controlador de sincronização ou "sincronizar agora" é executada no centro de configurações da empresa</span><span class="sxs-lookup"><span data-stu-id="12867-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="12867-139">As configurações do aplicativo e do Windows são sincronizadas entre o local de armazenamento de configurações e o cache local.</span><span class="sxs-lookup"><span data-stu-id="12867-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="12867-140">Observação</span><span class="sxs-lookup"><span data-stu-id="12867-140">Note</span></span></strong><br/><p><span data-ttu-id="12867-141">As alterações de configurações não são armazenadas em cache localmente até que o aplicativo seja fechado.</span><span class="sxs-lookup"><span data-stu-id="12867-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="12867-142">Este gatilho não importará alterações feitas em um aplicativo em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="12867-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="12867-143">Para configurações do Windows, isso significa que todas as alterações não serão armazenadas em cache localmente e exportadas até o próximo bloqueio (assíncrono) ou logoff (assíncrono e síncrono).</span><span class="sxs-lookup"><span data-stu-id="12867-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="12867-144">As configurações são aplicadas nestes casos:</span><span class="sxs-lookup"><span data-stu-id="12867-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="12867-145">As configurações assíncronas do Windows são aplicadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="12867-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="12867-146">As configurações do aplicativo são aplicadas quando o aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="12867-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="12867-147">As configurações assíncronas e assíncronas do Windows são aplicadas durante o próximo logon do Windows.</span><span class="sxs-lookup"><span data-stu-id="12867-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="12867-148">As configurações do aplicativo do Windows (AppX) são aplicadas durante a próxima atualização.</span><span class="sxs-lookup"><span data-stu-id="12867-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="12867-149">Consulte <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)"> monitorar configurações </a> do aplicativo para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="12867-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="12867-150">NA</span><span class="sxs-lookup"><span data-stu-id="12867-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12867-151">Configurações assíncronas atualizadas na loja remota \*</span><span class="sxs-lookup"><span data-stu-id="12867-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12867-152">Carregar e aplicar novas configurações assíncronas do cache.</span><span class="sxs-lookup"><span data-stu-id="12867-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="12867-153">Carregar e aplicar configurações do servidor central</span><span class="sxs-lookup"><span data-stu-id="12867-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="12867-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12867-154">Related topics</span></span>


[<span data-ttu-id="12867-155">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="12867-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="12867-156">Alterar a frequência das tarefas agendadas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="12867-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="12867-157">Escolha o método de configuração para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="12867-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









