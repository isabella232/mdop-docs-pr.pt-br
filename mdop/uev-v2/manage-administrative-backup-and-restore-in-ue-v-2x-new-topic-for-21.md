---
title: Gerenciar o backup e a restauração administrativos no UE-V 2. x
description: Gerenciar o backup e a restauração administrativos no UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800062"
---
# <span data-ttu-id="3466f-103">Gerenciar o backup e a restauração administrativos no UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="3466f-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="3466f-104">Como administrador do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, você pode restaurar as configurações do aplicativo e do Windows ao seu estado original.</span><span class="sxs-lookup"><span data-stu-id="3466f-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="3466f-105">E novo no UE-V 2,1, você também pode restaurar configurações adicionais quando um usuário adotar um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3466f-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="3466f-106">Restaurar as configurações no UE-V 2,1 ou no UE-V 2,1 SP1 quando um usuário adotar um novo dispositivo</span><span class="sxs-lookup"><span data-stu-id="3466f-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="3466f-107">Para restaurar as configurações quando um usuário adotar um novo dispositivo, você poderá colocar um modelo de local de configurações no perfil **backup** ou **roaming (padrão)** usando o cmdlet Set-UevTemplateProfile do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3466f-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="3466f-108">Isso permite que as configurações do computador sejam sincronizadas com o novo computador, além das configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="3466f-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="3466f-109">Os modelos atribuídos ao perfil de backup são incluídos em backup para esse dispositivo e configurados em cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3466f-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="3466f-110">Para fazer backup das configurações de um modelo, use o seguinte cmdlet no Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3466f-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="3466f-111">&lt;TemplateID &gt; é a ID do modelo UE-V</span><span class="sxs-lookup"><span data-stu-id="3466f-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="3466f-112">&lt;&gt;o backup pode ser backup ou roaming</span><span class="sxs-lookup"><span data-stu-id="3466f-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="3466f-113">Ao substituir o dispositivo de um usuário, o UE-V restaura automaticamente as configurações se o domínio do usuário, o nome de usuário e o nome do dispositivo corresponderem.</span><span class="sxs-lookup"><span data-stu-id="3466f-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="3466f-114">Todos os dados sincronizados e todos os dados de backup são restaurados automaticamente no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3466f-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="3466f-115">Você também pode usar o novo cmdlet do PowerShell, Restore-UevBackup, para restaurar as configurações de um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="3466f-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="3466f-116">Para clonar os pacotes de configurações para o novo dispositivo, use o cmdlet a seguir no Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3466f-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="3466f-117">onde &lt; MachineName &gt; é o nome do computador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3466f-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="3466f-118">Modelos como o modelo do Office 2013 que incluem muitos aplicativos podem ser incluídos no perfil móvel (padrão) ou de backup.</span><span class="sxs-lookup"><span data-stu-id="3466f-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="3466f-119">Os aplicativos individuais em um pacote de modelos seguem o grupo.</span><span class="sxs-lookup"><span data-stu-id="3466f-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="3466f-120">Os modelos in-box do Office 2013 incluem configurações de roaming e somente de backup.</span><span class="sxs-lookup"><span data-stu-id="3466f-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="3466f-121">As configurações somente de backup não podem ser incluídas em um perfil móvel.</span><span class="sxs-lookup"><span data-stu-id="3466f-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="3466f-122">Como parte do recurso de backup/restauração, o UE-V adicionou a **última mercadoria conhecida (LKG)** às opções para reverter as configurações.</span><span class="sxs-lookup"><span data-stu-id="3466f-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="3466f-123">Nesta versão, você pode reverter para as configurações originais ou configurações LKG.</span><span class="sxs-lookup"><span data-stu-id="3466f-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="3466f-124">As configurações do LKG permitem que os usuários voltem a um ponto intermediário e estável antes do estado anterior ao UE-V das configurações.</span><span class="sxs-lookup"><span data-stu-id="3466f-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="3466f-125">Como fazer backup/restaurar modelos com UE-V</span><span class="sxs-lookup"><span data-stu-id="3466f-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="3466f-126">Estes são os principais componentes de backup e restauração da UE-V:</span><span class="sxs-lookup"><span data-stu-id="3466f-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="3466f-127">Perfis de modelo</span><span class="sxs-lookup"><span data-stu-id="3466f-127">Template profiles</span></span>

