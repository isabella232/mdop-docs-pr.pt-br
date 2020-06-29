---
title: Métodos de sincronização para a UE-V 2.x
description: Métodos de sincronização para a UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799300"
---
# <span data-ttu-id="8ed25-103">Métodos de sincronização para a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="8ed25-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="8ed25-104">O agente do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 permite que você sincronize as configurações do aplicativo e do Windows do usuário com o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="8ed25-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="8ed25-105">A configuração do *método Sync* define como o agente UE-V carrega e baixa essas configurações para o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="8ed25-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="8ed25-106">O UE-V 2. x introduz um novo SyncMethod chamado de *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="8ed25-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="8ed25-107">Para obter mais informações sobre eventos de gatilho que iniciam a sincronização das configurações do aplicativo e do Windows, confira [sincronizar eventos de gatilho para UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="8ed25-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="8ed25-108">Configuração do SyncMethod</span><span class="sxs-lookup"><span data-stu-id="8ed25-108">SyncMethod Configuration</span></span>


<span data-ttu-id="8ed25-109">Esta tabela explica as alterações no SyncMethod do UE-V v 1.0 para o v 2.0 para o v 2.1, bem como as configurações para cada configuração:</span><span class="sxs-lookup"><span data-stu-id="8ed25-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8ed25-110">Configuração do SyncMethod</span><span class="sxs-lookup"><span data-stu-id="8ed25-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8ed25-111">V 1.0</span><span class="sxs-lookup"><span data-stu-id="8ed25-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8ed25-112">V 2.0</span><span class="sxs-lookup"><span data-stu-id="8ed25-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8ed25-113">V 2.1 e V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="8ed25-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8ed25-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ed25-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ed25-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="8ed25-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-116">n/d</span><span class="sxs-lookup"><span data-stu-id="8ed25-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-117">Padrão</span><span class="sxs-lookup"><span data-stu-id="8ed25-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-118">Padrão</span><span class="sxs-lookup"><span data-stu-id="8ed25-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-119">As alterações de configurações para um aplicativo específico ou configurações da área de trabalho global do Windows são salvas localmente em uma pasta de cache.</span><span class="sxs-lookup"><span data-stu-id="8ed25-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="8ed25-120">Essas alterações são sincronizadas com o local de armazenamento de configurações quando ocorre um evento de gatilho de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8ed25-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="8ed25-121">Ao enviar alterações, você salvará as alterações locais no caminho de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="8ed25-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="8ed25-122">Essa configuração padrão é o padrão ouro para computadores.</span><span class="sxs-lookup"><span data-stu-id="8ed25-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="8ed25-123">Essa opção tenta sincronizar a configuração e expira após um pequeno atraso para garantir que a inicialização do aplicativo ou do sistema operacional não seja adiada por um longo período de tempo.</span><span class="sxs-lookup"><span data-stu-id="8ed25-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="8ed25-124">Essa funcionalidade também está vinculada à tarefa agendada – aplicativo do controlador de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8ed25-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="8ed25-125">O administrador controla a frequência da tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="8ed25-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="8ed25-126">Por padrão, os computadores sincronizam as configurações a cada 30 min após o logon.</span><span class="sxs-lookup"><span data-stu-id="8ed25-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ed25-127">OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="8ed25-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-128">Padrão</span><span class="sxs-lookup"><span data-stu-id="8ed25-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-129">Preterido</span><span class="sxs-lookup"><span data-stu-id="8ed25-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-130">Preterido</span><span class="sxs-lookup"><span data-stu-id="8ed25-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-131">Comporta-se da mesma forma que o SyncProvider em V 2.0.</span><span class="sxs-lookup"><span data-stu-id="8ed25-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="8ed25-132">Se os arquivos offline estiverem habilitados e a pasta estiver fixada, o UE-V desafixará essa pasta e será sincronizado diretamente com o diretório SMB central.</span><span class="sxs-lookup"><span data-stu-id="8ed25-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="8ed25-133">Observação: </strong> em V 1.0 se você quisesse usar o UE-V em uma CorpNet desconectada (conhecida pela viagem com um laptop), a orientação é usar arquivos offline para garantir que as configurações sejam móveis.</span><span class="sxs-lookup"><span data-stu-id="8ed25-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="8ed25-134">Recebemos comentários suficientes do cliente que a ativação de arquivos offline é um bloqueador corporativo não trivial.</span><span class="sxs-lookup"><span data-stu-id="8ed25-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="8ed25-135">Portanto, na UE-V 2, criamos um mecanismo de sincronização rigidamente acoplado para armazenar seus dados localmente em cache e sincronizar as configurações para o servidor central.</span><span class="sxs-lookup"><span data-stu-id="8ed25-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="8ed25-136">Esta área de recursos não substitui os arquivos offline ou o redirecionamento de pastas.</span><span class="sxs-lookup"><span data-stu-id="8ed25-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="8ed25-137">O UE-V 2 não funciona bem com pastas offline, portanto, as orientações não definem o caminho de armazenamento de configurações para uma pasta fixa offline ou CSC.</span><span class="sxs-lookup"><span data-stu-id="8ed25-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ed25-138">Externo</span><span class="sxs-lookup"><span data-stu-id="8ed25-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-139">n/d</span><span class="sxs-lookup"><span data-stu-id="8ed25-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-140">n/d</span><span class="sxs-lookup"><span data-stu-id="8ed25-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-141">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8ed25-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-142">Novo no UE-V 2,1, esse método de configuração especifica que se as configurações de UE-V são gravadas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como o OneDrive for Business, as pastas de trabalho, o SharePoint ou o Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.</span><span class="sxs-lookup"><span data-stu-id="8ed25-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ed25-143">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="8ed25-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-144">Sim</span><span class="sxs-lookup"><span data-stu-id="8ed25-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-145">Sim</span><span class="sxs-lookup"><span data-stu-id="8ed25-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-146">Sim</span><span class="sxs-lookup"><span data-stu-id="8ed25-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ed25-147">Essa configuração de configuração foi projetada para a VDI (Virtual Desktop Infrastructure) e a experiência do aplicativo em fluxo principalmente.</span><span class="sxs-lookup"><span data-stu-id="8ed25-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="8ed25-148">Essa configuração deve ser usada em caixas do Windows Server usadas em um datacenter, onde a conexão sempre estará disponível.</span><span class="sxs-lookup"><span data-stu-id="8ed25-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="8ed25-149">Todas as alterações de configurações são salvas diretamente no servidor.</span><span class="sxs-lookup"><span data-stu-id="8ed25-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="8ed25-150">Se a conexão de rede com o caminho de armazenamento de configurações não estiver disponível, as alterações de configurações serão armazenadas em cache no dispositivo e sincronizadas na próxima vez que o provedor de sincronização for executado.</span><span class="sxs-lookup"><span data-stu-id="8ed25-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="8ed25-151">Se o caminho de armazenamento de configurações não for encontrado e o perfil do usuário for removido de um ambiente de VDI em pool no logoff, essas alterações serão perdidas, e o usuário deverá reaplicar a alteração quando o computador puder alcançar novamente o caminho de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="8ed25-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="8ed25-152">Os aplicativos e o sistema operacional aguardarão indefinidamente o local a ser apresentado.</span><span class="sxs-lookup"><span data-stu-id="8ed25-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="8ed25-153">Isso pode causar a carga do aplicativo ou o tempo de logon do sistema operacional para aumentar drasticamente se o local não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="8ed25-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8ed25-154">Você pode configurar o método de sincronização das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="8ed25-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="8ed25-155">Ao [implantar o UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) por meio de um parâmetro de linha de comando ou em um script em lotes</span><span class="sxs-lookup"><span data-stu-id="8ed25-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="8ed25-156">Por meio das configurações de [política de grupo](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed25-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="8ed25-157">Com o [pacote de configuração do System Center](https://technet.microsoft.com/library/dn458917.aspx) para UE-V</span><span class="sxs-lookup"><span data-stu-id="8ed25-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="8ed25-158">Após a instalação do UE-V Agent, usando o [Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed25-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="8ed25-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ed25-159">Related topics</span></span>


[<span data-ttu-id="8ed25-160">Implantar os recursos necessários na UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="8ed25-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="8ed25-161">Implantar os recursos necessários na UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="8ed25-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="8ed25-162">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="8ed25-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





