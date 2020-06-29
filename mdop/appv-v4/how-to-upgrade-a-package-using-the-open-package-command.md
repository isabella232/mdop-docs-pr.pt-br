---
title: Como fazer upgrade de um pacote usando o comando Abrir Pacote
description: Como fazer upgrade de um pacote usando o comando Abrir Pacote
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796941"
---
# <span data-ttu-id="6b131-103">Como fazer upgrade de um pacote usando o comando Abrir Pacote</span><span class="sxs-lookup"><span data-stu-id="6b131-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="6b131-104">Use o comando abrir pacote para atualizar ou aplicar uma atualização a um pacote de aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="6b131-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="6b131-105">Quando você atualiza um pacote de aplicativo virtual existente usando a linha de comando, a versão original do arquivo. sft é excluída.</span><span class="sxs-lookup"><span data-stu-id="6b131-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="6b131-106">Você deve fazer backup do arquivo. sft associado antes de atualizar o pacote usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="6b131-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="6b131-107">Para atualizar um pacote usando o comando abrir pacote</span><span class="sxs-lookup"><span data-stu-id="6b131-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="6b131-108">Para abrir o pacote que será atualizado, no console do Application Virtualization (App-V) **, clique em** **Abrir pacote para atualização**.</span><span class="sxs-lookup"><span data-stu-id="6b131-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="6b131-109">Na caixa de diálogo **abrir** , selecione o pacote que será atualizado.</span><span class="sxs-lookup"><span data-stu-id="6b131-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="6b131-110">Para iniciar o assistente de **sequenciamento** , selecione **ferramentas**, **Assistente de sequenciamento**.</span><span class="sxs-lookup"><span data-stu-id="6b131-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="6b131-111">Concluir o assistente que aplica as alterações de configuração, para salvar o novo aplicativo sequenciado, selecione **arquivo**, **salvar**.</span><span class="sxs-lookup"><span data-stu-id="6b131-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="6b131-112">Para acrescentar o número da versão ao nome do pacote, no console do sequenciador, selecione **ferramentas**, **Opções**.</span><span class="sxs-lookup"><span data-stu-id="6b131-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="6b131-113">Selecione **acrescentar versão do pacote ao nome do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="6b131-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="6b131-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b131-114">Click **OK**.</span></span>

    <span data-ttu-id="6b131-115">**Importante**  Atualizar o nome do arquivo com a versão do pacote é essencial para concluir a atualização com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b131-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="6b131-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b131-116">Related topics</span></span>


[<span data-ttu-id="6b131-117">Como gerenciar aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="6b131-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





