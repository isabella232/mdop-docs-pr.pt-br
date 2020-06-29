---
title: Como gerenciar isenções de criptografia BitLocker para computadores
description: Como gerenciar isenções de criptografia BitLocker para computadores
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799720"
---
# <span data-ttu-id="91dc1-103">Como gerenciar isenções de criptografia BitLocker para computadores</span><span class="sxs-lookup"><span data-stu-id="91dc1-103">How to Manage Computer BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="91dc1-104">A administração e o monitoramento do Microsoft BitLocker (MBAM) podem ser usados para isentar determinados computadores da proteção BitLocker.</span><span class="sxs-lookup"><span data-stu-id="91dc1-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to exempt certain computers from BitLocker protection.</span></span> <span data-ttu-id="91dc1-105">Por exemplo, uma organização pode decidir controlar a isenção de BitLocker individualmente em computador.</span><span class="sxs-lookup"><span data-stu-id="91dc1-105">For example, an organization may decide to control BitLocker exemption on a computer-by-computer basis.</span></span>

<span data-ttu-id="91dc1-106">Para isenta um computador da criptografia do BitLocker, você deve adicionar o computador a um grupo de segurança no ActiveDirectoryDomainServices para ignorar qualquer regra de proteção do BitLocker baseada em computador.</span><span class="sxs-lookup"><span data-stu-id="91dc1-106">To exempt a computer from BitLocker encryption, you must add the computer to a security group in ActiveDirectoryDomainServices in order to bypass any computer-based BitLocker protection rules.</span></span>

<span data-ttu-id="91dc1-107">**Observação**  Se o computador já estiver protegido pelo BitLocker, a política de isenção de computador não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="91dc1-107">**Note** If the computer is already BitLocker-protected, the computer exemption policy has no effect.</span></span>

 

**<span data-ttu-id="91dc1-108">Para isenta um computador da criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="91dc1-108">To exempt a computer from BitLocker encryption</span></span>**

1.  <span data-ttu-id="91dc1-109">Adicione a conta de computador que você deseja que seja isenta a um grupo de segurança no ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="91dc1-109">Add the computer account that you want to be exempted to a security group in ActiveDirectoryDomainServices.</span></span> <span data-ttu-id="91dc1-110">Isso permite ignorar qualquer regra de proteção do BitLocker baseada em computador.</span><span class="sxs-lookup"><span data-stu-id="91dc1-110">This allows you to bypass any computer-based BitLocker protection rules.</span></span>

2.  <span data-ttu-id="91dc1-111">Crie um objeto de política de grupo usando o modelo de política de grupo do MBAM e associe o objeto de política de grupo ao grupo do Active Directory que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="91dc1-111">Create a Group Policy Object by using the MBAM Group Policy template, then associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="91dc1-112">Para obter mais informações sobre como criar os objetos de política de grupo necessários, consulte [implantando objetos de política de grupo do MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="91dc1-112">For more information about creating the necessary Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

3.  <span data-ttu-id="91dc1-113">Quando um computador isento é iniciado, o cliente do MBAM verifica a configuração da política de isenção do computador e suspende a proteção com base no fato de o computador fazer parte do grupo de segurança de isenção de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="91dc1-113">When an exempted computer starts, the MBAM client checks the Computer Exemption Policy setting and suspends protection based on whether the computer is part of the BitLocker exemption security group.</span></span>

## <span data-ttu-id="91dc1-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91dc1-114">Related topics</span></span>


[<span data-ttu-id="91dc1-115">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="91dc1-115">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





