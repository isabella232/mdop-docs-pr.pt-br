---
title: Como alterar o tamanho do cache do FileSystem
description: Como alterar o tamanho do cache do FileSystem
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797238"
---
# <span data-ttu-id="ef625-103">Como alterar o tamanho do cache do FileSystem</span><span class="sxs-lookup"><span data-stu-id="ef625-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="ef625-104">Você pode alterar o tamanho do cache do sistema de arquivos usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ef625-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="ef625-105">Essa ação requer uma redefinição completa do cache e requer direitos administrativos.</span><span class="sxs-lookup"><span data-stu-id="ef625-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="ef625-106">Para alterar o tamanho do cache do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="ef625-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="ef625-107">Defina o seguinte valor do registro como 0 (zero):</span><span class="sxs-lookup"><span data-stu-id="ef625-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="ef625-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="ef625-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="ef625-109">Defina o valor do registro a seguir para o tamanho máximo do cache, em MB, que é necessário para manter os pacotes — por exemplo, 8192 MB:</span><span class="sxs-lookup"><span data-stu-id="ef625-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="ef625-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span><span class="sxs-lookup"><span data-stu-id="ef625-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="ef625-111">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="ef625-111">Restart the computer.</span></span>

## <span data-ttu-id="ef625-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef625-112">Related topics</span></span>


[<span data-ttu-id="ef625-113">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="ef625-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





