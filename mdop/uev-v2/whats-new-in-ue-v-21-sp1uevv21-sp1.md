---
title: Novidades da UE-V 2.1 SP1
description: Novidades da UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800070"
---
# <span data-ttu-id="6060d-103">Novidades da UE-V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="6060d-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="6060d-104">O User Experience Virtualization 2,1 SP1 oferece esses novos recursos e funcionalidades em comparação com o UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="6060d-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="6060d-105">As [notas de versão do Microsoft User Experience Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) fornecem mais informações sobre a versão do UE-v 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="6060d-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="6060d-106">Suporte para Windows 10</span><span class="sxs-lookup"><span data-stu-id="6060d-106">Support for Windows 10</span></span>


<span data-ttu-id="6060d-107">O UE-V 2,1 SP1 adiciona suporte para o Windows 10, além do mesmo software que é compatível com versões anteriores do UE-V.</span><span class="sxs-lookup"><span data-stu-id="6060d-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="6060d-108">Compatibilidade com o Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="6060d-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="6060d-109">O Windows 10 permite que os usuários corporativos sincronizem as configurações do aplicativo do Windows e do sistema operacional do Windows com o Azure em vez do OneDrive.</span><span class="sxs-lookup"><span data-stu-id="6060d-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="6060d-110">Você pode usar a funcionalidade de sincronização do Windows 10 Enterprise em conjunto com o UE-V para computadores somente associados a um domínio local.</span><span class="sxs-lookup"><span data-stu-id="6060d-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="6060d-111">Para habilitar a coexistência entre o Windows 10 e o UE-V, você deve desabilitar os seguintes modelos de UE-V usando o PowerShell em cada cliente ou política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6060d-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="6060d-112">Na política de grupo, no nó Microsoft User Experience Virtualization, defina estas configurações de política:</span><span class="sxs-lookup"><span data-stu-id="6060d-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="6060d-113">Habilitar "não sincronizar aplicativos do Windows"</span><span class="sxs-lookup"><span data-stu-id="6060d-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="6060d-114">Desabilitar "sincronizar configurações do Windows"</span><span class="sxs-lookup"><span data-stu-id="6060d-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="6060d-115">O comportamento de sincronização de configurações mudou para suporte do Windows 10</span><span class="sxs-lookup"><span data-stu-id="6060d-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="6060d-116">As configurações de barra de tarefas de roaming do UE-V 2,1 SP1 entre dispositivos Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6060d-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="6060d-117">No entanto, o UE-V não sincroniza as configurações da barra de tarefas entre dispositivos Windows 10 e dispositivos que executam sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="6060d-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="6060d-118">Além disso, o UE-V 2,1 SP1 não sincroniza as configurações entre a calculadora da Microsoft no Windows 10 e a calculadora da Microsoft em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="6060d-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="6060d-119">Suporte adicionado para impressoras de rede de roaming</span><span class="sxs-lookup"><span data-stu-id="6060d-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="6060d-120">O UE-V 2,1 SP1 permite que impressoras de rede sejam movidas entre dispositivos para que um usuário tenha acesso às suas impressoras de rede quando estiver conectado a qualquer dispositivo na rede.</span><span class="sxs-lookup"><span data-stu-id="6060d-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="6060d-121">Isso inclui o roaming da impressora definida como padrão.</span><span class="sxs-lookup"><span data-stu-id="6060d-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="6060d-122">O roaming da impressora no UE-V exige um dos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="6060d-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="6060d-123">O servidor de impressão pode baixar o driver necessário quando ele está em roaming para um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6060d-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="6060d-124">O driver para a impressora de rede de roaming está pré-instalado em qualquer dispositivo que precise acessar a impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="6060d-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="6060d-125">O driver da impressora pode ser obtido no Windows Update.</span><span class="sxs-lookup"><span data-stu-id="6060d-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="6060d-126">**Observação**  O recurso de roaming da impressora UE-V **não transfere** preferências ou configurações de impressora, como impressão em frente e verso.</span><span class="sxs-lookup"><span data-stu-id="6060d-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="6060d-127">Modelo de local de configurações do Office 2013</span><span class="sxs-lookup"><span data-stu-id="6060d-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="6060d-128">O UE-V 2,1 e o 2,1 SP1 incluem o modelo de local de configurações do Microsoft Office 2013 com suporte à assinatura do Outlook aprimorado.</span><span class="sxs-lookup"><span data-stu-id="6060d-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="6060d-129">Adicionamos a sincronização das configurações de assinatura padrão para emails novos, de resposta e encaminhados.</span><span class="sxs-lookup"><span data-stu-id="6060d-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="6060d-130">Os clientes não precisam mais escolher as configurações de assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="6060d-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="6060d-131">**Observação**  Um perfil do Outlook deve ser criado para qualquer dispositivo no qual o usuário deseja sincronizar a assinatura do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6060d-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="6060d-132">Se o perfil ainda não tiver sido criado, o usuário poderá criar um e, em seguida, reiniciar o Outlook nesse dispositivo para habilitar a sincronização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="6060d-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="6060d-133">Anteriormente, o UE-V incluía modelos de local de configurações do Microsoft Office 2010 que foram automaticamente distribuídos e registrados com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6060d-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="6060d-134">O UE-V 2,1 funciona com o Office 365 para determinar se as configurações do Office 2013 estão em roaming pelo Office 365.</span><span class="sxs-lookup"><span data-stu-id="6060d-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="6060d-135">Se as configurações estiverem em roaming pelo Office 365, elas não serão em roaming pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="6060d-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="6060d-136">[Visão geral sobre as configurações de usuário e roaming do Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fornecem mais informações.</span><span class="sxs-lookup"><span data-stu-id="6060d-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="6060d-137">Para habilitar a sincronização de configurações usando o UE-V 2,1, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="6060d-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="6060d-138">Usar a política de grupo para desabilitar a sincronização do Office 365</span><span class="sxs-lookup"><span data-stu-id="6060d-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="6060d-139">Não habilite a experiência de sincronização do Office 365 durante a instalação do Office 2013</span><span class="sxs-lookup"><span data-stu-id="6060d-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="6060d-140">O UE-V 2,1 envia os [modelos do office 2013 e do office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="6060d-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="6060d-141">Esta versão remove os modelos do Office 2007.</span><span class="sxs-lookup"><span data-stu-id="6060d-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="6060d-142">Os usuários ainda podem usar os modelos do Office 2007 do UE-V 2,0 ou versões anteriores e ainda podem obter os modelos da Galeria de modelos do UE-V localizada [aqui](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="6060d-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="6060d-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6060d-143">Related topics</span></span>


[<span data-ttu-id="6060d-144">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="6060d-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="6060d-145">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6060d-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="6060d-146">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="6060d-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





