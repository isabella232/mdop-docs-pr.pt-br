---
title: Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager
description: Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796031"
---
# <span data-ttu-id="0c2c6-103">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0c2c6-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="0c2c6-104">Se você estiver instalando o recurso de integração do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando o recurso de integração do System Center Configuration Manager, será necessário concluir os pré-requisitos descritos neste tópico, além daqueles dos [pré-requisitos do MBAM 2,5 Server para topologias autônomas e de integração do Configuration Manager](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c6-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="0c2c6-105">Você também deve criar ou modificar arquivos. mof necessários para a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0c2c6-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="0c2c6-106">Pré-requisitos para o recurso de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0c2c6-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="0c2c6-107">Se você estiver configurando o MBAM com a topologia de integração do System Center Configuration Manager, será necessário concluir pré-requisitos adicionais necessários para o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0c2c6-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="0c2c6-108">Pré-requisitos para o recurso de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0c2c6-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="0c2c6-109">Editar o arquivo Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="0c2c6-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="0c2c6-110">Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo Configuration. MOF para SystemCenter2012 ConfigurationManager e o Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="0c2c6-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="0c2c6-111">Edite o arquivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="0c2c6-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="0c2c6-112">Criar ou editar o arquivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="0c2c6-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="0c2c6-113">Para permitir que os computadores cliente relatem os detalhes de conformidade do BitLocker nos relatórios do Gerenciador de configuração do MBAM, você precisa criar ou editar o arquivo SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="0c2c6-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="0c2c6-114">Se estiver usando o SystemCenter2012 ConfigurationManager, você deve criar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0c2c6-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="0c2c6-115">No Configuration Manager 2007, o arquivo já existe, portanto, você precisa editar, mas não substituir, o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="0c2c6-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="0c2c6-116">Criar ou editar o arquivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="0c2c6-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="0c2c6-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c2c6-117">Related topics</span></span>


[<span data-ttu-id="0c2c6-118">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0c2c6-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="0c2c6-119">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0c2c6-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="0c2c6-120">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0c2c6-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="0c2c6-121">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="0c2c6-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0c2c6-122">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="0c2c6-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0c2c6-123">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0c2c6-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




