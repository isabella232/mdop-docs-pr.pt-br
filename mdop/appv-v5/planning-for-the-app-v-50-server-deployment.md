---
title: Planejamento da implantação do servidor App-V 5.0
description: Planejamento da implantação do servidor App-V 5.0
author: dansimp
ms.assetid: fd89b324-3961-471a-ad90-c8f9ae7a8155
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06c7c17fd081b89337bbecd31f20f6796338f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796254"
---
# <span data-ttu-id="81ea0-103">Planejamento da implantação do servidor App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="81ea0-103">Planning for the App-V 5.0 Server Deployment</span></span>


<span data-ttu-id="81ea0-104">A infraestrutura de servidor do Microsoft Application Virtualization (App-V) 5,0 consiste em um conjunto de recursos especializados que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa.</span><span class="sxs-lookup"><span data-stu-id="81ea0-104">The Microsoft Application Virtualization (App-V) 5.0 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="81ea0-105">Planejando a implantação do App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="81ea0-105">Planning for App-V 5.0 Server Deployment</span></span>


<span data-ttu-id="81ea0-106">O servidor do App-V 5,0 consiste nos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="81ea0-106">The App-V 5.0 server consists of the following features:</span></span>

-   <span data-ttu-id="81ea0-107">Servidor de gerenciamento – oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81ea0-107">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="81ea0-108">Banco de dados de gerenciamento – facilita as implantações de banco de dados do gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81ea0-108">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="81ea0-109">Publishing Server – fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="81ea0-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="81ea0-110">Servidor de relatórios – fornece o App-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="81ea0-110">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="81ea0-111">Banco de dados de relatórios – facilita a implantação de bancos de dados para relatórios do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81ea0-111">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

<span data-ttu-id="81ea0-112">A lista a seguir exibe os métodos recomendados para a instalação da infraestrutura de servidor do App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="81ea0-112">The following list displays the recommended methods for installing the App-V 5.0 server infrastructure:</span></span>

-   <span data-ttu-id="81ea0-113">Instale o servidor do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81ea0-113">Install the App-V 5.0 server.</span></span> <span data-ttu-id="81ea0-114">Para obter mais informações, consulte [como implantar o servidor do App-V 5,0](how-to-deploy-the-app-v-50-server-50sp3.md).</span><span class="sxs-lookup"><span data-stu-id="81ea0-114">For more information, see [How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md).</span></span>

-   <span data-ttu-id="81ea0-115">Instale os recursos de banco de dados, relatórios e gerenciamento em computadores separados.</span><span class="sxs-lookup"><span data-stu-id="81ea0-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="81ea0-116">Para obter mais informações, consulte [como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).</span><span class="sxs-lookup"><span data-stu-id="81ea0-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).</span></span>

-   <span data-ttu-id="81ea0-117">Use a ESD (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="81ea0-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="81ea0-118">Para obter mais informações, consulte [como implantar pacotes do App-V 5,0 usando a distribuição de software eletrônico](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="81ea0-118">For more information, see [How to deploy App-V 5.0 Packages Using Electronic Software Distribution](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="81ea0-119">Instale todos os recursos do servidor em um único computador.</span><span class="sxs-lookup"><span data-stu-id="81ea0-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-0-server-interaction"></a> <span data-ttu-id="81ea0-120">Interação do servidor do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="81ea0-120">App-V 5.0 Server Interaction</span></span>


<span data-ttu-id="81ea0-121">Esta seção contém informações sobre como as várias funções de servidor do App-V 5,0 interagem umas com as outras.</span><span class="sxs-lookup"><span data-stu-id="81ea0-121">This section contains information about how the various App-V 5.0 server roles interact with each other.</span></span>

<span data-ttu-id="81ea0-122">O servidor de gerenciamento do App-V 5,0 contém o repositório de pacotes e suas configurações atribuídas.</span><span class="sxs-lookup"><span data-stu-id="81ea0-122">The App-V 5.0 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="81ea0-123">Para servidores de publicação registrados com o servidor de gerenciamento, os metadados associados são fornecidos aos servidores de publicação para serem usados quando as solicitações de atualização de publicação são recebidas de computadores que executam o cliente do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81ea0-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.0 Client.</span></span> <span data-ttu-id="81ea0-124">Os servidores de publicação do App-V 5,0 gerenciados por um único servidor de gerenciamento podem servir para clientes diferentes e podem ter nomes de site e associações de porta diferentes.</span><span class="sxs-lookup"><span data-stu-id="81ea0-124">App-V 5.0 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="81ea0-125">Além disso, todos os servidores de publicação gerenciados pelo mesmo servidor de gerenciamento são réplicas uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="81ea0-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="81ea0-126">**Observação**  O servidor de gerenciamento não executa balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="81ea0-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="81ea0-127">Os metadados associados são simplesmente passados para o Publishing Server para uso durante o processamento de solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="81ea0-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="81ea0-128">Protocolos relacionados a servidor e recursos externos</span><span class="sxs-lookup"><span data-stu-id="81ea0-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="81ea0-129">As informações a seguir exibem informações sobre protocolos relacionados a servidor usados pelos servidores App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81ea0-129">The following displays information about server-related protocols used by the App-V 5.0 servers.</span></span> <span data-ttu-id="81ea0-130">A tabela também inclui o mecanismo de relatório para cada tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="81ea0-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="81ea0-131">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="81ea0-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="81ea0-132">Protocolos</span><span class="sxs-lookup"><span data-stu-id="81ea0-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="81ea0-133">Recursos externos necessários</span><span class="sxs-lookup"><span data-stu-id="81ea0-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="81ea0-134">Relatórios</span><span class="sxs-lookup"><span data-stu-id="81ea0-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81ea0-135">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="81ea0-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="81ea0-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="81ea0-136">HTTP</span></span></p>
<p><span data-ttu-id="81ea0-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="81ea0-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="81ea0-138">Essa combinação de protocolo de servidor requer um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="81ea0-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="81ea0-139">Ao usar HTTP ou HTTPS, use um servidor IIS e um firewall para proteger o servidor de exposição à Internet.</span><span class="sxs-lookup"><span data-stu-id="81ea0-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="81ea0-140">Interna</span><span class="sxs-lookup"><span data-stu-id="81ea0-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81ea0-141">Arquivo</span><span class="sxs-lookup"><span data-stu-id="81ea0-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="81ea0-142">SMB</span><span class="sxs-lookup"><span data-stu-id="81ea0-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="81ea0-143">Essa combinação de protocolo de servidor requer suporte para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="81ea0-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="81ea0-144">Use um computador cliente com o compartilhamento de arquivos ou o recurso de streaming.</span><span class="sxs-lookup"><span data-stu-id="81ea0-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="81ea0-145">Interna</span><span class="sxs-lookup"><span data-stu-id="81ea0-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="81ea0-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81ea0-146">Related topics</span></span>


[<span data-ttu-id="81ea0-147">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="81ea0-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="81ea0-148">Implantação do servidor App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="81ea0-148">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





