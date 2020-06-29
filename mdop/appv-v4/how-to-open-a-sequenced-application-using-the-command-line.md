---
title: Como abrir um aplicativo sequenciado usando a linha de comando
description: Como abrir um aplicativo sequenciado usando a linha de comando
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797021"
---
# <span data-ttu-id="c2196-103">Como abrir um aplicativo sequenciado usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="c2196-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="c2196-104">Você pode abrir pacotes de aplicativos virtuais usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c2196-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="c2196-105">Você deve executar o prompt **cmd** como administrador.</span><span class="sxs-lookup"><span data-stu-id="c2196-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="c2196-106">Use o procedimento a seguir para abrir pacotes de aplicativos sequenciados usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="c2196-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="c2196-107">Para abrir um aplicativo sequenciado usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="c2196-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="c2196-108">Para abrir o prompt de comando, clique em **Iniciar**e selecione **executar**, digite **cmd**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2196-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="c2196-109">Em um prompt de comando, digite **cd\\** e especifique o caminho para o diretório onde o sequenciador está instalado e pressione **Enter.**</span><span class="sxs-lookup"><span data-stu-id="c2196-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="c2196-110">No prompt de comando, digite o seguinte comando, substituindo o texto em itálico pelos valores:</span><span class="sxs-lookup"><span data-stu-id="c2196-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="c2196-111">SFTSequencer/OPEN:*"especifica o arquivo. sprj para abrir"*</span><span class="sxs-lookup"><span data-stu-id="c2196-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="c2196-112">Pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="c2196-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="c2196-113">Você também pode especificar os seguintes parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="c2196-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="c2196-114">No prompt de comando, digite os seguintes comandos, substituindo o texto em itálico pelos valores:</span><span class="sxs-lookup"><span data-stu-id="c2196-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="c2196-115">/PACKAGENAME: "*especifica o nome do pacote"*</span><span class="sxs-lookup"><span data-stu-id="c2196-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="c2196-116">/MSI-especifica a geração de um instalador do Microsoft Windows associado.</span><span class="sxs-lookup"><span data-stu-id="c2196-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="c2196-117">/COMPRESS – especifica se o pacote será compactado.</span><span class="sxs-lookup"><span data-stu-id="c2196-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="c2196-118">Por padrão, os pacotes não são compactados.</span><span class="sxs-lookup"><span data-stu-id="c2196-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="c2196-119">Pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="c2196-119">Press **Enter**.</span></span>

    <span data-ttu-id="c2196-120">**Observação**  Se o pacote de instalação ou o pacote do Windows Installer tiver uma interface gráfica do usuário, ela será exibida após a especificação dos parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c2196-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="c2196-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2196-121">Related topics</span></span>


[<span data-ttu-id="c2196-122">Como gerenciar aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="c2196-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





