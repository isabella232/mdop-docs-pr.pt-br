---
title: Como aplicar as configurações de rede a um espaço de trabalho do MED-V
description: Como aplicar as configurações de rede a um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799888"
---
# <span data-ttu-id="0bb57-103">Como aplicar as configurações de rede a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="0bb57-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="0bb57-104">Os administradores podem definir as configurações de rede para cada espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0bb57-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="0bb57-105">Todas as configurações de rede são configuradas no módulo de **política** , na guia **rede** .</span><span class="sxs-lookup"><span data-stu-id="0bb57-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="0bb57-106">Para aplicar as configurações de rede a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="0bb57-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="0bb57-107">Clique no espaço de trabalho do MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="0bb57-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="0bb57-108">No painel **rede** , defina as configurações conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0bb57-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="0bb57-109">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="0bb57-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="0bb57-110">Propriedades da rede do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="0bb57-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0bb57-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0bb57-111">Property</span></span></th>
<th align="left"><span data-ttu-id="0bb57-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bb57-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0bb57-113">Propriedades de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="0bb57-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="0bb57-114">Usar o endereço IP do host (NAT) </strong> — o espaço de trabalho usará o NAT para compartilhar o IP do host para o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="0bb57-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="0bb57-115">Use um endereço IP diferente do host (ponte) </strong> — o espaço de trabalho do MED-V terá seu próprio endereço de rede, geralmente obtido via DHCP.</span><span class="sxs-lookup"><span data-stu-id="0bb57-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="0bb57-116">Marque a <strong> caixa de seleção mapear vários adaptadores para espaço </strong> de trabalho quando o computador host tiver vários adaptadores.</span><span class="sxs-lookup"><span data-stu-id="0bb57-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="0bb57-117">É recomendável usar essa configuração quando o host se mover entre diferentes redes usando adaptadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="0bb57-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0bb57-118">Servidor DNS</span><span class="sxs-lookup"><span data-stu-id="0bb57-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="0bb57-119">Não alterar </strong> — as configurações de DNS definidas na máquina virtual do espaço de trabalho do MED-V não serão alteradas.</span><span class="sxs-lookup"><span data-stu-id="0bb57-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="0bb57-120">Usar o endereço DNS do host </strong> — as configurações de DNS do espaço de trabalho do MED-V serão sincronizadas para corresponder às configurações do host.</span><span class="sxs-lookup"><span data-stu-id="0bb57-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="0bb57-121">A sincronização de DNS é dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0bb57-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="0bb57-122">Ele é sincronizado periodicamente com o host, de forma que, se ele for alterado no host, será alterado dinamicamente no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0bb57-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="0bb57-123">Use endereços DNS específicos </strong> — o espaço de trabalho do MED-V usará um DNS específico, conforme especificado.</span><span class="sxs-lookup"><span data-stu-id="0bb57-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="0bb57-124">Nos <strong> campos principal </strong> e <strong> secundário </strong> , insira os endereços DNS primário e secundário.</span><span class="sxs-lookup"><span data-stu-id="0bb57-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="0bb57-125">Marque a <strong> caixa de seleção endereços de DNS do host de acréscimo </strong> para acrescentar o host aos endereços DNS configurados.</span><span class="sxs-lookup"><span data-stu-id="0bb57-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0bb57-126">Atribuir sufixos DNS</span><span class="sxs-lookup"><span data-stu-id="0bb57-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="0bb57-127">Atribuir os seguintes sufixos </strong> : Marque esta caixa de seleção para atribuir sufixos DNS específicos; na caixa, insira um sufixo ou vários sufixos separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0bb57-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="0bb57-128">Acrescentar sufixos </strong> de host — Marque essa caixa de seleção para acrescentar os sufixos de host ao endereço DNS.</span><span class="sxs-lookup"><span data-stu-id="0bb57-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0bb57-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bb57-129">Related topics</span></span>


[<span data-ttu-id="0bb57-130">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="0bb57-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="0bb57-131">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="0bb57-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





