---
title: Sobre aplicativos do Application Virtualization
description: Sobre aplicativos do Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797655"
---
# <span data-ttu-id="78a01-103">Sobre aplicativos do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="78a01-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="78a01-104">Na virtualização do aplicativo, um *aplicativo* é um programa executável, como o Microsoft Visio, que é transmitido para o cliente ou cliente da área de trabalho do Application Virtualization para serviços de área de trabalho remota (anteriormente serviços de terminal) de um servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="78a01-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="78a01-105">Para que um aplicativo possa ser transmitido para um cliente, o aplicativo deve estar preparado para streaming ao processá-lo com o sequenciador do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="78a01-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="78a01-106">Gerenciando aplicativos</span><span class="sxs-lookup"><span data-stu-id="78a01-106">Managing Applications</span></span>


<span data-ttu-id="78a01-107">Você deve adicionar aplicativos ao sistema para poder disponibilizá-los aos usuários.</span><span class="sxs-lookup"><span data-stu-id="78a01-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="78a01-108">O método mais comum para adicionar aplicativos ao sistema é importá-los.</span><span class="sxs-lookup"><span data-stu-id="78a01-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="78a01-109">Para acessar esse recurso, clique com o botão direito do mouse no nó **aplicativos** no console de gerenciamento do servidor do Application Virtualization e escolha **importar aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="78a01-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="78a01-110">Você pode importar mais de um arquivo OSD (Open Software Descriptor) ao mesmo tempo, ou pode importar um arquivo de projeto do sequenciador (SPRJ) que pode conter vários arquivos OSD.</span><span class="sxs-lookup"><span data-stu-id="78a01-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="78a01-111">Essa funcionalidade permite configurar aplicativos relacionados da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="78a01-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="78a01-112">Você também pode usar os seguintes recursos para ajudá-lo a gerenciar seus aplicativos:</span><span class="sxs-lookup"><span data-stu-id="78a01-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="78a01-113">**Grupos de aplicativos**— permite criar grupos lógicos de aplicativos para gerenciamento simplificado.</span><span class="sxs-lookup"><span data-stu-id="78a01-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="78a01-114">Quando são feitas alterações em um grupo (por exemplo, permissões de acesso), as alterações são aplicadas a todos os aplicativos do grupo.</span><span class="sxs-lookup"><span data-stu-id="78a01-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="78a01-115">Os aplicativos em um grupo podem vir de diferentes pacotes.</span><span class="sxs-lookup"><span data-stu-id="78a01-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="78a01-116">Seleção **múltipla**— permite que você selecione vários aplicativos ao mesmo tempo mantendo a tecla Ctrl pressionada ao clicar em um aplicativo para modificar as propriedades do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78a01-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="78a01-117">No entanto, se quiser manter uma relação entre os aplicativos, você deve criar um grupo de aplicativos para armazenar os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="78a01-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="78a01-118">**Cópia cruzada do sistema**— permite copiar aplicativos de um ambiente para outro que esteja executando a mesma versão do App-V em uma etapa.</span><span class="sxs-lookup"><span data-stu-id="78a01-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="78a01-119">Por exemplo, você pode ter um ambiente de teste de aceitação do usuário no qual você inicialmente implanta e configura aplicativos.</span><span class="sxs-lookup"><span data-stu-id="78a01-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="78a01-120">Depois de concluir a fase de teste, talvez você queira replicar o mesmo conjunto de aplicativos (incluindo permissões) para o ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="78a01-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="78a01-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78a01-121">Related topics</span></span>


[<span data-ttu-id="78a01-122">Sobre pacotes do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="78a01-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="78a01-123">Sobre o Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="78a01-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="78a01-124">Como gerenciar grupos de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="78a01-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="78a01-125">Como gerenciar aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="78a01-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





