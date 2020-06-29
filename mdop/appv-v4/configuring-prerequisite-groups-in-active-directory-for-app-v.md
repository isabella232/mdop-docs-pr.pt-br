---
title: Configurando grupos de pré-requisitos no Active Directory para o App-V
description: Configurando grupos de pré-requisitos no Active Directory para o App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798010"
---
# <span data-ttu-id="316b6-103">Configurando grupos de pré-requisitos no Active Directory para o App-V</span><span class="sxs-lookup"><span data-stu-id="316b6-103">Configuring Prerequisite Groups in Active Directory for App-V</span></span>


<span data-ttu-id="316b6-104">Antes de instalar o servidor de gerenciamento do Microsoft Application Virtualization (App-V), você deve criar os seguintes objetos no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="316b6-104">Before you install the Microsoft Application Virtualization (App-V) Management Server, you must create the following objects in Active Directory.</span></span> <span data-ttu-id="316b6-105">O App-V usa grupos do Active Directory para controlar o acesso a aplicativos e funções administrativas.</span><span class="sxs-lookup"><span data-stu-id="316b6-105">App-V uses Active Directory groups to control access to applications and administrative functions.</span></span> <span data-ttu-id="316b6-106">Você usará esses grupos durante o processo de instalação do servidor e durante a publicação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="316b6-106">You will use these groups during the server installation process and when publishing applications.</span></span>

## <span data-ttu-id="316b6-107">Configurando grupos de pré-requisitos no Active Directory para virtualização de aplicativos</span><span class="sxs-lookup"><span data-stu-id="316b6-107">Configuring Prerequisite Groups in Active Directory for Application Virtualization</span></span>


<span data-ttu-id="316b6-108">Esta tabela lista os grupos do Active Directory necessários para a instalação do App-V.</span><span class="sxs-lookup"><span data-stu-id="316b6-108">This table lists the Active Directory groups that are required for installing App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="316b6-109">Objeto</span><span class="sxs-lookup"><span data-stu-id="316b6-109">Object</span></span></th>
<th align="left"><span data-ttu-id="316b6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="316b6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="316b6-111">Unidade organizacional (UO)</span><span class="sxs-lookup"><span data-stu-id="316b6-111">Organizational Unit (OU)</span></span></p></td>
<td align="left"><p><span data-ttu-id="316b6-112">Crie uma OU no Active Directory para os grupos específicos necessários para o App-V.</span><span class="sxs-lookup"><span data-stu-id="316b6-112">Create an OU in Active Directory for the specific groups required for App-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="316b6-113">Grupo administrativo do App-V</span><span class="sxs-lookup"><span data-stu-id="316b6-113">App-V Administrative Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="316b6-114">Durante a instalação do servidor de gerenciamento do App-V, você deve selecionar um grupo do Active Directory para usá-lo como o grupo de administradores do App-V para controlar o acesso administrativo ao console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="316b6-114">During installation of the App-V Management Server, you must select an Active Directory group to use as the App-V Administrators group to control administrative access to the Management Console.</span></span> <span data-ttu-id="316b6-115">Crie um grupo de segurança para administradores do App-V e adicione a esse grupo todos os usuários que precisam usar o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="316b6-115">Create a security group for App-V administrators, and add to this group every user who needs to use the Management Console.</span></span> <span data-ttu-id="316b6-116">Você não pode criar esse grupo diretamente do instalador do App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="316b6-116">You cannot create this group directly from the App-V Management Server installer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="316b6-117">Grupo usuários do App-V</span><span class="sxs-lookup"><span data-stu-id="316b6-117">App-V Users Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="316b6-118">O App-V requer que todas as contas de usuário que acessam as funções do App-V sejam um membro de uma política de provedor associada a um único grupo para acesso geral à plataforma.</span><span class="sxs-lookup"><span data-stu-id="316b6-118">App-V requires that every User account that accesses App-V functions be a member of a provider policy associated with a single group for general platform access.</span></span> <span data-ttu-id="316b6-119">Usar um grupo existente; por exemplo, usuários do domínio, se todos os usuários tiverem acesso ao App-V ou criarem um novo grupo.</span><span class="sxs-lookup"><span data-stu-id="316b6-119">Use an existing group; for example, Domain Users, if all users are to have access to App-V, or create a new group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="316b6-120">Grupos de aplicativos</span><span class="sxs-lookup"><span data-stu-id="316b6-120">Application Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="316b6-121">O App-V associa o direito de usar um aplicativo individual com um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="316b6-121">App-V associates the right to use an individual application with an Active Directory group.</span></span> <span data-ttu-id="316b6-122">Crie um grupo do Active Directory para cada aplicativo e atribua usuários a esses grupos conforme necessário para controlar o acesso do usuário aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="316b6-122">Create an Active Directory group for each application, and assign users to these groups as needed to control user access to the applications.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="316b6-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="316b6-123">Related topics</span></span>


[<span data-ttu-id="316b6-124">Requisitos para implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="316b6-124">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="316b6-125">Como configurar o Windows Server 2008 paro App-V Management Servers</span><span class="sxs-lookup"><span data-stu-id="316b6-125">How to Configure Windows Server 2008 for App-V Management Servers</span></span>](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





