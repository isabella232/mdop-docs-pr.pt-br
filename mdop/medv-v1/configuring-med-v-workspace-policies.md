---
title: Configurando políticas de espaço de trabalho do MED-V
description: Configurando políticas de espaço de trabalho do MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799556"
---
# <span data-ttu-id="c9ee6-103">Configurando políticas de espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="c9ee6-104">Uma política de espaço de trabalho do MED-V é um grupo de configurações configuráveis que definem como o ambiente virtualizado e os aplicativos são executados no computador host.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="c9ee6-105">Os tópicos desta seção descrevem todas as configurações configuráveis na política de espaço de trabalho do MED-V, bem como as configurações que influenciam o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="c9ee6-106">Os seguintes tipos de espaço de trabalho do MED-V estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="c9ee6-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="c9ee6-107">**Persistente**– em um espaço de trabalho do MED-v persistente, todas as alterações e inclusões feitas pelo usuário no espaço de trabalho do MED-v são salvas no espaço de trabalho do MED-v entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="c9ee6-108">Além disso, um espaço de trabalho do MED-V persistente geralmente é usado em um ambiente de domínio.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="c9ee6-109">**Reversível**— em um espaço de trabalho do MED-v reversível, na conclusão de cada sessão (ou seja, quando o espaço de trabalho do MED-v é interrompido), o espaço de trabalho do MED-v é revertido ao seu estado original durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="c9ee6-110">Nenhuma alteração ou acréscimo feita pelo usuário é salva no espaço de trabalho do MED-V entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="c9ee6-111">Um espaço de trabalho do MED-V reversível não pode ser usado em um ambiente de domínio.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="c9ee6-112">É importante decidir o tipo de espaço de trabalho do MED-V que você está criando antes de implantar o espaço de trabalho do MED-V, porque não é recomendável reconfigurar o tipo de espaço de trabalho do MED-v após a implantação de uma política para os usuários.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="c9ee6-113">**Observação**  Ao configurar uma política, um símbolo de aviso é exibido ao lado de campos obrigatórios que não estão preenchidos.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="c9ee6-114">Se um campo obrigatório não for preenchido, o símbolo também será exibido na guia.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="c9ee6-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c9ee6-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="c9ee6-116">Como aplicar configurações gerais a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="c9ee6-117">Descreve as configurações gerais de um espaço de trabalho do MED-V e como aplicá-las a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="c9ee6-118">Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="c9ee6-119">Descreve as configurações da máquina virtual para um espaço de trabalho do MED-V e como aplicá-las a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="c9ee6-120">Como configurar um usuário ou grupo de domínio</span><span class="sxs-lookup"><span data-stu-id="c9ee6-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="c9ee6-121">Descreve como configurar usuários e grupos de domínio.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="c9ee6-122">Como configurar aplicativos publicados</span><span class="sxs-lookup"><span data-stu-id="c9ee6-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="c9ee6-123">Descreve os aplicativos e menus publicados e como aplicá-los a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="c9ee6-124">Como definir as configurações da Web de um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="c9ee6-125">Descreve as configurações da Web disponíveis para um espaço de trabalho do MED-V e como aplicá-las a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="c9ee6-126">Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="c9ee6-127">Descreve a configuração de máquina virtual para um espaço de trabalho do MED-V e como aplicá-lo a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="c9ee6-128">Como aplicar as configurações de rede a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="c9ee6-129">Descreve as configurações de rede de um espaço de trabalho do MED-V e como aplicá-las a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="c9ee6-130">Como aplicar as configurações de desempenho a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c9ee6-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="c9ee6-131">Descreve as configurações de desempenho de um espaço de trabalho do MED-V e como aplicá-las a uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="c9ee6-132">Como importar e exportar uma política</span><span class="sxs-lookup"><span data-stu-id="c9ee6-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="c9ee6-133">Descreve como importar e exportar uma política.</span><span class="sxs-lookup"><span data-stu-id="c9ee6-133">Describes how to import and export a policy.</span></span>

 

 





