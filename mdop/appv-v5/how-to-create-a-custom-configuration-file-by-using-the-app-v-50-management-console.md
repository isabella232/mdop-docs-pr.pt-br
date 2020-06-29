---
title: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0
description: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796472"
---
# <span data-ttu-id="a2f7c-103">Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a2f7c-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="a2f7c-104">Você pode usar uma configuração dinâmica para personalizar um pacote App-V 5,0 para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="a2f7c-105">No entanto, você deve primeiro criar o arquivo de configuração dinâmica do usuário (. xml) ou o arquivo de configuração de implantação dinâmica antes de poder usar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="a2f7c-106">A criação do arquivo é uma operação manual avançada.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="a2f7c-107">Para obter informações gerais sobre arquivos de configuração de usuários dinâmicos, consulte [sobre a configuração dinâmica do App-V 5,0](about-app-v-50-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a2f7c-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="a2f7c-108">Use o procedimento a seguir para criar um arquivo de configuração de usuário dinâmico usando o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="a2f7c-109">Para criar um arquivo de configuração de usuário dinâmico</span><span class="sxs-lookup"><span data-stu-id="a2f7c-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="a2f7c-110">Clique com o botão direito do mouse no nome do pacote que você deseja exibir e selecione **Editar acesso ao Active Directory** para exibir a configuração atribuída a um determinado grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="a2f7c-111">Ou, se preferir, selecione o pacote e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="a2f7c-112">Usando a lista de **entidades do anúncio com o Access**, selecione o grupo do anúncio que você deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="a2f7c-113">Selecione **personalizado** na lista suspensa, se ainda não estiver selecionado.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="a2f7c-114">Um link chamado **Editar** será exibido.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="a2f7c-115">Clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-115">Click **Edit**.</span></span> <span data-ttu-id="a2f7c-116">A configuração do usuário dinâmico atribuído ao grupo do anúncio será exibida.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="a2f7c-117">Clique em **avançado**e, em seguida, clique em **Exportar configuração**.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="a2f7c-118">Digite um nome de arquivo e clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="a2f7c-119">Agora, você pode editar o arquivo para configurar um pacote para um usuário.</span><span class="sxs-lookup"><span data-stu-id="a2f7c-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="a2f7c-120">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="a2f7c-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a2f7c-121">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a2f7c-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a2f7c-122">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="a2f7c-122">Got an App-V issue?</span></span>** <span data-ttu-id="a2f7c-123">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a2f7c-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a2f7c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2f7c-124">Related topics</span></span>


[<span data-ttu-id="a2f7c-125">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a2f7c-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





