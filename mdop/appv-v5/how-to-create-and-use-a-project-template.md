---
title: Como criar e usar um modelo de projeto
description: Como criar e usar um modelo de projeto
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796455"
---
# <span data-ttu-id="17f06-103">Como criar e usar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="17f06-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="17f06-104">Você pode usar um modelo de projeto App-V 5,0 para salvar as configurações comumente aplicadas associadas a um pacote de aplicativo virtual existente.</span><span class="sxs-lookup"><span data-stu-id="17f06-104">You can use an App-V 5.0 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="17f06-105">Essas configurações podem ser aplicadas quando você cria novos pacotes de aplicativos virtuais em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="17f06-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="17f06-106">Usar um modelo de projeto pode simplificar o processo de criação de pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="17f06-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="17f06-107">**Observação**  Você pode, em geral, aplicar um modelo de projeto App-V 5,0 durante uma atualização de pacote.</span><span class="sxs-lookup"><span data-stu-id="17f06-107">**Note** You can, and often should apply an App-V 5.0 project template during a package upgrade.</span></span> <span data-ttu-id="17f06-108">Por exemplo, se você tiver sequenciado um aplicativo com uma lista de exclusão personalizada, é recomendável que um modelo associado seja criado e salvo para uso posterior durante a atualização do aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="17f06-108">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>

<span data-ttu-id="17f06-109">Os modelos de projeto do App-V 5,0 diferem dos aceleradores de aplicativos do App-V 5,0 porque o App-V 5,0 Application Accelerators são específicos do aplicativo e os modelos de projeto do App-V 5,0 podem ser aplicados a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="17f06-109">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="17f06-110">Use os procedimentos a seguir para criar e aplicar um novo modelo.</span><span class="sxs-lookup"><span data-stu-id="17f06-110">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="17f06-111">Para criar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="17f06-111">To create a project template</span></span>**

1.  <span data-ttu-id="17f06-112">Para iniciar o sequenciador do App-V 5,0, no computador que está executando o sequenciador, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="17f06-112">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

<span data-ttu-id="17f06-113">**Observação**  Se o pacote de aplicativo virtual estiver aberto no console do App-V 5,0 Sequencer, pule para a etapa 3 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="17f06-113">**Note** If the virtual application package is currently open in the App-V 5.0 Sequencer console, skip to step 3 of this procedure.</span></span>

2. <span data-ttu-id="17f06-114">Para abrir o pacote de aplicativo virtual existente que contém as configurações que você deseja salvar com o modelo de projeto App-V 5,0, clique em **arquivo**  /  **abrir**e, em seguida, clique em **Editar pacote**.</span><span class="sxs-lookup"><span data-stu-id="17f06-114">To open the existing virtual application package that contains the settings you want to save with the App-V 5.0 project template, click **File** / **Open**, and then click **Edit Package**.</span></span> <span data-ttu-id="17f06-115">Na página **selecionar pacote** , clique em **procurar** e localize o pacote de aplicativo virtual que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="17f06-115">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="17f06-116">Clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="17f06-116">Click **Edit**.</span></span>

3. <span data-ttu-id="17f06-117">No console do sequenciador do App-V 5,0, para salvar o arquivo de modelo, clique em **arquivo**  /  **salvar como modelo**.</span><span class="sxs-lookup"><span data-stu-id="17f06-117">In the App-V 5.0 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="17f06-118">Depois de revisar as configurações que serão salvas com o novo modelo, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="17f06-118">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="17f06-119">Especifique um nome que será associado ao novo modelo de projeto do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17f06-119">Specify a name that will be associated with the new App-V 5.0 project template.</span></span> <span data-ttu-id="17f06-120">Clique em salvar.</span><span class="sxs-lookup"><span data-stu-id="17f06-120">Click Save.</span></span>
   <span data-ttu-id="17f06-121">O novo modelo de projeto do App-V 5,0 é salvo no diretório especificado na etapa 3 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="17f06-121">The new App-V 5.0 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="17f06-122">Para aplicar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="17f06-122">To apply a project template</span></span>**

<span data-ttu-id="17f06-123">**Importante**  Não há suporte para a criação de um pacote de aplicativo virtual usando um modelo de projeto em conjunto com um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="17f06-123">**Important** Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>

1.  <span data-ttu-id="17f06-124">Para iniciar o sequenciador do App-V 5,0, no computador que está executando o sequenciador, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="17f06-124">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="17f06-125">Para criar ou atualizar um novo pacote de aplicativo virtual usando um modelo de projeto App-V 5,0, clique em **arquivo**  /  **novo do modelo**.</span><span class="sxs-lookup"><span data-stu-id="17f06-125">To create or upgrade a new virtual application package by using an App-V 5.0 project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="17f06-126">Para selecionar o modelo de projeto que você deseja usar, navegue até o diretório onde o modelo de projeto foi salvo, selecione o modelo de projeto e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="17f06-126">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

    <span data-ttu-id="17f06-127">Crie o novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="17f06-127">Create the new virtual application package.</span></span> <span data-ttu-id="17f06-128">As configurações salvas com o modelo especificado serão aplicadas ao novo pacote de aplicativo virtual que você está criando.</span><span class="sxs-lookup"><span data-stu-id="17f06-128">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

    <span data-ttu-id="17f06-129">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="17f06-129">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="17f06-130">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="17f06-130">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="17f06-131">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="17f06-131">Got an App-V issue?</span></span>** <span data-ttu-id="17f06-132">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="17f06-132">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="17f06-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17f06-133">Related topics</span></span>


[<span data-ttu-id="17f06-134">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="17f06-134">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









