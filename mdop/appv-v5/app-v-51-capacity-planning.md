---
title: Planejamento de capacidade do App-V 5.1
description: Planejamento de capacidade do App-V 5.1
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796586"
---
# <span data-ttu-id="fa3b8-103">Planejamento de capacidade do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-103">App-V 5.1 Capacity Planning</span></span>


<span data-ttu-id="fa3b8-104">As seguintes recomendações podem ser usadas como uma linha de base para ajudar a determinar as informações de planejamento de capacidade apropriadas à infraestrutura do App-V do App-5,1 V da sua organização.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.1 infrastructure.</span></span>

<span data-ttu-id="fa3b8-105">**Importante**  Use as informações nesta seção apenas como um guia geral para planejar a implantação do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.1 deployment.</span></span> <span data-ttu-id="fa3b8-106">Os requisitos de capacidade do sistema dependerão dos detalhes específicos do seu ambiente de hardware e de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="fa3b8-107">Além disso, os números de desempenho exibidos neste documento são exemplos e os resultados podem variar.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="fa3b8-108">Determinar o escopo do projeto</span><span class="sxs-lookup"><span data-stu-id="fa3b8-108">Determine the Project Scope</span></span>


<span data-ttu-id="fa3b8-109">Antes de criar a infraestrutura do App-V 5,1, você deve determinar o escopo do projeto.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-109">Before you design the App-V 5.1 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="fa3b8-110">O escopo consiste em determinar quais aplicativos estarão disponíveis virtualmente e também para identificar os usuários de destino e seus locais.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="fa3b8-111">Essas informações ajudarão a determinar qual tipo de infraestrutura do App-V 5,1 deve ser implementado.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-111">This information will help determine what type of App-V 5.1 infrastructure should be implemented.</span></span> <span data-ttu-id="fa3b8-112">Decisões sobre o escopo do projeto devem ser baseadas nas necessidades específicas da sua organização.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-113">Tarefa</span><span class="sxs-lookup"><span data-stu-id="fa3b8-113">Task</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-114">Mais informações</span><span class="sxs-lookup"><span data-stu-id="fa3b8-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-115">Determinar o escopo do aplicativo</span><span class="sxs-lookup"><span data-stu-id="fa3b8-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-116">Dependendo dos aplicativos a serem virtualizados, a infraestrutura do App-V 5,1 pode ser configurada de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-116">Depending on the applications to be virtualized, the App-V 5.1 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="fa3b8-117">A primeira tarefa é definir quais aplicativos você deseja virtualizar.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-118">Determinar o escopo do local</span><span class="sxs-lookup"><span data-stu-id="fa3b8-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-119">Escopo de localização refere-se aos locais físicos (por exemplo, em toda a empresa ou em uma localização geográfica específica) em que você planeja executar os aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="fa3b8-120">Ele também pode se referir à população do usuário (por exemplo, um único departamento) que irá executar os aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="fa3b8-121">Você deve obter um mapa de rede que inclua os caminhos de conexão, bem como a largura de banda disponível para cada local e o número de usuários que usam aplicativos virtualizados e a velocidade do link de WAN.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fa3b8-122">Determine qual é a necessidade de infraestrutura do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-122">Determine Which App-V 5.1 Infrastructure is Required</span></span>


