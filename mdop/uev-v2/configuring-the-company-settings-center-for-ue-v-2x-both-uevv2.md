---
title: Configurando o centro de configurações de empresa para UE-V 2. x
description: Configurando o centro de configurações de empresa para UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799243"
---
# <span data-ttu-id="cc8ef-103">Configurando o centro de configurações de empresa para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="cc8ef-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="cc8ef-104">O Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 incluem um novo aplicativo, o centro de configurações da empresa, que ajuda os usuários a gerenciar as configurações para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="cc8ef-105">O centro de configurações de empresa é instalado usando o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="cc8ef-106">Os usuários acessam o centro de configurações da empresa no painel de controle, no menu **Iniciar** ou na tela **inicial** , e por meio do ícone da área de notificação do UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="cc8ef-107">O centro de configurações de empresa mostra quais configurações são sincronizadas e ajuda os usuários a ver o status de sincronização da UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="cc8ef-108">Os usuários podem usar o centro de configurações da empresa para selecionar quais aplicativos ou recursos do Windows sincronizam suas configurações entre computadores.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="cc8ef-109">Eles também podem clicar no botão **sincronizar agora** para sincronizar todas as configurações imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="cc8ef-110">O administrador também pode incluir um link para suporte no centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="cc8ef-111">Sobre o centro de configurações da empresa</span><span class="sxs-lookup"><span data-stu-id="cc8ef-111">About the Company Settings Center</span></span>


<span data-ttu-id="cc8ef-112">O aplicativo da área de trabalho do centro de configurações da empresa fornece aos usuários informações sobre a sincronização das configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="cc8ef-113">O centro de configurações de empresa pode ser acessado de várias maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="cc8ef-114">Ícone da área de notificação – com o **ícone da bandeja** configuração da política de grupo ou configuração do Windows PowerShell habilitada, o ícone do UE-V aparece na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="cc8ef-115">Clique no ícone do UE-V para abrir o centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="cc8ef-116">**Observação**  O ícone da área de notificação pode ser desabilitado usando as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="cc8ef-117">Configuração da política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="cc8ef-118">Cmdlet do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="cc8ef-119">Item de configuração no pacote de configuração do UE-V para SystemCenter2012 ConfigurationManager:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="cc8ef-120">Aplicativo painel de controle – no painel de controle, navegue até **aparência e personalização**e clique em **central de configurações da empresa**.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="cc8ef-121">Notificação de primeira utilização – a não ser que seja desabilitado, o UE-V Agent alertará o usuário de que as configurações agora são sincronizadas quando o UE-V Agent é executado pela primeira vez em um computador.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="cc8ef-122">Clique na caixa de diálogo de notificação para abrir o centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="cc8ef-123">A tela **inicial** ou o menu **Iniciar** inclui um link para o centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="cc8ef-124">Uma pesquisa pela central de configurações da empresa localiza o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="cc8ef-125">Configurando o link de suporte no centro de configurações da empresa</span><span class="sxs-lookup"><span data-stu-id="cc8ef-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="cc8ef-126">O centro de configurações da empresa pode incluir um hiperlink no qual os usuários podem clicar para obter suporte com problemas de sincronização das configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="cc8ef-127">Esse link pode abrir qualquer protocolo de URL válido, como http://para uma página da Web ou mailto://para um email.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="cc8ef-128">O link suporte pode ser configurado usando a política de grupo, o Windows PowerShell ou o pacote de configuração do UE-V do Gerenciador de configuração do 2012 do System Center.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="cc8ef-129">Como configurar o link de suporte do centro de configurações da empresa</span><span class="sxs-lookup"><span data-stu-id="cc8ef-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="cc8ef-130">Abra sua ferramenta de gerenciamento preferencial:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="cc8ef-131">**Política de grupo** -se você ainda não tiver feito isso, baixe o modelo ADMX para UE-V 2 de [modelos administrativos do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span><span class="sxs-lookup"><span data-stu-id="cc8ef-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="cc8ef-132">**Windows PowerShell** – em um computador com o UE-V Agent instalado, abra o **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="cc8ef-133">Para obter mais informações sobre como administrar o UE-V usando o Windows PowerShell, consulte [administrando o UE-v 2. x com o Windows PowerShell e o WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="cc8ef-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="cc8ef-134">**Pacote de configuração do System Center 2012 para Microsoft User Experience Virtualization (UE-v)** – importe o pacote de configuração do UE-v e siga a documentação do pacote de configuração para criar itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="cc8ef-135">Para obter mais informações sobre o pacote de configuração do UE-V, consulte [Configurando o UE-v 2. x com o System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="cc8ef-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="cc8ef-136">Edite as configurações das seguintes políticas:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="cc8ef-137">**Texto do link de ti de contato** -essa configuração especifica o texto do hiperlink da URL do contato no centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="cc8ef-138">Se você habilitar essa configuração, o centro de configurações da empresa exibirá o texto especificado no link para a URL do contato.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="cc8ef-139">Configurações da política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="cc8ef-140">Cmdlet do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="cc8ef-141">Item de configuração do pacote de configuração:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="cc8ef-142">**Entre em contato com a URL** -essa configuração especifica a URL do link para o seu contato no centro de configurações da empresa em um protocolo de URL válido, como http://para uma página da web ou mailto://para um email.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="cc8ef-143">Configurações da política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="cc8ef-144">Cmdlet do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="cc8ef-145">Item de configuração do pacote de configuração:</span><span class="sxs-lookup"><span data-stu-id="cc8ef-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="cc8ef-146">Implantar configurações nos computadores dos usuários usando a ferramenta de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="cc8ef-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





