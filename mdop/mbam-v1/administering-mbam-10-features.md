---
title: Administrando os Recursos do MBAM 1.0
description: Administrando os Recursos do MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797882"
---
# <span data-ttu-id="7dbf3-103">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7dbf3-103">Administering MBAM 1.0 Features</span></span>


<span data-ttu-id="7dbf3-104">Depois de concluir todo o planejamento e a implantação necessários do Microsoft BitLocker Administration and Monitoring (MBAM), você poderá configurar e usar o MBAM para gerenciar a criptografia do BitLocker corporativo.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-104">After you complete all necessary Microsoft BitLocker Administration and Monitoring (MBAM) planning and deployment, you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="7dbf3-105">As informações nesta seção descrevem tarefas de operações do recurso pós-instalação do dia-a-dia após a instalação MBAM.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-105">The information in this section describes post-installation day-to-day MBAM feature operations tasks.</span></span>

## <span data-ttu-id="7dbf3-106">Gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="7dbf3-106">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="7dbf3-107">Após a conclusão da instalação do MBAM para todos os recursos do servidor, os usuários administrativos devem ter acesso a esses recursos de servidor.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-107">After MBAM Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="7dbf3-108">Como prática recomendada, os administradores que gerenciam ou usam recursos do MBAM Server devem ser atribuídos aos grupos de segurança do Active Directory e esses grupos devem ser adicionados ao grupo local administrativo apropriado do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-108">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="7dbf3-109">Como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="7dbf3-109">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-1.md)

## <span data-ttu-id="7dbf3-110">Gerenciar a compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="7dbf3-110">Manage Hardware Compatibility</span></span>


<span data-ttu-id="7dbf3-111">O recurso de compatibilidade de hardware do MBAM pode ajudá-lo a garantir que somente o hardware do computador especificado como suporte para BitLocker será criptografado.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-111">The MBAM Hardware Compatibility feature can help you to ensure that only the computer hardware that you specify as supporting BitLocker will be encrypted.</span></span> <span data-ttu-id="7dbf3-112">Quando esse recurso estiver ativado, bit \ _admmontla criptografará apenas computadores marcados como compatíveis.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-112">When this feature is turned on, bit\_admmontla will encrypt only computers that are marked as Compatible.</span></span>

<span data-ttu-id="7dbf3-113">**Importante**  Quando esse recurso estiver desativado, todos os computadores nos quais a política MBAM é implantada serão criptografados.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-113">**Important** When this feature is turned off, all computers where the MBAM policy is deployed will be encrypted.</span></span>

 

<span data-ttu-id="7dbf3-114">O MBAM pode coletar informações sobre o fabricante e o modelo de computadores cliente se você implantar a política de grupo "permitir verificação de compatibilidade de hardware".</span><span class="sxs-lookup"><span data-stu-id="7dbf3-114">MBAM can collect information on both the make and model of client computers if you deploy the “Allow Hardware Compatibility Checking” Group Policy.</span></span> <span data-ttu-id="7dbf3-115">Se você configurar essa política, o agente MBAM relata as informações do modelo e do modelo do computador ao servidor MBAM quando o cliente MBAM é implantado em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-115">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

[<span data-ttu-id="7dbf3-116">Como gerenciar a compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="7dbf3-116">How to Manage Hardware Compatibility</span></span>](how-to-manage-hardware-compatibility-mbam-1.md)

[<span data-ttu-id="7dbf3-117">Como gerenciar isenções de criptografia BitLocker para usuários</span><span class="sxs-lookup"><span data-stu-id="7dbf3-117">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## <span data-ttu-id="7dbf3-118">Gerenciar isenções de criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="7dbf3-118">Manage BitLocker encryption exemptions</span></span>


<span data-ttu-id="7dbf3-119">MBAM pode conceder duas formas de isenção de criptografia BitLocker: isenção de computador e isenção de usuário.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-119">MBAM can grant two forms of exemption from BitLocker encryption: computer exemption and user exemption.</span></span> <span data-ttu-id="7dbf3-120">A isenção de computador geralmente é usada quando uma empresa tem computadores que não precisam ser criptografados, como computadores usados em desenvolvimento ou testes ou computadores mais antigos que não dão suporte ao BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-120">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="7dbf3-121">Em alguns casos, a lei local também pode exigir que determinados computadores não sejam criptografados.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-121">In some cases, local law may also require that certain computers are not encrypted.</span></span> <span data-ttu-id="7dbf3-122">Você também pode optar por não ter certeza de que os usuários que não precisam ou querem que suas unidades sejam criptografadas.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-122">You may also choose to exempt users who do not need or want their drives encrypted.</span></span>

[<span data-ttu-id="7dbf3-123">Como gerenciar isenções de criptografia BitLocker para computadores</span><span class="sxs-lookup"><span data-stu-id="7dbf3-123">How to Manage Computer BitLocker Encryption Exemptions</span></span>](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## <span data-ttu-id="7dbf3-124">Gerenciar as opções de criptografia do BitLocker do cliente MBAM usando o painel de controle</span><span class="sxs-lookup"><span data-stu-id="7dbf3-124">Manage MBAM Client BitLocker Encryption Options by using the Control Panel</span></span>


<span data-ttu-id="7dbf3-125">Se habilitado por meio de um GPO (objetos de política de grupo), um painel de controle do MBAM personalizado chamado opções de criptografia BitLocker estará disponível em **sistema e segurança**.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-125">If enabled through a Group Policy Objects (GPO), a custom MBAM control panel that is named BitLocker Encryption Options will be available under **System and Security**.</span></span> <span data-ttu-id="7dbf3-126">Este painel de controle personalizado substitui o painel de controle padrão do Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-126">This customized control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="7dbf3-127">O painel de controle do MBAM permite desbloquear unidades criptografadas (fixas e removíveis) e também ajuda você a gerenciar seu PIN ou senha.</span><span class="sxs-lookup"><span data-stu-id="7dbf3-127">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span>

[<span data-ttu-id="7dbf3-128">Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="7dbf3-128">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## <span data-ttu-id="7dbf3-129">Outros recursos para administrar recursos do MBAM</span><span class="sxs-lookup"><span data-stu-id="7dbf3-129">Other resources for Administering MBAM features</span></span>


[<span data-ttu-id="7dbf3-130">Operações do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7dbf3-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





