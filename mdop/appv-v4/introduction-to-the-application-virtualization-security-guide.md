---
title: Introdução ao guia de segurança do Application Virtualization
description: Introdução ao guia de segurança do Application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796891"
---
# <span data-ttu-id="6f1ba-103">Introdução ao guia de segurança do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6f1ba-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="6f1ba-104">Este guia de segurança do Microsoft Application Virtualization (App-V) fornece instruções para administradores que são responsáveis por configurar os recursos de segurança que foram selecionados para a implantação do App-V.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="6f1ba-105">**Observação**  Esta documentação não fornece orientação para escolher as opções de segurança específicas.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="6f1ba-106">Essas informações são fornecidas no White paper sobre as práticas recomendadas de segurança do App-V disponíveis em <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="6f1ba-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="6f1ba-107">Como administrador do App-V usando este guia, você deve estar familiarizado com as seguintes tecnologias relacionadas à segurança:</span><span class="sxs-lookup"><span data-stu-id="6f1ba-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="6f1ba-108">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6f1ba-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="6f1ba-109">Infraestrutura de chave pública (PKI)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="6f1ba-110">Segurança do protocolo Internet (IPsec)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="6f1ba-111">Políticas de grupo</span><span class="sxs-lookup"><span data-stu-id="6f1ba-111">Group Policies</span></span>

-   <span data-ttu-id="6f1ba-112">Serviços de informações da Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="6f1ba-113">Componentes da infraestrutura do APP-V</span><span class="sxs-lookup"><span data-stu-id="6f1ba-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="6f1ba-114">Ao planejar um ambiente Security App-V aprimorado, você pode considerar vários modelos de infraestrutura diferentes.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="6f1ba-115">**Observação**  Para obter mais informações sobre modelos de infraestrutura do App-V, consulte a seguinte documentação:</span><span class="sxs-lookup"><span data-stu-id="6f1ba-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="6f1ba-116">Guia de planejamento e implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="6f1ba-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="6f1ba-117">Planejamento de infraestrutura e série de guias de design</span><span class="sxs-lookup"><span data-stu-id="6f1ba-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="6f1ba-118">Esses modelos utilizam alguns, mas possivelmente não todos os componentes do App-V descritos na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![diagrama de filial do App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="6f1ba-120">Servidor de gerenciamento do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="6f1ba-121">O servidor de gerenciamento do App-V transmite o conteúdo do pacote e publica os atalhos e associações de tipo de arquivo para o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="6f1ba-122">O App-V Management Server também dá suporte à atualização ativa, ao gerenciamento de licenças e a um banco de dados que pode ser usado para relatórios.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="6f1ba-123">Servidor de streaming do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="6f1ba-124">O servidor de streaming App-V hospeda os pacotes para clientes de streaming para aplicativos do App-V em ambientes como filiais, onde a largura de banda da conexão com o servidor de gerenciamento do App-V é insuficiente para transmitir o conteúdo do pacote para os clientes.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="6f1ba-125">O servidor de streaming contém apenas a funcionalidade de streaming e não fornece o console de gerenciamento do App-V ou o serviço Web de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="6f1ba-126">Repositório de dados do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="6f1ba-127">O repositório de dados App-V, no banco de dados SQL, retém as informações relacionadas à infraestrutura do App-V.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="6f1ba-128">As informações no repositório de dados App-V incluem todos os registros de aplicativos, atribuições de aplicativo e quais grupos gerenciam o ambiente de virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="6f1ba-129">Serviço de gerenciamento do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="6f1ba-130">O serviço de gerenciamento do App-V comunica solicitações de leitura/gravação ao repositório de dados do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="6f1ba-131">Esse componente pode ser instalado no mesmo computador que o servidor de gerenciamento do App-V ou em um computador separado com o IIS instalado.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="6f1ba-132">Console de gerenciamento do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="6f1ba-133">O console de gerenciamento do App-V é um utilitário de gerenciamento de snap-in para administração do App-V Server.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="6f1ba-134">Esse componente pode ser instalado no mesmo computador que o servidor do App-V ou em uma estação de trabalho separada que tenha o MMC 3.0 e o. .NET 2.0 instalado.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="6f1ba-135">Sequenciador do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="6f1ba-136">O sequenciador do App-V monitora e captura a instalação de aplicativos e cria pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="6f1ba-137">A saída do sequenciador consiste no ícone do aplicativo, o arquivo OSD contendo informações de definição do aplicativo, um arquivo de manifesto do pacote e um arquivo SFT que contém os arquivos de conteúdo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="6f1ba-138">Opcionalmente, um arquivo do Windows Installer pode ser criado para instalar o pacote sem usar a infraestrutura do App-V.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="6f1ba-139">Cliente do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="6f1ba-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="6f1ba-140">O cliente App-V está instalado no computador cliente da área de trabalho do App-V ou no computador cliente dos serviços de terminal do App-V.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="6f1ba-141">Ele fornece o ambiente virtual para os pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="6f1ba-142">O cliente App-V gerencia o pacote de streaming para o cache, a atualização de publicação de aplicativo virtual e a interação com os servidores de virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6f1ba-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





