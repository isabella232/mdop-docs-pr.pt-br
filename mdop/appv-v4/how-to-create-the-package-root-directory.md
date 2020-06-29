---
title: Como criar o Diretório raiz de pacote
description: Como criar o Diretório raiz de pacote
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797163"
---
# <span data-ttu-id="7390b-103">Como criar o Diretório raiz de pacote</span><span class="sxs-lookup"><span data-stu-id="7390b-103">How to Create the Package Root Directory</span></span>


<span data-ttu-id="7390b-104">O diretório raiz do pacote é o diretório no computador que executa o sequenciador App-V em que os arquivos do aplicativo sequenciado são instalados.</span><span class="sxs-lookup"><span data-stu-id="7390b-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="7390b-105">Esse diretório também existe virtualmente no computador para o qual um aplicativo sequenciado será transmitido.</span><span class="sxs-lookup"><span data-stu-id="7390b-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="7390b-106">Você deve criar o diretório raiz do pacote antes de monitorar a instalação de um novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7390b-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="7390b-107">Depois de criar o diretório raiz do pacote, você pode começar a sequenciar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7390b-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="7390b-108">Para obter mais informações sobre como sequenciar um novo aplicativo, consulte [como instalar o sequenciador](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="7390b-108">For more information about sequencing a new application, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

**<span data-ttu-id="7390b-109">Para criar o diretório raiz do pacote</span><span class="sxs-lookup"><span data-stu-id="7390b-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="7390b-110">Para criar o diretório raiz do pacote, no computador que executa o sequenciador App-V, mapeie a unidade Q:\\ para o local de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="7390b-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="7390b-111">O local especificado deve ter espaço suficiente para salvar o aplicativo que você está sequenciando.</span><span class="sxs-lookup"><span data-stu-id="7390b-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="7390b-112">Para criar um diretório que você pode usar para um novo aplicativo virtual, crie uma pasta na unidade Q:\\ e atribua um nome a ela.</span><span class="sxs-lookup"><span data-stu-id="7390b-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="7390b-113">**Importante**  O nome que você atribui a arquivos de aplicativo virtual que serão salvos no diretório raiz do pacote deve usar o formato de nomenclatura do 8,3.</span><span class="sxs-lookup"><span data-stu-id="7390b-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="7390b-114">Os nomes dos arquivos não devem ter mais de 8 caracteres com uma extensão de nome de arquivo de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="7390b-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="7390b-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7390b-115">Related topics</span></span>


[<span data-ttu-id="7390b-116">Tarefas para o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="7390b-116">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





