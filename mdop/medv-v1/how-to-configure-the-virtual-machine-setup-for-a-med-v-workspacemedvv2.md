---
title: Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V
description: Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799999"
---
# <span data-ttu-id="c4e78-103">Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c4e78-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="c4e78-104">Todas as configurações de configuração da máquina virtual são configuradas no módulo de **política** , na guia **configuração da VM** .</span><span class="sxs-lookup"><span data-stu-id="c4e78-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="c4e78-105">Como configurar a configuração da máquina virtual para um espaço de trabalho do MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="c4e78-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="c4e78-106">Para configurar a configuração de máquina virtual para um espaço de trabalho do MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="c4e78-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="c4e78-107">Clique em um espaço de trabalho do MED-V persistente para ser configurado.</span><span class="sxs-lookup"><span data-stu-id="c4e78-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="c4e78-108">Na seção **configuração de VM persistente** , configure as propriedades conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4e78-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="c4e78-109">Observação</span><span class="sxs-lookup"><span data-stu-id="c4e78-109">Note</span></span>**  
    <span data-ttu-id="c4e78-110">As propriedades de configuração de VM persistente são habilitadas somente para um espaço de trabalho do MED-V persistente.</span><span class="sxs-lookup"><span data-stu-id="c4e78-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="c4e78-111">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="c4e78-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="c4e78-112">Propriedades de configuração de VM persistente</span><span class="sxs-lookup"><span data-stu-id="c4e78-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c4e78-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c4e78-113">Property</span></span></th>
<th align="left"><span data-ttu-id="c4e78-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4e78-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4e78-115">Executar a configuração da VM</span><span class="sxs-lookup"><span data-stu-id="c4e78-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4e78-116">Marque esta caixa de seleção para executar um script de instalação na primeira vez em que o espaço de trabalho do MED-V for executado.</span><span class="sxs-lookup"><span data-stu-id="c4e78-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4e78-117">Editor de scripts</span><span class="sxs-lookup"><span data-stu-id="c4e78-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4e78-118">Clique em para configurar o script de instalação.</span><span class="sxs-lookup"><span data-stu-id="c4e78-118">Click to configure the setup script.</span></span> <span data-ttu-id="c4e78-119">Para obter mais informações, consulte <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> como configurar ações de script </a> .</span><span class="sxs-lookup"><span data-stu-id="c4e78-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c4e78-120">Observação</span><span class="sxs-lookup"><span data-stu-id="c4e78-120">Note</span></span></strong><br/><p><span data-ttu-id="c4e78-121">Esse botão estará habilitado apenas quando <strong> executar o script de configuração da VM </strong> estiver selecionado.</span><span class="sxs-lookup"><span data-stu-id="c4e78-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4e78-122">Mensagem exibida quando o script está em execução</span><span class="sxs-lookup"><span data-stu-id="c4e78-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4e78-123">Uma mensagem a ser exibida enquanto o script estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="c4e78-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="c4e78-124">Se deixado em branco, a mensagem padrão será exibida.</span><span class="sxs-lookup"><span data-stu-id="c4e78-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c4e78-125">Observação</span><span class="sxs-lookup"><span data-stu-id="c4e78-125">Note</span></span></strong><br/><p><span data-ttu-id="c4e78-126">Este campo é habilitado somente quando <strong> a opção executar o script de configuração da VM </strong> está marcada.</span><span class="sxs-lookup"><span data-stu-id="c4e78-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c4e78-127">Como configurar a configuração da máquina virtual para um espaço de trabalho do MED-V reversível</span><span class="sxs-lookup"><span data-stu-id="c4e78-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="c4e78-128">Para configurar a configuração de máquina virtual para um espaço de trabalho do MED-V reversível</span><span class="sxs-lookup"><span data-stu-id="c4e78-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="c4e78-129">Clique em um espaço de trabalho do MED-V reversível para configurar.</span><span class="sxs-lookup"><span data-stu-id="c4e78-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="c4e78-130">Na seção **configuração de VM reversível** , configure as propriedades conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4e78-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="c4e78-131">Observação</span><span class="sxs-lookup"><span data-stu-id="c4e78-131">Note</span></span>**  
    <span data-ttu-id="c4e78-132">As propriedades de configuração da VM reversível são habilitadas somente para um espaço de trabalho do MED-V reversível.</span><span class="sxs-lookup"><span data-stu-id="c4e78-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="c4e78-133">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="c4e78-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="c4e78-134">Propriedades de configuração de VM reversível</span><span class="sxs-lookup"><span data-stu-id="c4e78-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c4e78-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c4e78-135">Property</span></span></th>
<th align="left"><span data-ttu-id="c4e78-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4e78-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4e78-137">Renomear a VM com base no padrão de nome do computador</span><span class="sxs-lookup"><span data-stu-id="c4e78-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4e78-138">Marque esta caixa de seleção para atribuir um nome exclusivo a cada computador usando o espaço de trabalho do MED-V para que você possa diferenciar vários computadores usando o mesmo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="c4e78-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="c4e78-139">Para obter mais informações sobre como configurar nomes de imagem de computador, consulte <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> como configurar propriedades do padrão de nome do computador VM </a> .</span><span class="sxs-lookup"><span data-stu-id="c4e78-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c4e78-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4e78-140">Related topics</span></span>


[<span data-ttu-id="c4e78-141">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="c4e78-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="c4e78-142">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="c4e78-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="c4e78-143">Exemplos de configurações de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c4e78-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