<span data-ttu-id="fa3b8-123">**Importante**  Os dois modelos a seguir exigem que o cliente do App-V 5,1 seja instalado no computador em que você planeja executar aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-123">**Important** Both of the following models require the App-V 5.1 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="fa3b8-124">Você também pode gerenciar seu ambiente do App-V 5,1 usando uma solução ESD (distribuição de software eletrônico), como o Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-124">You can also manage your App-V 5.1 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="fa3b8-125">Para obter mais informações, consulte [como implantar pacotes do App-V 5,1 usando a distribuição de software eletrônico](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-125">For more information see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

 

-   <span data-ttu-id="fa3b8-126">**Modelo autônomo** – o modelo autônomo permite que aplicativos virtuais sejam habilitados para Windows Installer para distribuição sem streaming.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="fa3b8-127">O App-V 5,1 no modo autônomo consiste do sequenciador e do cliente; nenhum componente adicional é necessário.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-127">App-V 5.1 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="fa3b8-128">Os aplicativos são preparados para virtualização usando um processo chamado sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="fa3b8-129">Para obter mais informações, consulte [planejando o sequenciador do App-V 5,1 e a implantação do cliente](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-129">For more information see, [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="fa3b8-130">O modelo autônomo é recomendado para os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="fa3b8-131">Com usuários remotos desconectados que não podem se conectar à infraestrutura do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-131">With disconnected remote users who cannot connect to the App-V 5.1 infrastructure.</span></span>

    -   <span data-ttu-id="fa3b8-132">Quando você estiver executando um sistema de gerenciamento de software, como o Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="fa3b8-133">Quando as limitações de largura de banda da rede inibem a distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="fa3b8-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="fa3b8-134">**Modelo de infra-estrutura completa** : o modelo de infra-estrutura completo oferece recursos de distribuição, gerenciamento e relatórios de software; Ele também inclui o fluxo de aplicativos na rede.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="fa3b8-135">O modelo de infraestrutura completa do App-V 5,1 consiste em um ou mais servidores de gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-135">The App-V 5.1 Full Infrastructure Model consists of one or more App-V 5.1 management servers.</span></span> <span data-ttu-id="fa3b8-136">O servidor de gerenciamento pode ser usado para publicar aplicativos para todos os clientes.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="fa3b8-137">O processo de publicação coloca os ícones do aplicativo virtual e os atalhos no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="fa3b8-138">Ele também pode transmitir aplicativos para usuários locais.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-138">It can also stream applications to local users.</span></span> <span data-ttu-id="fa3b8-139">Para obter mais informações sobre como instalar o servidor de gerenciamento, consulte [planejando a implantação do App-V server 5,1](planning-for-the-app-v-51-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-139">For more information about installing the management server see, [Planning for the App-V 5.1 Server Deployment](planning-for-the-app-v-51-server-deployment.md).</span></span> <span data-ttu-id="fa3b8-140">O modelo de infra-estrutura completo é recomendado para os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="fa3b8-141">**Importante**  O modelo de infraestrutura completa do App-V 5,1 exige que o Microsoft SQL Server armazene dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-141">**Important** The App-V 5.1 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="fa3b8-142">Para obter mais informações, consulte [configurações compatíveis com o App-V 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-142">For more information see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="fa3b8-143">Quando você quiser usar o servidor de gerenciamento para publicar o aplicativo em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="fa3b8-144">Para o provisionamento rápido de aplicativos para computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="fa3b8-145">Quando quiser usar os relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-145">When you want to use App-V 5.1 reporting.</span></span>

## <span data-ttu-id="fa3b8-146">Orientação de dimensionamento de servidor ponta a ponta</span><span class="sxs-lookup"><span data-stu-id="fa3b8-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="fa3b8-147">A seção a seguir fornece informações sobre o planejamento e o planejamento de um App-V 5,1 de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-147">The following section provides information about end-to-end App-V 5.1 sizing and planning.</span></span> <span data-ttu-id="fa3b8-148">Para obter informações mais específicas, consulte as seções subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="fa3b8-149">**Observação**  Tempo de resposta de ida e volta no cliente é o tempo levado pelo computador executando o cliente App-V 5,1 para receber uma notificação bem-sucedida do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.1 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="fa3b8-150">O tempo de resposta de ida e volta no servidor de publicação é o tempo usado pelo computador que executa o servidor de publicação para receber uma atualização de metadados de pacote bem-sucedida do servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="fa3b8-151">Os clientes do 20.000 podem direcionar um único servidor de publicação para obter as atualizações do pacote em um tempo de ida e volta aceitável.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="fa3b8-152">( &lt; 3 segundos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="fa3b8-153">Um único servidor de gerenciamento pode oferecer suporte a até 50 servidores de publicação para atualizações de metadados de pacote em um tempo de ida e volta aceitável.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="fa3b8-154">( &lt; 5 segundos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="fa3b8-155">Recomendações de planejamento de capacidade do servidor de gerenciamento do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-155">App-V 5.1 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="fa3b8-156">Os servidores de publicação do App-V 5,1 exigem o servidor de gerenciamento para solicitações de atualização de pacote e respostas de atualização do pacote.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-156">The App-V 5.1 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="fa3b8-157">Em seguida, o servidor de gerenciamento envia as informações para o banco de dados de gerenciamento para recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="fa3b8-158">Para obter mais informações sobre as configurações compatíveis do App-V 5,1 Management Server [, consulte Configurações compatíveis do App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-158">For more information about App-V 5.1 management server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="fa3b8-159">**Observação**  O tempo de atualização padrão no servidor de publicação do App-V 5,1 é de dez minutos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-159">**Note** The default refresh time on the App-V 5.1 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="fa3b8-160">Quando vários servidores de publicação simultaneamente entrarem em contato com um único servidor de gerenciamento para atualizações de metadados do pacote, os três fatores a seguir influenciarão o tempo de resposta de ida e volta no servidor de publicação:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="fa3b8-161">Número de servidores de publicação que fazem solicitações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="fa3b8-162">Número de grupos de conexão configurados no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="fa3b8-163">Número de grupos de acesso configurados no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="fa3b8-164">A tabela a seguir mostra mais informações sobre cada fator que impactam o tempo de viagem de ida e volta.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="fa3b8-165">**Observação**  Tempo de resposta de ida e volta é o tempo usado pelo computador executando o servidor de publicação do App-V 5,1 para receber uma atualização de metadados de pacote bem-sucedida do servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-166">Fatores que afetam o tempo de resposta de ida e volta</span><span class="sxs-lookup"><span data-stu-id="fa3b8-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-167">Mais informações</span><span class="sxs-lookup"><span data-stu-id="fa3b8-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-168">O número de servidores de publicação solicitando atualizações de metadados do pacote simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-169">Um único servidor de gerenciamento pode responder a até 320 servidores de publicação que solicitam metadados de publicação simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-170">O tempo de resposta de ida e volta para servidores pub do 320 é de aproximadamente 40 segundos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-171">Para &lt; servidores de publicação do 50 que solicitam metadados simultaneamente, o tempo de resposta de ida e volta é de &lt; 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-172">De 50 a 320 servidores de publicação, o tempo de resposta aumenta linearmente (aproximadamente 2x).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-173">O número de grupos de conexão configurados no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-174">Para até 100 grupos de conexão, não há alteração significativa no tempo de resposta de ida e volta no servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-175">Para os grupos de conexão do 100-400, há um aumento linear secundário no tempo de resposta de ida e volta.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-176">O número de grupos de acesso configurados no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-177">Para até 40 grupos de acesso, há um aumento linear (aproximadamente 3x) no tempo de resposta de ida e volta no servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-178">A tabela a seguir exibe exemplos de valores para cada um dos fatores anteriores.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="fa3b8-179">Em cada variação, os pacotes do 120 são atualizados a partir do servidor de gerenciamento do App-V 5.1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-179">In each variation, 120 packages are refreshed from the App-V 5.1management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-180">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-181">Variação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-182">Número de grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="fa3b8-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-183">Número de grupos de acesso</span><span class="sxs-lookup"><span data-stu-id="fa3b8-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-184">Número de servidores de publicação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-185">Servidor de publicação do tipo de conexão de rede/servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fa3b8-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-186">Tempo de resposta de ida e volta no servidor de publicação (em segundos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-187">Utilização da CPU no servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fa3b8-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-188">Servidores de publicação simultaneamente entrando em contato com o servidor de gerenciamento para publicar metadados.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-189">Número de servidores de publicação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-190">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-190">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-191">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-191">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-192">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-192">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-193">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-193">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-194">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-194">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-195">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-196">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-196">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-197">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-197">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-198">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-198">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-199">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-199">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-200">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-200">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-201">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-202">50</span><span class="sxs-lookup"><span data-stu-id="fa3b8-202">50</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-203">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-203">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-204">200</span><span class="sxs-lookup"><span data-stu-id="fa3b8-204">200</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-205">300</span><span class="sxs-lookup"><span data-stu-id="fa3b8-205">300</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-206">315</span><span class="sxs-lookup"><span data-stu-id="fa3b8-206">315</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-207">320</span><span class="sxs-lookup"><span data-stu-id="fa3b8-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-208">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-209">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-210">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-211">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-212">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-213">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-214">5</span><span class="sxs-lookup"><span data-stu-id="fa3b8-214">5</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-215">254</span><span class="sxs-lookup"><span data-stu-id="fa3b8-215">10</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-216">pol</span><span class="sxs-lookup"><span data-stu-id="fa3b8-216">19</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-217">32</span><span class="sxs-lookup"><span data-stu-id="fa3b8-217">32</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-218">30</span><span class="sxs-lookup"><span data-stu-id="fa3b8-218">30</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-219">37</span><span class="sxs-lookup"><span data-stu-id="fa3b8-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-220">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-220">17</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-221">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-221">17</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-222">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-222">17</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-223">15</span><span class="sxs-lookup"><span data-stu-id="fa3b8-223">15</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-224">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-224">17</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-225">15</span><span class="sxs-lookup"><span data-stu-id="fa3b8-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-226">Metadados de publicação contêm grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="fa3b8-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-227">Número de grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="fa3b8-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-228">254</span><span class="sxs-lookup"><span data-stu-id="fa3b8-228">10</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-229">50</span><span class="sxs-lookup"><span data-stu-id="fa3b8-229">50</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-230">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-230">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-231">150</span><span class="sxs-lookup"><span data-stu-id="fa3b8-231">150</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-232">300</span><span class="sxs-lookup"><span data-stu-id="fa3b8-232">300</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-233">400</span><span class="sxs-lookup"><span data-stu-id="fa3b8-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-234">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-234">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-235">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-235">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-236">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-236">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-237">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-237">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-238">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-238">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-239">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-240">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-240">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-241">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-241">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-242">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-242">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-243">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-243">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-244">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-244">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-245">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-246">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-247">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-248">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-249">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-250">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-251">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-252">254</span><span class="sxs-lookup"><span data-stu-id="fa3b8-252">10</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-253">11:00</span><span class="sxs-lookup"><span data-stu-id="fa3b8-253">11</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-254">11:00</span><span class="sxs-lookup"><span data-stu-id="fa3b8-254">11</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-255">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-255">16</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-256">22</span><span class="sxs-lookup"><span data-stu-id="fa3b8-256">22</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-257">25</span><span class="sxs-lookup"><span data-stu-id="fa3b8-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-258">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-258">17</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-259">pol</span><span class="sxs-lookup"><span data-stu-id="fa3b8-259">19</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-260">22</span><span class="sxs-lookup"><span data-stu-id="fa3b8-260">22</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-261">pol</span><span class="sxs-lookup"><span data-stu-id="fa3b8-261">19</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-262">cedido</span><span class="sxs-lookup"><span data-stu-id="fa3b8-262">20</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-263">cedido</span><span class="sxs-lookup"><span data-stu-id="fa3b8-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-264">Metadados de publicação contêm grupos de acesso</span><span class="sxs-lookup"><span data-stu-id="fa3b8-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-265">Número de grupos de acesso</span><span class="sxs-lookup"><span data-stu-id="fa3b8-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-266">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-266">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-267">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-267">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-268">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-268">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-269">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-270">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-270">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-271">254</span><span class="sxs-lookup"><span data-stu-id="fa3b8-271">10</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-272">cedido</span><span class="sxs-lookup"><span data-stu-id="fa3b8-272">20</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-273">40</span><span class="sxs-lookup"><span data-stu-id="fa3b8-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-274">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-274">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-275">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-275">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-276">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-276">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-277">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-278">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-279">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-280">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-281">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-282">254</span><span class="sxs-lookup"><span data-stu-id="fa3b8-282">10</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-283">43</span><span class="sxs-lookup"><span data-stu-id="fa3b8-283">43</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-284">153</span><span class="sxs-lookup"><span data-stu-id="fa3b8-284">153</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-285">535</span><span class="sxs-lookup"><span data-stu-id="fa3b8-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-286">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-286">17</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-287">26</span><span class="sxs-lookup"><span data-stu-id="fa3b8-287">26</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-288">24</span><span class="sxs-lookup"><span data-stu-id="fa3b8-288">24</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-289">24</span><span class="sxs-lookup"><span data-stu-id="fa3b8-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-290">A utilização de CPU do computador que está executando o servidor de gerenciamento está em cerca de 25%, independentemente do número de servidores de publicação direcionados a ele.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="fa3b8-291">As transações de banco de dados do Microsoft SQL Server/s, solicitações em lote/s e conexões de usuários são idênticas independentemente do número de servidores de publicação.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="fa3b8-292">Por exemplo: transações/s é ~ 30, solicitações em lote ~ 200 e o usuário se conecta aproximadamente 6.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="fa3b8-293">Usando uma implantação geograficamente distribuída, em que o servidor de gerenciamento & servidores de publicação utilizam uma rede de link lento entre eles, o tempo de resposta de ida e volta nos servidores de publicação está dentro dos limites de tempo aceitáveis ( &lt; 5 segundos), mesmo para solicitações simultâneas de 100 em um único servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-294">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-295">Variação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-296">Número de grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="fa3b8-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-297">Número de grupos de acesso</span><span class="sxs-lookup"><span data-stu-id="fa3b8-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-298">Número de servidores de publicação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-299">Servidor de publicação do tipo de conexão de rede/servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fa3b8-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-300">Tempo de resposta de ida e volta no servidor de publicação (em segundos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-301">Utilização da CPU no servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fa3b8-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-302">Conexão de rede entre o servidor de publicação e o servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fa3b8-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-303">Rede de link lento de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="fa3b8-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-304">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-304">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-305">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-306">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-306">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-307">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-308">50</span><span class="sxs-lookup"><span data-stu-id="fa3b8-308">50</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-309">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-310">Cabo DSL de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="fa3b8-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-311">Cabo DSL de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="fa3b8-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-312">4</span><span class="sxs-lookup"><span data-stu-id="fa3b8-312">4</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-313">5</span><span class="sxs-lookup"><span data-stu-id="fa3b8-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-314">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-314">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-315">2</span><span class="sxs-lookup"><span data-stu-id="fa3b8-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-316">Conexão de rede entre o servidor de publicação e o servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fa3b8-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-317">Rede LAN/WIFI</span><span class="sxs-lookup"><span data-stu-id="fa3b8-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-318">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-318">0</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-319">0</span><span class="sxs-lookup"><span data-stu-id="fa3b8-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-320">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-320">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-321">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-322">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-322">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-323">200</span><span class="sxs-lookup"><span data-stu-id="fa3b8-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-324">Wifi</span><span class="sxs-lookup"><span data-stu-id="fa3b8-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-325">Wifi</span><span class="sxs-lookup"><span data-stu-id="fa3b8-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-326">11:00</span><span class="sxs-lookup"><span data-stu-id="fa3b8-326">11</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-327">cedido</span><span class="sxs-lookup"><span data-stu-id="fa3b8-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-328">15</span><span class="sxs-lookup"><span data-stu-id="fa3b8-328">15</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-329">16</span><span class="sxs-lookup"><span data-stu-id="fa3b8-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-330">Se o servidor de gerenciamento e os servidores de publicação estiverem conectados em uma rede de link lento ou em uma rede de alta velocidade, o servidor de gerenciamento pode manipular aproximadamente 15.000 solicitações de atualização de pacote em 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="fa3b8-331">Recomendações de planejamento de capacidade do aplicativo do App-V 5,1 Reporting Server</span><span class="sxs-lookup"><span data-stu-id="fa3b8-331">App-V 5.1 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="fa3b8-332">Os clientes do App-V 5,1 enviam dados de relatório para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-332">App-V 5.1 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="fa3b8-333">Em seguida, o servidor de relatórios registra as informações no banco de dados do Microsoft SQL Server e retorna uma notificação bem-sucedida de volta para o computador que está executando o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.1 client.</span></span> <span data-ttu-id="fa3b8-334">Para obter mais informações sobre as configurações compatíveis do App-V 5,1 Reporting Server, consulte [configurações compatíveis do App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-334">For more information about App-V 5.1 Reporting Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="fa3b8-335">**Observação**  Tempo de resposta de ida e volta é o tempo usado pelo computador executando o cliente App-V 5,1 para enviar as informações de relatório para o servidor de relatórios e receber uma notificação bem-sucedida do servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-336">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-337">Resumo</span><span class="sxs-lookup"><span data-stu-id="fa3b8-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-338">Os clientes do 5,1 do App-V enviam informações de relatório para o servidor de relatórios simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-338">Multiple App-V 5.1 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-339">O tempo de resposta de ida e volta do servidor de relatório é de 2,6 segundos para os clientes do 500.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-340">O tempo de resposta de ida e volta do servidor de relatório é de 5,65 segundos para os clientes do 1000.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-341">O tempo de resposta de ida e volta aumenta linearmente dependendo do número de clientes.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-342">Solicitações por segundo processadas pelo servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-343">Um único servidor de relatórios e um único banco de dados, podem processar um máximo de solicitações 139 por segundo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="fa3b8-344">A média é de solicitações 121/segundo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-345">Ao usar dois relatórios de servidor de relatório para o mesmo banco de dados do Microsoft SQL Server, as médias de solicitações/segundo são semelhantes a um único servidor de relatórios = ~ 127, com um máximo de solicitações 278 de/segundo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-346">Um único servidor de relatórios pode processar conexões simultâneas/ativas do 500.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-347">Um único servidor de relatórios pode processar uma máxima conexão simultânea de 1500.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-348">Banco de dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-349">Bloquear a disputa no computador que executa o Microsoft SQL Server é o fator de limitação para solicitações/segundo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-350">A produtividade e o tempo de resposta são independentes do tamanho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-351">**Calculando o atraso aleatório**:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-351">**Calculating random delay**:</span></span>

<span data-ttu-id="fa3b8-352">O atraso aleatório especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="fa3b8-353">Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre **0** e **ReportingRandomDelay** e esperará a duração especificada antes de enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="fa3b8-354">Atraso aleatório = 4 \ \* número de clientes/solicitações médias por segundo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="fa3b8-355">Exemplo: para clientes do 500, com solicitações do 120 por segundo, o atraso aleatório é, 4 \ \* 500/120 = ~ 17 minutos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="fa3b8-356">Recomendações de planejamento de capacidade do servidor de publicação do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-356">App-V 5.1 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="fa3b8-357">Os computadores que executam o cliente App-V 5,1 se conectam ao servidor de publicação do App-V 5,1 para enviar uma solicitação de atualização de publicação e receber uma resposta.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-357">Computers running the App-V 5.1 client connect to the App-V 5.1 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="fa3b8-358">O tempo de resposta de ida e volta é medido no computador que executa o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-358">Round trip response time is measured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="fa3b8-359">O tempo do processador é medido no servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="fa3b8-360">Para obter mais informações sobre as configurações compatíveis do aplicativo de publicação do App-V 5,1, consulte [configurações compatíveis do App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-360">For more information about App-V 5.1 Publishing Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="fa3b8-361">**Importante**  A lista a seguir mostra os principais fatores a serem considerados ao configurar o servidor de publicação do App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.1 publishing server:</span></span>

-   <span data-ttu-id="fa3b8-362">O número de clientes que se conectam simultaneamente a um único servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="fa3b8-363">O número de pacotes em cada atualização.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="fa3b8-364">A largura de banda de rede disponível em seu ambiente entre o cliente e o servidor de publicação do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-364">The available network bandwidth in your environment between the client and the App-V 5.1 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-365">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-366">Resumo</span><span class="sxs-lookup"><span data-stu-id="fa3b8-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-367">Vários clientes do App-V 5,1 se conectam a um único servidor de publicação simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-367">Multiple App-V 5.1 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-368">Um servidor de publicação com processadores dual core pode responder a no máximo 5000 clientes que solicitam uma atualização simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-369">Para clientes do 5000-10000, o servidor de publicação requer um mínimo de quatro núcleos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-370">Para clientes do 10000-20000, o servidor de publicação deve ter núcleos de quatro processadores para tempos de resposta mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-371">Um servidor de publicação com quad core pode atualizar até 10000 pacotes em 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="fa3b8-372">(Compatível com 10000 clientes simultâneos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-373">Número de pacotes em cada atualização.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-374">O aumento do número de pacotes aumentará o tempo de resposta em cerca de 40% (até 1000 pacotes).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-375">Rede entre o cliente App-V 5,1 e o Publishing Server.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-375">Network between the App-V 5.1 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-376">Em uma rede lenta (largura de banda de 1,5 Mbps), há um aumento de 97% no tempo de resposta em comparação com a LAN (até 1000 usuários).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-377">**Observação**  O uso da CPU do servidor de publicação sempre é alto durante o intervalo de tempo em que é preciso processar solicitações simultâneas ( &gt; 90% na maioria dos casos).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="fa3b8-378">O servidor de publicação pode manipular solicitações de cliente ~ 1500 em 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-379">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-380">Variação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-381">Número de clientes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-381">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-382">Número de pacotes</span><span class="sxs-lookup"><span data-stu-id="fa3b8-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-383">Configuração do processador no servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-384">Servidor de publicação do tipo de conexão de rede/cliente do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-384">Network connection type publishing server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-385">Tempo de viagem de ida e volta no cliente do App-V 5,1 (em segundos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-385">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-386">Utilização da CPU no servidor de publicação (em%)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-387">App-V 5,1 o cliente envia uma solicitação &amp; de atualização de publicação recebe resposta, cada solicitação contendo pacotes 120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-387">App-V 5.1 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-388">Número de clientes</span><span class="sxs-lookup"><span data-stu-id="fa3b8-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-389">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-389">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-390">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-390">1000</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-391">5000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-391">5000</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-392">10000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-393">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-393">120</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-394">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-394">120</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-395">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-395">120</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-396">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-397">Dual Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-398">Dual Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-399">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-400">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-401">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-402">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-403">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-404">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-405">um</span><span class="sxs-lookup"><span data-stu-id="fa3b8-405">1</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-406">2</span><span class="sxs-lookup"><span data-stu-id="fa3b8-406">2</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-407">2</span><span class="sxs-lookup"><span data-stu-id="fa3b8-407">2</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-408">3D</span><span class="sxs-lookup"><span data-stu-id="fa3b8-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-409">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-409">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-410">99</span><span class="sxs-lookup"><span data-stu-id="fa3b8-410">99</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-411">89</span><span class="sxs-lookup"><span data-stu-id="fa3b8-411">89</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-412">77</span><span class="sxs-lookup"><span data-stu-id="fa3b8-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-413">Vários pacotes em cada atualização</span><span class="sxs-lookup"><span data-stu-id="fa3b8-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-414">Número de pacotes</span><span class="sxs-lookup"><span data-stu-id="fa3b8-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-415">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-415">1000</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-416">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-417">500</span><span class="sxs-lookup"><span data-stu-id="fa3b8-417">500</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-418">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-419">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-420">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-421">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-422">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-423">2</span><span class="sxs-lookup"><span data-stu-id="fa3b8-423">2</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-424">3D</span><span class="sxs-lookup"><span data-stu-id="fa3b8-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-425">92</span><span class="sxs-lookup"><span data-stu-id="fa3b8-425">92</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-426">91</span><span class="sxs-lookup"><span data-stu-id="fa3b8-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-427">Rede entre o cliente e o servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-428">rede de link lento de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="fa3b8-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-429">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-429">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-430">500</span><span class="sxs-lookup"><span data-stu-id="fa3b8-430">500</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-431">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-432">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-432">120</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-433">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-433">120</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-434">120</span><span class="sxs-lookup"><span data-stu-id="fa3b8-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-435">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-436">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-437">Quad Core</span><span class="sxs-lookup"><span data-stu-id="fa3b8-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-438">Rede intra-continental de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="fa3b8-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-439">3D</span><span class="sxs-lookup"><span data-stu-id="fa3b8-439">3</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-440">10 (com taxa de falha de 0,2%)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-441">17 (com uma taxa de falha de 1%)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="fa3b8-442">Recomendações de planejamento de capacidade de streaming do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-442">App-V 5.1 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="fa3b8-443">Os computadores que executam o cliente App-V 5,1 transmitem o pacote de aplicativo virtual do servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-443">Computers running the App-V 5.1 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="fa3b8-444">O tempo de resposta de ida e volta é medido no computador que executa o cliente App-V 5,1 e é o tempo levado para transmitir todo o pacote.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-444">Round trip response time is measured on the computer running the App-V 5.1 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="fa3b8-445">**Importante**  A lista a seguir identifica os principais fatores a serem considerados ao configurar o servidor de streaming do App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.1 streaming server:</span></span>

-   <span data-ttu-id="fa3b8-446">O número de pacotes de aplicativos de transmissão de clientes simultaneamente de um único servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="fa3b8-447">O tamanho do pacote que está sendo transmitido.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="fa3b8-448">A largura de banda de rede disponível em seu ambiente entre o cliente e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-449">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-450">Resumo</span><span class="sxs-lookup"><span data-stu-id="fa3b8-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-451">Vários clientes do App-V 5,1 transmitem aplicativos de um único servidor de streaming simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-451">Multiple App-V 5.1 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-452">Se o número de clientes que realizam streaming simultâneo do mesmo servidor aumentar, há uma relação linear com o tempo de download do pacote/tempo de streaming.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-453">Tamanho do pacote que está sendo transmitido.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-454">O tamanho do pacote tem um impacto significativo no tempo de streaming/download apenas para pacotes maiores com um tamanho de aproximadamente 1GB.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="fa3b8-455">Para tamanhos de pacote entre 3 MB e 100 MB, o tempo de transmissão varia de 20 a 100 segundos a 100 clientes simultâneos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-456">Rede entre o cliente do App-V 5,1 e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-456">Network between the App-V 5.1 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-457">Em uma rede lenta (largura de banda de 1,5 Mbps), há um aumento de 70-80% no tempo de resposta em comparação com a LAN (até 100 usuários).</span><span class="sxs-lookup"><span data-stu-id="fa3b8-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-458">A tabela a seguir exibe exemplos de valores para cada um dos fatores da lista anterior:</span><span class="sxs-lookup"><span data-stu-id="fa3b8-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa3b8-459">Cenário</span><span class="sxs-lookup"><span data-stu-id="fa3b8-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-460">Variação</span><span class="sxs-lookup"><span data-stu-id="fa3b8-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-461">Número de clientes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-461">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-462">Tamanho de cada pacote</span><span class="sxs-lookup"><span data-stu-id="fa3b8-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-463">Cliente do tipo de conexão de rede Server/App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-463">Network connection type streaming server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="fa3b8-464">Tempo de viagem de ida e volta no cliente do App-V 5,1 (em segundos)</span><span class="sxs-lookup"><span data-stu-id="fa3b8-464">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-465">Vários clientes do App-V 5,1 transmitindo pacotes de aplicativos virtuais de um servidor de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-465">Multiple App-V 5.1 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-466">Número de clientes.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-467">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-467">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-468">200</span><span class="sxs-lookup"><span data-stu-id="fa3b8-468">200</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-469">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-470">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-470">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-471">200</span><span class="sxs-lookup"><span data-stu-id="fa3b8-471">200</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-472">1000</span><span class="sxs-lookup"><span data-stu-id="fa3b8-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-473">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-474">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-475">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-476">5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-477">5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-478">5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-479">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-480">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-481">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-482">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-483">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-484">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-485">anos</span><span class="sxs-lookup"><span data-stu-id="fa3b8-485">29</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-486">39</span><span class="sxs-lookup"><span data-stu-id="fa3b8-486">39</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-487">391</span><span class="sxs-lookup"><span data-stu-id="fa3b8-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-488">35</span><span class="sxs-lookup"><span data-stu-id="fa3b8-488">35</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-489">68</span><span class="sxs-lookup"><span data-stu-id="fa3b8-489">68</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-490">461</span><span class="sxs-lookup"><span data-stu-id="fa3b8-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa3b8-491">Tamanho de cada pacote que está sendo transmitido.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-492">Tamanho de cada pacote.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-493">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-493">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-494">200</span><span class="sxs-lookup"><span data-stu-id="fa3b8-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-495">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-495">100</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-496">200</span><span class="sxs-lookup"><span data-stu-id="fa3b8-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-497">21 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-498">21 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-499">109</span><span class="sxs-lookup"><span data-stu-id="fa3b8-499">109</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-500">109</span><span class="sxs-lookup"><span data-stu-id="fa3b8-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-501">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-502">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-503">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="fa3b8-504">LAN</span><span class="sxs-lookup"><span data-stu-id="fa3b8-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="fa3b8-505">33</span><span class="sxs-lookup"><span data-stu-id="fa3b8-505">33</span></span></p>
<p><span data-ttu-id="fa3b8-506">83</span><span class="sxs-lookup"><span data-stu-id="fa3b8-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="fa3b8-507">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-507">100</span></span></p>
<p><span data-ttu-id="fa3b8-508">160</span><span class="sxs-lookup"><span data-stu-id="fa3b8-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa3b8-509">Conexão de rede entre o servidor de streaming do cliente e do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-509">Network connection between client and App-V 5.1 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa3b8-510">rede de link lento de 1,5 Mbps.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-511">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-512">100</span><span class="sxs-lookup"><span data-stu-id="fa3b8-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-513">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="fa3b8-514">5 MB</span><span class="sxs-lookup"><span data-stu-id="fa3b8-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="fa3b8-515">Rede intra-continental de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="fa3b8-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="fa3b8-516">102</span><span class="sxs-lookup"><span data-stu-id="fa3b8-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="fa3b8-517">121</span><span class="sxs-lookup"><span data-stu-id="fa3b8-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fa3b8-518">Cada servidor de streaming do App-V 5,1 deve ser capaz de manipular um mínimo de 200 clientes que transmitiram simultaneamente aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-518">Each App-V 5.1 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="fa3b8-519">**Observação**  O tempo real para o fluxo será determinado principalmente pelo número de clientes que estão sendo transmitidos simultaneamente, número de pacotes, tamanho do pacote, atividade da rede do servidor e condições da rede.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="fa3b8-520">Por exemplo, um usuário médio pode transmitir um pacote de 100 MB em menos de 2 minutos, quando 100 clientes simultâneos estão transmitindo do servidor.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="fa3b8-521">No entanto, um pacote de tamanho 1 GB pode levar até 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="fa3b8-522">Na maioria dos ambientes do mundo real, a demanda de transmissão não é distribuída de maneira uniforme, você precisará compreender os requisitos de streaming de pico aproximados presentes no ambiente para dimensionar corretamente o número de servidores de streaming necessários.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="fa3b8-523">O número de clientes em que um servidor de streaming pode oferecer suporte pode ser aumentado significativamente e os requisitos de pico de streaming reduzidos se você armazenar previamente em cache seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="fa3b8-524">Você também pode aumentar o número de clientes para o qual um servidor de streaming pode oferecer suporte usando pacotes otimizados sob demanda e pacotes otimizados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="fa3b8-525">Combinando funções de servidor do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-525">Combining App-V 5.1 Server Roles</span></span>


<span data-ttu-id="fa3b8-526">Com a descontamento dos requisitos de dimensionamento e tolerância a falhas, o número mínimo de servidores necessários para um local com conectividade com o Active Directory é um.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="fa3b8-527">Este servidor hospedará as funções servidor de gerenciamento, serviço servidor de gerenciamento e Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="fa3b8-528">As funções de servidor, portanto, podem ser organizadas em qualquer combinação desejada porque elas não entram em conflito umas com as outras.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="fa3b8-529">Ignorar requisitos de dimensionamento, o número mínimo de servidores necessários para fornecer uma implementação tolerante a falhas é de quatro.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="fa3b8-530">O servidor de gerenciamento e as funções do Microsoft SQL Server dão suporte a serem colocadas em configurações tolerantes a falhas.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="fa3b8-531">O serviço do servidor de gerenciamento pode ser combinado com qualquer uma das funções, mas permanece um ponto único de falha.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="fa3b8-532">Embora existam várias estratégias e tecnologias de tolerância a falhas disponíveis, nem todas são aplicáveis a um serviço específico.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="fa3b8-533">Além disso, se as funções do App-V 5,1 forem combinadas, algumas opções de tolerância a falhas não poderão mais se aplicar devido a incompatibilidades.</span><span class="sxs-lookup"><span data-stu-id="fa3b8-533">Additionally, if App-V 5.1 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="fa3b8-534">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa3b8-534">Related topics</span></span>


[<span data-ttu-id="fa3b8-535">Configurações com suporte ao App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-535">App-V 5.1 Supported Configurations</span></span>](app-v-51-supported-configurations.md)

[<span data-ttu-id="fa3b8-536">Planejamento de alta disponibilidade com o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fa3b8-536">Planning for High Availability with App-V 5.1</span></span>](planning-for-high-availability-with-app-v-51.md)

[<span data-ttu-id="fa3b8-537">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="fa3b8-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





