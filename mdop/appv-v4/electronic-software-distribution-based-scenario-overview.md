---
title: Visão geral de cenário baseado em Distribuição Eletrônica de Software
description: Visão geral de cenário baseado em Distribuição Eletrônica de Software
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797957"
---
# <span data-ttu-id="c37be-103">Visão geral de cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="c37be-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="c37be-104">Se você pretende usar uma solução ESD (Electronic Software Distribution) para implantar aplicativos virtuais, é importante entender os fatores que entram e são afetados por essa decisão.</span><span class="sxs-lookup"><span data-stu-id="c37be-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="c37be-105">Este tópico descreve os benefícios de usar um cenário baseado em ESD e fornece informações sobre os métodos de publicação e streaming de pacote que você precisará considerar ao prosseguir com a implantação.</span><span class="sxs-lookup"><span data-stu-id="c37be-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="c37be-106">**Importante**  Seja qual for a solução ESD que você usa, você deve estar familiarizado com os requisitos de sua solução específica.</span><span class="sxs-lookup"><span data-stu-id="c37be-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="c37be-107">Se você estiver usando o Gerenciador de configuração do Microsoft EndPoint, consulte a documentação do Configuration Manager em <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="c37be-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="c37be-108">O uso de um sistema ESD existente oferece os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="c37be-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="c37be-109">Elimina duas infra-estruturas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c37be-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="c37be-110">Reduz o custo de hardware adicional</span><span class="sxs-lookup"><span data-stu-id="c37be-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="c37be-111">Reduz o custo de licenças adicionais do sistema operacional e do banco de dados</span><span class="sxs-lookup"><span data-stu-id="c37be-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="c37be-112">Métodos de publicação</span><span class="sxs-lookup"><span data-stu-id="c37be-112">Publishing Methods</span></span>


<span data-ttu-id="c37be-113">Ao usar um cenário baseado em ESD, você tem as seguintes opções para publicar o aplicativo para os clientes:</span><span class="sxs-lookup"><span data-stu-id="c37be-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="c37be-114">Windows Installer autônomo.</span><span class="sxs-lookup"><span data-stu-id="c37be-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="c37be-115">O arquivo do Windows Installer contém o manifesto e os arquivos OSD e ICO que os clientes usam para configurar um pacote.</span><span class="sxs-lookup"><span data-stu-id="c37be-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="c37be-116">O arquivo do Windows Installer também copia o arquivo SFT para o cliente porque esse cenário não usa um servidor.</span><span class="sxs-lookup"><span data-stu-id="c37be-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="c37be-117">Windows Installer com o manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="c37be-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="c37be-118">O arquivo do Windows Installer contém o manifesto e os arquivos OSD e ICO que os clientes usam para configurar um pacote.</span><span class="sxs-lookup"><span data-stu-id="c37be-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="c37be-119">O arquivo SFT está armazenado em um servidor.</span><span class="sxs-lookup"><span data-stu-id="c37be-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="c37be-120">Um parâmetro de linha de comando direciona o cliente para o local do arquivo SFT.</span><span class="sxs-lookup"><span data-stu-id="c37be-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="c37be-121">Comandos SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="c37be-121">SFTMIME commands.</span></span>** <span data-ttu-id="c37be-122">Os comandos SFTMIME são usados com os arquivos manifest, OSD, ICO e SFT para adicionar pacotes ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c37be-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="c37be-123">O arquivo de manifesto deve estar no computador cliente ou deve ser acessível por meio de um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="c37be-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="c37be-124">Dependendo da configuração do cliente e das opções da linha de comando, os arquivos OSD, ICO e SFT podem estar no computador cliente ou em um servidor.</span><span class="sxs-lookup"><span data-stu-id="c37be-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="c37be-125">Para obter informações mais detalhadas sobre os métodos de publicação precedentes, consulte [determinar o método de publicação](determine-your-publishing-method.md).</span><span class="sxs-lookup"><span data-stu-id="c37be-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="c37be-126">Métodos de streaming de pacote</span><span class="sxs-lookup"><span data-stu-id="c37be-126">Package Streaming Methods</span></span>


