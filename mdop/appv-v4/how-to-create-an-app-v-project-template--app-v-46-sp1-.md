---
title: Como criar um modelo de projeto App-V (App-V 4.6 SP1)
description: Como criar um modelo de projeto App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797167"
---
# <span data-ttu-id="acc19-103">Como criar um modelo de projeto App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="acc19-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="acc19-104">Você pode usar um modelo de projeto App-V para salvar configurações comumente aplicadas associadas a um pacote de aplicativo virtual existente.</span><span class="sxs-lookup"><span data-stu-id="acc19-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="acc19-105">Essas configurações podem ser aplicadas quando você cria novos pacotes de aplicativo virtual em seu ambiente que podem ajudar a simplificar o processo de criação de pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="acc19-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="acc19-106">**Observação**  Você só pode aplicar um modelo de projeto App-V ao criar um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="acc19-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="acc19-107">Não há suporte para a aplicação de modelos de projeto a pacotes de aplicativos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="acc19-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="acc19-108">Para obter mais informações sobre como aplicar um modelo de projeto App-V, consulte [como aplicar um modelo de projeto App-v (App-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="acc19-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="acc19-109">Os modelos de projetos do App-V diferem dos aceleradores de aplicativos do App-v porque os aceleradores de aplicativo do App-V são específicos do aplicativo, e os modelos de projeto do App-V podem ser aplicados a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="acc19-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="acc19-110">Além disso, você não pode usar um modelo de projeto quando usa um acelerador de pacote para criar um pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="acc19-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="acc19-111">As seguintes configurações gerais são salvas com um modelo de projeto App-V:</span><span class="sxs-lookup"><span data-stu-id="acc19-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="acc19-112">**Opções avançadas de monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="acc19-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="acc19-113">Permite que o Microsoft Update seja executado durante o monitoramento, a troca **de base. dll**.</span><span class="sxs-lookup"><span data-stu-id="acc19-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="acc19-114">**Configurações de implantação do pacote**.</span><span class="sxs-lookup"><span data-stu-id="acc19-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="acc19-115">Contém **protocolo**, **nome do host**, **porta**, **caminho**, **sistemas operacionais**, **impor descritores de segurança**, **criar MSI**, **compactar pacote**.</span><span class="sxs-lookup"><span data-stu-id="acc19-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="acc19-116">**Opções gerais**.</span><span class="sxs-lookup"><span data-stu-id="acc19-116">**General Options**.</span></span> <span data-ttu-id="acc19-117">Permite gerar pacote **MSI (Microsoft Windows Installer)** , permitir a **virtualização de eventos**, **permitir a virtualização de serviços**, **acrescentar a versão do pacote ao nome do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="acc19-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="acc19-118">**Itens de exclusão**.</span><span class="sxs-lookup"><span data-stu-id="acc19-118">**Exclusion Items**.</span></span> <span data-ttu-id="acc19-119">Contém a lista de padrões de exclusão.</span><span class="sxs-lookup"><span data-stu-id="acc19-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="acc19-120">Para criar um modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="acc19-120">To create a project template</span></span>**

1.  <span data-ttu-id="acc19-121">Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.</span><span class="sxs-lookup"><span data-stu-id="acc19-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="acc19-122">Se o pacote de aplicativo virtual estiver aberto no momento no sequenciador App-V, pule para a etapa 3 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="acc19-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="acc19-123">Para abrir o pacote de aplicativo virtual existente que contém as configurações que você deseja salvar com o modelo de projeto App-V, clique em **arquivo**  /  **abrir** e clique em **Editar** **pacote**.</span><span class="sxs-lookup"><span data-stu-id="acc19-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="acc19-124">Na página **selecionar pacote** , clique em **procurar** e localize o pacote de aplicativo virtual que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="acc19-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="acc19-125">Clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="acc19-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="acc19-126">No console do App-V Sequencer, clique em **arquivo**  /  **salvar como modelo**.</span><span class="sxs-lookup"><span data-stu-id="acc19-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="acc19-127">Depois de revisar as configurações que serão salvas com o novo modelo, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="acc19-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="acc19-128">Especifique um nome que será associado ao novo modelo de projeto do App-V.</span><span class="sxs-lookup"><span data-stu-id="acc19-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="acc19-129">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="acc19-129">Click **Save**.</span></span>

    <span data-ttu-id="acc19-130">O novo modelo de projeto do App-V é salvo no diretório especificado na etapa 3 deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="acc19-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="acc19-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="acc19-131">Related topics</span></span>


[<span data-ttu-id="acc19-132">Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="acc19-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="acc19-133">Como aplicar um modelo de projeto do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="acc19-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





