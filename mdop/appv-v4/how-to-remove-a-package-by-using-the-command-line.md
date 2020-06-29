---
title: Como remover um pacote usando a linha de comando
description: Como remover um pacote usando a linha de comando
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797002"
---
# <span data-ttu-id="dd853-103">Como remover um pacote usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="dd853-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="dd853-104">Você pode usar os seguintes procedimentos de linha de comando para excluir um pacote de aplicativo virtual do cliente Application Virtualization (App-V) em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="dd853-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="dd853-105">Para excluir um pacote de aplicativo virtual para todos os usuários</span><span class="sxs-lookup"><span data-stu-id="dd853-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="dd853-106">Se o pacote foi adicionado anteriormente para todos os usuários usando a opção/GLOBAL, use o comando a seguir para excluir o pacote e os tipos de arquivo e atalhos globais.</span><span class="sxs-lookup"><span data-stu-id="dd853-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="dd853-107">É necessário ter direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="dd853-107">Administrator rights are required.</span></span> <span data-ttu-id="dd853-108">A opção/GLOBAL não é necessária nesse caso porque o comando sempre executa uma exclusão global do pacote.</span><span class="sxs-lookup"><span data-stu-id="dd853-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="dd853-109">Para excluir um pacote adicionado anteriormente para usuários individuais</span><span class="sxs-lookup"><span data-stu-id="dd853-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="dd853-110">Se o pacote foi adicionado anteriormente para usuários individuais, você tem várias opções.</span><span class="sxs-lookup"><span data-stu-id="dd853-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="dd853-111">Execute o seguinte comando uma vez na conta de usuário de cada pessoa na qual o pacote foi publicado.</span><span class="sxs-lookup"><span data-stu-id="dd853-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="dd853-112">Isso recusa o acesso do usuário aos aplicativos se eles se em outro computador.</span><span class="sxs-lookup"><span data-stu-id="dd853-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="dd853-113">Ele exclui as configurações, atalhos e tipos de arquivo do usuário específico do perfil, e ele interrompe as cargas em segundo plano sob o contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd853-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="dd853-114">Você também pode executar o seguinte comando sob a conta de usuário de cada pessoa na qual o pacote foi publicado.</span><span class="sxs-lookup"><span data-stu-id="dd853-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="dd853-115">Em seguida, execute esse comando para o pacote.</span><span class="sxs-lookup"><span data-stu-id="dd853-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="dd853-116">Isso remove completamente o pacote e exclui todas as configurações de usuário, atalhos e tipos de arquivo dos perfis.</span><span class="sxs-lookup"><span data-stu-id="dd853-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="dd853-117">Se o pacote for adicionado novamente, os usuários precisarão especificar as configurações novamente.</span><span class="sxs-lookup"><span data-stu-id="dd853-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="dd853-118">Somente a permissão "excluir aplicativos" (**DeleteApp**) é necessária para executar este comando.</span><span class="sxs-lookup"><span data-stu-id="dd853-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="dd853-119">Como terceira alternativa, você pode simplesmente executar o comando **excluir pacote** sem usar o comando **Cancelar publicação do pacote** .</span><span class="sxs-lookup"><span data-stu-id="dd853-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="dd853-120">Nesse caso, os tipos de arquivo e atalhos de cada usuário são ocultos, em vez de excluídos, e as configurações do usuário são mantidas.</span><span class="sxs-lookup"><span data-stu-id="dd853-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="dd853-121">Isso significa que, se o pacote for adicionado novamente para o usuário, os tipos de arquivo e atalhos serão restaurados e as configurações do usuário serão reaplicadas.</span><span class="sxs-lookup"><span data-stu-id="dd853-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="dd853-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd853-122">Related topics</span></span>


[<span data-ttu-id="dd853-123">Como adicionar um pacote usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="dd853-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="dd853-124">Como excluir todos os aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="dd853-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





