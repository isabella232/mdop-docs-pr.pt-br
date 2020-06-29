---
title: Exemplos de configurações de máquina virtual
description: Exemplos de configurações de máquina virtual
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799502"
---
# <span data-ttu-id="b8440-103">Exemplos de configurações de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b8440-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="b8440-104">Veja a seguir exemplos de configurações típicas da máquina virtual: uma em um espaço de trabalho do MED-V persistente e uma em um espaço de trabalho do MED-V reversível.</span><span class="sxs-lookup"><span data-stu-id="b8440-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="b8440-105">**Observação**  Esses exemplos não são destinados ao uso em todos os ambientes.</span><span class="sxs-lookup"><span data-stu-id="b8440-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="b8440-106">Ajuste a configuração de acordo com seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="b8440-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="b8440-107">Para configurar uma configuração de domínio típica em um espaço de trabalho do MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="b8440-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="b8440-108">Configure o Sysprep na imagem base para criar um SID exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b8440-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="b8440-109">Para obter mais informações, consulte [criando uma imagem do Virtual PC para o MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span><span class="sxs-lookup"><span data-stu-id="b8440-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="b8440-110">Na guia **configuração da VM** , marque a caixa de seleção **executar configuração da VM** .</span><span class="sxs-lookup"><span data-stu-id="b8440-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="b8440-111">Na seção **padrão de nome de computador da VM** , configure o padrão para o nome da imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="b8440-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="b8440-112">Para obter mais informações, consulte [como configurar as propriedades do padrão de nome do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8440-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="b8440-113">Clique em **Editor de script**e, na caixa de diálogo Editor de script de configuração da **VM** , configure as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="b8440-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="b8440-114">Renomear computador</span><span class="sxs-lookup"><span data-stu-id="b8440-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="b8440-115">Reiniciar o Windows</span><span class="sxs-lookup"><span data-stu-id="b8440-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="b8440-116">Verificar a conectividade</span><span class="sxs-lookup"><span data-stu-id="b8440-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="b8440-117">Ingressar no domínio</span><span class="sxs-lookup"><span data-stu-id="b8440-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="b8440-118">Desabilitar logon automático</span><span class="sxs-lookup"><span data-stu-id="b8440-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="b8440-119">Para obter mais informações, consulte [como configurar ações de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b8440-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="b8440-120">No menu **política** , clique em **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="b8440-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="b8440-121">Para configurar uma configuração típica em um espaço de trabalho reversível</span><span class="sxs-lookup"><span data-stu-id="b8440-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="b8440-122">Na guia **configuração da VM** , marque a caixa de seleção **renomear a VM com base no padrão de nome do computador** .</span><span class="sxs-lookup"><span data-stu-id="b8440-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="b8440-123">Na seção **padrão de nome de computador da VM** , configure o padrão para o nome da imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="b8440-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="b8440-124">Para obter mais informações, consulte [como configurar as propriedades do padrão de nome do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8440-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="b8440-125">No menu **política** , clique em **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="b8440-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="b8440-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8440-126">Related topics</span></span>


[<span data-ttu-id="b8440-127">Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="b8440-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="b8440-128">Como configurar as propriedades de padrão de nomes do computador VM</span><span class="sxs-lookup"><span data-stu-id="b8440-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="b8440-129">Como configurar ações de script</span><span class="sxs-lookup"><span data-stu-id="b8440-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





