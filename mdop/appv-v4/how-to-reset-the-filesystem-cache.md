---
title: Como redefinir o cache do FileSystem
description: Como redefinir o cache do FileSystem
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796980"
---
# <span data-ttu-id="890bf-103">Como redefinir o cache do FileSystem</span><span class="sxs-lookup"><span data-stu-id="890bf-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="890bf-104">A redefinição do cache do sistema de arquivos não é algo que geralmente deve ser necessária.</span><span class="sxs-lookup"><span data-stu-id="890bf-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="890bf-105">No entanto, se precisar redefinir completamente o cache do sistema de arquivos, talvez para fins de solução de problemas, você pode usar o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="890bf-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="890bf-106">São necessários direitos administrativos para executar esta ação.</span><span class="sxs-lookup"><span data-stu-id="890bf-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="890bf-107">Para redefinir o cache do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="890bf-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="890bf-108">Defina o seguinte valor do registro como 0 (zero):</span><span class="sxs-lookup"><span data-stu-id="890bf-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="890bf-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="890bf-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="890bf-110">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="890bf-110">Restart the computer.</span></span>

## <span data-ttu-id="890bf-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="890bf-111">Related topics</span></span>


[<span data-ttu-id="890bf-112">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="890bf-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





