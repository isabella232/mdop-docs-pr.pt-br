---
title: Como aplicar um modelo de projeto do App-V (App-V 4.6 SP1)
description: Como aplicar um modelo de projeto do App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 8ef120ab-8cfb-438c-8136-671167b7bd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b5f04f3f31838bfb13c19eee5f2314c3a3d291f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797912"
---
# <span data-ttu-id="2d1de-103">Como aplicar um modelo de projeto do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="2d1de-103">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="2d1de-104">Você pode usar um modelo de projeto App-V para aplicar configurações comuns associadas a um pacote de aplicativo virtual existente a um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="2d1de-104">You can use an App-V project template to apply common settings associated with an existing virtual application package to a new virtual application package.</span></span> <span data-ttu-id="2d1de-105">Usar os modelos de projeto do App-V pode ajudar a simplificar o processo de criação de pacotes de aplicativos virtuais definindo configurações comuns antes de começar a sequenciar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d1de-105">Using App-V project templates can help streamline the process of creating virtual application packages by configuring common settings before you begin sequencing an application.</span></span>

<span data-ttu-id="2d1de-106">**Observação**  Você só pode aplicar um modelo de projeto App-V ao criar um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="2d1de-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="2d1de-107">Não há suporte para a aplicação de modelos de projeto a pacotes de aplicativos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="2d1de-107">Applying project templates to existing virtual application packages is not supported.</span></span> <span data-ttu-id="2d1de-108">Além disso, você não pode usar um modelo de projeto em conjunto com um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="2d1de-108">Additionally, you cannot use a project template in conjunction with a Package Accelerator.</span></span>

 

<span data-ttu-id="2d1de-109">Para obter mais informações sobre como criar modelos de projeto do App-V, consulte [como criar um modelo de projeto App-v (App-v 4,6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="2d1de-109">For more information about creating App-V project templates, see [How to Create an App-V Project Template (App-V 4.6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="2d1de-110">Para aplicar um modelo de projeto App-V</span><span class="sxs-lookup"><span data-stu-id="2d1de-110">To apply an App-V project template</span></span>**

1.  <span data-ttu-id="2d1de-111">Para iniciar o Microsoft Application Virtualization Sequencer, no computador em que o sequenciador do App-V está instalado, clique em **Iniciar**  /  **todos os programas**Microsoft Application Virtualization  /  **Microsoft Application Virtualization**  /  **Sequencer**Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2d1de-111">To start the Microsoft Application Virtualization Sequencer, on the computer on which App-V Sequencer is installed, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="2d1de-112">Para criar um novo pacote de aplicativo virtual usando um modelo App-V Project, clique em **arquivo**  /  **novo do modelo**.</span><span class="sxs-lookup"><span data-stu-id="2d1de-112">To create a new virtual application package by using an App-V project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="2d1de-113">Para selecionar o modelo de projeto que você deseja usar, navegue até o diretório onde o modelo de projeto foi salvo, selecione o modelo de projeto e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="2d1de-113">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

4.  <span data-ttu-id="2d1de-114">Crie o novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="2d1de-114">Create the new virtual application package.</span></span> <span data-ttu-id="2d1de-115">As configurações salvas com o modelo especificado serão aplicadas ao novo pacote de aplicativo virtual que você está criando.</span><span class="sxs-lookup"><span data-stu-id="2d1de-115">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span> <span data-ttu-id="2d1de-116">Para obter mais informações sobre como criar um novo pacote de aplicativo virtual, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)e selecione o procedimento apropriado.</span><span class="sxs-lookup"><span data-stu-id="2d1de-116">For more information about creating a new virtual application package, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md), and select the appropriate procedure.</span></span>

## <span data-ttu-id="2d1de-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d1de-117">Related topics</span></span>


[<span data-ttu-id="2d1de-118">Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="2d1de-118">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="2d1de-119">Como criar um modelo de projeto App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="2d1de-119">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-create-an-app-v-project-template--app-v-46-sp1-.md)

 

 





