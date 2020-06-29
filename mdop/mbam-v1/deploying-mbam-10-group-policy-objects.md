---
title: Implantar Objetos de Política de Grupo no MBAM 1.0
description: Implantar Objetos de Política de Grupo no MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797881"
---
# <span data-ttu-id="f37ff-103">Implantar Objetos de Política de Grupo no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f37ff-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="f37ff-104">Para implantar com êxito a administração e o monitoramento do Microsoft BitLocker (MBAM), você deve primeiro determinar as políticas de grupo que usará na implementação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="f37ff-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="f37ff-105">Para obter mais informações sobre as várias políticas disponíveis, consulte [planejando os requisitos da política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f37ff-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="f37ff-106">Depois de determinar as políticas que você vai usar, você deve usar o modelo de política de grupo do MBAM 1,0 para criar e implantar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f37ff-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="f37ff-107">Instalar o modelo de política de grupo do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="f37ff-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="f37ff-108">Além de fornecer recursos relacionados ao servidor do MBAM, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="f37ff-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="f37ff-109">Você pode instalar esse modelo em qualquer computador que possa executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="f37ff-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="f37ff-110">Como instalar o Modelo de Política de Grupo do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f37ff-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="f37ff-111">Implantar configurações de política de grupo do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="f37ff-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="f37ff-112">Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização.</span><span class="sxs-lookup"><span data-stu-id="f37ff-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="f37ff-113">Como editar Configurações GPO do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f37ff-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="f37ff-114">Exibir o painel de controle do MBAM no Windows</span><span class="sxs-lookup"><span data-stu-id="f37ff-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="f37ff-115">Como o MBAM oferece um painel de controle personalizado do MBAM que pode substituir o painel de controle padrão do Windows BitLocker, você também pode optar por ocultar o painel de controle padrão do BitLocker dos usuários finais usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f37ff-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="f37ff-116">Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows</span><span class="sxs-lookup"><span data-stu-id="f37ff-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="f37ff-117">Outros recursos para a implantação de objetos de política de grupo do MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="f37ff-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="f37ff-118">Implantando o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f37ff-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





