---
title: Como publicar um pacote usando o Console de Gerenciamento
description: Como publicar um pacote usando o Console de Gerenciamento
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796332"
---
# <span data-ttu-id="f30ed-103">Como publicar um pacote usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f30ed-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="f30ed-104">Use o procedimento a seguir para publicar um pacote do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f30ed-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="f30ed-105">Depois que você publica um pacote, os computadores que executam o cliente App-V 5,1 podem acessar e executar os aplicativos nesse pacote.</span><span class="sxs-lookup"><span data-stu-id="f30ed-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="f30ed-106">**Observação**  A capacidade de habilitar somente os administradores para publicar ou cancelar a publicação de pacotes (descritos abaixo) tem suporte a partir do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="f30ed-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="f30ed-107">Para publicar um pacote do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f30ed-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="f30ed-108">No console de gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f30ed-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="f30ed-109">Clique ou clique com o botão direito do mouse no nome do pacote a ser publicado.</span><span class="sxs-lookup"><span data-stu-id="f30ed-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="f30ed-110">Selecione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="f30ed-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="f30ed-111">Examine a coluna **status** para verificar se o pacote foi publicado e agora está disponível.</span><span class="sxs-lookup"><span data-stu-id="f30ed-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="f30ed-112">Se o pacote estiver disponível, o status **publicado** será exibido.</span><span class="sxs-lookup"><span data-stu-id="f30ed-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="f30ed-113">Se o pacote não for publicado com êxito, o status não **publicado** será exibido, juntamente com o texto de erro que explica por que o pacote não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f30ed-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="f30ed-114">Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="f30ed-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="f30ed-115">Navegue até o seguinte nó de objeto de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="f30ed-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="f30ed-116">**Configuração &gt; do computador Política &gt; modelos administrativos &gt; do &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="f30ed-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="f30ed-117">Habilite a configuração de política **exigir publicação como administrador** .</span><span class="sxs-lookup"><span data-stu-id="f30ed-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="f30ed-118">Para usar opcionalmente o PowerShell para definir esse item, consulte [como gerenciar pacotes do App-V 5,1 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="f30ed-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="f30ed-119">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="f30ed-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f30ed-120">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f30ed-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f30ed-121">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="f30ed-121">Got an App-V issue?</span></span>** <span data-ttu-id="f30ed-122">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f30ed-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f30ed-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f30ed-123">Related topics</span></span>


[<span data-ttu-id="f30ed-124">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f30ed-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="f30ed-125">Como configurar o acesso a pacotes usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f30ed-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





