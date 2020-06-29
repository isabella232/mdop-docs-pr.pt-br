---
title: Como iniciar, parar e reiniciar um espaço de trabalho do MED-V
description: Como iniciar, parar e reiniciar um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799729"
---
# <span data-ttu-id="36196-103">Como iniciar, parar e reiniciar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="36196-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="36196-104">Para iniciar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="36196-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="36196-105">Na área de notificação, clique com o botão direito do mouse no ícone do MED-V.</span><span class="sxs-lookup"><span data-stu-id="36196-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="36196-106">No submenu, clique em **Iniciar espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="36196-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="36196-107">Se houver vários espaços de trabalho do MED-V em execução no computador, a janela de **seleção do espaço de trabalho** será exibida.</span><span class="sxs-lookup"><span data-stu-id="36196-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="36196-108">Selecione um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="36196-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="36196-109">Marque a caixa de seleção **iniciar o espaço de trabalho selecionado sem me perguntar** para ignorar esta janela da próxima vez que o cliente for iniciado e para abrir automaticamente o espaço de trabalho do MED-V selecionado.</span><span class="sxs-lookup"><span data-stu-id="36196-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="36196-110">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="36196-110">Click **OK**.</span></span>

    <span data-ttu-id="36196-111">A janela **autenticação do espaço de trabalho inicial** é exibida.</span><span class="sxs-lookup"><span data-stu-id="36196-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="36196-112">Se houver vários espaços de trabalho do MED-V no computador e se você tiver optado por usar um espaço de trabalho do MED-V especificado, a janela mostrada na figura a seguir será exibida.</span><span class="sxs-lookup"><span data-stu-id="36196-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="36196-113">Se houver apenas um espaço de trabalho do MED-V no computador, a opção "Iniciar último espaço de trabalho usado" não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="36196-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="36196-114">Digite suas credenciais de usuário do domínio.</span><span class="sxs-lookup"><span data-stu-id="36196-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="36196-115">**Observação**  Na primeira vez que um espaço de trabalho do MED-V for iniciado, o nome do usuário deve estar no seguinte formato: &lt; nome de usuário do nome do domínio &gt; \\ &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="36196-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="36196-116">Selecione **salvar minha senha** para salvar sua senha entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="36196-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="36196-117">**Observação**  Para habilitar o recurso salvar senha, o atributo EnableSavePassword deve ser definido como true no arquivo ClientSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="36196-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="36196-118">O arquivo pode ser encontrado na pasta *Servers\\Configuration Server\\* .</span><span class="sxs-lookup"><span data-stu-id="36196-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="36196-119">Desmarque a caixa de seleção **Iniciar último espaço de trabalho usado** para escolher um espaço de trabalho do MED-V diferente.</span><span class="sxs-lookup"><span data-stu-id="36196-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="36196-120">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="36196-120">Click **OK**.</span></span>

    <span data-ttu-id="36196-121">Várias telas de status aparecem dependendo da configuração do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="36196-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="36196-122">A tela **inicial do espaço de trabalho** é exibida.</span><span class="sxs-lookup"><span data-stu-id="36196-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="36196-123">Para reiniciar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="36196-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="36196-124">Quando o cliente estiver em execução, na área de notificação, clique com o botão direito do mouse no ícone do MED-V.</span><span class="sxs-lookup"><span data-stu-id="36196-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="36196-125">No submenu, clique em **reiniciar espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="36196-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="36196-126">O espaço de trabalho do MED-V é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="36196-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="36196-127">Em um espaço de trabalho do MED-V persistente, a máquina virtual é desligada e reiniciada.</span><span class="sxs-lookup"><span data-stu-id="36196-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="36196-128">Em um espaço de trabalho do MED-V reversível, a máquina virtual não desliga realmente; em vez disso, ele retorna ao seu estado original.</span><span class="sxs-lookup"><span data-stu-id="36196-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="36196-129">Para parar um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="36196-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="36196-130">Na área de notificação, clique com o botão direito do mouse no ícone do MED-V.</span><span class="sxs-lookup"><span data-stu-id="36196-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="36196-131">No submenu, clique em **parar espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="36196-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="36196-132">O espaço de trabalho do MED-V é interrompido.</span><span class="sxs-lookup"><span data-stu-id="36196-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="36196-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36196-133">Related topics</span></span>


[<span data-ttu-id="36196-134">Como iniciar e fechar o cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="36196-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 





