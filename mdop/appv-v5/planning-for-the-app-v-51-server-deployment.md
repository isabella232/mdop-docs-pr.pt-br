---
title: Planejamento da implantação do servidor App-V 5.1
description: Planejamento da implantação do servidor App-V 5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796249"
---
# <span data-ttu-id="fe561-103">Planejamento da implantação do servidor App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fe561-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="fe561-104">A infraestrutura de servidor do Microsoft Application Virtualization (App-V) 5,1 consiste em um conjunto de recursos especializados que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa.</span><span class="sxs-lookup"><span data-stu-id="fe561-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="fe561-105">Planejando a implantação do App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="fe561-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="fe561-106">O servidor do App-V 5,1 consiste nos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="fe561-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="fe561-107">Servidor de gerenciamento – oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fe561-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="fe561-108">Banco de dados de gerenciamento – facilita as implantações de banco de dados do gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fe561-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="fe561-109">Publishing Server – fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="fe561-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="fe561-110">Servidor de relatórios – fornece o App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="fe561-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="fe561-111">Banco de dados de relatórios – facilita a implantação de bancos de dados para relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fe561-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="fe561-112">A lista a seguir exibe os métodos recomendados para a instalação da infraestrutura de servidor do App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="fe561-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="fe561-113">Instale o servidor do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fe561-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="fe561-114">Para obter mais informações, consulte [como implantar o servidor do App-V 5,1](how-to-deploy-the-app-v-51-server.md).</span><span class="sxs-lookup"><span data-stu-id="fe561-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="fe561-115">Instale os recursos de banco de dados, relatórios e gerenciamento em computadores separados.</span><span class="sxs-lookup"><span data-stu-id="fe561-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="fe561-116">Para obter mais informações, consulte [como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span><span class="sxs-lookup"><span data-stu-id="fe561-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="fe561-117">Use a ESD (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="fe561-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="fe561-118">Para obter mais informações, consulte [como implantar pacotes do App-V 5,1 usando a distribuição de software eletrônico](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="fe561-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="fe561-119">Instale todos os recursos do servidor em um único computador.</span><span class="sxs-lookup"><span data-stu-id="fe561-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="fe561-120">Interação do servidor do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fe561-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="fe561-121">Esta seção contém informações sobre como as várias funções de servidor do App-V 5,1 interagem umas com as outras.</span><span class="sxs-lookup"><span data-stu-id="fe561-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="fe561-122">O servidor de gerenciamento do App-V 5,1 contém o repositório de pacotes e suas configurações atribuídas.</span><span class="sxs-lookup"><span data-stu-id="fe561-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="fe561-123">Para servidores de publicação registrados com o servidor de gerenciamento, os metadados associados são fornecidos aos servidores de publicação para serem usados quando as solicitações de atualização de publicação são recebidas de computadores que executam o cliente do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fe561-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="fe561-124">Os servidores de publicação do App-V 5,1 gerenciados por um único servidor de gerenciamento podem servir para clientes diferentes e podem ter nomes de site e associações de porta diferentes.</span><span class="sxs-lookup"><span data-stu-id="fe561-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="fe561-125">Além disso, todos os servidores de publicação gerenciados pelo mesmo servidor de gerenciamento são réplicas uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="fe561-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="fe561-126">**Observação**  O servidor de gerenciamento não executa balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="fe561-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="fe561-127">Os metadados associados são simplesmente passados para o Publishing Server para uso durante o processamento de solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="fe561-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="fe561-128">Protocolos relacionados a servidor e recursos externos</span><span class="sxs-lookup"><span data-stu-id="fe561-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="fe561-129">As informações a seguir exibem informações sobre protocolos relacionados a servidor usados pelos servidores App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fe561-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="fe561-130">A tabela também inclui o mecanismo de relatório para cada tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="fe561-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="fe561-131">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="fe561-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="fe561-132">Protocolos</span><span class="sxs-lookup"><span data-stu-id="fe561-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="fe561-133">Recursos externos necessários</span><span class="sxs-lookup"><span data-stu-id="fe561-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="fe561-134">Relatórios</span><span class="sxs-lookup"><span data-stu-id="fe561-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe561-135">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="fe561-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe561-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="fe561-136">HTTP</span></span></p>
<p><span data-ttu-id="fe561-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="fe561-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe561-138">Essa combinação de protocolo de servidor requer um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe561-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="fe561-139">Ao usar HTTP ou HTTPS, use um servidor IIS e um firewall para proteger o servidor de exposição à Internet.</span><span class="sxs-lookup"><span data-stu-id="fe561-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe561-140">Interna</span><span class="sxs-lookup"><span data-stu-id="fe561-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe561-141">Arquivo</span><span class="sxs-lookup"><span data-stu-id="fe561-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe561-142">SMB</span><span class="sxs-lookup"><span data-stu-id="fe561-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe561-143">Essa combinação de protocolo de servidor requer suporte para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe561-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="fe561-144">Use um computador cliente com o compartilhamento de arquivos ou o recurso de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe561-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe561-145">Interna</span><span class="sxs-lookup"><span data-stu-id="fe561-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="fe561-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe561-146">Related topics</span></span>


[<span data-ttu-id="fe561-147">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="fe561-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="fe561-148">Implantação do servidor App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fe561-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





