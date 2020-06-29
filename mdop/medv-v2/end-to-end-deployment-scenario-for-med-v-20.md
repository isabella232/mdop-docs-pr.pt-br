---
title: Cenário de implantação de ponta a ponta para a MED-V 2.0
description: Cenário de implantação de ponta a ponta para a MED-V 2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799819"
---
# <span data-ttu-id="fcb09-103">Cenário de implantação de ponta a ponta para a MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="fcb09-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="fcb09-104">Este cenário de exemplo para a virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 ajuda você a implantar os componentes do MED-V na sua empresa usando vários cenários de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="fcb09-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="fcb09-105">Você pode pensar nesse exemplo de cenário como um estudo de caso que ajuda a colocar os cenários e procedimentos individuais em contexto.</span><span class="sxs-lookup"><span data-stu-id="fcb09-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="fcb09-106">Esta seção fornece informações básicas e instruções para a implantação de componentes do MED-V como uma solução completa na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fcb09-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="fcb09-107">Cenário passo a passo de implantação do MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb09-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="fcb09-108">Os tópicos deste cenário passo a passo incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fcb09-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="fcb09-109">[As configurações compatíveis com o MED-V 2,0](med-v-20-supported-configurations.md) discutem os requisitos que você deve ter para instalar e executar o Microsoft Enterprise Desktop VIRTUALIZATION (MED-v) 2.0 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="fcb09-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="fcb09-110">Este tópico especifica os requisitos do sistema operacional, os requisitos de configuração e os requisitos do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb09-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="fcb09-111">Este tópico também inclui informações de localização sobre os idiomas aos quais o MED-V 2,0 oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="fcb09-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="fcb09-112">[Visão geral da implantação do MED-V 2,0](med-v-20-deployment-overview.md) discute informações gerais e instruções para ajudá-lo a instalar e implantar o MED-v em toda a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fcb09-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="fcb09-113">Os componentes do MED-V são baseados em cliente e são entregues e gerenciados usando sua infraestrutura e processos corporativos existentes.</span><span class="sxs-lookup"><span data-stu-id="fcb09-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="fcb09-114">Este tópico fornece uma visão geral da solução MED-V que inclui informações sobre os arquivos de instalação do MED-V e os componentes do MED-V que você implanta.</span><span class="sxs-lookup"><span data-stu-id="fcb09-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="fcb09-115">Este tópico também fornece uma visão geral de alto nível do processo de instalação e implantação do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb09-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="fcb09-116">[Preparar o ambiente de implantação do MED-v](prepare-the-deployment-environment-for-med-v.md) discute como preparar seu ambiente para uma implantação do MED-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="fcb09-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="fcb09-117">Esta seção descreve os pré-requisitos necessários para o ambiente do MED-V, como o Microsoft Windows 7 e uma infraestrutura do Active Directory na qual você usa a política de grupo para fornecer gerenciamento centralizado e configuração de sistemas operacionais, aplicativos e configurações dos usuários.</span><span class="sxs-lookup"><span data-stu-id="fcb09-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="fcb09-118">Esta seção também descreve os pré-requisitos que você deve ter para instalar e implantar o MED-V 2,0 em toda a sua empresa, como o Windows Virtual PC e a atualização necessária do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="fcb09-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="fcb09-119">[Implantar os componentes do MED-V](deploy-the-med-v-components.md) discute as diferentes maneiras de instalar todos os arquivos de instalação necessários e os componentes do MED-v em toda a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fcb09-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="fcb09-120">Para instalar e implantar o MED-V, você geralmente segue estas etapas:</span><span class="sxs-lookup"><span data-stu-id="fcb09-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="fcb09-121">Instale o **pacote do espaço de trabalho do MED-v** no computador administrador que você usará para criar os pacotes do espaço de trabalho do MED-v.</span><span class="sxs-lookup"><span data-stu-id="fcb09-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="fcb09-122">Para obter mais informações, consulte [como instalar o pacote do espaço de trabalho do MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="fcb09-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="fcb09-123">Criar e testar seus pacotes de espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb09-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="fcb09-124">Para obter mais informações, consulte [criar um pacote do espaço de trabalho do MED-v](create-a-med-v-workspace-package.md) e [testar o pacote do espaço de trabalho do MED-v](testing-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="fcb09-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="fcb09-125">Implante o MED-V em toda a sua empresa usando o método existente da sua empresa para a implantação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fcb09-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="fcb09-126">Para obter mais informações, consulte [implantando o pacote do espaço de trabalho do MED-V](deploying-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="fcb09-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="fcb09-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcb09-127">Related topics</span></span>


[<span data-ttu-id="fcb09-128">Implantação da MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb09-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="fcb09-129">Cenário de planejamento de ponta a ponta para a MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="fcb09-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="fcb09-130">Cenário de operações de ponta a ponta para a MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="fcb09-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





