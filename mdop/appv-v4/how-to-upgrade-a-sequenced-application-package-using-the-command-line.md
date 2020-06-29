---
title: Como fazer upgrade de um pacote de aplicativo sequenciado usando a linha de comando
description: Como fazer upgrade de um pacote de aplicativo sequenciado usando a linha de comando
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796935"
---
# <span data-ttu-id="a8f81-103">Como fazer upgrade de um pacote de aplicativo sequenciado usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="a8f81-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="a8f81-104">Use o procedimento a seguir para atualizar um aplicativo virtual usando uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a8f81-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="a8f81-105">Quando você atualiza um pacote de aplicativo virtual existente usando a linha de comando, a versão original do arquivo. sft é excluída.</span><span class="sxs-lookup"><span data-stu-id="a8f81-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="a8f81-106">Você deve fazer backup do arquivo. sft associado antes de atualizar o pacote usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a8f81-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="a8f81-107">Para atualizar um aplicativo virtual</span><span class="sxs-lookup"><span data-stu-id="a8f81-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="a8f81-108">No computador que está executando o sequenciador do Application Virtualization (App-V), para abrir o prompt de comando, selecione **Iniciar**, **executar**e digite **cmd**.</span><span class="sxs-lookup"><span data-stu-id="a8f81-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="a8f81-109">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8f81-109">Click **OK**.</span></span>

2.  <span data-ttu-id="a8f81-110">No prompt de comando, especifique o local em que o sequenciador do App-V está instalado.</span><span class="sxs-lookup"><span data-stu-id="a8f81-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="a8f81-111">Por exemplo, no prompt de comando, você pode digitar o seguinte: **CD c:\\Arquivos de Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="a8f81-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="a8f81-112">No prompt de comando, digite o seguinte comando, substituindo o texto entre aspas pelos valores:</span><span class="sxs-lookup"><span data-stu-id="a8f81-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="a8f81-113">Observação</span><span class="sxs-lookup"><span data-stu-id="a8f81-113">Note</span></span>**  
    <span data-ttu-id="a8f81-114">Você pode especificar parâmetros adicionais usando a linha de comando, dependendo da complexidade do aplicativo que está atualizando.</span><span class="sxs-lookup"><span data-stu-id="a8f81-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="a8f81-115">Para obter uma lista completa de parâmetros disponíveis para uso com o sequenciador App-V, consulte [parâmetros de linha de comando](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a8f81-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



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
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="a8f81-116">Pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="a8f81-116">Press **Enter**.</span></span>

## <span data-ttu-id="a8f81-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8f81-117">Related topics</span></span>


[<span data-ttu-id="a8f81-118">Como gerenciar aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="a8f81-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









