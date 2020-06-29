---
title: Como preparar seu ambiente para o MBAM 2.0
description: Como preparar seu ambiente para o MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799706"
---
# <span data-ttu-id="aba7b-103">Como preparar seu ambiente para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="aba7b-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="aba7b-104">Antes de iniciar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), você deve verificar se atendeu os pré-requisitos para instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="aba7b-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="aba7b-105">Quando você sabe o que os pré-requisitos estão antecipadamente, você pode implantar o produto com eficiência e habilitar seus recursos para que ele dê suporte aos objetivos de negócios da sua organização de forma mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="aba7b-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="aba7b-106">Se você estiver implantando a administração e o monitoramento do Microsoft BitLocker com o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="aba7b-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="aba7b-107">Revisar os pré-requisitos de implantação do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="aba7b-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="aba7b-108">O cliente MBAM e cada um dos recursos do servidor MBAM têm pré-requisitos específicos que devem ser atendidos para que possam ser instalados com êxito.</span><span class="sxs-lookup"><span data-stu-id="aba7b-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="aba7b-109">Para garantir a instalação bem-sucedida de clientes do MBAM e recursos do MBAM Server, certifique-se de que os computadores especificados para a instalação do MBAM cliente ou do MBAM Server estejam adequadamente preparados para a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="aba7b-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="aba7b-110">**Observação**  MBAM a instalação verifica se todos os pré-requisitos são atendidos antes do início da instalação.</span><span class="sxs-lookup"><span data-stu-id="aba7b-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="aba7b-111">Se todos os pré-requisitos não forem atendidos, a instalação não será bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aba7b-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="aba7b-112">Pré-requisitos para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="aba7b-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="aba7b-113">Plano para requisitos de política de grupo do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="aba7b-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="aba7b-114">Antes que o MBAM possa gerenciar clientes na empresa, você deve definir a política de grupo para os requisitos de criptografia do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="aba7b-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="aba7b-115">**Importante**  O MBAM não funcionará com políticas para criptografia de unidade de disco BitLocker autônoma.</span><span class="sxs-lookup"><span data-stu-id="aba7b-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="aba7b-116">As configurações de política de grupo devem ser definidas para MBAM, ou a criptografia e a imposição do BitLocker falharão.</span><span class="sxs-lookup"><span data-stu-id="aba7b-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="aba7b-117">Planejar Requisitos de Política de Grupo do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="aba7b-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="aba7b-118">Planejar as funções de administrador do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="aba7b-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="aba7b-119">As funções de administrador do MBAM são gerenciadas por grupos locais criados pela configuração do MBAM ao instalar o servidor de administração e monitoramento do BitLocker, o recurso de relatórios de auditoria e conformidade e o banco de dados de status de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="aba7b-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="aba7b-120">A Associação das funções de administração e administração do Microsoft BitLocker pode ser gerenciada pela criação de grupos de segurança no ActiveDirectoryDomainServices, adição das contas de administrador apropriadas a esses grupos e, em seguida, adição desses grupos de segurança aos grupos locais de administração e monitoramento do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aba7b-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="aba7b-121">Para obter mais informações, consulte [como gerenciar as funções de administrador do MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="aba7b-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="aba7b-122">Outros recursos para o planejamento do MBAM</span><span class="sxs-lookup"><span data-stu-id="aba7b-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="aba7b-123">Planejamento para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="aba7b-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="aba7b-124">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="aba7b-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





