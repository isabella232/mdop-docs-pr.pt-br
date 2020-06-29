---
title: Determinar o método de streaming
description: Determinar o método de streaming
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797971"
---
# <span data-ttu-id="52c21-103">Determinar o método de streaming</span><span class="sxs-lookup"><span data-stu-id="52c21-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="52c21-104">Na primeira vez que um usuário clica duas vezes no ícone que foi colocado em um computador por meio do processo de publicação, o cliente de virtualização do aplicativo obtém o conteúdo do pacote do aplicativo virtual de um local de origem de streaming.</span><span class="sxs-lookup"><span data-stu-id="52c21-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="52c21-105">**Observação** 
 *Streaming* é o termo usado para descrever o processo de obter conteúdo de um pacote de aplicativo sequenciado, começando com o bloco de recursos principal e, em seguida, obtendo blocos adicionais conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="52c21-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="52c21-106">O local de origem de streaming é geralmente um servidor acessível pelo computador do usuário; no entanto, alguns sistemas de distribuição eletrônicos, como o Microsoft Endpoint Configuration Manager, podem distribuir o arquivo SFT para o computador do usuário e, em seguida, transmitir o pacote de aplicativo virtual localmente do cache do computador.</span><span class="sxs-lookup"><span data-stu-id="52c21-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="52c21-107">**Observação**  Um local de origem de streaming para pacotes virtuais pode ser configurado em um computador que não seja um servidor.</span><span class="sxs-lookup"><span data-stu-id="52c21-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="52c21-108">Isso é especialmente útil em um escritório de filial pequeno que não tem servidor.</span><span class="sxs-lookup"><span data-stu-id="52c21-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="52c21-109">As fontes de streaming que podem ser usadas para armazenar aplicativos sequenciados são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="52c21-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

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
<th align="left"><span data-ttu-id="52c21-110">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="52c21-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="52c21-111">Protocolo</span><span class="sxs-lookup"><span data-stu-id="52c21-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="52c21-112">Vantagens</span><span class="sxs-lookup"><span data-stu-id="52c21-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="52c21-113">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="52c21-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="52c21-114">Links</span><span class="sxs-lookup"><span data-stu-id="52c21-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="52c21-115">Servidor de arquivos</span><span class="sxs-lookup"><span data-stu-id="52c21-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="52c21-116">Arquivo</span><span class="sxs-lookup"><span data-stu-id="52c21-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="52c21-117">Solução simples de baixo custo para configurar o servidor de arquivos existente com o \CONTENT share</span><span class="sxs-lookup"><span data-stu-id="52c21-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="52c21-118">Sem atualização ativa</span><span class="sxs-lookup"><span data-stu-id="52c21-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="52c21-119">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="52c21-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="52c21-120">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="52c21-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="52c21-121">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="52c21-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="52c21-122">Dá suporte à segurança aprimorada usando o protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="52c21-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="52c21-123">Suporte a streaming para computadores remotos pela Internet</span><span class="sxs-lookup"><span data-stu-id="52c21-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="52c21-124">Apenas uma porta em Firewall para abrir</span><span class="sxs-lookup"><span data-stu-id="52c21-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="52c21-125">Altamente dimensionável</span><span class="sxs-lookup"><span data-stu-id="52c21-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="52c21-126">Protocolo familiar</span><span class="sxs-lookup"><span data-stu-id="52c21-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="52c21-127">É necessário gerenciar o IIS</span><span class="sxs-lookup"><span data-stu-id="52c21-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="52c21-128">Sem atualização ativa</span><span class="sxs-lookup"><span data-stu-id="52c21-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="52c21-129">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="52c21-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="52c21-130">Servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="52c21-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="52c21-131">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="52c21-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="52c21-132">Atualização ativa</span><span class="sxs-lookup"><span data-stu-id="52c21-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="52c21-133">Suporta a segurança aprimorada usando o protocolo RTSP</span><span class="sxs-lookup"><span data-stu-id="52c21-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="52c21-134">Somente uma porta em Firewall para abrir (somente RTSP)</span><span class="sxs-lookup"><span data-stu-id="52c21-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="52c21-135">Duas infra-estruturas</span><span class="sxs-lookup"><span data-stu-id="52c21-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="52c21-136">Requisito de administração do servidor</span><span class="sxs-lookup"><span data-stu-id="52c21-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="52c21-137">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="52c21-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="52c21-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52c21-138">Related topics</span></span>


[<span data-ttu-id="52c21-139">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="52c21-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="52c21-140">Visão geral de cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="52c21-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="52c21-141">Determinar o método de publicação</span><span class="sxs-lookup"><span data-stu-id="52c21-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





