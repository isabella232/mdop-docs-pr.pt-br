---
title: Preparando seu ambiente para o MBAM 1.0
description: Preparando seu ambiente para o MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799223"
---
# <span data-ttu-id="e1d0d-103">Preparando seu ambiente para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-103">Preparing your Environment for MBAM 1.0</span></span>


<span data-ttu-id="e1d0d-104">Antes de começar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), certifique-se de que você atendeu aos pré-requisitos necessários para instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you have met the necessary prerequisites to install the product.</span></span> <span data-ttu-id="e1d0d-105">Se você souber os pré-requisitos antecipadamente, poderá implantar eficientemente o produto e habilitar seus recursos, o que pode dar suporte a objetivos comerciais da sua organização com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-105">If you know the prerequisites in advance, you can efficiently deploy the product and enable its features, which can support the business objectives of your organization more effectively.</span></span>

## <span data-ttu-id="e1d0d-106">Revisar os pré-requisitos de implantação do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-106">Review MBAM 1.0 deployment prerequisites</span></span>


<span data-ttu-id="e1d0d-107">O cliente MBAM e cada um dos recursos do servidor MBAM têm pré-requisitos específicos que devem ser atendidos para que possam ser instalados com êxito.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-107">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="e1d0d-108">Para garantir a instalação bem-sucedida dos clientes do MBAM e dos recursos do MBAM Server, você deve planejar a garantia de que os computadores especificados para MBAM cliente ou MBAM instalação de recursos de servidor estejam adequadamente preparados para a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-108">To ensure successful installation of MBAM Clients and MBAM Server features, you should plan to ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="e1d0d-109">**Observação**  A instalação do MBAM verifica se todos os pré-requisitos são atendidos antes do início da instalação.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-109">**Note** MBAM Setup verifies if all prerequisites are met before installation starts.</span></span> <span data-ttu-id="e1d0d-110">Se não forem atendidas, a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-110">If they are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="e1d0d-111">Pré-requisitos para implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-111">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)

## <span data-ttu-id="e1d0d-112">Plano para requisitos de política de grupo do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-112">Plan for MBAM 1.0 Group Policy requirements</span></span>


<span data-ttu-id="e1d0d-113">Antes que o MBAM possa gerenciar clientes na empresa, você deve definir a política de grupo para os requisitos de criptografia do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-113">Before MBAM can manage clients in the enterprise, you must define the Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="e1d0d-114">**Importante**  O MBAM não funcionará com políticas para criptografia de unidade de disco BitLocker autônoma.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-114">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="e1d0d-115">A política de grupo deve ser definida para MBAM; caso contrário, haverá falha na criptografia e na imposição do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-115">Group Policy must be defined for MBAM; otherwise, the BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="e1d0d-116">Planejar Requisitos de Política de Grupo do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-116">Planning for MBAM 1.0 Group Policy Requirements</span></span>](planning-for-mbam-10-group-policy-requirements.md)

## <span data-ttu-id="e1d0d-117">Planejar as funções de administrador do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-117">Plan for MBAM 1.0 administrator roles</span></span>


<span data-ttu-id="e1d0d-118">As funções de administrador do MBAM são gerenciadas por grupos locais criados pela configuração do MBAM quando você instala o seguinte: servidor de administração e monitoramento do BitLocker, recurso de relatórios de auditoria e conformidade e banco de dados de status de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-118">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the following: BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="e1d0d-119">A associação de funções de MBAM pode ser gerenciada com mais eficiência se você criar grupos de segurança no ActiveDirectoryDomainServices, adicionar as contas de administrador apropriadas a esses grupos e, em seguida, adicionar esses grupos de segurança aos grupos locais do MBAM.</span><span class="sxs-lookup"><span data-stu-id="e1d0d-119">The membership of MBAM roles can be managed more effectively if you create security groups in ActiveDirectoryDomainServices, add the appropriate administrator accounts to those groups, and then add those security groups to the MBAM local groups.</span></span> <span data-ttu-id="e1d0d-120">Para obter mais informações, consulte [como gerenciar as funções de administrador do MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="e1d0d-120">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md).</span></span>

[<span data-ttu-id="e1d0d-121">Planejamento para Funções de Administrador do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-121">Planning for MBAM 1.0 Administrator Roles</span></span>](planning-for-mbam-10-administrator-roles.md)

## <span data-ttu-id="e1d0d-122">Outros recursos para o planejamento do MBAM</span><span class="sxs-lookup"><span data-stu-id="e1d0d-122">Other resources for MBAM planning</span></span>


[<span data-ttu-id="e1d0d-123">Planejamento para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1d0d-123">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





