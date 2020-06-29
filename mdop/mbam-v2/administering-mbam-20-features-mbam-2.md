---
title: Administrando os Recursos do MBAM 2.0
description: Administrando os Recursos do MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799286"
---
# <span data-ttu-id="a8ee5-103">Administrando os Recursos do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a8ee5-103">Administering MBAM 2.0 Features</span></span>


<span data-ttu-id="a8ee5-104">Depois de concluir o planejamento necessário e a implantação do Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurá-lo e usá-lo para gerenciar a criptografia do BitLocker na empresa as informações nesta seção descrevem as tarefas de operações do recurso de administração e monitoramento do Microsoft BitLocker do dia-a-dia após a instalação.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-104">After completing all necessary planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker encryption across the enterprise The information in this section describes post-installation day-to-day Microsoft BitLocker Administration and Monitoring feature operations tasks.</span></span>

## <span data-ttu-id="a8ee5-105">Gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="a8ee5-105">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="a8ee5-106">Após a conclusão da instalação do MBAM para todos os recursos do servidor, os usuários administrativos devem receber acesso a eles.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-106">After MBAM Setup is complete for all server features, administrative users have to be granted access to them.</span></span> <span data-ttu-id="a8ee5-107">Como prática recomendada, os administradores que gerenciam ou usam os recursos do MBAM Server devem ser atribuídos aos grupos de segurança dos serviços de domínio Active Directory e esses grupos devem ser adicionados ao grupo local administrativo MBAM apropriado.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-107">As a best practice, administrators who will manage or use MBAM server features should be assigned to Active Directory Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="a8ee5-108">Como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="a8ee5-108">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-2.md)

## <span data-ttu-id="a8ee5-109">Gerenciar isenções de criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="a8ee5-109">Manage BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="a8ee5-110">O MBAM permite que você conceda isenções de criptografia a usuários específicos que não precisam ou querem que suas unidades sejam criptografadas.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-110">MBAM lets you grant encryption exemptions to specific users who do not need or want their drives encrypted.</span></span> <span data-ttu-id="a8ee5-111">A isenção de computador geralmente é usada quando uma empresa tem computadores que não precisam ser criptografados, como computadores usados em desenvolvimento ou testes ou computadores mais antigos que não dão suporte ao BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-111">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="a8ee5-112">Em alguns casos, a lei local também pode exigir que determinados computadores não sejam criptografados.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-112">In some cases, local law may also require that certain computers are not encrypted.</span></span>

[<span data-ttu-id="a8ee5-113">Como gerenciar isenções de criptografia BitLocker para usuários</span><span class="sxs-lookup"><span data-stu-id="a8ee5-113">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## <span data-ttu-id="a8ee5-114">Gerenciar as opções de criptografia do BitLocker do cliente MBAM usando o painel de controle</span><span class="sxs-lookup"><span data-stu-id="a8ee5-114">Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="a8ee5-115">O MBAM fornece um painel de controle personalizado, chamado opções de criptografia do BitLocker, que aparecerá em **sistema e segurança**.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-115">MBAM provides a custom control panel, called BitLocker Encryption Options, that will appear under **System and Security**.</span></span> <span data-ttu-id="a8ee5-116">O painel de controle do MBAM pode ser usado para desbloquear unidades fixas e removíveis criptografadas e também gerenciar seu PIN ou senha.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-116">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span>

<span data-ttu-id="a8ee5-117">**Observação**  Este painel de controle personalizado não substitui o painel de controle padrão do Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-117">**Note** This customized control panel does not replace the default Windows BitLocker control panel.</span></span>

 

[<span data-ttu-id="a8ee5-118">Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="a8ee5-118">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## <span data-ttu-id="a8ee5-119">Outros recursos para administrar recursos do MBAM</span><span class="sxs-lookup"><span data-stu-id="a8ee5-119">Other Resources for Administering MBAM Features</span></span>


[<span data-ttu-id="a8ee5-120">Operações do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a8ee5-120">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





