---
title: Como publicar um pacote usando o Console de Gerenciamento
description: Como publicar um pacote usando o Console de Gerenciamento
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796336"
---
# <span data-ttu-id="6ef7e-103">Como publicar um pacote usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6ef7e-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="6ef7e-104">Use o procedimento a seguir para publicar um pacote do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="6ef7e-105">Depois que você publica um pacote, os computadores que executam o cliente App-V 5,0 podem acessar e executar os aplicativos nesse pacote.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="6ef7e-106">**Observação**  A capacidade de habilitar somente os administradores para publicar ou cancelar a publicação de pacotes (descritos abaixo) tem suporte a partir do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="6ef7e-107">Para publicar um pacote do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6ef7e-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="6ef7e-108">No console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="6ef7e-109">Clique com o botão direito do mouse no nome do pacote a ser publicado e selecione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="6ef7e-110">Examine a coluna **status** para verificar se o pacote foi publicado e agora está disponível.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="6ef7e-111">Se o pacote estiver disponível, o status **publicado** será exibido.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="6ef7e-112">Se o pacote não for publicado com êxito, o status não **publicado** será exibido, juntamente com o texto de erro que explica por que o pacote não está disponível.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="6ef7e-113">Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="6ef7e-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="6ef7e-114">Navegue até o seguinte nó de objeto de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="6ef7e-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="6ef7e-115">**Configuração &gt; do computador Política &gt; modelos administrativos &gt; do &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="6ef7e-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="6ef7e-116">Habilite a configuração de política **exigir publicação como administrador** .</span><span class="sxs-lookup"><span data-stu-id="6ef7e-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="6ef7e-117">Para usar opcionalmente o PowerShell para definir esse item, consulte [como gerenciar pacotes do App-V 5,0 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="6ef7e-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="6ef7e-118">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="6ef7e-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6ef7e-119">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6ef7e-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6ef7e-120">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="6ef7e-120">Got an App-V issue?</span></span>** <span data-ttu-id="6ef7e-121">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6ef7e-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6ef7e-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ef7e-122">Related topics</span></span>


[<span data-ttu-id="6ef7e-123">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6ef7e-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="6ef7e-124">Como configurar o acesso a pacotes usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6ef7e-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





