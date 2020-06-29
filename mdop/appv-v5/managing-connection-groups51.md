---
title: Gerenciando grupos de conexão
description: Gerenciando grupos de conexão
author: dansimp
ms.assetid: 22c9d3cb-7246-4173-9742-4ba1c24b0a6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c89fab70fa13a66c2c27b8d014a5bac034f21bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796283"
---
# <span data-ttu-id="73656-103">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="73656-103">Managing Connection Groups</span></span>


<span data-ttu-id="73656-104">Os grupos de conexão permitem que os aplicativos dentro de um pacote interajam uns com os outros no ambiente virtual, enquanto restam isolado do restante do sistema.</span><span class="sxs-lookup"><span data-stu-id="73656-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="73656-105">Ao usar grupos de conexão, os administradores podem gerenciar pacotes independentemente e podem evitar ter que adicionar o mesmo aplicativo várias vezes a um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="73656-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="73656-106">**Observação**  Em algumas versões anteriores do App-V, os grupos de conexão eram referidos como composição do pacote dinâmico.</span><span class="sxs-lookup"><span data-stu-id="73656-106">**Note** In some previous versions of App-V, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="73656-107">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="73656-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment51.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment51.md)"><span data-ttu-id="73656-108">Sobre o ambiente Virtual do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="73656-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="73656-109">Descreve o ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="73656-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file51.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file51.md)"><span data-ttu-id="73656-110">Sobre o arquivo do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="73656-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="73656-111">Descreve o arquivo de grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="73656-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group51.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group51.md)"><span data-ttu-id="73656-112">Como criar um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="73656-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="73656-113">Explica como criar um novo grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="73656-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md)"><span data-ttu-id="73656-114">Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados</span><span class="sxs-lookup"><span data-stu-id="73656-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="73656-115">Explica como criar um novo grupo de conexão que contém uma combinação de pacotes que são publicados para o usuário e publicadas globalmente.</span><span class="sxs-lookup"><span data-stu-id="73656-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group51.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group51.md)"><span data-ttu-id="73656-116">Como excluir um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="73656-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="73656-117">Explica como excluir um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="73656-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group51.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group51.md)"><span data-ttu-id="73656-118">Como publicar um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="73656-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="73656-119">Explica como publicar um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="73656-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="73656-120">Outros recursos para grupos de conexão do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="73656-120">Other resources for App-V 5.1 connection groups</span></span>


-   [<span data-ttu-id="73656-121">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="73656-121">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