-   <span data-ttu-id="3466f-128">Local dos pacotes de configurações no modelo de local de armazenamento configurações</span><span class="sxs-lookup"><span data-stu-id="3466f-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="3466f-129">Gatilho de backup</span><span class="sxs-lookup"><span data-stu-id="3466f-129">Backup trigger</span></span>

-   <span data-ttu-id="3466f-130">Como as configurações são restauradas</span><span class="sxs-lookup"><span data-stu-id="3466f-130">How settings are restored</span></span>

**<span data-ttu-id="3466f-131">Perfis de modelo</span><span class="sxs-lookup"><span data-stu-id="3466f-131">Template Profiles</span></span>**

<span data-ttu-id="3466f-132">Um perfil de modelo UE-V é definido quando o modelo é registrado no dispositivo ou após o registro de postagem por meio do utilitário de configuração do PowerShell/WMI.</span><span class="sxs-lookup"><span data-stu-id="3466f-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="3466f-133">Os tipos de perfil incluem:</span><span class="sxs-lookup"><span data-stu-id="3466f-133">The profile types include:</span></span>

-   <span data-ttu-id="3466f-134">Roaming (padrão)</span><span class="sxs-lookup"><span data-stu-id="3466f-134">Roaming (default)</span></span>

-   <span data-ttu-id="3466f-135">Backup</span><span class="sxs-lookup"><span data-stu-id="3466f-135">Backup</span></span>

-   <span data-ttu-id="3466f-136">Independemente</span><span class="sxs-lookup"><span data-stu-id="3466f-136">BackupOnly</span></span>

<span data-ttu-id="3466f-137">Todos os modelos são incluídos no perfil móvel quando registrados, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3466f-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="3466f-138">Esses modelos sincronizam as configurações para todos os dispositivos habilitados para UE-V com o modelo correspondente habilitado.</span><span class="sxs-lookup"><span data-stu-id="3466f-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="3466f-139">Os modelos podem ser adicionados ao perfil de backup com o PowerShell ou WMI usando o cmdlet Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="3466f-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="3466f-140">Os modelos no perfil de backup reservam essas configurações para o local de armazenamento de configurações em um diretório de nome de dispositivo especial.</span><span class="sxs-lookup"><span data-stu-id="3466f-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="3466f-141">O backup das configurações especificadas é feito neste local.</span><span class="sxs-lookup"><span data-stu-id="3466f-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="3466f-142">Modelos designados incorretamente incluem configurações específicas do dispositivo que não devem ser sincronizadas, a menos que explicitamente restaurados.</span><span class="sxs-lookup"><span data-stu-id="3466f-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="3466f-143">Essas configurações são armazenadas no mesmo local do pacote de configurações específicas do dispositivo no local de armazenamento de configurações como as configurações do Backedup.</span><span class="sxs-lookup"><span data-stu-id="3466f-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="3466f-144">Esses modelos têm um identificador especial inserido no modelo que especifica que eles devem fazer parte desse perfil.</span><span class="sxs-lookup"><span data-stu-id="3466f-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="3466f-145">Local dos pacotes de configurações no modelo de local de armazenamento configurações</span><span class="sxs-lookup"><span data-stu-id="3466f-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="3466f-146">As configurações do perfil de roaming são armazenadas no local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="3466f-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="3466f-147">Os modelos atribuídos ao backup ou ao perfil indesejado armazenam suas configurações no local de armazenamento de configurações em um diretório de nome de dispositivo especial.</span><span class="sxs-lookup"><span data-stu-id="3466f-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="3466f-148">Cada dispositivo com modelos nesses perfis tem seu próprio nome de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3466f-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="3466f-149">O UE-V não limpa esses diretórios.</span><span class="sxs-lookup"><span data-stu-id="3466f-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="3466f-150">Gatilho de backup</span><span class="sxs-lookup"><span data-stu-id="3466f-150">Backup trigger</span></span>**

