---
title: Referência de comando SFTMIME
description: Referência de comando SFTMIME
author: dansimp
ms.assetid: a4a69228-9dd3-4623-b773-899d03c0cf10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47aac9110febaf3f349461d74fef840326b1c6e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796707"
---
# <span data-ttu-id="9c693-103">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="9c693-103">SFTMIME Command Reference</span></span>


<span data-ttu-id="9c693-104">SFTMIME é uma interface de linha de comando usada pelo Application Virtualization (App-V) que permite que você gerencie muitos detalhes de configuração do cliente.</span><span class="sxs-lookup"><span data-stu-id="9c693-104">SFTMIME is a command-line interface used by Application Virtualization (App-V) that enables you to manage many client configuration details.</span></span> <span data-ttu-id="9c693-105">Esta seção contém todos os comandos e seus parâmetros, com uma breve descrição de cada um deles.</span><span class="sxs-lookup"><span data-stu-id="9c693-105">This section contains all the commands and their parameters, with a brief description of each.</span></span>

**<span data-ttu-id="9c693-106">Importante</span><span class="sxs-lookup"><span data-stu-id="9c693-106">Important</span></span>**  
-   <span data-ttu-id="9c693-107">Todos os caracteres de barra invertida devem ter escape usando uma barra invertida precedente ou o caminho não será analisado corretamente.</span><span class="sxs-lookup"><span data-stu-id="9c693-107">All backslash characters must be escaped using a preceding backslash, or the path will not be parsed correctly.</span></span>

-   <span data-ttu-id="9c693-108">Se você estiver usando um programa de chamada para invocar SFTMIME com **CreateProcess**, deve garantir que o primeiro parâmetro é o caminho para sftmime.exe.</span><span class="sxs-lookup"><span data-stu-id="9c693-108">If you are using a calling program to invoke SFTMIME with **CreateProcess**, you must ensure that the first parameter is the path to sftmime.exe.</span></span>

-   <span data-ttu-id="9c693-109">A saída do comando SFTMIME **Query obj** não pode ser canalizada para o comando **findstr** para pesquisar uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9c693-109">The output of the SFTMIME **QUERY OBJ** command cannot be piped to the **findstr** command to search for a string.</span></span>

-   <span data-ttu-id="9c693-110">O uso da opção **global** exige direitos de administrador local.</span><span class="sxs-lookup"><span data-stu-id="9c693-110">Use of the **GLOBAL** switch requires local administrator rights.</span></span>

-   <span data-ttu-id="9c693-111">O uso de caminhos curtos e caminhos relativos pode levar a resultados inesperados e deve ser evitado.</span><span class="sxs-lookup"><span data-stu-id="9c693-111">Use of short paths and relative paths can lead to unexpected results and should be avoided.</span></span> <span data-ttu-id="9c693-112">Sempre use caminhos completos.</span><span class="sxs-lookup"><span data-stu-id="9c693-112">Always use full paths.</span></span>

 

## <span data-ttu-id="9c693-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9c693-113">In This Section</span></span>


[<span data-ttu-id="9c693-114">ADD APP</span><span class="sxs-lookup"><span data-stu-id="9c693-114">ADD APP</span></span>](add-app.md)

[<span data-ttu-id="9c693-115">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-115">ADD PACKAGE</span></span>](add-package.md)

[<span data-ttu-id="9c693-116">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="9c693-116">ADD SERVER</span></span>](add-server.md)

[<span data-ttu-id="9c693-117">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="9c693-117">ADD TYPE</span></span>](add-type.md)

[<span data-ttu-id="9c693-118">CLEAR APP</span><span class="sxs-lookup"><span data-stu-id="9c693-118">CLEAR APP</span></span>](clear-app.md)

[<span data-ttu-id="9c693-119">CLEAR OBJ</span><span class="sxs-lookup"><span data-stu-id="9c693-119">CLEAR OBJ</span></span>](clear-obj.md)

[<span data-ttu-id="9c693-120">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="9c693-120">CONFIGURE APP</span></span>](configure-app.md)

[<span data-ttu-id="9c693-121">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-121">CONFIGURE PACKAGE</span></span>](configure-package.md)

[<span data-ttu-id="9c693-122">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="9c693-122">CONFIGURE SERVER</span></span>](configure-server.md)

[<span data-ttu-id="9c693-123">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="9c693-123">CONFIGURE TYPE</span></span>](configure-type.md)

[<span data-ttu-id="9c693-124">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="9c693-124">DELETE APP</span></span>](delete-app.md)

[<span data-ttu-id="9c693-125">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="9c693-125">DELETE OBJ</span></span>](delete-obj.md)

[<span data-ttu-id="9c693-126">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-126">DELETE PACKAGE</span></span>](delete-package.md)

[<span data-ttu-id="9c693-127">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="9c693-127">DELETE SERVER</span></span>](delete-server.md)

[<span data-ttu-id="9c693-128">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="9c693-128">DELETE TYPE</span></span>](delete-type.md)

[<span data-ttu-id="9c693-129">HELP</span><span class="sxs-lookup"><span data-stu-id="9c693-129">HELP</span></span>](help.md)

[<span data-ttu-id="9c693-130">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="9c693-130">LOAD APP</span></span>](load-app.md)

[<span data-ttu-id="9c693-131">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-131">LOAD PACKAGE</span></span>](load-package.md)

[<span data-ttu-id="9c693-132">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="9c693-132">LOCK APP</span></span>](lock-app.md)

[<span data-ttu-id="9c693-133">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="9c693-133">PUBLISH APP</span></span>](publish-app.md)

[<span data-ttu-id="9c693-134">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-134">PUBLISH PACKAGE</span></span>](publish-package.md)

[<span data-ttu-id="9c693-135">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="9c693-135">QUERY OBJ</span></span>](query-obj.md)

[<span data-ttu-id="9c693-136">REFRESH SERVER</span><span class="sxs-lookup"><span data-stu-id="9c693-136">REFRESH SERVER</span></span>](refresh-server.md)

[<span data-ttu-id="9c693-137">REPAIR APP</span><span class="sxs-lookup"><span data-stu-id="9c693-137">REPAIR APP</span></span>](repair-app.md)

[<span data-ttu-id="9c693-138">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="9c693-138">UNLOAD APP</span></span>](unload-app.md)

[<span data-ttu-id="9c693-139">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-139">UNLOAD PACKAGE</span></span>](unload-package.md)

[<span data-ttu-id="9c693-140">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="9c693-140">UNLOCK APP</span></span>](unlock-app.md)

[<span data-ttu-id="9c693-141">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9c693-141">UNPUBLISH PACKAGE</span></span>](unpublish-package.md)

 

 





