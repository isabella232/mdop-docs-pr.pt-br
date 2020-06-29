---
title: Criando um espaço de trabalho do MED-V
description: Criando um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799557"
---
# <span data-ttu-id="1a498-103">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="1a498-104">Um espaço de trabalho do MED-V é o ambiente da área de trabalho no qual os usuários finais interagem com a máquina virtual fornecida pelo MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a498-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="1a498-105">O espaço de trabalho do MED-V é criado e personalizado pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="1a498-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="1a498-106">Ele consiste em uma imagem e a política, que define as regras e a funcionalidade do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a498-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="1a498-107">Vários espaços de trabalho do MED-V podem ser criados, cada um personalizado com sua própria configuração, configurações e regras.</span><span class="sxs-lookup"><span data-stu-id="1a498-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="1a498-108">Um usuário, grupo ou vários usuários ou grupos podem ser associados a cada espaço de trabalho do MED-V, tornando o espaço de trabalho do MED-V disponível somente para os computadores dos usuários ou grupos associados.</span><span class="sxs-lookup"><span data-stu-id="1a498-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="1a498-109">Como adicionar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="1a498-110">Para adicionar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="1a498-111">Clique no botão gerenciamento de **políticas** para abrir o módulo de **política** .</span><span class="sxs-lookup"><span data-stu-id="1a498-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="1a498-112">O módulo de **política** consiste no menu de **espaços de trabalho** à esquerda e na guia **geral**, **máquina virtual**, **implantação**, **aplicativos**, **Web**, **configuração de VM**, **rede**e **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="1a498-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="1a498-113">No menu **política** , selecione **novo espaço de trabalho**ou clique em **Adicionar** para criar um novo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a498-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="1a498-114">Na guia **geral** , no campo **nome** , insira o nome do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a498-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="1a498-115">No campo **Descrição** , insira uma descrição para o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a498-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="1a498-116">No campo **informações de contato de suporte** , insira as informações de contato do suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="1a498-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="1a498-117">Para obter mais informações sobre como configurar um espaço de trabalho do MED-V, consulte [Configurando políticas do espaço de trabalho do MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1a498-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="1a498-118">Como clonar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="1a498-119">Um espaço de trabalho do MED-V pode ser clonado para que você possa criar um espaço de trabalho do MED-v idêntico a um espaço de trabalho do MED-V existente.</span><span class="sxs-lookup"><span data-stu-id="1a498-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="1a498-120">Para clonar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="1a498-121">Clique no espaço de trabalho do MED-V para clonar.</span><span class="sxs-lookup"><span data-stu-id="1a498-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="1a498-122">No menu **política** , selecione **clonar espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="1a498-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="1a498-123">Um novo espaço de trabalho do MED-V é criado com o nome &lt; original do espaço de trabalho do MED-v original &gt; -2.</span><span class="sxs-lookup"><span data-stu-id="1a498-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="1a498-124">Como excluir um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="1a498-125">Para excluir um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="1a498-126">No módulo de **política** , enquanto o painel espaço de trabalho está em foco, clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="1a498-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="1a498-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a498-127">Related topics</span></span>


[<span data-ttu-id="1a498-128">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="1a498-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





