---
title: Implantar Objetos de Política de Grupo no MBAM 2.0
description: Implantar Objetos de Política de Grupo no MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799283"
---
# <span data-ttu-id="16997-103">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16997-103">Deploying MBAM 2.0 Group Policy Objects</span></span>


<span data-ttu-id="16997-104">Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), primeiro você precisa determinar as políticas de grupo que usará na implementação da administração e do monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="16997-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="16997-105">Consulte [planejando os requisitos da política de grupo do MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obter mais informações sobre as diferentes políticas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="16997-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="16997-106">Depois de determinar as políticas que você vai usar, você deve criar e implantar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política para o MBAM usando o modelo de política de grupo MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16997-106">When you have determined the policies that you are going to use, you then must create and deploy one or more Group Policy Objects (GPO) that include the policy settings for MBAM by using the MBAM 2.0 Group Policy template.</span></span>

## <span data-ttu-id="16997-107">Instalar o modelo de política de grupo do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="16997-107">Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="16997-108">Além dos recursos de administração e monitoramento do Microsoft BitLocker relacionados a servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="16997-108">In addition to the server-related Microsoft BitLocker Administration and Monitoring features, the server setup application includes a MBAM Group Policy template.</span></span> <span data-ttu-id="16997-109">Este modelo pode ser instalado em qualquer computador capaz de executar o GPMC (console de gerenciamento de política de grupo) ou no AGPM (gerenciamento avançado de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="16997-109">This template can be installed on any computer able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="16997-110">Como instalar o Modelo de Política de Grupo do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16997-110">How to Install the MBAM 2.0 Group Policy Template</span></span>](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## <span data-ttu-id="16997-111">Implantar configurações de política de grupo do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="16997-111">Deploy MBAM 2.0 Group Policy Settings</span></span>


<span data-ttu-id="16997-112">Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização.</span><span class="sxs-lookup"><span data-stu-id="16997-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="16997-113">Como editar Configurações GPO do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16997-113">How to Edit MBAM 2.0 GPO Settings</span></span>](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## <span data-ttu-id="16997-114">Exibir o painel de controle do MBAM no Windows</span><span class="sxs-lookup"><span data-stu-id="16997-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="16997-115">Como o MBAM oferece um painel de controle personalizado do MBAM que pode substituir o painel de controle padrão do Windows BitLocker, você também pode optar por ocultar o painel de controle padrão do BitLocker dos usuários finais usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="16997-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="16997-116">Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows</span><span class="sxs-lookup"><span data-stu-id="16997-116">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## <span data-ttu-id="16997-117">Outros recursos para a implantação de objetos de política de grupo do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="16997-117">Other Resources for Deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="16997-118">Implantando o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="16997-118">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





