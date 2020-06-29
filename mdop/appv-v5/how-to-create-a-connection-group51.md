---
title: Como criar um grupo de conexão
description: Como criar um grupo de conexão
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796473"
---
# <span data-ttu-id="3b900-103">Como criar um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="3b900-103">How to Create a Connection Group</span></span>


<span data-ttu-id="3b900-104">Use estas etapas para criar um grupo de conexão usando o console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="3b900-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="3b900-105">Para usar o PowerShell para criar grupos de conexão, consulte [como gerenciar grupos de conexão em um computador autônomo usando o PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="3b900-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span></span>

<span data-ttu-id="3b900-106">Quando você coloca pacotes em um grupo de conexão, os caminhos raiz do pacote são mesclados.</span><span class="sxs-lookup"><span data-stu-id="3b900-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="3b900-107">Se você remover pacotes, somente os pacotes restantes mantêm a raiz mesclada.</span><span class="sxs-lookup"><span data-stu-id="3b900-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="3b900-108">Para criar um grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="3b900-108">To create a connection group</span></span>**

1.  <span data-ttu-id="3b900-109">No console de gerenciamento do App-V 5,1, selecione **grupos de conexão** para exibir a biblioteca de grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="3b900-109">In the App-V 5.1 Management Console, select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

2.  <span data-ttu-id="3b900-110">Selecione **Adicionar grupo de conexão** para criar um novo grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="3b900-110">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

3.  <span data-ttu-id="3b900-111">No painel **novo grupo de conexão** , digite uma descrição para o grupo.</span><span class="sxs-lookup"><span data-stu-id="3b900-111">In the **New Connection Group** pane, type a description for the group.</span></span>

4.  <span data-ttu-id="3b900-112">Clique em **Editar** no painel **pacotes conectados** para adicionar um novo aplicativo ao grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="3b900-112">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

5.  <span data-ttu-id="3b900-113">No painel **pacotes e biblioteca inteira** , selecione o aplicativo a ser adicionado e clique na seta para adicionar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b900-113">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="3b900-114">Para remover um aplicativo, selecione o aplicativo a ser removido no painel **pacotes** e clique na seta.</span><span class="sxs-lookup"><span data-stu-id="3b900-114">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="3b900-115">Para repriorizar os aplicativos no seu grupo de conexão, use as setas no painel **pacotes no** painel.</span><span class="sxs-lookup"><span data-stu-id="3b900-115">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="3b900-116">**Importante**  Por padrão, as configurações de acesso dos serviços de domínio Active Directory associadas a um aplicativo específico não são adicionadas ao grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="3b900-116">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="3b900-117">Para transferir a configuração do acesso ao Active Directory, selecione **Adicionar acesso ao pacote ao acesso a grupo**, localizado no painel **pacotes no** painel.</span><span class="sxs-lookup"><span data-stu-id="3b900-117">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

6.  <span data-ttu-id="3b900-118">Após adicionar todos os aplicativos e configurar o acesso ao Active Directory, clique em **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="3b900-118">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="3b900-119">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="3b900-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3b900-120">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="3b900-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3b900-121">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="3b900-121">Got an App-V issue?</span></span>** <span data-ttu-id="3b900-122">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3b900-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3b900-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b900-123">Related topics</span></span>


[<span data-ttu-id="3b900-124">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3b900-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="3b900-125">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="3b900-125">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





