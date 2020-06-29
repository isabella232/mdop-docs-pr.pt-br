---
title: Como ramificar um pacote
description: Como ramificar um pacote
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797263"
---
# <span data-ttu-id="08529-103">Como ramificar um pacote</span><span class="sxs-lookup"><span data-stu-id="08529-103">How to Branch a Package</span></span>


<span data-ttu-id="08529-104">Use este procedimento para modificar um pacote de aplicativo sequenciado existente para que você possa executá-lo lado a lado com o pacote de aplicativo sequenciado original.</span><span class="sxs-lookup"><span data-stu-id="08529-104">Use this procedure to modify an existing sequenced application package so you can run it side-by-side with the original sequenced application package.</span></span> <span data-ttu-id="08529-105">Esse processo é chamado de ramificação.</span><span class="sxs-lookup"><span data-stu-id="08529-105">This process is called branching.</span></span> <span data-ttu-id="08529-106">Ao ramificar um pacote de aplicativo virtual, você pode executar duas versões do mesmo pacote.</span><span class="sxs-lookup"><span data-stu-id="08529-106">When you branch a virtual application package you are able to run two versions of the same package.</span></span> <span data-ttu-id="08529-107">Por exemplo, você pode aplicar um Service Pack a um pacote existente e executá-lo lado a lado com o pacote de aplicativo virtual sequenciado original.</span><span class="sxs-lookup"><span data-stu-id="08529-107">For example, you can apply a service pack to an existing package, and run it side-by-side with the original sequenced virtual application package.</span></span>

<span data-ttu-id="08529-108">Use o procedimento a seguir para ramificar um pacote de aplicativo virtual sequenciado.</span><span class="sxs-lookup"><span data-stu-id="08529-108">Use the following procedure to branch a sequenced virtual application package.</span></span>

**<span data-ttu-id="08529-109">Para ramificar um pacote de aplicativo virtual sequenciado</span><span class="sxs-lookup"><span data-stu-id="08529-109">To branch a sequenced virtual application package</span></span>**

1.  <span data-ttu-id="08529-110">Abra o sequenciador do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="08529-110">Open the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="08529-111">Para especificar o diretório de destino que contém o pacote (. sprj) que você deseja ramificar selecionar **arquivo**, **abra**.</span><span class="sxs-lookup"><span data-stu-id="08529-111">To specify the destination directory that contains the package (.sprj) you want to branch select **File**, **Open**.</span></span>

2.  <span data-ttu-id="08529-112">Navegue até o diretório que contém o aplicativo sequenciado que você planeja ramificar e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="08529-112">Navigate to the directory that contains the sequenced application you plan to branch and click **Open**.</span></span>

3.  <span data-ttu-id="08529-113">Para salvar uma cópia do pacote, na sequência App-V, selecione **arquivo**, **salvar como**.</span><span class="sxs-lookup"><span data-stu-id="08529-113">To save a copy of the package, in the App-V Sequencer, select **File**, **Save As**.</span></span> <span data-ttu-id="08529-114">Especifique um novo nome exclusivo e especifique um novo diretório raiz exclusivo do pacote para a cópia do pacote.</span><span class="sxs-lookup"><span data-stu-id="08529-114">Specify a new, unique name, and specify a new unique package root directory for the copy of the package.</span></span> <span data-ttu-id="08529-115">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="08529-115">Click **Save**.</span></span>

    **<span data-ttu-id="08529-116">Importante</span><span class="sxs-lookup"><span data-stu-id="08529-116">Important</span></span>**  
    <span data-ttu-id="08529-117">Você deve especificar um novo nome de pacote ou substituirá a versão existente do pacote.</span><span class="sxs-lookup"><span data-stu-id="08529-117">You must specify a new package name or you will overwrite the existing version of the package.</span></span>



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. <span data-ttu-id="08529-118">Depois de salvar a nova versão, você pode aplicar as alterações de configuração necessárias e salvar os arquivos ICO, OSD, SFT e SPRJ associados para corrigir o local no servidor do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="08529-118">After you save the new version you can apply the required configuration changes and save the associated ICO, OSD, SFT, and SPRJ files to correct location on the Application Virtualization (App-V) server.</span></span>

## <span data-ttu-id="08529-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08529-119">Related topics</span></span>


[<span data-ttu-id="08529-120">Tarefas para o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="08529-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)









