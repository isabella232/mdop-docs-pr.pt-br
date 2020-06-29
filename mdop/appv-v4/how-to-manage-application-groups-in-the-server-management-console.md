---
title: Como gerenciar grupos de aplicativos no Server Management Console
description: Como gerenciar grupos de aplicativos no Server Management Console
author: dansimp
ms.assetid: 46997971-bdc8-4565-aefd-f47e90d6d7a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 59a357d93ea63cc728f59a0633b7a5b9953aad14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797078"
---
# <span data-ttu-id="ec5d5-103">Como gerenciar grupos de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ec5d5-103">How to Manage Application Groups in the Server Management Console</span></span>


<span data-ttu-id="ec5d5-104">Você pode exibir e gerenciar um ou mais aplicativos em grupos de aplicativos no console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-104">You can display and manage one or more applications in application groups in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="ec5d5-105">Isso pode ser útil quando você deseja fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ec5d5-105">This can be useful when you want to do the following:</span></span>

-   <span data-ttu-id="ec5d5-106">Organize muitos aplicativos em subgrupos mais gerenciáveis.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-106">Organize many applications into more manageable subgroups.</span></span>

-   <span data-ttu-id="ec5d5-107">Crie grupos de aplicativos específicos para um departamento ou outra divisão da empresa.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-107">Create groups of applications specific to a department or other company division.</span></span>

-   <span data-ttu-id="ec5d5-108">Agrupe tipos semelhantes de aplicativos, como software financeiro.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-108">Group similar types of applications, such as financial software.</span></span>

-   <span data-ttu-id="ec5d5-109">Simplifique as permissões de acesso ou o gerenciamento de licenças por grupo.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-109">Simplify access permissions or license management by group.</span></span>

-   <span data-ttu-id="ec5d5-110">Alterar as propriedades de aplicativos e grupos de aplicativos em um grupo simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-110">Change the properties of applications and application groups within a group simultaneously.</span></span>

<span data-ttu-id="ec5d5-111">Você pode criar um grupo, colocá-lo onde deseja na árvore de **aplicativos** do console e importar aplicativos para o grupo.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-111">You can create a group, place it where you would like in the console's **Applications** tree, and import applications to the group.</span></span> <span data-ttu-id="ec5d5-112">Em seguida, você pode configurar e gerenciar as propriedades do grupo para afetar todos os seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-112">Then you can configure and manage the group's properties to affect all of its applications.</span></span> <span data-ttu-id="ec5d5-113">Você também pode mover aplicativos entre grupos.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-113">You can also move applications among groups.</span></span>

<span data-ttu-id="ec5d5-114">**Observação**  Mover aplicativos para grupos não afeta os locais dos arquivos (SFT, OSD ou SPRJ) no sistema de arquivos do servidor.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-114">**Note** Moving applications into groups does not affect the locations of their files (SFT, OSD, or SPRJ) on the server's file system.</span></span>

 

## <span data-ttu-id="ec5d5-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ec5d5-115">In This Section</span></span>


<a href="" id="how-to-create-an-application-group"></a>[<span data-ttu-id="ec5d5-116">Como criar um grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ec5d5-116">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)  
<span data-ttu-id="ec5d5-117">Fornece instruções passo a passo para a criação de um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-117">Provides step-by-step instructions for creating an application group.</span></span>

<a href="" id="how-to-move-an-application-group"></a>[<span data-ttu-id="ec5d5-118">Como mover um grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ec5d5-118">How to Move an Application Group</span></span>](how-to-move-an-application-group.md)  
<span data-ttu-id="ec5d5-119">Fornece instruções passo a passo para mover um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-119">Provides step-by-step instructions for moving an application group.</span></span>

<a href="" id="how-to-rename-an-application-group"></a>[<span data-ttu-id="ec5d5-120">Como renomear um grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ec5d5-120">How to Rename an Application Group</span></span>](how-to-rename-an-application-group.md)  
<span data-ttu-id="ec5d5-121">Fornece instruções passo a passo para renomear um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-121">Provides step-by-step instructions for renaming an application group.</span></span>

<a href="" id="how-to-remove-an-application-group"></a>[<span data-ttu-id="ec5d5-122">Como remover um grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ec5d5-122">How to Remove an Application Group</span></span>](how-to-remove-an-application-group.md)  
<span data-ttu-id="ec5d5-123">Fornece instruções passo a passo para remover ou excluir um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ec5d5-123">Provides step-by-step instructions for removing or deleting an application group.</span></span>

## <span data-ttu-id="ec5d5-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec5d5-124">Related topics</span></span>


[<span data-ttu-id="ec5d5-125">Como gerenciar aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ec5d5-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="ec5d5-126">Como realizar tarefas administrativas no Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ec5d5-126">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





