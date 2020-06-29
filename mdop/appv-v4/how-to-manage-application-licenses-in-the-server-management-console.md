---
title: Como gerenciar licenças de aplicativos no Server Management Console
description: Como gerenciar licenças de aplicativos no Server Management Console
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797082"
---
# <span data-ttu-id="f31c7-103">Como gerenciar licenças de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="f31c7-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="f31c7-104">O console de gerenciamento de servidor do Application Virtualization é a interface que você usa para gerenciar a plataforma de virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f31c7-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="f31c7-105">Nele, você pode adicionar, remover, configurar e controlar grupos de licenças de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f31c7-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="f31c7-106">**Importante**  Se a configuração da raiz da fonte de aplicativos do aplicativo cliente (ASR) do App-V estiver configurada para usar qualquer tipo de fonte de transmissão diferente do servidor de gerenciamento, por exemplo, um servidor de streaming, um servidor IIS ou um servidor de arquivos, o servidor de gerenciamento não poderá impor sua política de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="f31c7-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="f31c7-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f31c7-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="f31c7-108">Como criar um grupo de licenças de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f31c7-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="f31c7-109">Fornece um procedimento para criar um novo aplicativo em um grupo de licenças.</span><span class="sxs-lookup"><span data-stu-id="f31c7-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="f31c7-110">Como associar um aplicativo a um grupo de licenças</span><span class="sxs-lookup"><span data-stu-id="f31c7-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="f31c7-111">Fornece um procedimento para adicionar um aplicativo a um grupo de licenças.</span><span class="sxs-lookup"><span data-stu-id="f31c7-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="f31c7-112">Como remover um aplicativo de um grupo de licenças</span><span class="sxs-lookup"><span data-stu-id="f31c7-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="f31c7-113">Fornece um procedimento para remover um aplicativo de um grupo de licenças.</span><span class="sxs-lookup"><span data-stu-id="f31c7-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="f31c7-114">Como remover um grupo de licenças de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f31c7-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="f31c7-115">Esta seção inclui as etapas necessárias para excluir um grupo de licenças de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f31c7-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="f31c7-116">Como configurar um grupo de licenças ilimitadas</span><span class="sxs-lookup"><span data-stu-id="f31c7-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="f31c7-117">Fornece um procedimento para criar um novo grupo de licença ilimitado, permitindo que um número ilimitado de usuários acesse os aplicativos no grupo.</span><span class="sxs-lookup"><span data-stu-id="f31c7-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="f31c7-118">Como configurar um grupo de licenças simultâneas</span><span class="sxs-lookup"><span data-stu-id="f31c7-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="f31c7-119">Fornece um procedimento para criar um novo grupo de licenças simultâneas, permitindo que um número específico de usuários simultâneos acesse os aplicativos do grupo.</span><span class="sxs-lookup"><span data-stu-id="f31c7-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="f31c7-120">Como configurar um grupo de licenças nomeadas</span><span class="sxs-lookup"><span data-stu-id="f31c7-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="f31c7-121">Fornece um procedimento para criar um novo grupo de licença ilimitado, permitindo que usuários específicos acessem os aplicativos no grupo.</span><span class="sxs-lookup"><span data-stu-id="f31c7-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="f31c7-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f31c7-122">Related topics</span></span>


[<span data-ttu-id="f31c7-123">Como realizar tarefas administrativas no Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="f31c7-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





