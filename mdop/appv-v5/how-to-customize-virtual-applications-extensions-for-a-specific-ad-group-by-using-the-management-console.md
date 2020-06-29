---
title: Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento
description: Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento
author: dansimp
ms.assetid: 4f249ee3-cc2d-4b1e-afe5-d1cbf9cabd88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57ce4b82cc552e0a4adc2272f849111d8da0be71
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796453"
---
# <span data-ttu-id="2530a-103">Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2530a-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="2530a-104">Use o procedimento a seguir para personalizar as extensões de aplicativo virtual para um grupo do Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="2530a-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="2530a-105">Para personalizar extensões de aplicativos virtuais para um grupo de anúncios</span><span class="sxs-lookup"><span data-stu-id="2530a-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="2530a-106">Para exibir o pacote que você deseja configurar, abra o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2530a-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="2530a-107">Para exibir a configuração atribuída a um determinado grupo de usuários, selecione o pacote e clique com o botão direito do mouse no nome do pacote e selecione **Editar acesso ao Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="2530a-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="2530a-108">Ou, se preferir, selecione o pacote e clique em **Editar** no painel **acesso ao anúncio** .</span><span class="sxs-lookup"><span data-stu-id="2530a-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="2530a-109">Para personalizar um grupo do AD, você pode encontrar o grupo na lista de **entidades do anúncio com o Access**.</span><span class="sxs-lookup"><span data-stu-id="2530a-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="2530a-110">Em seguida, usando a caixa suspensa no painel de **configuração atribuído** , selecione **personalizado**e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="2530a-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="2530a-111">Para desabilitar todas as extensões para um determinado aplicativo, desmarque **habilitar**.</span><span class="sxs-lookup"><span data-stu-id="2530a-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="2530a-112">Para adicionar um novo atalho para o aplicativo selecionado, clique com o botão direito do mouse no aplicativo no painel **atalhos** e selecione **Adicionar novo atalho**.</span><span class="sxs-lookup"><span data-stu-id="2530a-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="2530a-113">Para remover um atalho, clique com o botão direito do mouse no aplicativo no painel **atalhos** e selecione **remover atalho**.</span><span class="sxs-lookup"><span data-stu-id="2530a-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="2530a-114">Para editar um atalho existente, clique com o botão direito do mouse no aplicativo e selecione **Editar atalho**.</span><span class="sxs-lookup"><span data-stu-id="2530a-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="2530a-115">Para exibir outras extensões de aplicativo, clique em **avançado**e em **Exportar configuração**.</span><span class="sxs-lookup"><span data-stu-id="2530a-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="2530a-116">Digite um nome de arquivo e clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="2530a-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="2530a-117">Você pode exibir todas as extensões de aplicativo associadas ao pacote usando o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="2530a-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="2530a-118">Para editar extensões de aplicativo adicionais, modifique o arquivo de configuração e clique em **importar e substitua essa configuração**.</span><span class="sxs-lookup"><span data-stu-id="2530a-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="2530a-119">Selecione o arquivo modificado e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="2530a-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="2530a-120">Na caixa de diálogo, clique em **substituir** para concluir o processo.</span><span class="sxs-lookup"><span data-stu-id="2530a-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="2530a-121">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="2530a-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2530a-122">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="2530a-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2530a-123">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="2530a-123">Got an App-V issue?</span></span>** <span data-ttu-id="2530a-124">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2530a-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2530a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2530a-125">Related topics</span></span>


[<span data-ttu-id="2530a-126">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2530a-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





