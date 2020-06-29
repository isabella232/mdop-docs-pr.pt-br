---
title: Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server
description: Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796811"
---
# <span data-ttu-id="eb82b-103">Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="eb82b-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="eb82b-104">Se você quiser usar os servidores de streaming do Application Virtualization em conjunto com a implementação baseada em servidor de gerenciamento do Application Virtualization, poderá escolher entre várias alternativas, tirando proveito de qualquer infraestrutura que já esteja no lugar.</span><span class="sxs-lookup"><span data-stu-id="eb82b-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="eb82b-105">Por exemplo, se você já tem servidores em suas filiais de campo, pode colocar o compartilhamento do \\CONTENT do Application Virtualization nesses servidores e, em seguida, configurar os clientes para usar esse compartilhamento de conteúdo como fonte de conteúdo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb82b-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="eb82b-106">Se você optar por usar somente servidores de gerenciamento do Application Virtualization — por exemplo, se tiver apenas um único escritório, os clientes podem transmitir conteúdo desse servidor.</span><span class="sxs-lookup"><span data-stu-id="eb82b-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="eb82b-107">As opções com suporte incluem o uso de um servidor de arquivos, um servidor IIS ou um servidor de streaming do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="eb82b-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="eb82b-108">Você também pode instalar o servidor de streaming do Application Virtualization em um servidor de arquivos ou servidor IIS existente.</span><span class="sxs-lookup"><span data-stu-id="eb82b-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="eb82b-109">As características dessas diferentes opções são resumidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb82b-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="eb82b-110">**Observação**  O recurso atualização ativa permite que uma nova versão de um aplicativo seja adicionada a um servidor de gerenciamento do App-V ou servidor de fluxo contínuo sem afetar os usuários que atualmente executam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb82b-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="eb82b-111">Os clientes App-V receberão automaticamente a versão mais recente do aplicativo do servidor de gerenciamento do App-V ou do servidor de streaming na próxima vez em que o usuário iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb82b-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="eb82b-112">O uso do protocolo RTSP (S) é necessário para este recurso.</span><span class="sxs-lookup"><span data-stu-id="eb82b-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

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
<th align="left"><span data-ttu-id="eb82b-113">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="eb82b-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="eb82b-114">Protocolo</span><span class="sxs-lookup"><span data-stu-id="eb82b-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="eb82b-115">Vantagens</span><span class="sxs-lookup"><span data-stu-id="eb82b-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="eb82b-116">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="eb82b-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="eb82b-117">Links</span><span class="sxs-lookup"><span data-stu-id="eb82b-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb82b-118">Servidor de arquivos</span><span class="sxs-lookup"><span data-stu-id="eb82b-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb82b-119">SMB</span><span class="sxs-lookup"><span data-stu-id="eb82b-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-120">Solução simples de baixo custo para configurar o servidor de arquivos existente com o \CONTENT share</span><span class="sxs-lookup"><span data-stu-id="eb82b-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-121">Sem atualização ativa</span><span class="sxs-lookup"><span data-stu-id="eb82b-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="eb82b-122">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="eb82b-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb82b-123">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="eb82b-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb82b-124">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="eb82b-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-125">Suporte à segurança aprimorada usando o protocolo HTTPS</span><span class="sxs-lookup"><span data-stu-id="eb82b-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="eb82b-126">Suporte a streaming para computadores remotos pela Internet</span><span class="sxs-lookup"><span data-stu-id="eb82b-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="eb82b-127">Apenas uma porta em Firewall para abrir</span><span class="sxs-lookup"><span data-stu-id="eb82b-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="eb82b-128">Escaláveis</span><span class="sxs-lookup"><span data-stu-id="eb82b-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="eb82b-129">Protocolo familiar</span><span class="sxs-lookup"><span data-stu-id="eb82b-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-130">É necessário gerenciar o IIS</span><span class="sxs-lookup"><span data-stu-id="eb82b-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="eb82b-131">Sem atualização ativa</span><span class="sxs-lookup"><span data-stu-id="eb82b-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="eb82b-132">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="eb82b-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb82b-133">Servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="eb82b-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb82b-134">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="eb82b-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-135">Atualização ativa</span><span class="sxs-lookup"><span data-stu-id="eb82b-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="eb82b-136">Suporta a segurança aprimorada usando o protocolo RTSP</span><span class="sxs-lookup"><span data-stu-id="eb82b-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="eb82b-137">Apenas uma porta em Firewall para abrir</span><span class="sxs-lookup"><span data-stu-id="eb82b-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-138">Duas infra-estruturas</span><span class="sxs-lookup"><span data-stu-id="eb82b-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="eb82b-139">Requisito de administração do servidor</span><span class="sxs-lookup"><span data-stu-id="eb82b-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="eb82b-140">Como configurar os Application Virtualization Streaming Servers</span><span class="sxs-lookup"><span data-stu-id="eb82b-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb82b-141">Servidor de gerenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="eb82b-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb82b-142">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="eb82b-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-143">Atualização ativa</span><span class="sxs-lookup"><span data-stu-id="eb82b-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="eb82b-144">Suporta a segurança aprimorada usando o protocolo RTSP</span><span class="sxs-lookup"><span data-stu-id="eb82b-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="eb82b-145">Apenas uma porta em Firewall para abrir</span><span class="sxs-lookup"><span data-stu-id="eb82b-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb82b-146">Duas infra-estruturas</span><span class="sxs-lookup"><span data-stu-id="eb82b-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="eb82b-147">Requisito de administração do servidor</span><span class="sxs-lookup"><span data-stu-id="eb82b-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="eb82b-148">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="eb82b-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="eb82b-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb82b-149">Related topics</span></span>


[<span data-ttu-id="eb82b-150">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="eb82b-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="eb82b-151">Visão geral dos Componentes do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="eb82b-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="eb82b-152">Publicação de aplicativos virtuais usando os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="eb82b-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





