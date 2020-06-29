---
title: Novidades da UE-V 2.1
description: Novidades da UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799837"
---
# <span data-ttu-id="ecdb8-103">Novidades da UE-V 2.1</span><span class="sxs-lookup"><span data-stu-id="ecdb8-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="ecdb8-104">O User Experience Virtualization 2,1 oferece esses novos recursos e funcionalidades em comparação com o UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="ecdb8-105">As [notas de versão do Microsoft User Experience Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) fornecem mais informações sobre o lançamento do UE-v 2,1.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="ecdb8-106">Modelo de local de configurações do Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecdb8-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="ecdb8-107">O UE-V 2,1 inclui o modelo de local de configurações do Microsoft Office 2013 com suporte de assinatura do Outlook aprimorado.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="ecdb8-108">No UE-V 2,1, os dados de assinatura são sincronizados entre os dispositivos do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="ecdb8-109">Adicionamos a sincronização das configurações de assinatura padrão para emails novos, de resposta e encaminhados.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="ecdb8-110">Os clientes não precisam mais escolher as configurações de assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="ecdb8-111">**Observação**  Um perfil do Outlook deve ser criado para qualquer dispositivo no qual o usuário deseja sincronizar a assinatura do Outlook.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="ecdb8-112">Se o perfil ainda não tiver sido criado, o usuário poderá criar um e, em seguida, reiniciar o Outlook nesse dispositivo para habilitar a sincronização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="ecdb8-113">Anteriormente, o UE-V incluía modelos de local de configurações do Microsoft Office 2010 que foram automaticamente distribuídos e registrados com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="ecdb8-114">O UE-V 2,1 funciona com o Office 365 para determinar se as configurações do Office 2013 estão em roaming pelo Office 365.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="ecdb8-115">Se as configurações estiverem em roaming pelo Office 365, elas não serão em roaming pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="ecdb8-116">[Visão geral sobre as configurações de usuário e roaming do Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fornecem mais informações.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="ecdb8-117">Para habilitar a sincronização de configurações usando o UE-V 2,1, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="ecdb8-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="ecdb8-118">Usar a política de grupo para desabilitar a sincronização do Office 365</span><span class="sxs-lookup"><span data-stu-id="ecdb8-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="ecdb8-119">Não habilite a experiência de sincronização do Office 365 durante a instalação do Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecdb8-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="ecdb8-120">O UE-V 2,1 envia os [modelos do office 2013 e do office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="ecdb8-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="ecdb8-121">Esta versão remove os modelos do Office 2007.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="ecdb8-122">Os usuários ainda podem usar os modelos do Office 2007 do UE-V 2,0 ou versões anteriores e ainda podem obter os modelos da Galeria de modelos do UE-V localizada [aqui](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="ecdb8-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="ecdb8-123">Correção para usuários de namespace do sistema de arquivos distribuídos</span><span class="sxs-lookup"><span data-stu-id="ecdb8-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="ecdb8-124">O UE-V aprimorou o suporte do Distributed File System namespace (DFSN), adicionando uma configuração de UE-V chamada SyncProviderPingEnabled.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="ecdb8-125">Desabilitar essa configuração usando o PowerShell ou o WMI permite que os usuários desabilitem o ping do UE-V.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="ecdb8-126">O ping do UE-V causa um erro ao usar os servidores DFSN porque esses servidores não respondem aos pings.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="ecdb8-127">A não resposta impede que o UE-V sincronize as configurações.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="ecdb8-128">Desabilitar o ping do UE-V permite que a sincronização do UE-V funcione normalmente.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="ecdb8-129">Para desativar o UE-V ping, use este cmdlet do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ecdb8-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="ecdb8-130">Sincronização de credenciais</span><span class="sxs-lookup"><span data-stu-id="ecdb8-130">Synchronization for Credentials</span></span>


