---
title: Detecções de alterações na rede que afetam a MED-V
description: Detecções de alterações na rede que afetam a MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799259"
---
# <span data-ttu-id="f71d6-103">Detecções de alterações na rede que afetam a MED-V</span><span class="sxs-lookup"><span data-stu-id="f71d6-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="f71d6-104">A solução Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 permite que você configure seu ambiente para detectar determinadas alterações de rede que podem ocorrer após a implantação do espaço de trabalho do MED-V, e isso pode afetar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="f71d6-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="f71d6-105">O recurso inclui um componente em execução no sistema operacional convidado que é notificado sobre alterações de configuração de rede no computador host.</span><span class="sxs-lookup"><span data-stu-id="f71d6-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="f71d6-106">Ele permite que um ESD ou outro aplicativo que não seja da Microsoft seja executado no convidado resolva os mesmos pontos de extremidade de rede que o host ESD ou o aplicativo resolve.</span><span class="sxs-lookup"><span data-stu-id="f71d6-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="f71d6-107">**Observação**  Esse recurso só estará disponível se a máquina virtual estiver configurada para o modo NAT (conversão de endereços de rede).</span><span class="sxs-lookup"><span data-stu-id="f71d6-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="f71d6-108">Se a máquina virtual estiver configurada para o modo de ponte, nenhum indicações de alteração será gerado.</span><span class="sxs-lookup"><span data-stu-id="f71d6-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="f71d6-109">Esta seção fornece informações e instruções para ajudá-lo a monitorar as alterações de rede que podem afetar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="f71d6-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="f71d6-110">Para detectar as alterações de rede do MED-V</span><span class="sxs-lookup"><span data-stu-id="f71d6-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="f71d6-111">Depois de implantar seus espaços de trabalho do MED-V, você pode monitorar as alterações em determinadas configurações de rede, preformando as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f71d6-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="f71d6-112">Crie um arquivo MOF (formato de objeto gerenciado) que irá procurar as alterações de configuração de rede que você deseja monitorar.</span><span class="sxs-lookup"><span data-stu-id="f71d6-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="f71d6-113">O código a seguir mostra um exemplo do arquivo MOF que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="f71d6-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="f71d6-114">Compile o arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="f71d6-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="f71d6-115">Instale o arquivo MOF no convidado.</span><span class="sxs-lookup"><span data-stu-id="f71d6-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="f71d6-116">Depois de instalar o arquivo MOF, você pode criar uma assinatura de evento que assine os eventos de criação, modificação ou exclusão da Windows Management Instrumentation (WMI) para a classe **CCM \ _NetworkAdapters** .</span><span class="sxs-lookup"><span data-stu-id="f71d6-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="f71d6-117">Isso detecta as seguintes alterações no host:</span><span class="sxs-lookup"><span data-stu-id="f71d6-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="f71d6-118">Há alguma alteração de configuração na rede, como alterações no endereço IP ou adaptador de rede?</span><span class="sxs-lookup"><span data-stu-id="f71d6-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="f71d6-119">A rede está disponível ou não está disponível?</span><span class="sxs-lookup"><span data-stu-id="f71d6-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="f71d6-120">A configuração de rede foi alterada do modo de ponte para o modo NAT?</span><span class="sxs-lookup"><span data-stu-id="f71d6-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="f71d6-121">A configuração de rede foi alterada do modo NAT para o modo de ponte?</span><span class="sxs-lookup"><span data-stu-id="f71d6-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="f71d6-122">Um componente do MED-V no host monitora a rede em busca dessas alterações e, em seguida, sinaliza o convidado da alteração.</span><span class="sxs-lookup"><span data-stu-id="f71d6-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="f71d6-123">Um componente no convidado cria uma instância do WMI para monitorar o espaço de trabalho do MED-V para essas alterações.</span><span class="sxs-lookup"><span data-stu-id="f71d6-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="f71d6-124">A assinatura de evento que você criou fornece uma notificação pelo sistema WMI quando uma ou mais dessas alterações de rede – ocorre a criação, modificação ou exclusão – ocorre.</span><span class="sxs-lookup"><span data-stu-id="f71d6-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="f71d6-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f71d6-125">Related topics</span></span>


[<span data-ttu-id="f71d6-126">Monitorar espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="f71d6-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="f71d6-127">Gerenciar configurações de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="f71d6-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





