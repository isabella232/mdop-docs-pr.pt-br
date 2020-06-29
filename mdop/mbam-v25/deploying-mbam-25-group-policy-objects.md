---
title: Implantando objetos de Política de Grupo do MBAM 2.5
description: Implantando objetos de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799462"
---
# <span data-ttu-id="aa261-103">Implantando objetos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa261-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="aa261-104">Para implantar o MBAM, você precisa definir configurações de política de grupo que definem as configurações de implementação de MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aa261-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="aa261-105">Para concluir essa tarefa, você deve copiar os modelos de política de grupo do MBAM para um servidor ou uma estação de trabalho que sejam capazes de executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) e, em seguida, editar as configurações.</span><span class="sxs-lookup"><span data-stu-id="aa261-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="aa261-106">**Importante**  Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="aa261-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="aa261-107">Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.</span><span class="sxs-lookup"><span data-stu-id="aa261-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="aa261-108">Copiando os modelos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa261-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="aa261-109">Antes de instalar o cliente do MBAM, você deve copiar objetos de política de grupo (GPOs) específicos do MBAM para a estação de trabalho de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="aa261-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="aa261-110">Esses GPOs definem as configurações de implementação do MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aa261-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="aa261-111">Você pode copiar os modelos de política de grupo para qualquer servidor ou estação de trabalho que seja compatível com Windows Server ou computador cliente e que possa executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="aa261-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="aa261-112">Copiando os modelos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa261-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="aa261-113">Editando MBAM 2,0 configurações do GPO</span><span class="sxs-lookup"><span data-stu-id="aa261-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="aa261-114">Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização.</span><span class="sxs-lookup"><span data-stu-id="aa261-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="aa261-115">Para exibir e criar GPOs, você deve ter o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) instalado.</span><span class="sxs-lookup"><span data-stu-id="aa261-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="aa261-116">Editando as configurações de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa261-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="aa261-117">Mostrar ou ocultar o painel de controle do MBAM no painel de controle do Windows</span><span class="sxs-lookup"><span data-stu-id="aa261-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="aa261-118">Como o MBAM oferece um painel de controle personalizado do MBAM que pode substituir o painel de controle padrão do Windows BitLocker, você também pode optar por mostrar ou ocultar o painel de controle padrão do BitLocker dos usuários finais usando as configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="aa261-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="aa261-119">Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="aa261-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="aa261-120">Outros recursos para a implantação de objetos de política de grupo do MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="aa261-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="aa261-121">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa261-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="aa261-122">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="aa261-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="aa261-123">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="aa261-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="aa261-124">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="aa261-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





