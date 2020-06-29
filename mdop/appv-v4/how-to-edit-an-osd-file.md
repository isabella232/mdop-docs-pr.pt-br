---
title: Como editar um arquivo OSD
description: Como editar um arquivo OSD
author: dansimp
ms.assetid: 0d126ba7-72fb-42ce-982e-90ed01a852c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a0ff4a8efe1fa177f6847c344add94bca3648cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797125"
---
# <span data-ttu-id="f93ab-103">Como editar um arquivo OSD</span><span class="sxs-lookup"><span data-stu-id="f93ab-103">How to Edit an OSD File</span></span>


<span data-ttu-id="f93ab-104">Use os procedimentos a seguir para modificar o arquivo Open Software Descriptor (OSD) do pacote de aplicativo sequenciado adicionando ou excluindo um elemento ou um atributo.</span><span class="sxs-lookup"><span data-stu-id="f93ab-104">Use the following procedures to modify a sequenced application package's Open Software Descriptor (OSD) file by adding or deleting an element or an attribute.</span></span>

<span data-ttu-id="f93ab-105">**Observação**  Alguns elementos não têm um atributo, portanto, não é possível adicionar um atributo para todos os elementos.</span><span class="sxs-lookup"><span data-stu-id="f93ab-105">**Note** Some elements do not have an attribute, so it is not possible to add an attribute to every element.</span></span>

 

<span data-ttu-id="f93ab-106">**Importante**  Se você usar o editor OSD para alterar o nome do arquivo. SFT, o atributo HREF do elemento CODEBASE no arquivo OSD, você deve usar o comando **salvar como** para salvar a alteração nos arquivos do projeto.</span><span class="sxs-lookup"><span data-stu-id="f93ab-106">**Important** If you use the OSD editor to change the .sft file name, the HREF attribute of the CODEBASE element in the OSD file, you must use the **Save As** command to save the change to the project files.</span></span>

 

**<span data-ttu-id="f93ab-107">Para adicionar um elemento</span><span class="sxs-lookup"><span data-stu-id="f93ab-107">To add an element</span></span>**

1.  <span data-ttu-id="f93ab-108">Clique na guia **arquivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="f93ab-108">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="f93ab-109">No painel de navegação, selecione o arquivo OSD do pacote do aplicativo sequenciado que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="f93ab-109">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="f93ab-110">No painel de navegação, clique com o botão direito do mouse no elemento que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="f93ab-110">In the navigation pane, right-click the element that you want to modify.</span></span> <span data-ttu-id="f93ab-111">No menu, selecione **elemento** e selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-111">On the menu, select **Element** and select **Add**.</span></span>

4.  <span data-ttu-id="f93ab-112">No menu, selecione o elemento que você deseja adicionar, por exemplo, **codebase**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-112">From the menu, select the element you want to add—for example, **Codebase**.</span></span>

5.  <span data-ttu-id="f93ab-113">No menu **arquivo** , selecione **salvar**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-113">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="f93ab-114">Para excluir um elemento</span><span class="sxs-lookup"><span data-stu-id="f93ab-114">To delete an element</span></span>**

1.  <span data-ttu-id="f93ab-115">Clique na guia **arquivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="f93ab-115">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="f93ab-116">No painel de navegação, selecione o arquivo OSD do pacote do aplicativo sequenciado que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="f93ab-116">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="f93ab-117">No painel de navegação, clique com o botão direito do mouse no elemento que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="f93ab-117">In the navigation pane, right-click the element that you want to delete.</span></span> <span data-ttu-id="f93ab-118">No menu, selecione **elemento** e escolha **excluir**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-118">On the menu, select **Element** and select **Delete**.</span></span>

4.  <span data-ttu-id="f93ab-119">No menu **arquivo** , selecione **salvar**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-119">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="f93ab-120">Para adicionar um atributo</span><span class="sxs-lookup"><span data-stu-id="f93ab-120">To add an attribute</span></span>**

1.  <span data-ttu-id="f93ab-121">Clique na guia **arquivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="f93ab-121">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="f93ab-122">No painel de navegação, selecione o arquivo OSD do pacote do aplicativo sequenciado que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="f93ab-122">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="f93ab-123">No painel esquerdo, clique com o botão direito do mouse no elemento ao qual você deseja adicionar um atributo.</span><span class="sxs-lookup"><span data-stu-id="f93ab-123">In the left pane, right-click the element to which you want to add an attribute.</span></span> <span data-ttu-id="f93ab-124">No menu, selecione **atributo** e selecione **Adicionar**, escolha dos atributos disponíveis listados.</span><span class="sxs-lookup"><span data-stu-id="f93ab-124">On the menu, select **Attribute** and select **Add**, choosing from the listed available attributes.</span></span>

4.  <span data-ttu-id="f93ab-125">No menu **arquivo** , selecione **salvar**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-125">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="f93ab-126">Para excluir um atributo</span><span class="sxs-lookup"><span data-stu-id="f93ab-126">To delete an attribute</span></span>**

1.  <span data-ttu-id="f93ab-127">Clique na guia **arquivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="f93ab-127">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="f93ab-128">No painel de navegação, selecione o arquivo OSD do pacote do aplicativo sequenciado que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="f93ab-128">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="f93ab-129">No painel de navegação, clique com o botão direito do mouse no elemento do qual você deseja excluir um atributo.</span><span class="sxs-lookup"><span data-stu-id="f93ab-129">In the navigation pane, right-click the element from which you want to delete an attribute.</span></span> <span data-ttu-id="f93ab-130">No menu, selecione **atributo** e, em seguida, selecione **excluir**, escolha o atributo que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="f93ab-130">On the menu, select **Attribute** and then select **Delete**, choosing the attribute you wish to delete.</span></span>

4.  <span data-ttu-id="f93ab-131">No menu **arquivo** , selecione **salvar**.</span><span class="sxs-lookup"><span data-stu-id="f93ab-131">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="f93ab-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f93ab-132">Related topics</span></span>


[<span data-ttu-id="f93ab-133">Sobre a guia OSD</span><span class="sxs-lookup"><span data-stu-id="f93ab-133">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="f93ab-134">Como editar um arquivo OSD usando um editor de texto</span><span class="sxs-lookup"><span data-stu-id="f93ab-134">How to Edit an OSD File Using a Text Editor</span></span>](how-to-edit-an-osd-file-using-a-text-editor.md)

[<span data-ttu-id="f93ab-135">Elementos de arquivo OSD</span><span class="sxs-lookup"><span data-stu-id="f93ab-135">OSD File Elements</span></span>](osd-file-elements.md)

[<span data-ttu-id="f93ab-136">Console do Sequencer</span><span class="sxs-lookup"><span data-stu-id="f93ab-136">Sequencer Console</span></span>](sequencer-console.md)

 

 