<span data-ttu-id="3466f-151">O backup é acionado pelos mesmos eventos que disparam uma sincronização de UE-V.</span><span class="sxs-lookup"><span data-stu-id="3466f-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="3466f-152">Como as configurações são restauradas</span><span class="sxs-lookup"><span data-stu-id="3466f-152">How settings are restored</span></span>**

<span data-ttu-id="3466f-153">Restaurar o dispositivo de um usuário restaura as configurações do modelo atualmente registadas da pasta de backup de outro dispositivo e todas as configurações sincronizadas para o computador atual.</span><span class="sxs-lookup"><span data-stu-id="3466f-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="3466f-154">As configurações são restauradas destas duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="3466f-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="3466f-155">Restauração automática</span><span class="sxs-lookup"><span data-stu-id="3466f-155">Automatic restore</span></span>**

    <span data-ttu-id="3466f-156">Se o caminho de armazenamento, o domínio e o nome do computador do usuário do UE-V são compatíveis com o usuário atual, todas as configurações do usuário serão sincronizadas, com apenas as configurações mais recentes aplicadas.</span><span class="sxs-lookup"><span data-stu-id="3466f-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="3466f-157">Se um usuário fizer logon em um novo dispositivo pela primeira vez e esses critérios forem atendidos, os dados de configurações serão aplicados a esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3466f-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="3466f-158">Observação</span><span class="sxs-lookup"><span data-stu-id="3466f-158">Note</span></span>**  
    <span data-ttu-id="3466f-159">As configurações de acessibilidade e de área de trabalho do Windows exigem que o usuário faça logon novamente no Windows para ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="3466f-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="3466f-160">Restauração manual</span><span class="sxs-lookup"><span data-stu-id="3466f-160">Manual Restore</span></span>**

    <span data-ttu-id="3466f-161">Se quiser ajudar os usuários restaurando um dispositivo durante uma atualização, você pode optar por usar o cmdlet Restore-UevBackup.</span><span class="sxs-lookup"><span data-stu-id="3466f-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="3466f-162">Esse comando faz com que as configurações do usuário sejam baixadas do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="3466f-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="3466f-163">Restaurar o aplicativo e as configurações do Windows para o estado original</span><span class="sxs-lookup"><span data-stu-id="3466f-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="3466f-164">Os comandos do WMI e do Windows PowerShell permitem restaurar as configurações do aplicativo e do Windows para os valores de configurações que estavam no computador na primeira vez que o aplicativo foi iniciado após a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="3466f-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="3466f-165">Essa ação de restauração é realizada em uma base de configurações por aplicativo ou Windows.</span><span class="sxs-lookup"><span data-stu-id="3466f-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="3466f-166">As configurações serão restauradas na próxima vez que o aplicativo for executado, ou as configurações serão restauradas quando o usuário fizer logon no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3466f-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="3466f-167">Para restaurar as configurações do aplicativo e as configurações do Windows com o Windows PowerShell para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="3466f-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="3466f-168">Abra a janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3466f-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="3466f-169">Digite o seguinte cmdlet do Windows PowerShell para restaurar as configurações do aplicativo e as configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="3466f-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="3466f-170">Cmdlet do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3466f-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="3466f-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="3466f-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="3466f-172">Restaura as configurações de usuário para um aplicativo ou restaura um grupo de configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="3466f-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="3466f-173">Para restaurar as configurações do aplicativo e as configurações do Windows com WMI</span><span class="sxs-lookup"><span data-stu-id="3466f-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="3466f-174">Abra uma janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3466f-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="3466f-175">Digite o seguinte comando WMI para restaurar as configurações do aplicativo e as configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="3466f-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="3466f-176">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="3466f-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="3466f-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="3466f-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="3466f-178">Restaura as configurações de usuário para um aplicativo ou restaura um grupo de configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="3466f-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="3466f-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3466f-179">Related topics</span></span>


[<span data-ttu-id="3466f-180">Administração do UE-V 2. x com o Windows PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="3466f-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="3466f-181">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="3466f-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









