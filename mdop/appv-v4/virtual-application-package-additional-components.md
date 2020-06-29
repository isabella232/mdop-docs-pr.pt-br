---
title: Componentes adicionais do pacote de aplicativo virtual
description: Componentes adicionais do pacote de aplicativo virtual
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796653"
---
# <span data-ttu-id="7d257-103">Componentes adicionais do pacote de aplicativo virtual</span><span class="sxs-lookup"><span data-stu-id="7d257-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="7d257-104">O sequenciador App-V detectou um diretório que contém arquivos executáveis de 64 bits e 32 bits e/ou biblioteca de vínculo dinâmico (. dll) que dependem do mesmo assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="7d257-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="7d257-105">Geralmente, o sequenciador cria assemblies lado a lado privados para todos os assemblies públicos que são usados pelo pacote; no entanto, não é possível criar versões de 32 bits e de 64 bits dos assemblies particulares no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="7d257-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="7d257-106">Se o sequenciador detectar um único conflito, ele irá executar as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="7d257-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="7d257-107">Remova todos os assemblies particulares de 64 bits existentes em todo o pacote, independentemente de o diretório ter ou não conflito.</span><span class="sxs-lookup"><span data-stu-id="7d257-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="7d257-108">Crie somente versões de 32 bits dos conjuntos lado a lado privados.</span><span class="sxs-lookup"><span data-stu-id="7d257-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="7d257-109">Você deve instalar nativamente as versões públicas de todos os assemblies de 64 bits necessários no computador que executa o sequenciador e em todos os computadores cliente do App-V.</span><span class="sxs-lookup"><span data-stu-id="7d257-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="7d257-110">Para localizar os assemblies públicos existentes necessários, abra o diretório onde o pacote foi salvo e procure na pasta **VFS** .</span><span class="sxs-lookup"><span data-stu-id="7d257-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="7d257-111">Por exemplo, se a raiz do pacote for **Q:\\MyApp**, quando você sequenciar o aplicativo, procure em **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** e localize todos os assemblies públicos existentes.</span><span class="sxs-lookup"><span data-stu-id="7d257-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="7d257-112">As versões de 64 bits desses arquivos sempre serão iniciadas com o seguinte texto no início do nome do manifesto: **AMD64...**.</span><span class="sxs-lookup"><span data-stu-id="7d257-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="7d257-113">O nome exato e a versão do assembly podem ser encontrados no arquivo de manifesto associado.</span><span class="sxs-lookup"><span data-stu-id="7d257-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="7d257-114">Use qualquer um dos links a seguir para baixar e instalar a versão correta dos pré-requisitos obrigatórios:</span><span class="sxs-lookup"><span data-stu-id="7d257-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="7d257-115">Pacote redistribuível do Microsoft Visual C++ 2005 (x64)</span><span class="sxs-lookup"><span data-stu-id="7d257-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="7d257-116">Pacote redistribuível do Microsoft Visual C++ 2005 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="7d257-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="7d257-117">Pacote redistribuível do Microsoft Visual C++ 2008 (x64)</span><span class="sxs-lookup"><span data-stu-id="7d257-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="7d257-118">Pacote redistribuível do Microsoft Visual C++ 2008 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="7d257-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





