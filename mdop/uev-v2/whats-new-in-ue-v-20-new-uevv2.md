---
title: Novidades da UE-V 2.0
description: Novidades da UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799577"
---
# <span data-ttu-id="60da3-103">Novidades da UE-V 2.0</span><span class="sxs-lookup"><span data-stu-id="60da3-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="60da3-104">O Microsoft User Experience Virtualization (UE-V) 2,0 oferece esses novos recursos e funcionalidades em comparação com o UE-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="60da3-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="60da3-105">As [notas de versão do Microsoft User Experience Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) fornecem mais informações sobre o lançamento do UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="60da3-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="60da3-106">O CSC (cache do lado do cliente) não é mais necessário</span><span class="sxs-lookup"><span data-stu-id="60da3-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="60da3-107">Esta versão do UE-V apresenta o **provedor de sincronização**, que substitui a necessidade do recurso de arquivos offline do Windows para dar suporte a um cache de configurações do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="60da3-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="60da3-108">Enquanto o UE-V é usado para sincronizar as configurações somente quando um aplicativo é aberto, fechado ou quando o Windows foi bloqueado ou desbloqueado, ou no logon ou logoff, o provedor de sincronização também...</span><span class="sxs-lookup"><span data-stu-id="60da3-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="60da3-109">Sincroniza o aplicativo local e as configurações do Windows fora da faixa usando "**disparar eventos**"</span><span class="sxs-lookup"><span data-stu-id="60da3-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="60da3-110">Usa uma **tarefa agendada** para sincronizar o pacote de armazenamento de configurações em qualquer intervalo que você escolher para seus requisitos de empresa (a cada 30 minutos por padrão)</span><span class="sxs-lookup"><span data-stu-id="60da3-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="60da3-111">Determinadas condições fornecem sincronização mais frequente.</span><span class="sxs-lookup"><span data-stu-id="60da3-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="60da3-112">As configurações são sincronizadas quando o usuário clica no botão **sincronizar agora** no novo aplicativo da central de configurações de empresa.</span><span class="sxs-lookup"><span data-stu-id="60da3-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="60da3-113">O provedor de sincronização também pode iniciar para um único aplicativo sem aguardar a tarefa de sincronização programada.</span><span class="sxs-lookup"><span data-stu-id="60da3-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="60da3-114">Por exemplo, quando um aplicativo é fechado, todas as alterações de configurações são gravadas no cache local, e o processo do provedor de sincronização é executado de forma assíncrona para mover as alterações de novas configurações para o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="60da3-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="60da3-115">Sincronização do aplicativo Windows</span><span class="sxs-lookup"><span data-stu-id="60da3-115">Windows app synchronization</span></span>


<span data-ttu-id="60da3-116">O desenvolvedor de um aplicativo do Windows pode definir quais configurações, se houver, serão sincronizadas, e essas configurações agora podem ser capturadas e sincronizadas com UE-V.</span><span class="sxs-lookup"><span data-stu-id="60da3-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="60da3-117">Por padrão, o UE-V sincroniza as configurações de muitos aplicativos do Windows incluídos no Windows 8 e no Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="60da3-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="60da3-118">Você pode modificar a lista de aplicativos sincronizados com o Windows PowerShell, a instrumentação de gerenciamento do Windows (WMI) ou a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="60da3-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="60da3-119">**Observação**  O UE-V não sincroniza as configurações de aplicativo do Windows se os usuários do domínio vinculem suas credenciais de entrada à conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60da3-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="60da3-120">Essa vinculação sincronizará as configurações com o Microsoft OneDrive para que o UE-V sincronize somente os aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="60da3-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="60da3-121">Vinculação de conta da Microsoft</span><span class="sxs-lookup"><span data-stu-id="60da3-121">Microsoft account linking</span></span>


<span data-ttu-id="60da3-122">A sincronização de configurações pelo OneDrive é nova para o Windows 8 quando você está conectado com uma conta da Microsoft ou se você vincula sua conta da Microsoft à sua conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="60da3-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="60da3-123">Se um usuário de domínio usa UE-V e se conectou a uma conta da Microsoft, então...</span><span class="sxs-lookup"><span data-stu-id="60da3-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="60da3-124">O UE-V sincroniza apenas as configurações para aplicativos da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="60da3-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="60da3-125">Conta da Microsoft manipula configurações do aplicativo Windows e as configurações da área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="60da3-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="60da3-126">Centro de configurações da empresa</span><span class="sxs-lookup"><span data-stu-id="60da3-126">Company Settings Center</span></span>


<span data-ttu-id="60da3-127">Você pode fornecer a seus usuários algum controle sobre quais configurações são sincronizadas por meio de um aplicativo no UE-V 2 chamado centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="60da3-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="60da3-128">O centro de configurações da empresa é instalado juntamente com o UE-V Agent e os usuários podem acessá-lo no painel de controle, no menu **Iniciar** ou na tela **inicial** e no ícone da área de notificação do UE-V.</span><span class="sxs-lookup"><span data-stu-id="60da3-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="60da3-129">O centro de configurações de empresa mostra quais configurações são sincronizadas e permite que os usuários vejam o status de sincronização da UE-V.</span><span class="sxs-lookup"><span data-stu-id="60da3-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="60da3-130">Se você permitir, os usuários poderão usar o centro de configurações da empresa para selecionar quais configurações sincronizar.</span><span class="sxs-lookup"><span data-stu-id="60da3-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="60da3-131">Eles também podem clicar no botão **sincronizar agora** para sincronizar todas as configurações imediatamente.</span><span class="sxs-lookup"><span data-stu-id="60da3-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="60da3-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60da3-132">Related topics</span></span>


[<span data-ttu-id="60da3-133">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="60da3-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="60da3-134">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="60da3-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="60da3-135">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="60da3-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





