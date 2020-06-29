---
title: Sobre o Microsoft Application Virtualization 4.5
description: Sobre o Microsoft Application Virtualization 4.5
author: dansimp
ms.assetid: 39f45a6f-ac55-4fd7-8a83-865e1a7034f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 30f285680ab24e9c638ff8a200946925074bddf1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797643"
---
# <span data-ttu-id="e00f9-103">Sobre o Microsoft Application Virtualization 4.5</span><span class="sxs-lookup"><span data-stu-id="e00f9-103">About Microsoft Application Virtualization 4.5</span></span>


<span data-ttu-id="e00f9-104">Anteriormente conhecido como SoftGrid Application Virtualization, o Microsoft Application Virtualization (App-V) 4,5 é o primeiro lançamento da marca Microsoft do produto.</span><span class="sxs-lookup"><span data-stu-id="e00f9-104">Formerly known as SoftGrid Application Virtualization, Microsoft Application Virtualization (App-V) 4.5 is the first Microsoft-branded release of the product.</span></span> <span data-ttu-id="e00f9-105">Ele inclui novos recursos que tornam mais fácil para as organizações de ti de empresas dar suporte a implementações de virtualização de aplicativos globais de grande escala.</span><span class="sxs-lookup"><span data-stu-id="e00f9-105">It includes new capabilities that make it easy for enterprise IT organizations to support large-scale, global application virtualization implementations.</span></span>

-   <span data-ttu-id="e00f9-106">Virtualização dinâmica: o App-V 4,5 fornece a flexibilidade para controlar a interação do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="e00f9-106">Dynamic Virtualization: App-V 4.5 provides the flexibility to control virtual application interaction.</span></span> <span data-ttu-id="e00f9-107">Os administradores que desejam consolidar ambientes virtuais e permitir a administração mais fácil e rápida podem usar a composição do pacote dinâmico do produto, que sequencia e gerencia pacotes para aplicativos middleware separadamente do aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="e00f9-107">Administrators who want to consolidate virtual environments and enable faster, easier administration, can use the product’s Dynamic Suite Composition, which sequences and manages packages for middleware applications separately from the main application.</span></span> <span data-ttu-id="e00f9-108">Ele reduz o tamanho do pacote potencial ao eliminar o empacotamento redundante do middleware.</span><span class="sxs-lookup"><span data-stu-id="e00f9-108">It shrinks potential package size by eliminating redundant packaging of middleware.</span></span> <span data-ttu-id="e00f9-109">Isso permite que vários aplicativos da Web se comuniquem com a mesma instância única de um aplicativo virtualizado, por exemplo, Microsoft .NET Framework ou Sun Java Runtime Environment (JRE).</span><span class="sxs-lookup"><span data-stu-id="e00f9-109">This lets multiple Web applications communicate with the same single instance of a virtualized application of, for example, Microsoft .NET Framework or Sun Java Runtime Environment (JRE).</span></span> <span data-ttu-id="e00f9-110">As atualizações para middleware virtual comum são simplificadas e um aplicativo virtual é atualizado em vez de vários.</span><span class="sxs-lookup"><span data-stu-id="e00f9-110">Updates for the common virtual middleware are simplified and one virtual application is updated instead of several.</span></span> <span data-ttu-id="e00f9-111">Essa funcionalidade "muitos-para-um" reduz bastante o custo das atualizações.</span><span class="sxs-lookup"><span data-stu-id="e00f9-111">This “many-to-one” capability greatly reduces the cost of updates.</span></span> <span data-ttu-id="e00f9-112">Ele também facilita a implantação e o gerenciamento de aplicativos que usam vários plug-ins e suplementos, além de melhorar o gerenciamento da distribuição de plug-in para grupos de usuários diferentes.</span><span class="sxs-lookup"><span data-stu-id="e00f9-112">It also makes it easier to deploy and manage applications that use multiple plug-ins and add-ins, and improves management of plug-in distribution to different user groups.</span></span>

