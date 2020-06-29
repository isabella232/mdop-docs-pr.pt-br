---
title: Como excluir todos os aplicativos virtuais usando a linha de comando
description: Como excluir todos os aplicativos virtuais usando a linha de comando
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797145"
---
# <span data-ttu-id="b1323-103">Como excluir todos os aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="b1323-103">How to Delete All Virtual Applications by Using the Command Line</span></span>


<span data-ttu-id="b1323-104">Você pode usar o procedimento a seguir para excluir todos os aplicativos virtuais de um computador específico.</span><span class="sxs-lookup"><span data-stu-id="b1323-104">You can use the following procedure to delete all virtual applications from a specific computer.</span></span>

<span data-ttu-id="b1323-105">**Observação**  Quando todos os aplicativos são excluídos de um pacote, o cliente do Application Virtualization (App-V) também exclui o pacote.</span><span class="sxs-lookup"><span data-stu-id="b1323-105">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

 

**<span data-ttu-id="b1323-106">Para excluir todos os aplicativos</span><span class="sxs-lookup"><span data-stu-id="b1323-106">To delete all applications</span></span>**

-   <span data-ttu-id="b1323-107">Execute o comando a seguir para excluir todos os aplicativos da conta de usuário sob a qual o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="b1323-107">Run the following command to delete all applications for the user account under which the command is run.</span></span> <span data-ttu-id="b1323-108">Se você executar o comando com a opção/GLOBAL opcional, usando uma conta com direitos administrativos, todos os aplicativos serão excluídos para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="b1323-108">If you run the command with the optional /GLOBAL switch, using an account with administrative rights, all applications are deleted for all users.</span></span>

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    <span data-ttu-id="b1323-109">**Observação**  Quando todos os aplicativos são excluídos de um pacote, o cliente do Application Virtualization (App-V) também exclui o pacote.</span><span class="sxs-lookup"><span data-stu-id="b1323-109">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

     

## <span data-ttu-id="b1323-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1323-110">Related topics</span></span>


[<span data-ttu-id="b1323-111">Como adicionar um pacote usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="b1323-111">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="b1323-112">Como remover um pacote usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="b1323-112">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





