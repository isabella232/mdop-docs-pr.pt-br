---
title: Arquitetura de alto nível para o App-V 5.0
description: Arquitetura de alto nível para o App-V 5.0
author: dansimp
ms.assetid: fdf8b841-918f-4672-b352-0f2b9519581b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0ec105ffcc3213e488615603484b2de6bafce4d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796529"
---
# <span data-ttu-id="84c2d-103">Arquitetura de alto nível para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="84c2d-103">High Level Architecture for App-V 5.0</span></span>


<span data-ttu-id="84c2d-104">Use as informações a seguir para ajudar a simplificar a implantação do Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="84c2d-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

## <span data-ttu-id="84c2d-105">Visão geral da arquitetura</span><span class="sxs-lookup"><span data-stu-id="84c2d-105">Architecture Overview</span></span>


<span data-ttu-id="84c2d-106">Uma implementação típica do App-V 5,0 consiste nos elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="84c2d-106">A typical App-V 5.0 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84c2d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="84c2d-107">Element</span></span></th>
<th align="left"><span data-ttu-id="84c2d-108">Mais informações</span><span class="sxs-lookup"><span data-stu-id="84c2d-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84c2d-109">Servidor de gerenciamento do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="84c2d-109">App-V 5.0 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="84c2d-110">O servidor de gerenciamento do App-V 5,0 oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="84c2d-110">The App-V 5.0 Management server provides overall management functionality for the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="84c2d-111">Além disso, você pode instalar mais de uma instância do servidor de gerenciamento em seu ambiente, que oferece os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="84c2d-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="84c2d-112">Tolerância a falhas e alta disponibilidade – instalar e configurar o servidor de gerenciamento do App-V 5,0 em dois computadores separados pode ajudar em situações em que um dos servidores está indisponível ou offline.</span><span class="sxs-lookup"><span data-stu-id="84c2d-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.0 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="84c2d-113">Você também pode ajudar a aumentar a disponibilidade do App-V 5,0 Instalando o servidor de gerenciamento em vários computadores.</span><span class="sxs-lookup"><span data-stu-id="84c2d-113">You can also help increase App-V 5.0 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="84c2d-114">Nesse cenário, um balanceador de carga de rede também deve ser considerado para que as solicitações do servidor sejam balanceadas.</span><span class="sxs-lookup"><span data-stu-id="84c2d-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="84c2d-115">Escalabilidade – você pode adicionar mais servidores de gerenciamento conforme necessário para dar suporte a uma alta carga, por exemplo, você pode instalar vários servidores atrás de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="84c2d-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84c2d-116">Servidor de publicação do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="84c2d-116">App-V 5.0 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="84c2d-117">O servidor de publicação do App-V 5,0 fornece funcionalidade para hospedagem e streaming de aplicativos virtual.</span><span class="sxs-lookup"><span data-stu-id="84c2d-117">The App-V 5.0 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="84c2d-118">O servidor de publicação não requer uma conexão de banco de dados e é compatível com os seguintes protocolos:</span><span class="sxs-lookup"><span data-stu-id="84c2d-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="84c2d-119">HTTP e HTTPS</span><span class="sxs-lookup"><span data-stu-id="84c2d-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="84c2d-120">Você também pode ajudar a aumentar a disponibilidade do App-V 5,0 Instalando o servidor de publicação em vários computadores.</span><span class="sxs-lookup"><span data-stu-id="84c2d-120">You can also help increase App-V 5.0 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="84c2d-121">Um balanceador de carga de rede também deve ser considerado para que as solicitações do servidor sejam balanceadas.</span><span class="sxs-lookup"><span data-stu-id="84c2d-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84c2d-122">Servidor de relatórios do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="84c2d-122">App-V 5.0 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="84c2d-123">O servidor de relatórios do App-V 5,0 permite que os usuários autorizados executem e visualizem relatórios ad hoc e relatórios ad hoc existentes do 5,0 app-v e possam ajudá-los a gerenciar a infraestrutura do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="84c2d-123">The App-V 5.0 Reporting server enables authorized users to run and view existing App-V 5.0 reports and ad hoc reports that can help them manage the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="84c2d-124">O servidor de relatório requer uma conexão com o banco de dados de relatórios do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="84c2d-124">The Reporting server requires a connection to the App-V 5.0 reporting database.</span></span> <span data-ttu-id="84c2d-125">Você também pode ajudar a aumentar a disponibilidade do App-V 5,0 Instalando o servidor de relatórios em vários computadores.</span><span class="sxs-lookup"><span data-stu-id="84c2d-125">You can also help increase App-V 5.0 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="84c2d-126">Um balanceador de carga de rede também deve ser considerado para que as solicitações do servidor sejam balanceadas.</span><span class="sxs-lookup"><span data-stu-id="84c2d-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84c2d-127">Cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="84c2d-127">App-V 5.0 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="84c2d-128">O cliente App-V 5,0 permite que pacotes criados usando o App-V 5,0 sejam executados em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="84c2d-128">The App-V 5.0 client enables packages created using App-V 5.0 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="84c2d-129">**Observação**  Se você estiver usando o App-V 5,0 com ESD (Electronic Software Distribution), não será necessário usar o servidor de gerenciamento do App-V 5,0, mas ainda poderá usar a funcionalidade de relatório e de streaming do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="84c2d-129">**Note** If you are using App-V 5.0 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.0 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.0.</span></span>

 






## <span data-ttu-id="84c2d-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84c2d-130">Related topics</span></span>


[<span data-ttu-id="84c2d-131">Introdução ao App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="84c2d-131">Getting Started with App-V 5.0</span></span>](getting-started-with-app-v-50--rtm.md)

 

 