-   <span data-ttu-id="e00f9-113">Escalabilidade estendida: escolha entre três modos de implantação flexíveis:</span><span class="sxs-lookup"><span data-stu-id="e00f9-113">Extended Scalability: Choose among three flexible deployment modes:</span></span>

    1.  <span data-ttu-id="e00f9-114">O servidor de gerenciamento do Application Virtualization, que é fornecido como parte do Microsoft Desktop Optimization Pack e do Microsoft Application Virtualization para pacotes de serviços de área de trabalho remota, permite o fluxo dinâmico, incluindo pacotes e atualizações ativas, e requer o Microsoft SQL Server e os serviços de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e00f9-114">Application Virtualization Management Server, which ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, enables dynamic streaming including package and active upgrades, and requires Microsoft Active Directory Domain Services and Microsoft SQL Server.</span></span>

    2.  <span data-ttu-id="e00f9-115">O servidor de streaming do Application Virtualization, uma versão simples que também é fornecida como parte do Microsoft Desktop Optimization Pack e do Microsoft Application Virtualization para pacotes de serviços de área de trabalho remota, oferece streaming de aplicativos, incluindo pacotes e atualizações ativas, sem os serviços de domínio Active Directory e o banco de dados e permite que os administradores implantem em servidores existentes ou adicionem o streaming a sistemas ESD</span><span class="sxs-lookup"><span data-stu-id="e00f9-115">Application Virtualization Streaming Server, a lightweight version which also ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, offers application streaming including package and active upgrades without the Active Directory Domain Services and database overheads, and enables administrators to deploy to existing servers or add streaming to Electronic Software Delivery (ESD) systems.</span></span>

    3.  <span data-ttu-id="e00f9-116">O modo autônomo permite que aplicativos virtuais sejam executados sem streaming e sejam interoperáveis com o Microsoft Endpoint Configuration Manager e sistemas ESD de terceiros.</span><span class="sxs-lookup"><span data-stu-id="e00f9-116">Standalone mode enables virtual applications to run without streaming and is interoperable with Microsoft Endpoint Configuration Manager and third-party ESD systems.</span></span>

-   <span data-ttu-id="e00f9-117">Globalização: o produto é localizado entre 11 idiomas, inclui suporte a aplicativos de idioma estrangeiro que usam caracteres especiais e suporte à detecção de idioma estrangeiro do Active Directory e servidores e à detecção de localidade do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e00f9-117">Globalization: The product is localized across 11 languages, includes support for foreign language applications that use special characters, and supports foreign language Active Directory and servers and runtime locale detection.</span></span>

-   <span data-ttu-id="e00f9-118">Padrões de segurança da Microsoft: o Microsoft Application Virtualization (App-V) 4,5 está em conformidade com os padrões de segurança da Microsoft, incluindo computação confiável, iniciativa proteger do Windows e ciclo de vida de desenvolvimento de segurança.</span><span class="sxs-lookup"><span data-stu-id="e00f9-118">Microsoft Security Standards: Microsoft Application Virtualization (App-V) 4.5 complies with Microsoft security standards including Trustworthy Computing, Secure Windows Initiative and Security Development Lifecycle.</span></span> <span data-ttu-id="e00f9-119">Ele inclui suporte a cenários voltados para a Internet e fornece segurança por configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="e00f9-119">It includes support for Internet-facing scenarios and provides Secure by Default configuration out of the box.</span></span>

## <span data-ttu-id="e00f9-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e00f9-120">In This Section</span></span>


<a href="" id="microsoft-application-virtualization-management-system-release-notes"></a>[<span data-ttu-id="e00f9-121">Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e00f9-121">Microsoft Application Virtualization Management System Release Notes</span></span>](microsoft-application-virtualization-management-system-release-notes.md)  
<span data-ttu-id="e00f9-122">Fornece as informações mais atualizadas sobre problemas conhecidos com o Microsoft Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="e00f9-122">Provides the most up-to-date information about known issues with Microsoft Application Virtualization (App-V) 4.5.</span></span>

 

 





