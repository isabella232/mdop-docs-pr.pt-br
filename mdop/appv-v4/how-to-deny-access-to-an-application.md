---
title: Como negar acesso a um aplicativo
description: Como negar acesso a um aplicativo
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797141"
---
# <span data-ttu-id="adfcb-103">Como negar acesso a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="adfcb-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="adfcb-104">Os usuários devem estar na lista de **permissões de acesso** do aplicativo para carregar e usar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="adfcb-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="adfcb-105">Embora o console de gerenciamento do aplicativo virtualização do aplicativo não dê suporte à negação explícita de um acesso a um grupo de usuários a um aplicativo, você pode remover os grupos de usuários das propriedades de um aplicativo para conseguir isso.</span><span class="sxs-lookup"><span data-stu-id="adfcb-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="adfcb-106">Para negar acesso a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="adfcb-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="adfcb-107">Para um aplicativo existente, clique no nó **aplicativos** no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="adfcb-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="adfcb-108">Clique com o botão direito do mouse em um aplicativo no painel direito e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="adfcb-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="adfcb-109">Em seguida, selecione a guia **permissões de acesso** .</span><span class="sxs-lookup"><span data-stu-id="adfcb-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="adfcb-110">Para remover o acesso de um grupo de usuários, realce o grupo de usuários e clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="adfcb-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="adfcb-111">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="adfcb-111">Click **OK**.</span></span>

    <span data-ttu-id="adfcb-112">**Observação**  Para controlar o acesso aos aplicativos, você também pode limitar as licenças do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="adfcb-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="adfcb-113">A configuração dos grupos de usuários adequados nos serviços de domínio Active Directory fornece a maneira mais fácil de conceder e negar acesso a conjuntos de usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="adfcb-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="adfcb-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adfcb-114">Related topics</span></span>


[<span data-ttu-id="adfcb-115">Como conceder acesso a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="adfcb-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="adfcb-116">Como gerenciar licenças de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="adfcb-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="adfcb-117">Como gerenciar aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="adfcb-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





