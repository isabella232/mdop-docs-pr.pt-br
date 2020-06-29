---
title: Planejamento para Funções de Administrador do MBAM 2.0
description: Planejamento para Funções de Administrador do MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799563"
---
# <span data-ttu-id="4d182-103">Planejamento para Funções de Administrador do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4d182-103">Planning for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="4d182-104">Este tópico lista e descreve as funções de administrador disponíveis que estão disponíveis no Microsoft BitLocker Administration and Monitoring (MBAM), bem como os locais do servidor em que os grupos locais são criados.</span><span class="sxs-lookup"><span data-stu-id="4d182-104">This topic lists and describes the available administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM) as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="4d182-105">Funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="4d182-105">MBAM Administrator Roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="4d182-106">Administradores do sistema do MBAM</span><span class="sxs-lookup"><span data-stu-id="4d182-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="4d182-107">Os administradores nesta função têm acesso a todos os recursos de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4d182-107">Administrators in this role have access to all Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="4d182-108">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4d182-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="4d182-109">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="4d182-109">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="4d182-110">Os administradores nesta função têm acesso aos recursos de suporte técnico do MBAM.</span><span class="sxs-lookup"><span data-stu-id="4d182-110">Administrators in this role have access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="4d182-111">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4d182-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-report-users"></a> **<span data-ttu-id="4d182-112">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="4d182-112">MBAM Report Users</span></span>**  
<span data-ttu-id="4d182-113">Os administradores nesta função têm acesso aos relatórios de conformidade e auditoria do MBAM.</span><span class="sxs-lookup"><span data-stu-id="4d182-113">Administrators in this role have access to the Compliance and Audit Reports from MBAM.</span></span> <span data-ttu-id="4d182-114">O grupo local para esta função é instalado no servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="4d182-114">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **<span data-ttu-id="4d182-115">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="4d182-115">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="4d182-116">Os administradores nesta função têm acesso melhorado aos recursos de suporte técnico do MBAM.</span><span class="sxs-lookup"><span data-stu-id="4d182-116">Administrators in this role have increased access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="4d182-117">O grupo local para esta função é instalado no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="4d182-117">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="4d182-118">Se um usuário for membro de usuários da assistência técnica do MBAM e MBAM usuários avançados da assistência técnica, as MBAM permissões de usuários avançados da assistência técnica substituirão as permissões de usuário MBAM da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="4d182-118">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will override the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="4d182-119">**Importante**  Para exibir relatórios, um usuário administrativo deve ser membro do grupo de segurança **usuários de relatório do MBAM** no servidor de administração e monitoramento, banco de dados de conformidade e auditoria e no servidor que hospeda o recurso de conformidade e relatórios de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4d182-119">**Important** To view reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports feature.</span></span> <span data-ttu-id="4d182-120">Como prática recomendada, crie um grupo de segurança nos serviços de domínio Active Directory com direitos no grupo de segurança **usuários de relatório do MBAM** local no servidor de administração e monitoramento e no servidor que hospeda os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="4d182-120">As a best practice, create a security group in Active Directory Domain Services with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and the server that hosts the Compliance and Audit Reports.</span></span>

 

## <span data-ttu-id="4d182-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d182-121">Related topics</span></span>


[<span data-ttu-id="4d182-122">Como preparar seu ambiente para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4d182-122">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