<span data-ttu-id="c37be-127">Você precisará determinar o método que o sistema de virtualização de aplicativos usará para transmitir os pacotes de aplicativos virtuais ou arquivos SFT do servidor para os clientes.</span><span class="sxs-lookup"><span data-stu-id="c37be-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="c37be-128">As opções de streaming a seguir estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="c37be-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="c37be-129">Servidor de streaming do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c37be-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="c37be-130">Se você usar um servidor de streaming do Application Virtualization em sua configuração, os arquivos SFT serão transmitidos para os clientes desse servidor usando protocolos RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="c37be-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="c37be-131">Você deve instalar o software do servidor em um computador e deve configurá-lo por meio do registro, mas essa configuração não depende de serviços como SQL ou dos serviços de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c37be-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="c37be-132">Os arquivos SFT são armazenados no servidor em um local acessível pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="c37be-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="c37be-133">As informações de publicação podem ser distribuídas para os clientes por meio de qualquer mecanismo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="c37be-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="c37be-134">No entanto, quando configurado, o cliente recebe atualizações automáticas de pacote e atualização ativa é compatível.</span><span class="sxs-lookup"><span data-stu-id="c37be-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="c37be-135">Servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c37be-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="c37be-136">Se você usar um servidor de gerenciamento do Application Virtualization em sua configuração, os arquivos SFT serão transmitidos para os clientes desse servidor usando protocolos RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="c37be-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="c37be-137">Você gerencia esse servidor por meio do console de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c37be-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="c37be-138">Essa configuração usa um banco de dados SQL e os serviços do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c37be-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="c37be-139">O servidor pode distribuir informações de publicação para os clientes, portanto, outros mecanismos de publicação não são necessários.</span><span class="sxs-lookup"><span data-stu-id="c37be-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="c37be-140">Servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c37be-140">File server.</span></span>** <span data-ttu-id="c37be-141">Se você usar um servidor de arquivos em sua configuração, os arquivos SFT serão transmitidos para os outros computadores cliente usando protocolos SMB.</span><span class="sxs-lookup"><span data-stu-id="c37be-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="c37be-142">Os servidores de arquivos usados nessa configuração são gerenciados pela criação de listas de controle de acesso (ACLs) nos arquivos de compartilhamento e arquivos SFT.</span><span class="sxs-lookup"><span data-stu-id="c37be-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="c37be-143">Deve-se ter cuidado para direcionar os clientes para os arquivos corretos no servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c37be-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="c37be-144">Servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="c37be-144">IIS server.</span></span>** <span data-ttu-id="c37be-145">Se você usar um servidor IIS na configuração, os arquivos SFT serão transmitidos para os clientes desse servidor usando protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c37be-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="c37be-146">O servidor IIS é fácil de configurar e gerenciar.</span><span class="sxs-lookup"><span data-stu-id="c37be-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="c37be-147">Deve-se tomar cuidado para direcionar os clientes para os arquivos corretos no servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="c37be-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="c37be-148">Para obter informações mais detalhadas sobre os métodos de transmissão anteriores, consulte [determinar o método de transmissão](determine-your-streaming-method.md).</span><span class="sxs-lookup"><span data-stu-id="c37be-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="c37be-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c37be-149">Related topics</span></span>


[<span data-ttu-id="c37be-150">Parâmetros de linha de comando do instalador do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="c37be-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="c37be-151">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c37be-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="c37be-152">Determinar o método de publicação</span><span class="sxs-lookup"><span data-stu-id="c37be-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="c37be-153">Determinar o método de streaming</span><span class="sxs-lookup"><span data-stu-id="c37be-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="c37be-154">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="c37be-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="c37be-155">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c37be-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





