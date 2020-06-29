---
title: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1
description: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796471"
---
# <span data-ttu-id="1d09c-103">Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="1d09c-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="1d09c-104">Você pode usar uma configuração dinâmica para personalizar um pacote App-V 5,1 para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="1d09c-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="1d09c-105">No entanto, você deve primeiro criar o arquivo de configuração dinâmica do usuário (. xml) ou o arquivo de configuração de implantação dinâmica antes de poder usar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="1d09c-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="1d09c-106">A criação do arquivo é uma operação manual avançada.</span><span class="sxs-lookup"><span data-stu-id="1d09c-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="1d09c-107">Para obter informações gerais sobre arquivos de configuração de usuários dinâmicos, consulte [sobre a configuração dinâmica do App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="1d09c-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="1d09c-108">Use o procedimento a seguir para criar um arquivo de configuração de usuário dinâmico usando o console de gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="1d09c-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="1d09c-109">Para criar um arquivo de configuração de usuário dinâmico</span><span class="sxs-lookup"><span data-stu-id="1d09c-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="1d09c-110">Clique com o botão direito do mouse no nome do pacote que você deseja exibir e selecione **Editar acesso ao Active Directory** para exibir a configuração atribuída a um determinado grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="1d09c-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="1d09c-111">Ou, se preferir, selecione o pacote e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1d09c-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="1d09c-112">Usando a lista de **entidades do anúncio com o Access**, selecione o grupo do anúncio que você deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="1d09c-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="1d09c-113">Selecione **personalizado** na lista suspensa, se ainda não estiver selecionado.</span><span class="sxs-lookup"><span data-stu-id="1d09c-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="1d09c-114">Um link chamado **Editar** será exibido.</span><span class="sxs-lookup"><span data-stu-id="1d09c-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="1d09c-115">Clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1d09c-115">Click **Edit**.</span></span> <span data-ttu-id="1d09c-116">A configuração do usuário dinâmico atribuído ao grupo do anúncio será exibida.</span><span class="sxs-lookup"><span data-stu-id="1d09c-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="1d09c-117">Clique em **avançado**e, em seguida, clique em **Exportar configuração**.</span><span class="sxs-lookup"><span data-stu-id="1d09c-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="1d09c-118">Digite um nome de arquivo e clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="1d09c-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="1d09c-119">Agora, você pode editar o arquivo para configurar um pacote para um usuário.</span><span class="sxs-lookup"><span data-stu-id="1d09c-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="1d09c-120">Observação</span><span class="sxs-lookup"><span data-stu-id="1d09c-120">Note</span></span>**  
    <span data-ttu-id="1d09c-121">Para exportar uma configuração durante a execução no Windows Server, você deve desabilitar "configuração de segurança avançada do IE".</span><span class="sxs-lookup"><span data-stu-id="1d09c-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="1d09c-122">Se ele estiver habilitado e definido para bloquear downloads, não será possível baixar nada do servidor do App-V.</span><span class="sxs-lookup"><span data-stu-id="1d09c-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="1d09c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d09c-123">Related topics</span></span>


[<span data-ttu-id="1d09c-124">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="1d09c-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









