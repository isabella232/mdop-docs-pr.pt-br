---
title: Sobre como usar a linha de comando do Sequencer
description: Sobre como usar a linha de comando do Sequencer
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797618"
---
# <span data-ttu-id="8f23b-103">Sobre como usar a linha de comando do Sequencer</span><span class="sxs-lookup"><span data-stu-id="8f23b-103">About Using the Sequencer Command Line</span></span>


<span data-ttu-id="8f23b-104">Você pode usar a linha de comando para criar pacotes de aplicativos sequenciados.</span><span class="sxs-lookup"><span data-stu-id="8f23b-104">You can use the command line to create sequenced application packages.</span></span> <span data-ttu-id="8f23b-105">Usar a linha de comando para criar aplicativos virtuais é útil nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="8f23b-105">Using the command line to create virtual applications is useful in the following scenarios:</span></span>

-   <span data-ttu-id="8f23b-106">Você precisa criar um grande número de pacotes de aplicativos sequenciados.</span><span class="sxs-lookup"><span data-stu-id="8f23b-106">You need to create a large number of sequenced application packages.</span></span>

-   <span data-ttu-id="8f23b-107">Você precisa criar um pacote de aplicativo sequenciado em uma base recorrente.</span><span class="sxs-lookup"><span data-stu-id="8f23b-107">You need to create a sequenced application package on a recurring basis.</span></span>

<span data-ttu-id="8f23b-108">**Importante**  O sequenciamento no prompt de comando permite somente o sequenciamento padrão.</span><span class="sxs-lookup"><span data-stu-id="8f23b-108">**Important** Sequencing at the command prompt allows for default sequencing only.</span></span> <span data-ttu-id="8f23b-109">Se precisar alterar os parâmetros de sequenciamento padrão, você deve modificar manualmente um pacote de aplicativo sequenciado ou resequenciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8f23b-109">If you need to change default sequencing parameters, you must either manually modify a sequenced application package or re-sequence the application.</span></span>

 

<span data-ttu-id="8f23b-110">Todas as modificações subsequentes em pacotes de aplicativos sequenciados existentes devem ser feitas usando o assistente de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="8f23b-110">All subsequent modifications to existing sequenced application packages must be made using the sequencing wizard.</span></span>

## <span data-ttu-id="8f23b-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="8f23b-111">Prerequisites</span></span>


<span data-ttu-id="8f23b-112">Para sequenciar um aplicativo usando o prompt de comando, as seguintes condições devem ser atendidas:</span><span class="sxs-lookup"><span data-stu-id="8f23b-112">To sequence an application by using the command prompt, the following conditions must be met:</span></span>

-   <span data-ttu-id="8f23b-113">O aplicativo que está prestes a ser sequenciado não deve exigir alterações ou soluções alternativas feitas a ele fora do instalador ou do pacote do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8f23b-113">The application that is about to be sequenced must not require changes or workarounds made to it outside the installer or Windows Installer package.</span></span>

-   <span data-ttu-id="8f23b-114">Antes de sequenciamento, você deve preparar uma lista de arquivos em lotes para criar pacotes de aplicativos sequenciados.</span><span class="sxs-lookup"><span data-stu-id="8f23b-114">Before sequencing, you must prepare a list of batch files for creating the sequenced application packages.</span></span>

-   <span data-ttu-id="8f23b-115">Revise para obter mais informações sobre os parâmetros de linha de comando, consulte [parâmetros de linha de comando](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8f23b-115">Review For more information about the command line parameters, see [Command-Line Parameters](command-line-parameters.md).</span></span>

-   <span data-ttu-id="8f23b-116">Revise os erros que podem ser exibidos ao criar um pacote de aplicativo sequenciado usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="8f23b-116">Review the errors that might be displayed when creating a sequenced application package by using the command line.</span></span> <span data-ttu-id="8f23b-117">Para obter mais informações, consulte esses erros, consulte [erros de linha de comando](command-line-errors.md).</span><span class="sxs-lookup"><span data-stu-id="8f23b-117">For more information, see these errors, see [Command-Line Errors](command-line-errors.md).</span></span>

## <span data-ttu-id="8f23b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f23b-118">Related topics</span></span>


[<span data-ttu-id="8f23b-119">Como gerenciar aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="8f23b-119">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





