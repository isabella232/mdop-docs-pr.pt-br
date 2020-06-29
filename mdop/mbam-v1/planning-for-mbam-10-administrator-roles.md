---
title: Planejamento para Funções de Administrador do MBAM 1.0
description: Planejamento para Funções de Administrador do MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799762"
---
# <span data-ttu-id="da229-103">Planejamento para Funções de Administrador do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="da229-103">Planning for MBAM 1.0 Administrator Roles</span></span>


<span data-ttu-id="da229-104">Este tópico inclui e descreve as funções de administrador que estão disponíveis no Microsoft BitLocker Administration and Monitoring (MBAM), bem como os locais do servidor em que os grupos locais são criados.</span><span class="sxs-lookup"><span data-stu-id="da229-104">This topic includes and describes the administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM), as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="da229-105">Funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="da229-105">MBAM Administrator roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="da229-106">Administradores do sistema do MBAM</span><span class="sxs-lookup"><span data-stu-id="da229-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="da229-107">Os administradores nessa função têm acesso a todos os recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="da229-107">Administrators in this role have access to all MBAM features.</span></span> <span data-ttu-id="da229-108">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="da229-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-hardware-users"></a> **<span data-ttu-id="da229-109">Usuários de hardware MBAM</span><span class="sxs-lookup"><span data-stu-id="da229-109">MBAM Hardware Users</span></span>**  
<span data-ttu-id="da229-110">Os administradores nesta função têm acesso aos recursos de recursos de hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="da229-110">Administrators in this role have access to the Hardware Capability features from MBAM.</span></span> <span data-ttu-id="da229-111">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="da229-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="da229-112">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="da229-112">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="da229-113">Os administradores nesta função têm acesso aos recursos da assistência técnica a partir do MBAM.</span><span class="sxs-lookup"><span data-stu-id="da229-113">Administrators in this role have access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="da229-114">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="da229-114">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam--report-users"></a> **<span data-ttu-id="da229-115">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="da229-115">MBAM Report Users</span></span>**  
<span data-ttu-id="da229-116">Os administradores nesta função têm acesso ao recurso de relatórios de conformidade e auditoria do MBAM.</span><span class="sxs-lookup"><span data-stu-id="da229-116">Administrators in this role have access to the Compliance and Audit Reports feature from MBAM.</span></span> <span data-ttu-id="da229-117">O grupo local para esta função é instalado no servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="da229-117">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **<span data-ttu-id="da229-118">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="da229-118">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="da229-119">Os administradores nesta função têm melhorado o acesso aos recursos da assistência técnica a partir do MBAM.</span><span class="sxs-lookup"><span data-stu-id="da229-119">Administrators in this role have increased access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="da229-120">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="da229-120">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="da229-121">Se um usuário for membro de usuários da assistência técnica do MBAM e MBAM usuários avançados da assistência técnica, as MBAM permissões de usuários avançados da assistência técnica substituirão as permissões de usuário MBAM da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="da229-121">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will overwrite the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="da229-122">**Importante**  Para exibir os relatórios, um usuário administrativo deve ser membro do grupo de segurança **usuários de relatório do MBAM** no servidor de administração e monitoramento, banco de dados de conformidade e auditoria e no servidor que hospeda o recurso de conformidade e relatórios.</span><span class="sxs-lookup"><span data-stu-id="da229-122">**Important** To view the reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Reports feature.</span></span> <span data-ttu-id="da229-123">Como prática recomendada, crie um grupo de segurança no Active Directory com direitos no grupo de segurança **usuários de relatório do MBAM** local no servidor de administração e monitoramento e no servidor que hospeda a conformidade e os relatórios.</span><span class="sxs-lookup"><span data-stu-id="da229-123">As a best practice, create a security group in Active Directory with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and on the server that hosts the Compliance and Reports.</span></span>

 

## <span data-ttu-id="da229-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da229-124">Related topics</span></span>


[<span data-ttu-id="da229-125">Preparando seu ambiente para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="da229-125">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)

 

 





