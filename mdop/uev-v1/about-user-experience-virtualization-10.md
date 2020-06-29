---
title: Sobre a User Experience Virtualization 1.0
description: Sobre a User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799127"
---
# <span data-ttu-id="7d30c-103">Sobre a User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="7d30c-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="7d30c-104">O Microsoft User Experience Virtualization (UE-V Experience Virtualization) monitora as alterações feitas pelos usuários nas configurações do aplicativo e configurações do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="7d30c-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="7d30c-105">As configurações do usuário são capturadas e centralizadas em um local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="7d30c-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="7d30c-106">Essas configurações podem ser aplicadas a diferentes computadores acessados pelo usuário, incluindo computadores de mesa, laptops e sessões de infraestrutura de área de trabalho virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="7d30c-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="7d30c-107">A virtualização da experiência do usuário usa modelos de local de configurações para especificar quais aplicativos e configurações do Windows nos computadores dos usuários são monitorados e centralizados.</span><span class="sxs-lookup"><span data-stu-id="7d30c-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="7d30c-108">O modelo de local de configurações é um arquivo XML que especifica quais locais de arquivo e registro estão associados a cada aplicativo ou configuração do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7d30c-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="7d30c-109">O modelo não contém valores para as configurações; Ele contém somente os locais das configurações que devem ser monitoradas.</span><span class="sxs-lookup"><span data-stu-id="7d30c-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="7d30c-110">As configurações do aplicativo e as configurações do Windows são monitoradas pela UE-V quando os usuários trabalham em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="7d30c-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="7d30c-111">Os valores das configurações do aplicativo são armazenados no servidor de armazenamento de configurações quando o usuário fecha o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7d30c-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="7d30c-112">Os valores das configurações do Windows são armazenados quando o usuário faz logoff, quando o computador está bloqueado ou quando eles são desconectados remotamente de um computador.</span><span class="sxs-lookup"><span data-stu-id="7d30c-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="7d30c-113">Um administrador pode criar um modelo de local de configurações do UE-V para especificar quais configurações do aplicativo empresarial serão transferidas para o roaming.</span><span class="sxs-lookup"><span data-stu-id="7d30c-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="7d30c-114">O UE-V inclui um conjunto de modelos de local de configurações para algumas configurações do Windows e aplicativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d30c-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="7d30c-115">Para obter uma lista de aplicativos e configurações padrão no UE-V, consulte [planejar quais aplicativos sincronizar com o UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="7d30c-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="7d30c-116">Notas de versão do UEV 1,0</span><span class="sxs-lookup"><span data-stu-id="7d30c-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="7d30c-117">Para saber mais e saber mais sobre as últimas notícias que não o fizeram na documentação, confira [notas de versão do Microsoft User Experience Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="7d30c-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="7d30c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d30c-118">Related topics</span></span>


[<span data-ttu-id="7d30c-119">Introdução à User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="7d30c-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="7d30c-120">Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="7d30c-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="7d30c-121">Arquitetura de alto nível para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7d30c-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





