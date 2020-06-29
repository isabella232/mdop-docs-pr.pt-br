---
title: Gerenciando grupos de conexão
description: Gerenciando grupos de conexão
author: dansimp
ms.assetid: 1a9c8f26-f421-4b70-b7e2-da8118e8198c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2e57b9dbe56072e6049e8fabef5705c374d022c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796285"
---
# <span data-ttu-id="06fb9-103">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="06fb9-103">Managing Connection Groups</span></span>


<span data-ttu-id="06fb9-104">Os grupos de conexão permitem que os aplicativos dentro de um pacote interajam uns com os outros no ambiente virtual, enquanto restam isolado do restante do sistema.</span><span class="sxs-lookup"><span data-stu-id="06fb9-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="06fb9-105">Ao usar grupos de conexão, os administradores podem gerenciar pacotes independentemente e podem evitar ter que adicionar o mesmo aplicativo várias vezes a um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="06fb9-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="06fb9-106">**Observação**  Em versões anteriores do App-V 5,0, os grupos de conexão eram referidos como composição do pacote dinâmico.</span><span class="sxs-lookup"><span data-stu-id="06fb9-106">**Note** In previous versions of App-V 5.0, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="06fb9-107">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="06fb9-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md)"><span data-ttu-id="06fb9-108">Sobre o ambiente Virtual do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="06fb9-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="06fb9-109">Descreve o ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="06fb9-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file.md)"><span data-ttu-id="06fb9-110">Sobre o arquivo do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="06fb9-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="06fb9-111">Descreve o arquivo de grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="06fb9-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group.md)"><span data-ttu-id="06fb9-112">Como criar um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="06fb9-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="06fb9-113">Explica como criar um novo grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="06fb9-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="06fb9-114">Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados</span><span class="sxs-lookup"><span data-stu-id="06fb9-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="06fb9-115">Explica como criar um novo grupo de conexão que contém uma combinação de pacotes que são publicados para o usuário e publicadas globalmente.</span><span class="sxs-lookup"><span data-stu-id="06fb9-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group.md)"><span data-ttu-id="06fb9-116">Como excluir um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="06fb9-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="06fb9-117">Explica como excluir um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="06fb9-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group.md)"><span data-ttu-id="06fb9-118">Como publicar um grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="06fb9-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="06fb9-119">Explica como publicar um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="06fb9-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="06fb9-120">Outros recursos para grupos de conexão do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="06fb9-120">Other resources for App-V 5.0 connection groups</span></span>


-   [<span data-ttu-id="06fb9-121">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="06fb9-121">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





