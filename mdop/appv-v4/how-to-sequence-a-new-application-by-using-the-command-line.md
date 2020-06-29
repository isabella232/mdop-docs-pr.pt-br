---
title: Como sequenciar um novo aplicativo usando a linha de comando
description: Como sequenciar um novo aplicativo usando a linha de comando
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796975"
---
# <span data-ttu-id="1e2da-103">Como sequenciar um novo aplicativo usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="1e2da-103">How to Sequence a New Application by Using the Command Line</span></span>


<span data-ttu-id="1e2da-104">Você pode usar uma linha de comando para sequenciar um novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1e2da-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="1e2da-105">Usar uma linha de comando é útil quando você precisa criar um grande número de aplicativos virtuais ou quando precisa criar aplicativos sequenciados em uma base recorrente.</span><span class="sxs-lookup"><span data-stu-id="1e2da-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="1e2da-106">Importante</span><span class="sxs-lookup"><span data-stu-id="1e2da-106">Important</span></span>**  
<span data-ttu-id="1e2da-107">O sequenciamento de linha de comando permite somente o sequenciamento padrão.</span><span class="sxs-lookup"><span data-stu-id="1e2da-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="1e2da-108">Se precisar alterar as configurações de instalação padrão do aplicativo que você está sequenciando, você deve modificar manualmente o aplicativo virtual ou atualizar o aplicativo virtual usando o sequenciador Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="1e2da-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="1e2da-109">Para obter mais informações sobre como atualizar um aplicativo virtual usando o sequenciador App-V, consulte [como atualizar um aplicativo virtual existente](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="1e2da-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="1e2da-110">Use o procedimento a seguir para criar um aplicativo virtual usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1e2da-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="1e2da-111">Para sequenciar um aplicativo usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="1e2da-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="1e2da-112">No computador que está executando o sequenciador App-V, abra o prompt de comando selecionando **Iniciar**, **executar**e, em seguida, digite **cmd**.</span><span class="sxs-lookup"><span data-stu-id="1e2da-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="1e2da-113">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e2da-113">Click **OK**.</span></span>

2.  <span data-ttu-id="1e2da-114">Use o prompt de comando para especificar o local de onde o sequenciador do App-V está instalado.</span><span class="sxs-lookup"><span data-stu-id="1e2da-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="1e2da-115">Por exemplo, no prompt de comando, você pode digitar o seguinte: **CD c:\\Arquivos de Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="1e2da-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="1e2da-116">No prompt de comando, digite o seguinte comando, substituindo o texto entre aspas pelos valores:</span><span class="sxs-lookup"><span data-stu-id="1e2da-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="1e2da-117">Observação</span><span class="sxs-lookup"><span data-stu-id="1e2da-117">Note</span></span>**  
    <span data-ttu-id="1e2da-118">Você pode especificar parâmetros adicionais usando a linha de comando, dependendo da complexidade do aplicativo que está sequenciando.</span><span class="sxs-lookup"><span data-stu-id="1e2da-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="1e2da-119">Para obter uma lista completa de parâmetros disponíveis para uso com o sequenciador App-V, consulte [parâmetros de linha de comando do sequenciador](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e2da-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="1e2da-120">Pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="1e2da-120">Press **Enter**.</span></span>

## <span data-ttu-id="1e2da-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e2da-121">Related topics</span></span>


[<span data-ttu-id="1e2da-122">Como criar ou atualizar aplicativos virtuais usando o sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="1e2da-122">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="1e2da-123">Códigos de erro de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="1e2da-123">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="1e2da-124">Parâmetros de linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="1e2da-124">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









