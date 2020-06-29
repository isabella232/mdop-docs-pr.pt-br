---
title: Gerenciando o agente e os pacotes do UE-V 2. x com o Windows PowerShell e o WMI
description: Gerenciando o agente e os pacotes do UE-V 2. x com o Windows PowerShell e o WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799945"
---
# <span data-ttu-id="c4b91-103">Gerenciando o agente e os pacotes do UE-V 2. x com o Windows PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="c4b91-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="c4b91-104">Você pode usar a instrumentação de gerenciamento do Windows (WMI) e o Windows PowerShell para gerenciar a configuração e o comportamento de sincronização do agente do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="c4b91-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="c4b91-105">Para obter uma lista completa dos cmdlets do PowerShell do UE-V, consulte [referência do cmdlet do UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="c4b91-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="c4b91-106">Para implantar o UE-V Agent usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4b91-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c4b91-107">Testar o arquivo do instalador do UE-V em um compartilhamento de rede acessível.</span><span class="sxs-lookup"><span data-stu-id="c4b91-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="c4b91-108">Observação</span><span class="sxs-lookup"><span data-stu-id="c4b91-108">Note</span></span>**  
    <span data-ttu-id="c4b91-109">Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c4b91-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="c4b91-110">Os pacotes do Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura.</span><span class="sxs-lookup"><span data-stu-id="c4b91-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="c4b91-111">Para desinstalar o UE-V Agent posteriormente, usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4b91-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="c4b91-112">Use um dos seguintes comandos do Windows PowerShell para instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c4b91-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="c4b91-113">Para configurar o UE-V Agent usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4b91-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="c4b91-114">Abra uma janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c4b91-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="c4b91-115">Para gerenciar as configurações do computador que afetam todos os usuários do computador usando o parâmetro *computador* , abra a janela com uma conta com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="c4b91-116">Use os seguintes comandos do Windows PowerShell para configurar o agente.</span><span class="sxs-lookup"><span data-stu-id="c4b91-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c4b91-117">comando do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4b91-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="c4b91-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4b91-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-119">Obtém as configurações efetivas do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c4b91-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="c4b91-120">As configurações específicas do usuário têm precedência sobre as configurações do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-121">Obtém os valores das configurações do UE-V Agent somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c4b91-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-122">Obtém os valores das configurações de configuração do UE-V Agent para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-123">Obtém os detalhes para cada configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="c4b91-124">Exibe onde a configuração está configurada ou se usa o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c4b91-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="c4b91-125">Será exibido se a configuração atual for válida.</span><span class="sxs-lookup"><span data-stu-id="c4b91-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-126">Define o texto que é exibido no centro de configurações da empresa para o link ajuda.</span><span class="sxs-lookup"><span data-stu-id="c4b91-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-127">Define a URL do link no centro de configurações da empresa para o link ajuda.</span><span class="sxs-lookup"><span data-stu-id="c4b91-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="c4b91-128">Qualquer protocolo de URL pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="c4b91-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-129">Configura o UE-V Agent para não sincronizar nenhum aplicativo do Windows para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-130">Configura o UE-V Agent para não sincronizar nenhum aplicativo do Windows para o usuário atual do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-131">Configura o UE-V Agent para exibir a notificação na primeira vez que o agente é executado para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-132">Configura o UE-V Agent para não exibir a notificação na primeira vez que o agente é executado para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-133">Configura o UE-V Agent para notificar todos os usuários do computador quando a sincronização de configurações é atrasada.</span><span class="sxs-lookup"><span data-stu-id="c4b91-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="c4b91-134">Use o <em> </em> parâmetro DisableSettingsImportNotify para desabilitar a notificação.</span><span class="sxs-lookup"><span data-stu-id="c4b91-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-135">Configura o UE-V Agent para notificar o usuário atual quando a sincronização de configurações é adiada.</span><span class="sxs-lookup"><span data-stu-id="c4b91-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="c4b91-136">Use o <em> </em> parâmetro DisableSettingsImportNotify para desabilitar a notificação.</span><span class="sxs-lookup"><span data-stu-id="c4b91-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-137">Configura o UE-V Agent para sincronizar todos os aplicativos do Windows que não são explicitamente desabilitados pela lista de aplicativos do Windows para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="c4b91-138">Para obter mais informações, consulte &quot; Get-UevAppxPackage &quot; em <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="c4b91-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="c4b91-139">Use o <em> </em> parâmetro DisableSyncUnlistedWindows8Apps para configurar o UE-V Agent para sincronizar apenas aplicativos do Windows que são explicitamente habilitados pela lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c4b91-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-140">Configura o UE-V Agent para sincronizar todos os aplicativos do Windows que não são explicitamente desabilitados pela lista de aplicativos do Windows para o usuário atual no computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="c4b91-141">Para obter mais informações, consulte &quot; Get-UevAppxPackage &quot; em <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="c4b91-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="c4b91-142">Use o <em> </em> parâmetro DisableSyncUnlistedWindows8Apps para configurar o UE-V Agent para sincronizar apenas aplicativos do Windows que são explicitamente habilitados pela lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c4b91-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-143">Desabilita o UE-V para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="c4b91-144">Use o <em> </em> parâmetro EnableSync para habilitar ou desabilitar novamente.</span><span class="sxs-lookup"><span data-stu-id="c4b91-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-145">Desabilita o UE-V para o usuário atual no computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="c4b91-146">Use o <em> </em> parâmetro EnableSync para habilitar ou desabilitar novamente.</span><span class="sxs-lookup"><span data-stu-id="c4b91-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-147">Habilita o ícone do UE-V na área de notificação para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="c4b91-148">Use o <em> </em> parâmetro DisableTrayIcon para desabilitar o ícone.</span><span class="sxs-lookup"><span data-stu-id="c4b91-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-149">Configura o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atinge o limite definido para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="c4b91-150">Define o tamanho do pacote de limite em bytes.</span><span class="sxs-lookup"><span data-stu-id="c4b91-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-151">Configura o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atinge o limite definido.</span><span class="sxs-lookup"><span data-stu-id="c4b91-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="c4b91-152">Define o limite de aviso do tamanho do pacote para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c4b91-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-153">Especifica o tempo em segundos antes de o usuário ser notificado para todos os usuários do computador</span><span class="sxs-lookup"><span data-stu-id="c4b91-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-154">Especifica o tempo em segundos antes de a notificação para o usuário atual ser enviada.</span><span class="sxs-lookup"><span data-stu-id="c4b91-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-155">Define um local de armazenamento de configurações por computador para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-156">Define um local de armazenamento de configurações por usuário.</span><span class="sxs-lookup"><span data-stu-id="c4b91-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-157">Define o caminho do catálogo de modelos de configurações para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-158">Define o método de sincronização para todos os usuários do computador: SyncProvider ou None.</span><span class="sxs-lookup"><span data-stu-id="c4b91-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-159">Define o método de sincronização para o usuário atual: SyncProvider ou None.</span><span class="sxs-lookup"><span data-stu-id="c4b91-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-160">Define o tempo limite de sincronização em milissegundos para todos os usuários do computador</span><span class="sxs-lookup"><span data-stu-id="c4b91-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-161">Definir o tempo limite de sincronização para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c4b91-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-162">Limpa a configuração especificada para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-163">Limpa a configuração especificada somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c4b91-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-164">Exporta a configuração do computador UE-V para um arquivo de migração de configurações.</span><span class="sxs-lookup"><span data-stu-id="c4b91-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="c4b91-165">A extensão de nome de arquivo deve ser. UEV.</span><span class="sxs-lookup"><span data-stu-id="c4b91-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="c4b91-166">O <code>Export</code> cmdlet exporta todas as configurações do UE-V Agent que são configuráveis com o <em> </em> parâmetro Computer.</span><span class="sxs-lookup"><span data-stu-id="c4b91-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c4b91-167">Importa a configuração do computador UE-V de um arquivo de migração de configurações.</span><span class="sxs-lookup"><span data-stu-id="c4b91-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="c4b91-168">A extensão de nome de arquivo deve ser. UEV.</span><span class="sxs-lookup"><span data-stu-id="c4b91-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="c4b91-169">Para exportar as configurações do pacote do UE-V e reparar os modelos do UE-V usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4b91-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c4b91-170">Abra uma janela do Windows PowerShell como administrador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="c4b91-171">Use os seguintes comandos do Windows PowerShell para configurar o agente.</span><span class="sxs-lookup"><span data-stu-id="c4b91-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c4b91-172">comando do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4b91-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="c4b91-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4b91-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c4b91-174">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="c4b91-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-175">Extrai as configurações de um arquivo de pacote calculadora da Microsoft e converte-as em um formato legível por pessoas em XML.</span><span class="sxs-lookup"><span data-stu-id="c4b91-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c4b91-176">Reparar-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="c4b91-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-177">Repara o índice dos modelos de local de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c4b91-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="c4b91-178">Para configurar o UE-V Agent usando WMI</span><span class="sxs-lookup"><span data-stu-id="c4b91-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="c4b91-179">A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="c4b91-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="c4b91-180">Os administradores podem usar essa interface para configurar o UE-V Agent na linha de comando e automatizar tarefas típicas de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="c4b91-181">Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c4b91-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="c4b91-182">Use os seguintes comandos WMI para configurar o agente.</span><span class="sxs-lookup"><span data-stu-id="c4b91-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="c4b91-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4b91-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-184">Exibe as configurações ativas do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c4b91-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="c4b91-185">As configurações específicas do usuário têm precedência sobre as configurações do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-186">Exibe a configuração do UE-V Agent definida para um usuário.</span><span class="sxs-lookup"><span data-stu-id="c4b91-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-187">Exibe a configuração do UE-V Agent definida para um computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-188">Exibe os detalhes de cada item de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="c4b91-189">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c4b91-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-190">Define um local de armazenamento de configurações por computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-191">Define um local de armazenamento de configurações por usuário.</span><span class="sxs-lookup"><span data-stu-id="c4b91-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-192">Define o tempo limite de sincronização em milissegundos para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-193">Configura o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atinge um limite definido.</span><span class="sxs-lookup"><span data-stu-id="c4b91-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="c4b91-194">Defina o tamanho do arquivo do pacote de limite em bytes para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-195">Define o método de sincronização para todos os usuários do computador: SyncProvider ou None.</span><span class="sxs-lookup"><span data-stu-id="c4b91-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-196">Para habilitar uma configuração específica por computador, desmarque a configuração e use <em> $NULL </em> como o valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="c4b91-197">Use userconfiguration para configurações por usuário.</span><span class="sxs-lookup"><span data-stu-id="c4b91-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-198">Para desabilitar uma configuração específica por computador, desmarque a configuração e use <em> $NULL </em> como o valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="c4b91-199">Use a configuração do usuário para configurações por usuário.</span><span class="sxs-lookup"><span data-stu-id="c4b91-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-200">Atualiza uma configuração específica por computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="c4b91-201">Para limpar a configuração, use <em> $NULL </em> como o valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="c4b91-202">$config. &lt; definindo o &gt;  =  &lt; valor da configuração de nome&gt;</span><span class="sxs-lookup"><span data-stu-id="c4b91-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-203">Atualiza uma configuração específica por usuário para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="c4b91-204">Para limpar a configuração, use <em> $NULL </em> como o valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4b91-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="c4b91-205">Para exportar as configurações do pacote do UE-V e reparar os modelos do UE-V usando o WMI</span><span class="sxs-lookup"><span data-stu-id="c4b91-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="c4b91-206">O UE-V fornece o seguinte conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="c4b91-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="c4b91-207">Os administradores podem usar essa interface para exportar um pacote ou reparar modelos do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c4b91-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="c4b91-208">Use os comandos WMI a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4b91-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c4b91-209">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="c4b91-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="c4b91-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4b91-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-211">Extrai as configurações de um arquivo de pacote e converte-as em um formato legível por pessoas em XML.</span><span class="sxs-lookup"><span data-stu-id="c4b91-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="c4b91-212">Repara o índice dos modelos de local de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c4b91-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="c4b91-213">Deve ser executado como administrador.</span><span class="sxs-lookup"><span data-stu-id="c4b91-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="c4b91-214">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4b91-214">Related topics</span></span>


[<span data-ttu-id="c4b91-215">Administração do UE-V 2. x com o Windows PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="c4b91-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="c4b91-216">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c4b91-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









