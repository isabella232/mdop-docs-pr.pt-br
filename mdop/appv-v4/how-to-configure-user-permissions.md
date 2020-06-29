---
title: Como configurar permissões de usuário
description: Como configurar permissões de usuário
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797184"
---
# <span data-ttu-id="caebc-103">Como configurar permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="caebc-103">How to Configure User Permissions</span></span>


<span data-ttu-id="caebc-104">Você pode habilitar e desabilitar algumas ações para usuários que não têm direitos administrativos editando os valores de chave na chave do registro **Permissions** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions).</span><span class="sxs-lookup"><span data-stu-id="caebc-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="caebc-105">Essa chave é projetada principalmente para ajudar a impedir que os usuários façam erros em vez de fornecer qualquer segurança especial, pois os usuários com direitos administrativos podem editar qualquer um desses valores de chave.</span><span class="sxs-lookup"><span data-stu-id="caebc-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="caebc-106">Os procedimentos a seguir são exemplos de como alterar os valores de chave.</span><span class="sxs-lookup"><span data-stu-id="caebc-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="caebc-107">Para obter mais informações sobre as chaves e os valores do cliente do Application Virtualization (App-V), consulte <https://go.microsoft.com/fwlink/?LinkId=121528> .</span><span class="sxs-lookup"><span data-stu-id="caebc-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="caebc-108">Para alterar permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="caebc-108">To change user permissions</span></span>**

1.  <span data-ttu-id="caebc-109">Para permitir que os usuários escolham executar o cliente no modo offline, defina o valor da chave a seguir como 1:</span><span class="sxs-lookup"><span data-stu-id="caebc-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="caebc-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="caebc-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="caebc-111">Para permitir que os usuários visualizem todos os aplicativos por meio da interface do usuário, defina o valor da chave a seguir como 1.</span><span class="sxs-lookup"><span data-stu-id="caebc-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="caebc-112">Definir o valor como 0 (zero) permite que os usuários vejam apenas os aplicativos que estão disponíveis para eles.</span><span class="sxs-lookup"><span data-stu-id="caebc-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="caebc-113">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="caebc-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="caebc-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="caebc-114">Related topics</span></span>


[<span data-ttu-id="caebc-115">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="caebc-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="caebc-116">Permissões de acesso de usuário no Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="caebc-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





