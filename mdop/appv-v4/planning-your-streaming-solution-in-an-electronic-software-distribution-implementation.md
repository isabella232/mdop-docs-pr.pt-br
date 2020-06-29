---
title: Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software
description: Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796809"
---
# <span data-ttu-id="75f8e-103">Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="75f8e-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="75f8e-104">Se você decidir usar os servidores de streaming em conjunto com o seu sistema ESD para disponibilizar o conteúdo do aplicativo para os computadores dos usuários finais, poderá escolher entre várias alternativas, tirando proveito de qualquer infraestrutura que já esteja no lugar.</span><span class="sxs-lookup"><span data-stu-id="75f8e-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="75f8e-105">Por exemplo, se o seu sistema ESD tiver compartilhamentos de distribuição de software nos servidores nas filiais do campo, você poderá colocar o compartilhamento de \\CONTENT do Application Virtualization nesses servidores e, em seguida, configurar os clientes para usar esse compartilhamento de conteúdo como fonte de conteúdo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75f8e-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="75f8e-106">As opções com suporte incluem o uso de um servidor de arquivos ou um servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="75f8e-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="75f8e-107">Você também pode instalar o servidor de streaming do Application Virtualization em um servidor de arquivos ou servidor IIS existente.</span><span class="sxs-lookup"><span data-stu-id="75f8e-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="75f8e-108">O servidor de streaming do Application Virtualization oferece suporte para o recurso atualização ativa na virtualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75f8e-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="75f8e-109">O recurso atualização ativa permite que uma nova versão de um aplicativo seja adicionada a um servidor de gerenciamento do App-V ou servidor de fluxo contínuo sem afetar os usuários que atualmente executam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75f8e-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="75f8e-110">Os clientes App-V receberão automaticamente a versão mais recente do aplicativo do servidor de gerenciamento do App-V ou do servidor de streaming na próxima vez em que o usuário iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75f8e-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="75f8e-111">O uso do protocolo RTSP (S) é necessário para este recurso.</span><span class="sxs-lookup"><span data-stu-id="75f8e-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="75f8e-112">Se você optar por não usar o servidor de streaming do Application Virtualization, será necessário gerenciar explicitamente as atualizações dos pacotes de aplicativos usando o sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="75f8e-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="75f8e-113">**Observação**  O acesso aos aplicativos é controlado por meio de grupos de segurança nos serviços de domínio Active Directory, portanto, você precisará planejar um processo para configurar um grupo de segurança para cada aplicativo virtual e para gerenciar quais usuários serão adicionados a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="75f8e-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="75f8e-114">O administrador do sistema do Application Virtualization configura cada servidor de streaming para usar esses grupos do Active Directory aplicando ACLs aos diretórios de aplicativos no compartilhamento de conteúdo, que controla o acesso aos pacotes com base em associações de grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75f8e-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="75f8e-115">As características das opções de streaming disponíveis são resumidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="75f8e-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="75f8e-116">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="75f8e-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="75f8e-117">Protocolo</span><span class="sxs-lookup"><span data-stu-id="75f8e-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="75f8e-118">Vantagens</span><span class="sxs-lookup"><span data-stu-id="75f8e-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="75f8e-119">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="75f8e-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="75f8e-120">Links</span><span class="sxs-lookup"><span data-stu-id="75f8e-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75f8e-121">Servidor de arquivos</span><span class="sxs-lookup"><span data-stu-id="75f8e-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="75f8e-122">SMB</span><span class="sxs-lookup"><span data-stu-id="75f8e-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="75f8e-123">Solução simples de baixo custo para configurar o servidor de arquivos existente com o \CONTENT share</span><span class="sxs-lookup"><span data-stu-id="75f8e-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="75f8e-124">Sem atualização ativa</span><span class="sxs-lookup"><span data-stu-id="75f8e-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="75f8e-125">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="75f8e-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75f8e-126">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="75f8e-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="75f8e-127">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="75f8e-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="75f8e-128">Suporte à segurança aprimorada usando o protocolo HTTPS</span><span class="sxs-lookup"><span data-stu-id="75f8e-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="75f8e-129">Suporte a streaming para computadores remotos pela Internet</span><span class="sxs-lookup"><span data-stu-id="75f8e-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="75f8e-130">Apenas uma porta em Firewall para abrir</span><span class="sxs-lookup"><span data-stu-id="75f8e-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="75f8e-131">Escaláveis</span><span class="sxs-lookup"><span data-stu-id="75f8e-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="75f8e-132">Protocolo familiar</span><span class="sxs-lookup"><span data-stu-id="75f8e-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="75f8e-133">É necessário gerenciar o IIS</span><span class="sxs-lookup"><span data-stu-id="75f8e-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="75f8e-134">Sem atualização ativa</span><span class="sxs-lookup"><span data-stu-id="75f8e-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="75f8e-135">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="75f8e-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75f8e-136">Servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="75f8e-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="75f8e-137">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="75f8e-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="75f8e-138">Atualização ativa</span><span class="sxs-lookup"><span data-stu-id="75f8e-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="75f8e-139">Suporta a segurança aprimorada usando o protocolo RTSP</span><span class="sxs-lookup"><span data-stu-id="75f8e-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="75f8e-140">Apenas uma porta em Firewall para abrir</span><span class="sxs-lookup"><span data-stu-id="75f8e-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="75f8e-141">Duas infra-estruturas</span><span class="sxs-lookup"><span data-stu-id="75f8e-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="75f8e-142">Requisito de administração do servidor</span><span class="sxs-lookup"><span data-stu-id="75f8e-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="75f8e-143">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="75f8e-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="75f8e-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75f8e-144">Related topics</span></span>


[<span data-ttu-id="75f8e-145">Como configurar servidores para a implantação baseada em ESD</span><span class="sxs-lookup"><span data-stu-id="75f8e-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="75f8e-146">Visão geral de segurança e proteção</span><span class="sxs-lookup"><span data-stu-id="75f8e-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="75f8e-147">Publicação de aplicativos virtuais usando a Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="75f8e-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





