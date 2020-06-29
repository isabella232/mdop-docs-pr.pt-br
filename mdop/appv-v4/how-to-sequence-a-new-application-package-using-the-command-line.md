---
title: Como sequenciar um novo pacote de aplicativo usando a linha de comando
description: Como sequenciar um novo pacote de aplicativo usando a linha de comando
author: dansimp
ms.assetid: de72912b-d9e7-45b5-a601-12528f1a4cac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2dd638a7e4765cedbf1d8050626fb8cc54b2ce8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796973"
---
# <span data-ttu-id="0902b-103">Como sequenciar um novo pacote de aplicativo usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="0902b-103">How to Sequence a New Application Package Using the Command Line</span></span>


<span data-ttu-id="0902b-104">Você pode usar uma linha de comando para sequenciar um novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0902b-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="0902b-105">Usar uma linha de comando é útil quando você precisa criar um grande número de aplicativos virtuais ou quando precisa criar aplicativos sequenciados em uma base recorrente.</span><span class="sxs-lookup"><span data-stu-id="0902b-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="0902b-106">Importante</span><span class="sxs-lookup"><span data-stu-id="0902b-106">Important</span></span>**  
<span data-ttu-id="0902b-107">O sequenciamento de linha de comando permite somente o sequenciamento padrão.</span><span class="sxs-lookup"><span data-stu-id="0902b-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="0902b-108">Se precisar alterar as configurações de instalação padrão do aplicativo que você está sequenciando, você deve modificar manualmente o aplicativo virtual ou atualizar o aplicativo virtual usando o sequenciador Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="0902b-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="0902b-109">Para obter mais informações sobre como atualizar um aplicativo virtual usando o sequenciador App-V, consulte [como atualizar um aplicativo virtual existente](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="0902b-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="0902b-110">Use o procedimento a seguir para criar um aplicativo virtual usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0902b-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="0902b-111">Para sequenciar um aplicativo usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="0902b-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="0902b-112">No computador que está executando o sequenciador App-V, abra o prompt de comando selecionando **Iniciar**, **executar**e, em seguida, digite **cmd**.</span><span class="sxs-lookup"><span data-stu-id="0902b-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="0902b-113">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="0902b-113">Click **OK**.</span></span>

2.  <span data-ttu-id="0902b-114">Use o prompt de comando para especificar o local de onde o sequenciador do App-V está instalado.</span><span class="sxs-lookup"><span data-stu-id="0902b-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="0902b-115">Por exemplo, no prompt de comando, você pode digitar o seguinte: **CD c:\\Arquivos de Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="0902b-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="0902b-116">No prompt de comando, digite o seguinte comando, substituindo o texto entre aspas pelos valores:</span><span class="sxs-lookup"><span data-stu-id="0902b-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="0902b-117">Observação</span><span class="sxs-lookup"><span data-stu-id="0902b-117">Note</span></span>**  
    <span data-ttu-id="0902b-118">Você pode especificar parâmetros adicionais usando a linha de comando, dependendo da complexidade do aplicativo que está sequenciando.</span><span class="sxs-lookup"><span data-stu-id="0902b-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="0902b-119">Para obter uma lista completa de parâmetros disponíveis para uso com o sequenciador App-V, consulte [linha de comando do sequenciador do Application Virtualization](application-virtualization-sequencer-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="0902b-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Application Virtualization Sequencer Command Line](application-virtualization-sequencer-command-line.md).</span></span>



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
<td align="left"><p>Specifies the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="0902b-120">Pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="0902b-120">Press **Enter**.</span></span>

## <span data-ttu-id="0902b-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0902b-121">Related topics</span></span>


[<span data-ttu-id="0902b-122">Como gerenciar aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="0902b-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









