---
title: Como modificar a configuração do cliente usando o PowerShell
description: Como modificar a configuração do cliente usando o PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796347"
---
# <span data-ttu-id="089aa-103">Como modificar a configuração do cliente usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="089aa-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="089aa-104">Use o procedimento a seguir para configurar a configuração do cliente do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="089aa-104">Use the following procedure to configure the App-V 5.0 client configuration.</span></span>

**<span data-ttu-id="089aa-105">Para modificar a configuração do cliente do App-V 5,0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="089aa-105">To modify App-V 5.0 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="089aa-106">Para definir as configurações do cliente usando o PowerShell, use o cmdlet **set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="089aa-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span>

2.  <span data-ttu-id="089aa-107">Para modificar a configuração do cliente, abra um prompt de comando do PowerShell e execute o cmdlet **set-AppvClientConfiguration** a seguir com todos os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="089aa-107">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="089aa-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="089aa-108">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="089aa-109">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="089aa-109">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="089aa-110">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="089aa-110">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="089aa-111">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="089aa-111">Got an App-V issue?</span></span>** <span data-ttu-id="089aa-112">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="089aa-112">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="089aa-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="089aa-113">Related topics</span></span>


[<span data-ttu-id="089aa-114">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="089aa-114">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





