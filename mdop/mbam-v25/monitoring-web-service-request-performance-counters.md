---
title: Monitorando os contadores de desempenho das solicitações de serviço Web
description: Monitorando os contadores de desempenho das solicitações de serviço Web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799360"
---
# <span data-ttu-id="27979-103">Monitorando os contadores de desempenho das solicitações de serviço Web</span><span class="sxs-lookup"><span data-stu-id="27979-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="27979-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) fornecem contadores de desempenho que registram o desempenho de solicitações que são enviadas para os seguintes serviços Web:</span><span class="sxs-lookup"><span data-stu-id="27979-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="27979-105">**StatusReportingService. svc** – serviço que recebe solicitações de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="27979-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="27979-106">**CoreService. svc** – serviço que recebe solicitações para tentativas de recuperação de chave</span><span class="sxs-lookup"><span data-stu-id="27979-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="27979-107">Contadores de desempenho que o MBAM fornece</span><span class="sxs-lookup"><span data-stu-id="27979-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="27979-108">O MBAM fornece os seguintes contadores de desempenho para cada um dos métodos públicos implementados por seus serviços Web do StatusReportingService e do CoreService:</span><span class="sxs-lookup"><span data-stu-id="27979-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27979-109">Tipo de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="27979-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="27979-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="27979-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27979-111">Número total de solicitações</span><span class="sxs-lookup"><span data-stu-id="27979-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="27979-112">Fornece uma contagem de incremento que começa do zero quando o servidor é iniciado ou reiniciado.</span><span class="sxs-lookup"><span data-stu-id="27979-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="27979-113">Fornece uma visão geral da atividade do sistema.</span><span class="sxs-lookup"><span data-stu-id="27979-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="27979-114">Pode ser monitorado por ferramentas automatizadas para garantir a integridade do servidor e validar que o contador é incrementado continuamente durante um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="27979-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27979-115">Solicitações por segundo</span><span class="sxs-lookup"><span data-stu-id="27979-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="27979-116">Indica a taxa de transferência atual do servidor MBAM, pois ele dá suporte à base de clientes do MBAM.</span><span class="sxs-lookup"><span data-stu-id="27979-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="27979-117">Permite que os administradores de sites:</span><span class="sxs-lookup"><span data-stu-id="27979-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="27979-118">Calcular o número médio de solicitações por segundo, com base no número de clientes do MBAM e na sua frequência de relatórios.</span><span class="sxs-lookup"><span data-stu-id="27979-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="27979-119">Valide se o número de solicitações por segundo correlaciona-se amplamente com o número médio de solicitações calculadas por segundo.</span><span class="sxs-lookup"><span data-stu-id="27979-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="27979-120">Uma variação significativa pode indicar que o cliente MBAM não está instalado em uma porcentagem da base do cliente ou que um objeto de política de grupo do MBAM não foi implantado com êxito.</span><span class="sxs-lookup"><span data-stu-id="27979-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27979-121">Duração da solicitação</span><span class="sxs-lookup"><span data-stu-id="27979-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="27979-122">Registra a duração de solicitações em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="27979-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="27979-123">Embora esse contador seja atualizado com a duração de cada solicitação, o monitor de desempenho do Windows o amostra apenas periodicamente (geralmente a cada segundo), para que você possa ver uma variabilidade no valor.</span><span class="sxs-lookup"><span data-stu-id="27979-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="27979-124">Por esse motivo, considere usar o valor médio exibido pelo monitor de desempenho.</span><span class="sxs-lookup"><span data-stu-id="27979-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="27979-125">Resultados e recomendações do contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="27979-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="27979-126">À medida que você adicionar novos clientes do MBAM a um servidor MBAM com capacidade de sobra, espera ver um aumento no número de solicitações por segundo.</span><span class="sxs-lookup"><span data-stu-id="27979-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="27979-127">Esse aumento será proporcional ao número de novos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="27979-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="27979-128">A duração média da solicitação permanecerá relativamente estática.</span><span class="sxs-lookup"><span data-stu-id="27979-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="27979-129">Como o servidor se aproxima da capacidade máxima, as solicitações por segundo começam a se redistribuirem e a média da duração da solicitação começa a ser mais longa.</span><span class="sxs-lookup"><span data-stu-id="27979-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="27979-130">Se você se preocupa se seus servidores do MBAM podem dar suporte à base de clientes, considere a implantação de MBAM em fases em diferentes conjuntos de computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="27979-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="27979-131">Ao implantar o MBAM em cada conjunto de computadores cliente, recomendamos que você faça instantâneos dos contadores de desempenho para ver o impacto relativo da implantação em cada novo conjunto de clientes.</span><span class="sxs-lookup"><span data-stu-id="27979-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="27979-132">Se o número de solicitações por segundo começar a redistribuir e a média da duração da solicitação aumentar, considere aprimorar sua infraestrutura de servidor do MBAM seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="27979-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="27979-133">Mover o banco de dados do MBAM para um cluster exclusivo do Microsoft SQL Server ou SQL Server</span><span class="sxs-lookup"><span data-stu-id="27979-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="27979-134">Balanceamento de carga MBAM em vários servidores Web dos serviços de informações da Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="27979-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="27979-135">Implantando o MBAM em um hardware de servidor mais potente</span><span class="sxs-lookup"><span data-stu-id="27979-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="27979-136">Exibindo contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="27979-136">Viewing performance counters</span></span>


<span data-ttu-id="27979-137">A ferramenta recomendada para exibir os contadores de desempenho do MBAM é o monitor de desempenho do Windows, que vem com o Windows.</span><span class="sxs-lookup"><span data-stu-id="27979-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="27979-138">Se você estiver usando o Windows PowerShell, não será necessário habilitar os contadores antes de exibi-los, pois eles são automaticamente registrados pelo cmdlet **Enable-WebApplication** do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27979-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="27979-139">Para obter instruções detalhadas sobre como exibir contadores de desempenho, consulte [como exibir contadores de desempenho do MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).</span><span class="sxs-lookup"><span data-stu-id="27979-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="27979-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27979-140">Related topics</span></span>


[<span data-ttu-id="27979-141">Manutenção do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27979-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="27979-142">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="27979-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="27979-143">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="27979-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="27979-144">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="27979-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>


