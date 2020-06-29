---
title: Como criar e usar um modelo de projeto
description: Como criar e usar um modelo de projeto
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796452"
---
# <span data-ttu-id="ad697-103">Como criar e usar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="ad697-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="ad697-104">Você pode usar um modelo de projeto App-V 5,1 para salvar as configurações comumente aplicadas associadas a um pacote de aplicativo virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ad697-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="ad697-105">Essas configurações podem ser aplicadas quando você cria novos pacotes de aplicativos virtuais em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="ad697-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="ad697-106">Usar um modelo de projeto pode simplificar o processo de criação de pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="ad697-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="ad697-107">Observação</span><span class="sxs-lookup"><span data-stu-id="ad697-107">Note</span></span>**  
<span data-ttu-id="ad697-108">Você pode, em geral, aplicar um modelo de projeto App-V 5,1 durante uma atualização de pacote.</span><span class="sxs-lookup"><span data-stu-id="ad697-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="ad697-109">Por exemplo, se você tiver sequenciado um aplicativo com uma lista de exclusão personalizada, é recomendável que um modelo associado seja criado e salvo para uso posterior durante a atualização do aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="ad697-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="ad697-110">Os modelos de projeto do App-V 5,1 diferem dos aceleradores de aplicativos do App-V 5,1 porque o App-V 5,1 Application Accelerators são específicos do aplicativo e os modelos de projeto do App-V 5,1 podem ser aplicados a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ad697-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="ad697-111">Use os procedimentos a seguir para criar e aplicar um novo modelo.</span><span class="sxs-lookup"><span data-stu-id="ad697-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="ad697-112">Para criar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="ad697-112">To create a project template</span></span>**

1.  <span data-ttu-id="ad697-113">Para iniciar o sequenciador do App-V 5,1, no computador que está executando o sequenciador, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="ad697-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="ad697-114">Observação</span><span class="sxs-lookup"><span data-stu-id="ad697-114">Note</span></span>**  
    <span data-ttu-id="ad697-115">Se o pacote de aplicativo virtual estiver aberto no console do App-V 5,1 Sequencer, pule para a etapa 3 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="ad697-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="ad697-116">No console do sequenciador do App-V 5,1, para salvar o arquivo de modelo, clique em **arquivo**  /  **salvar como modelo**.</span><span class="sxs-lookup"><span data-stu-id="ad697-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="ad697-117">Depois de revisar as configurações que serão salvas com o novo modelo, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad697-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="ad697-118">Especifique um nome que será associado ao novo modelo de projeto do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="ad697-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="ad697-119">Clique em salvar.</span><span class="sxs-lookup"><span data-stu-id="ad697-119">Click Save.</span></span>

   <span data-ttu-id="ad697-120">O novo modelo de projeto do App-V 5,1 é salvo no diretório especificado na etapa 3 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="ad697-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="ad697-121">Para aplicar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="ad697-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="ad697-122">Importante</span><span class="sxs-lookup"><span data-stu-id="ad697-122">Important</span></span>**  
    <span data-ttu-id="ad697-123">Não há suporte para a criação de um pacote de aplicativo virtual usando um modelo de projeto em conjunto com um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="ad697-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="ad697-124">Para criar ou atualizar um novo pacote de aplicativo virtual usando um modelo de projeto App-V 5,1, clique em **arquivo**  /  **novo do modelo**.</span><span class="sxs-lookup"><span data-stu-id="ad697-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="ad697-125">Para selecionar o modelo de projeto que você deseja usar, navegue até o diretório onde o modelo de projeto foi salvo, selecione o modelo de projeto e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="ad697-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="ad697-126">Crie o novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="ad697-126">Create the new virtual application package.</span></span> <span data-ttu-id="ad697-127">As configurações salvas com o modelo especificado serão aplicadas ao novo pacote de aplicativo virtual que você está criando.</span><span class="sxs-lookup"><span data-stu-id="ad697-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="ad697-128">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="ad697-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ad697-129">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="ad697-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ad697-130">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="ad697-130">Got an App-V issue?</span></span>** <span data-ttu-id="ad697-131">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ad697-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ad697-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad697-132">Related topics</span></span>


[<span data-ttu-id="ad697-133">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ad697-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









