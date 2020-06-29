---
title: Como gerenciar funções de administrador do MBAM
description: Como gerenciar funções de administrador do MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796132"
---
# <span data-ttu-id="dac06-103">Como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="dac06-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="dac06-104">Após a conclusão da instalação do Microsoft BitLocker Administration and Monitoring (MBAM) para todos os recursos do servidor, os usuários administrativos devem ter acesso a esses recursos de servidor.</span><span class="sxs-lookup"><span data-stu-id="dac06-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="dac06-105">Como prática recomendada, os administradores que gerenciam ou usam recursos do MBAM Server devem ser atribuídos aos grupos de segurança do Active Directory e esses grupos devem ser adicionados ao grupo local administrativo apropriado do MBAM.</span><span class="sxs-lookup"><span data-stu-id="dac06-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="dac06-106">Para gerenciar associações de funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="dac06-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="dac06-107">Atribua usuários administrativos a grupos de segurança nos serviços do ActiveDirectoryDomain.</span><span class="sxs-lookup"><span data-stu-id="dac06-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="dac06-108">Adicione grupos de segurança de serviços do ActiveDirectoryDomain às funções para MBAM grupos locais administrativos no servidor de administração e monitoramento do Microsoft BitLocker para os respectivos recursos.</span><span class="sxs-lookup"><span data-stu-id="dac06-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="dac06-109">As funções de usuário são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dac06-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="dac06-110">**Os administradores de sistema do MBAM** têm acesso a todos os recursos de administração e monitoramento do Microsoft BitLocker no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="dac06-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="dac06-111">**Os usuários de hardware do MBAM** têm acesso aos recursos de compatibilidade de hardware no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="dac06-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="dac06-112">**Os usuários da assistência técnica do MBAM** têm acesso às opções gerenciar TPM e recuperação de unidade no site de administração do MBAM, mas devem preencher todos os campos quando usarem qualquer uma dessas opções.</span><span class="sxs-lookup"><span data-stu-id="dac06-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="dac06-113">**Os usuários de relatório MBAM** têm acesso aos relatórios de conformidade e auditoria no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="dac06-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="dac06-114">O **MBAM Advanced helpdesk usa** tem acesso às opções gerenciar TPM e recuperação de unidade no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="dac06-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="dac06-115">Esses usuários não precisam preencher todos os campos quando usam qualquer uma dessas opções.</span><span class="sxs-lookup"><span data-stu-id="dac06-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="dac06-116">Para obter mais informações sobre as funções de administração e monitoramento do Microsoft BitLocker, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="dac06-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="dac06-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dac06-117">Related topics</span></span>


[<span data-ttu-id="dac06-118">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="dac06-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





