---
title: Cenários de servidor voltado para a Internet para redes de perímetro
description: Cenários de servidor voltado para a Internet para redes de perímetro
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796894"
---
# <span data-ttu-id="e3868-103">Cenários de servidor voltado para a Internet para redes de perímetro</span><span class="sxs-lookup"><span data-stu-id="e3868-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="e3868-104">O App-V 4.5 é compatível com cenários de servidor voltados para a Internet, em que os usuários que não estão conectados à rede corporativa ou que desconectam-se da rede ainda podem usar o App-V.</span><span class="sxs-lookup"><span data-stu-id="e3868-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="e3868-105">Conforme mostrado na ilustração a seguir, só há suporte para o uso de protocolos seguros na Internet (RTSPs e HTTPS).</span><span class="sxs-lookup"><span data-stu-id="e3868-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![diagrama de posicionamento do firewall do App-v](images/appvfirewalls.gif)

<span data-ttu-id="e3868-107">Você pode configurar uma solução voltada à Internet usando um ISA Server, no qual a infraestrutura do App-V está na rede interna das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="e3868-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="e3868-108">Crie uma regra de publicação na Web para o servidor IIS que hospeda os arquivos ICO e OSD, e, opcionalmente, os pacotes para transmissão, localizado na rede interna.</span><span class="sxs-lookup"><span data-stu-id="e3868-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="e3868-109">As etapas detalhadas são fornecidas em <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="e3868-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="e3868-110">Crie uma regra de publicação de servidor para o servidor de gerenciamento da Web do App-V (RTSPs).</span><span class="sxs-lookup"><span data-stu-id="e3868-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="e3868-111">As etapas detalhadas são fornecidas em [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="e3868-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="e3868-112">Conforme mostrado na ilustração a seguir, se a infraestrutura tiver implementado outros firewalls entre o cliente e o servidor ISA ou entre o ISA Server e a rede interna, as regras de firewall RTSP (TCP 322) e HTTPS (TCP 443) devem ser criadas para dar suporte ao fluxo de tráfego.</span><span class="sxs-lookup"><span data-stu-id="e3868-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="e3868-113">Além disso, se os firewalls foram implementados entre o ISA Server e a rede interna, o tráfego padrão necessário para os membros do domínio deve ser permitido para o encapsulamento por meio do firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span><span class="sxs-lookup"><span data-stu-id="e3868-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![diagrama de firewall de rede de perímetro do App-v](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="e3868-115">Como as soluções de firewall variam de um ambiente para o ambiente, as orientações fornecidas neste tópico descrevem o tráfego que seria necessário para configurar um ambiente do App-V para a Internet na rede de perímetro.</span><span class="sxs-lookup"><span data-stu-id="e3868-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="e3868-116">Essas informações também incluem os servidores de rede internos recomendados.</span><span class="sxs-lookup"><span data-stu-id="e3868-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="e3868-117">Coloque os seguintes servidores na rede de perímetro:</span><span class="sxs-lookup"><span data-stu-id="e3868-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="e3868-118">Servidor de gerenciamento do App-V</span><span class="sxs-lookup"><span data-stu-id="e3868-118">App-V Management Server</span></span>

-   <span data-ttu-id="e3868-119">Servidor IIS para publicação e streaming</span><span class="sxs-lookup"><span data-stu-id="e3868-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="e3868-120">**Observação**  É uma prática recomendada colocar o servidor de gerenciamento e o servidor IIS em computadores separados.</span><span class="sxs-lookup"><span data-stu-id="e3868-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="e3868-121">Coloque os seguintes servidores na rede interna:</span><span class="sxs-lookup"><span data-stu-id="e3868-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="e3868-122">Servidor de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e3868-122">Content server</span></span>

-   <span data-ttu-id="e3868-123">Repositório de dados (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="e3868-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="e3868-124">Controlador de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="e3868-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="e3868-125">Requisitos de tráfego</span><span class="sxs-lookup"><span data-stu-id="e3868-125">Traffic Requirements</span></span>


<span data-ttu-id="e3868-126">As tabelas a seguir listam os requisitos de tráfego para comunicação da Internet e da rede de perímetro e da rede de perímetro para a rede interna.</span><span class="sxs-lookup"><span data-stu-id="e3868-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3868-127">Requisitos de tráfego da Internet para a rede de perímetro</span><span class="sxs-lookup"><span data-stu-id="e3868-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="e3868-128">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e3868-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3868-129">RTSPs (atualização de publicação e pacotes de streaming)</span><span class="sxs-lookup"><span data-stu-id="e3868-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-130">TCP 322 por padrão; Isso pode ser alterado no servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="e3868-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3868-131">HTTPS (arquivos. ICO e OSD de publicação e pacotes de streaming)</span><span class="sxs-lookup"><span data-stu-id="e3868-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-132">TCP 443 por padrão; Isso pode ser alterado na configuração do IIS.</span><span class="sxs-lookup"><span data-stu-id="e3868-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3868-133">Requisitos de tráfego da rede de perímetro para a rede interna</span><span class="sxs-lookup"><span data-stu-id="e3868-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="e3868-134">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e3868-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3868-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="e3868-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-136">O TCP 1433 é o padrão, mas pode ser configurado no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e3868-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3868-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="e3868-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-138">Se o diretório de conteúdo estiver localizado remotamente a partir do (s) servidor (es) de gerenciamento ou do IIS (recomendado).</span><span class="sxs-lookup"><span data-stu-id="e3868-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3868-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="e3868-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-140">TCP e UDP 88</span><span class="sxs-lookup"><span data-stu-id="e3868-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3868-141">LDAP</span><span class="sxs-lookup"><span data-stu-id="e3868-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-142">TCP e UDP 389</span><span class="sxs-lookup"><span data-stu-id="e3868-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3868-143">DNS</span><span class="sxs-lookup"><span data-stu-id="e3868-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3868-144">Para a resolução de nomes de recursos internos (pode ser eliminada com o uso do arquivo do host em servidores de rede de perímetro)</span><span class="sxs-lookup"><span data-stu-id="e3868-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





