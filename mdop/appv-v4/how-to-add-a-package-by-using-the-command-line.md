---
title: Como adicionar um pacote usando a linha de comando
description: Como adicionar um pacote usando a linha de comando
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797919"
---
# <span data-ttu-id="57b04-103">Como adicionar um pacote usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="57b04-103">How to Add a Package by Using the Command Line</span></span>


<span data-ttu-id="57b04-104">Os procedimentos a seguir listam as etapas necessárias para adicionar um pacote de aplicativo virtual ao cliente do Application Virtualization (App-V) em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="57b04-104">The following procedures list the steps that are necessary to add a virtual application package to the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="57b04-105">Para adicionar um pacote de aplicativo virtual para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="57b04-105">To add a virtual application package for a specific user</span></span>**

-   <span data-ttu-id="57b04-106">Execute o seguinte comando na conta de usuário da pessoa que está para obter o pacote.</span><span class="sxs-lookup"><span data-stu-id="57b04-106">Run the following command under the user account of the person who is to get the package.</span></span> <span data-ttu-id="57b04-107">O comando adiciona e publica o pacote para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="57b04-107">The command adds and publishes the package for that user.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**<span data-ttu-id="57b04-108">Para adicionar um pacote de aplicativo virtual para todos os usuários</span><span class="sxs-lookup"><span data-stu-id="57b04-108">To add a virtual application package for all users</span></span>**

-   <span data-ttu-id="57b04-109">Execute o seguinte comando em uma conta com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="57b04-109">Run the following command under an account that has administrator rights.</span></span> <span data-ttu-id="57b04-110">O pacote é adicionado e publicado para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="57b04-110">The package is added and published for all users on the computer.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**<span data-ttu-id="57b04-111">Para adicionar um pacote usando um sistema de distribuição de software eletrônico</span><span class="sxs-lookup"><span data-stu-id="57b04-111">To add a package using an electronic software distribution system</span></span>**

1.  <span data-ttu-id="57b04-112">Se você estiver usando um sistema de distribuição de software eletrônico que executa os comandos na conta do **sistema** do computador, o pacote será publicado somente para essa conta, a menos que você use a opção/global</span><span class="sxs-lookup"><span data-stu-id="57b04-112">If you are using an electronic software distribution system that runs the commands under the computer’s **SYSTEM** account, the package is published for that account only, unless you use the /GLOBAL switch.</span></span> <span data-ttu-id="57b04-113">Execute o seguinte comando para adicionar e publicar o pacote para todos os usuários do computador:</span><span class="sxs-lookup"><span data-stu-id="57b04-113">Run the following command to add and publish the package for all users on the computer:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    <span data-ttu-id="57b04-114">Se você quiser adicionar o pacote somente para usuários específicos, execute o comando **Adicionar pacote** e, em seguida, publique explicitamente o pacote para cada usuário executando o seguinte comando de **pacote de publicação** na conta de usuário de cada pessoa:</span><span class="sxs-lookup"><span data-stu-id="57b04-114">If you want to add the package for specific users only, run the **ADD PACKAGE** command, and then explicitly publish the package for each user by running the following **PUBLISH PACKAGE** command under each person’s user account:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    <span data-ttu-id="57b04-115">Publicar o pacote sem o parâmetro GLOBAL concede ao usuário acesso aos aplicativos no pacote e publica os tipos de arquivo e atalhos listados no manifesto para o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="57b04-115">Publishing the package without the GLOBAL parameter grants the user access to the applications in the package and publishes the file types and shortcuts that are listed in the manifest to the user’s profile.</span></span> <span data-ttu-id="57b04-116">As permissões necessárias são "gerenciar associações de tipo de arquivo" (**ManageTypes**) e "publicar atalhos" (**PublishShortcut**).</span><span class="sxs-lookup"><span data-stu-id="57b04-116">Permissions required are “Manage file type associations” (**ManageTypes**) and “Publish shortcuts” (**PublishShortcut**).</span></span>

## <span data-ttu-id="57b04-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57b04-117">Related topics</span></span>


[<span data-ttu-id="57b04-118">Como excluir todos os aplicativos virtuais usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="57b04-118">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[<span data-ttu-id="57b04-119">Como remover um pacote usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="57b04-119">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