<span data-ttu-id="ecdb8-131">O UE-V 2,1 oferece aos clientes a capacidade de sincronizar credenciais e certificados armazenados no Gerenciador de credenciais do Windows.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="ecdb8-132">Esse componente é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-132">This component is disabled by default.</span></span> <span data-ttu-id="ecdb8-133">Habilitar esse componente permite que os usuários mantenham suas credenciais de domínio e certificados em sincronia. Os usuários podem entrar uma vez em um dispositivo, e essas credenciais serão transferidas para aquele usuário em todos os dispositivos habilitados da UE-V.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="ecdb8-134">[Gerenciar credenciais com o UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) fornece mais informações.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="ecdb8-135">**Observação**  No Windows 8 e posteriores, o Gerenciador de credenciais contém credenciais da Web.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="ecdb8-136">Essas credenciais não são sincronizadas entre os dispositivos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="ecdb8-137">Sincronização da conta do UE-V e da Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecdb8-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="ecdb8-138">O UE-V detecta se as "configurações de sincronização com o OneDrive", também conhecidas como sincronização da conta da Microsoft, está ativada.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="ecdb8-139">Se a conta da Microsoft não estiver configurada para sincronizar as configurações, o UE-V sincronizará aplicativos do Windows, pacotes AppX e configurações da área de trabalho do Windows entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="ecdb8-140">Isso permite que os usuários acessem seus aplicativos da loja, música, imagens e outros aplicativos habilitados para contas da Microsoft sem sincronização fora do firewall da empresa.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="ecdb8-141">O UE-V Verifica se a política de grupo vai parar de sincronizar as configurações com o OneDrive ou se o usuário desabilitar a **sincronização de suas configurações neste computador** nos controles de usuário.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="ecdb8-142">Suporte para o SyncMethod external</span><span class="sxs-lookup"><span data-stu-id="ecdb8-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="ecdb8-143">Uma nova [configuração de SyncMethod](https://technet.microsoft.com/library/dn554321.aspx) chamada **external** especifica que, se as configurações de UE-V forem gravadas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como o onedrive for Business, as pastas de trabalho, o SharePoint ou o Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="ecdb8-144">Suporte aprimorado para o modo VDI</span><span class="sxs-lookup"><span data-stu-id="ecdb8-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="ecdb8-145">O UE-V 2,1 inclui [suporte a sessões do VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) compartilhadas entre os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="ecdb8-146">Como administrador, você pode registrar e configurar um modelo VDI especial, o que garante que o UE-V mantém toda a funcionalidade intacta em sessões de VDI não persistentes.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="ecdb8-147">**Observação**  Se você não habilitar o modo VDI para sessões de VDI não persistentes, alguns recursos não funcionarão, como backup/restauração e LKG.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="ecdb8-148">Backup e restauração administrativos</span><span class="sxs-lookup"><span data-stu-id="ecdb8-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="ecdb8-149">Você pode restaurar configurações adicionais quando um usuário adotar um novo dispositivo colocando um modelo de local de configurações no perfil **backup** ou **roaming (padrão)** usando o cmdlet Set-UevTemplateProfile do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="ecdb8-150">Isso permite que as configurações do computador sejam sincronizadas com o novo computador, além das configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="ecdb8-151">Os modelos atribuídos ao perfil de backup são incluídos em backup para esse dispositivo e configurados em cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="ecdb8-152">[Gerenciar o backup e a restauração administrativos no UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) fornece mais informações.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="ecdb8-153">Sincronização para configurações adicionais do Windows</span><span class="sxs-lookup"><span data-stu-id="ecdb8-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="ecdb8-154">O UE-V agora sincroniza a personalização do teclado virtual, o dicionário ortográfico e permite que o aplicativo alterne para aplicativos recentes e configurações de borda da tela para sincronizar entre os dispositivos Windows 8 e Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="ecdb8-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="ecdb8-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecdb8-155">Related topics</span></span>


[<span data-ttu-id="ecdb8-156">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="ecdb8-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="ecdb8-157">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="ecdb8-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="ecdb8-158">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecdb8-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





