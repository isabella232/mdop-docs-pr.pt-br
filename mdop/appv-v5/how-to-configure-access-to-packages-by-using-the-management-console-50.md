---
title: Como configurar o acesso a pacotes usando o Console de Gerenciamento
description: Como configurar o acesso a pacotes usando o Console de Gerenciamento
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796495"
---
# <span data-ttu-id="3eb24-103">Como configurar o acesso a pacotes usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3eb24-103">How to Configure Access to Packages by Using the Management Console</span></span>


<span data-ttu-id="3eb24-104">Antes de implantar um pacote virtualizado do App-V 5,0, você deve configurar os grupos de segurança dos serviços de domínio Active Directory (AD DS) que terão permissão para acessar e executar os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3eb24-104">Before you deploy an App-V 5.0 virtualized package, you must configure the Active Directory Domain Services (AD DS) security groups that will be allowed to access and run the applications.</span></span> <span data-ttu-id="3eb24-105">Os grupos de segurança podem conter computadores ou usuários.</span><span class="sxs-lookup"><span data-stu-id="3eb24-105">The security groups may contain computers or users.</span></span> <span data-ttu-id="3eb24-106">Entitling um pacote a um grupo de computador publica o pacote globalmente em todos os computadores do grupo.</span><span class="sxs-lookup"><span data-stu-id="3eb24-106">Entitling a package to a computer group publishes the package globally to all computers in the group.</span></span>

<span data-ttu-id="3eb24-107">Use o procedimento a seguir para configurar o acesso a pacotes virtualizados.</span><span class="sxs-lookup"><span data-stu-id="3eb24-107">Use the following procedure to configure access to virtualized packages.</span></span>

**<span data-ttu-id="3eb24-108">Para conceder acesso a um pacote do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3eb24-108">To grant access to an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="3eb24-109">Localize o pacote que você deseja configurar:</span><span class="sxs-lookup"><span data-stu-id="3eb24-109">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="3eb24-110">Abra o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3eb24-110">Open the App-V 5.0 Management console.</span></span>

    2.  <span data-ttu-id="3eb24-111">Para exibir a página de **acesso do AD** , clique com o botão direito do mouse no pacote a ser configurado e selecione **Editar acesso ao Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-111">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="3eb24-112">Ou, se preferir, selecione o pacote e clique em **Editar** no painel **acesso ao anúncio** .</span><span class="sxs-lookup"><span data-stu-id="3eb24-112">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="3eb24-113">Provisionar um grupo de segurança para o pacote:</span><span class="sxs-lookup"><span data-stu-id="3eb24-113">Provision a security group for the package:</span></span>

    1.  <span data-ttu-id="3eb24-114">Vá para a página **localizar nomes válidos do Active Directory e conceder acesso** .</span><span class="sxs-lookup"><span data-stu-id="3eb24-114">Go to the **FIND VALID ACTIVE DIRECTORY NAMES AND GRANT ACCESS** page.</span></span>

    2.  <span data-ttu-id="3eb24-115">Usando o formato **mydomain**  \\  **GroupName**, digite o nome ou parte do nome de um objeto de grupo do Active Directory e clique em **verificar**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-115">Using the format **mydomain** \\ **groupname**, type the name or part of the name of an Active Directory group object, and click **Check**.</span></span>

        <span data-ttu-id="3eb24-116">**Observação**  Certifique-se de fornecer um nome de domínio associado para o grupo que você está procurando.</span><span class="sxs-lookup"><span data-stu-id="3eb24-116">**Note** Ensure that you provide an associated domain name for the group that you are searching for.</span></span>

         

3.  <span data-ttu-id="3eb24-117">Para conceder acesso ao pacote, selecione o grupo desejado e clique em **conceder acesso**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-117">To grant access to the package, select the desired group and click **Grant Access**.</span></span> <span data-ttu-id="3eb24-118">O grupo recém-adicionado é exibido no painel **entidades do anúncio com acesso** .</span><span class="sxs-lookup"><span data-stu-id="3eb24-118">The newly added group is displayed in the **AD ENTITIES WITH ACCESS** pane.</span></span>

4.  

    <span data-ttu-id="3eb24-119">Para aceitar as configurações padrão e fechar a página de **acesso do AD** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-119">To accept the default configuration settings and close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="3eb24-120">Para personalizar as configurações de um grupo específico, clique no menu suspenso **configurações atribuídas** e selecione **personalizado**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-120">To customize configurations for a specific group, click the **ASSIGNED CONFIGURATIONS** drop-down and select **Custom**.</span></span> <span data-ttu-id="3eb24-121">Para definir as configurações personalizadas, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-121">To configure the custom configurations, click **EDIT**.</span></span> <span data-ttu-id="3eb24-122">Após conceder o acesso, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-122">After you grant access, click **Close**.</span></span>

**<span data-ttu-id="3eb24-123">Para remover o acesso a um pacote do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3eb24-123">To remove access to an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="3eb24-124">Localize o pacote que você deseja configurar:</span><span class="sxs-lookup"><span data-stu-id="3eb24-124">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="3eb24-125">Abra o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3eb24-125">Open the App-V 5.0 Management console.</span></span>

    2.  <span data-ttu-id="3eb24-126">Para exibir a página de **acesso do AD** , clique com o botão direito do mouse no pacote a ser configurado e selecione **Editar acesso ao Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-126">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="3eb24-127">Ou, se preferir, selecione o pacote e clique em **Editar** no painel **acesso ao anúncio** .</span><span class="sxs-lookup"><span data-stu-id="3eb24-127">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="3eb24-128">Selecione o grupo que você deseja remover e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-128">Select the group you want to remove, and click **DELETE**.</span></span>

3.  <span data-ttu-id="3eb24-129">Para fechar a página de **acesso do AD** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="3eb24-129">To close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="3eb24-130">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="3eb24-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3eb24-131">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="3eb24-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3eb24-132">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="3eb24-132">Got an App-V issue?</span></span>** <span data-ttu-id="3eb24-133">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3eb24-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3eb24-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3eb24-134">Related topics</span></span>


[<span data-ttu-id="3eb24-135">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3eb24-135">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





