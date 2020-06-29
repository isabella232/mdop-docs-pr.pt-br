---
title: Como modificar os sistemas operacionais associados a um arquivo existente do Windows Installer
description: Como modificar os sistemas operacionais associados a um arquivo existente do Windows Installer
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797028"
---
# <span data-ttu-id="835e5-103">Como modificar os sistemas operacionais associados a um arquivo existente do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="835e5-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="835e5-104">Use o procedimento a seguir para modificar as versões do sistema operacional associadas a um arquivo existente do Windows Installer (**MSI**) que foi criado usando o sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="835e5-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="835e5-105">Para modificar os sistemas operacionais de um arquivo existente do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="835e5-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="835e5-106">Instale o sequenciador do App-V em um computador em seu ambiente que tenha somente o sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="835e5-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="835e5-107">Você também pode instalar o sequenciador em um computador que executa um ambiente virtual, por exemplo, Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="835e5-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="835e5-108">Esse método é útil porque é mais fácil manter um ambiente de sequenciamento de limpeza que você pode reutilizar com uma configuração adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="835e5-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="835e5-109">Para obter mais informações sobre como instalar o App-V Sequencer, consulte [como instalar o sequenciador](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="835e5-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="835e5-110">Copie todo o pacote de aplicativo virtual que contém o arquivo do Windows Installer que você deseja modificar para o computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="835e5-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="835e5-111">Para modificar o arquivo do Windows Installer, abra o console do sequenciador, selecione **pacote**  /  **aberto**e, em seguida, navegue até o local onde o pacote do aplicativo virtual associado ao arquivo do Windows Installer foi salvo.</span><span class="sxs-lookup"><span data-stu-id="835e5-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="835e5-112">Para adicionar ou remover sistemas operacionais, selecione a guia **implantação** no console do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="835e5-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="835e5-113">Para especificar sistemas operacionais adicionais que serão associados ao arquivo do Windows Installer, selecione o sistema operacional desejado e, em seguida, clique na seta que aponta para o controle de lista do sistema operacional **selecionado** .</span><span class="sxs-lookup"><span data-stu-id="835e5-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="835e5-114">Para remover uma associação de sistema operacional, selecione o sistema operacional que você deseja remover e, em seguida, clique na seta que aponta para o controle de lista do sistema operacional **disponível** .</span><span class="sxs-lookup"><span data-stu-id="835e5-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="835e5-115">Para criar um novo Windows Installer que será associado ao pacote de aplicativo virtual, selecione **gerar pacote do Microsoft Windows Installer (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="835e5-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="835e5-116">Você também pode selecionar **ferramentas**  /  **Create MSI**.</span><span class="sxs-lookup"><span data-stu-id="835e5-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="835e5-117">**Observação**  Se você selecionar **ferramentas** / , **criar MSI** para criar um novo arquivo do Windows Installer, ignore a **etapa 6** deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="835e5-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="835e5-118">Para salvar o pacote de aplicativo virtual, **Package**selecione  /  **salvar**pacote.</span><span class="sxs-lookup"><span data-stu-id="835e5-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="835e5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="835e5-119">Related topics</span></span>


[<span data-ttu-id="835e5-120">Tarefas para o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="835e5-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





