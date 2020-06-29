---
title: Como gerenciar funções de administrador do MBAM
description: Como gerenciar funções de administrador do MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799608"
---
# <span data-ttu-id="099dc-103">Como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="099dc-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="099dc-104">Após a conclusão da instalação do Microsoft BitLocker Administration and Monitoring (MBAM) para todos os recursos do servidor, os usuários administrativos terão que conceder acesso a eles.</span><span class="sxs-lookup"><span data-stu-id="099dc-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users will have to be granted access to them.</span></span> <span data-ttu-id="099dc-105">Como prática recomendada, os administradores que gerenciam ou usam os recursos de servidor de administração e monitoramento do Microsoft BitLocker devem ser atribuídos a grupos de segurança de serviços de domínio e esses grupos devem ser adicionados ao grupo local administrativo MBAM apropriado.</span><span class="sxs-lookup"><span data-stu-id="099dc-105">As a best practice, administrators who will manage or use Microsoft BitLocker Administration and Monitoring Server features should be assigned to Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="099dc-106">Para gerenciar associações de funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="099dc-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="099dc-107">Atribua usuários administrativos a grupos de segurança nos serviços de domínio do ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="099dc-107">Assign administrative users to security groups in ActiveDirectory Domain Services.</span></span>

2.  <span data-ttu-id="099dc-108">Adicione grupos de segurança do ActiveDirectory às funções dos grupos locais administrativos do MBAM no servidor MBAM para os respectivos recursos.</span><span class="sxs-lookup"><span data-stu-id="099dc-108">Add ActiveDirectory security groups to the roles for MBAM administrative local groups on the MBAM server for the respective features.</span></span>

    -   <span data-ttu-id="099dc-109">**Os administradores do sistema do MBAM** têm acesso a todos os recursos do MBAM no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="099dc-109">**MBAM System Administrators** have access to all MBAM features in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="099dc-110">**Usuários da assistência técnica do MBAM** têm acesso às opções gerenciar TPM e recuperação de unidade no site de administração e monitoramento do MBAM, mas devem preencher todos os campos quando usarem qualquer uma dessas opções.</span><span class="sxs-lookup"><span data-stu-id="099dc-110">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="099dc-111">**MBAM relatório os usuários** têm acesso aos relatórios de conformidade e auditoria no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="099dc-111">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="099dc-112">**Os usuários de helpdesk avançados do MBAM** têm acesso às opções gerenciar TPM e recuperação de unidade no site de administração e monitoramento do MBAM, mas não são necessários para preencher todos os campos quando eles usam qualquer uma dessas opções.</span><span class="sxs-lookup"><span data-stu-id="099dc-112">**MBAM Advanced Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="099dc-113">Para obter mais informações sobre as funções de administração e monitoramento do Microsoft BitLocker, consulte [planejando funções de administrador do MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="099dc-113">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="099dc-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="099dc-114">Related topics</span></span>


[<span data-ttu-id="099dc-115">Administrando os Recursos do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="099dc-115">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





