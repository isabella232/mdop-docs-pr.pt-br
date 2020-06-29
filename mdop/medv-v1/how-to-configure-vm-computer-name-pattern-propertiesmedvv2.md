---
title: Como configurar as propriedades de padrão de nomes do computador VM
description: Como configurar as propriedades de padrão de nomes do computador VM
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800000"
---
# <span data-ttu-id="7d311-103">Como configurar as propriedades de padrão de nomes do computador VM</span><span class="sxs-lookup"><span data-stu-id="7d311-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="7d311-104">Um padrão de nome de computador de máquina virtual pode ser atribuído para os espaços de trabalho reversível e para os espaços de trabalho do MED-V persistentes.</span><span class="sxs-lookup"><span data-stu-id="7d311-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="7d311-105">Reversível — os administradores podem atribuir um nome exclusivo a cada instância reversível do espaço de trabalho do MED-V para diferenciar entre vários computadores usando o mesmo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d311-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="7d311-106">Persistente – em um espaço de trabalho do MED-V persistente, os administradores podem definir um computador para ser renomeado durante um script de instalação.</span><span class="sxs-lookup"><span data-stu-id="7d311-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="7d311-107">Como atribuir um padrão de nome de computador de máquina virtual a um espaço de trabalho do MED-V reversível</span><span class="sxs-lookup"><span data-stu-id="7d311-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="7d311-108">Para atribuir um padrão de nome de computador de máquina virtual a um espaço de trabalho do MED-V reversível</span><span class="sxs-lookup"><span data-stu-id="7d311-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="7d311-109">Clique no espaço de trabalho do MED-V reversível para configurar.</span><span class="sxs-lookup"><span data-stu-id="7d311-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="7d311-110">Na seção **configuração de VM reversível** , marque a caixa de seleção **renomear a VM com base no padrão de nome do computador** .</span><span class="sxs-lookup"><span data-stu-id="7d311-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="7d311-111">Na seção **máquina de nome do computador VM** , digite o padrão a ser usado para nomear imagens da máquina virtual, usando as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7d311-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="7d311-112">**Constante**— Insira um texto livre que será constante em todos os computadores usando o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d311-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="7d311-113">**Variável**— Insira uma variável clicando em **Inserir variável**e selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7d311-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="7d311-114">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="7d311-114">User name</span></span>**

        -   **<span data-ttu-id="7d311-115">Nome do domínio</span><span class="sxs-lookup"><span data-stu-id="7d311-115">Domain name</span></span>**

        -   **<span data-ttu-id="7d311-116">Nome do host</span><span class="sxs-lookup"><span data-stu-id="7d311-116">Host name</span></span>**

        -   **<span data-ttu-id="7d311-117">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="7d311-117">Workspace name</span></span>**

        -   **<span data-ttu-id="7d311-118">Nome da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7d311-118">Virtual machine name</span></span>**

        <span data-ttu-id="7d311-119">A variável selecionada será específica do computador usando o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d311-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="7d311-120">Por exemplo, se o **nome do domínio** for selecionado, o nome exclusivo de cada computador incluirá o nome de domínio do computador.</span><span class="sxs-lookup"><span data-stu-id="7d311-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="7d311-121">**Caracteres aleatórios**— insira "\ #" para cada caractere aleatório a ser incluído no padrão.</span><span class="sxs-lookup"><span data-stu-id="7d311-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="7d311-122">Cada computador que usa o espaço de trabalho do MED-V terá um sufixo do comprimento especificado, que é gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="7d311-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="7d311-123">Observação</span><span class="sxs-lookup"><span data-stu-id="7d311-123">Note</span></span>**  
    <span data-ttu-id="7d311-124">O nome do computador tem um limite de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d311-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="7d311-125">Se o padrão exceder o limite, ele será truncado.</span><span class="sxs-lookup"><span data-stu-id="7d311-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="7d311-126">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7d311-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="7d311-127">Observação</span><span class="sxs-lookup"><span data-stu-id="7d311-127">Note</span></span>**  
    <span data-ttu-id="7d311-128">Um padrão de nome de computador VM reversível pode ser atribuído somente quando você **renomeia a VM com base nos padrões de nome de computador** (na seção **configuração de VM reversível** ) está marcada.</span><span class="sxs-lookup"><span data-stu-id="7d311-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="7d311-129">Como atribuir um padrão de nome de computador virtual a um espaço de trabalho do MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="7d311-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="7d311-130">Para atribuir um padrão de nome de computador de máquina virtual a um espaço de trabalho do MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="7d311-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="7d311-131">Clique no espaço de trabalho persistente do MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="7d311-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="7d311-132">Na seção **configuração de VM persistente** , clique em **Editor de script**.</span><span class="sxs-lookup"><span data-stu-id="7d311-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="7d311-133">Na caixa de diálogo **ações de script** , clique em **Adicionar**e, no submenu, clique em **renomear computador**.</span><span class="sxs-lookup"><span data-stu-id="7d311-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="7d311-134">Clique em **OK** para fechar a caixa de diálogo **ações de script** .</span><span class="sxs-lookup"><span data-stu-id="7d311-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="7d311-135">Na guia **configuração da VM** , na seção **padrão de nome do computador VM** , digite o padrão a ser usado para renomear o computador, usando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7d311-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="7d311-136">**Constante**— Insira um texto livre que será incluído no nome do computador.</span><span class="sxs-lookup"><span data-stu-id="7d311-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="7d311-137">**Variável**— Insira uma variável clicando em **Inserir variável**e selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7d311-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="7d311-138">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="7d311-138">User name</span></span>**

        -   **<span data-ttu-id="7d311-139">Nome do domínio</span><span class="sxs-lookup"><span data-stu-id="7d311-139">Domain name</span></span>**

        -   **<span data-ttu-id="7d311-140">Nome do host</span><span class="sxs-lookup"><span data-stu-id="7d311-140">Host name</span></span>**

        -   **<span data-ttu-id="7d311-141">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="7d311-141">Workspace name</span></span>**

        -   **<span data-ttu-id="7d311-142">Nome da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7d311-142">Virtual machine name</span></span>**

        <span data-ttu-id="7d311-143">A variável selecionada será específica para o computador que está sendo renomeado.</span><span class="sxs-lookup"><span data-stu-id="7d311-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="7d311-144">Por exemplo, se o **nome do domínio** estiver selecionado, o nome do computador incluirá o nome de domínio do computador.</span><span class="sxs-lookup"><span data-stu-id="7d311-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="7d311-145">**Caracteres aleatórios**— insira "\ #" para cada caractere aleatório a ser incluído no padrão.</span><span class="sxs-lookup"><span data-stu-id="7d311-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="7d311-146">O computador terá um sufixo do comprimento especificado, que é gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="7d311-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="7d311-147">Observação</span><span class="sxs-lookup"><span data-stu-id="7d311-147">Note</span></span>**  
    <span data-ttu-id="7d311-148">O nome do computador tem um limite de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d311-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="7d311-149">Se o padrão exceder o limite, ele será truncado.</span><span class="sxs-lookup"><span data-stu-id="7d311-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="7d311-150">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7d311-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="7d311-151">Observação</span><span class="sxs-lookup"><span data-stu-id="7d311-151">Note</span></span>**  
    <span data-ttu-id="7d311-152">O computador será renomeado somente se for definido como uma ação na caixa de diálogo **ações de script** .</span><span class="sxs-lookup"><span data-stu-id="7d311-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="7d311-153">Para obter informações detalhadas, consulte [como configurar ações de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7d311-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="7d311-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d311-154">Related topics</span></span>


[<span data-ttu-id="7d311-155">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="7d311-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="7d311-156">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="7d311-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="7d311-157">Como configurar ações de script</span><span class="sxs-lookup"><span data-stu-id="7d311-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="7d311-158">Exemplos de configurações de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7d311-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









