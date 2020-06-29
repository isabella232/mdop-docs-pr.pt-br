---
title: Visão geral do Cenário baseado no Application Virtualization Server
description: Visão geral do Cenário baseado no Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799003"
---
# <span data-ttu-id="9268a-103">Visão geral do Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="9268a-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="9268a-104">Se você pretende usar um cenário de implantação baseado em servidor para o seu ambiente do Microsoft Application Virtualization, é importante entender as diferenças entre o *servidor de gerenciamento do Application Virtualization* e o *servidor de streaming do Application Virtualization*.</span><span class="sxs-lookup"><span data-stu-id="9268a-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="9268a-105">Este tópico descreve essas diferenças e também fornece informações sobre métodos de entrega de pacote, protocolos de transmissão e componentes externos que você precisará considerar enquanto prossegue com a implantação.</span><span class="sxs-lookup"><span data-stu-id="9268a-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="9268a-106">Servidor de gerenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9268a-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="9268a-107">O servidor de gerenciamento do Application Virtualization executa a função de publicação e a função streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="9268a-108">O servidor publica os ícones de aplicativos, atalhos e associações de tipo de arquivo para os clientes do App-V para usuários autorizados.</span><span class="sxs-lookup"><span data-stu-id="9268a-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="9268a-109">Quando solicitações de usuário para aplicativos são recebidas, o servidor transmite os dados sob demanda para usuários autorizados usando protocolos RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="9268a-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="9268a-110">Na maioria das configurações usando este servidor, um ou mais servidores de gerenciamento compartilham um repositório de dados comum para informações de configuração e pacote.</span><span class="sxs-lookup"><span data-stu-id="9268a-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="9268a-111">Os servidores de gerenciamento do Application Virtualization usam grupos do Active Directory para gerenciar a autorização do usuário.</span><span class="sxs-lookup"><span data-stu-id="9268a-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="9268a-112">Além dos serviços de domínio Active Directory, esses servidores têm o SQL Server instalado para gerenciar o banco de dados e o repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="9268a-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="9268a-113">O servidor de gerenciamento é controlado por meio do console de gerenciamento do Application Virtualization, um snap-in para o console de gerenciamento da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9268a-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="9268a-114">Como os servidores de gerenciamento do Application Virtualization transmitem aplicativos para usuários finais sob demanda, esses servidores são adequados para configurações de sistema que têm LANs confiáveis e de alta largura de banda.</span><span class="sxs-lookup"><span data-stu-id="9268a-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="9268a-115">Servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9268a-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="9268a-116">O servidor de streaming do Application Virtualization oferece os mesmos recursos de streaming e atualização de pacote fornecidos pelo servidor de gerenciamento, mas sem seus requisitos do Active Directory ou do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9268a-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="9268a-117">No entanto, o servidor de streaming não tem um serviço de publicação, nem tem recursos de licenciamento ou medição.</span><span class="sxs-lookup"><span data-stu-id="9268a-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="9268a-118">O serviço de publicação de um servidor de gerenciamento do App-V separado é usado em conjunto com o servidor de streaming do App-V.</span><span class="sxs-lookup"><span data-stu-id="9268a-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="9268a-119">O servidor de streaming App-V atende às necessidades de empresas que desejam usar a virtualização de aplicativos em vários locais com os recursos de streaming da configuração do servidor clássico, mas talvez não tenham a infraestrutura para dar suporte a servidores de gerenciamento do App-V em todos os locais.</span><span class="sxs-lookup"><span data-stu-id="9268a-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="9268a-120">O servidor de streaming do Application Virtualization também pode ser usado em ambientes com um ESD (sistema de distribuição de software eletrônico) existente.</span><span class="sxs-lookup"><span data-stu-id="9268a-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="9268a-121">Use o ESD para gerenciar os aplicativos de streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="9268a-122">Ao contrário do servidor de gerenciamento do Application Virtualization, o servidor de streaming não usa SQL ou um console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9268a-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="9268a-123">Esses servidores usam listas de controle de acesso (ACLs) para conceder autorização ao usuário.</span><span class="sxs-lookup"><span data-stu-id="9268a-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="9268a-124">Métodos de entrega de pacote</span><span class="sxs-lookup"><span data-stu-id="9268a-124">Package Delivery Methods</span></span>


<span data-ttu-id="9268a-125">Se você planeja usar um servidor de virtualização de aplicativos como o método de entrega de publicação, será necessário determinar qual dos seguintes métodos de entrega de pacote o seu cenário emprega:</span><span class="sxs-lookup"><span data-stu-id="9268a-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="9268a-126">Entrega de pacote dinâmico</span><span class="sxs-lookup"><span data-stu-id="9268a-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="9268a-127">Carregar de entrega de pacote de arquivo</span><span class="sxs-lookup"><span data-stu-id="9268a-127">Load from file package delivery</span></span>*

### <span data-ttu-id="9268a-128">Entrega de pacote dinâmico</span><span class="sxs-lookup"><span data-stu-id="9268a-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="9268a-129">Durante a distribuição de pacote dinâmico, o servidor (servidor de gerenciamento do Application Virtualization, o servidor de streaming do Application Virtualization ou o servidor IIS) fornece os aplicativos virtualizados aos usuários finais por meio da implantação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="9268a-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="9268a-130">O servidor fornece os aplicativos e pacotes virtualizados para um computador cliente somente quando um usuário tenta iniciar um aplicativo pela primeira vez (sob demanda).</span><span class="sxs-lookup"><span data-stu-id="9268a-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="9268a-131">O servidor transmite apenas os blocos necessários para iniciar o aplicativo (bloco de recursos primário).</span><span class="sxs-lookup"><span data-stu-id="9268a-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="9268a-132">Depois que o bloco de recursos principal é entregue ao cliente, o aplicativo é executado; o cliente não recebe o aplicativo completo (implantação incremental) a menos que o cliente precise acessar uma parte do aplicativo que não está incluída no bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="9268a-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="9268a-133">Quando isso ocorre, o cliente executa uma solicitação fora de sequência e o bloco de recursos secundário é transmitido para o cliente.</span><span class="sxs-lookup"><span data-stu-id="9268a-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="9268a-134">A entrega de pacote dinâmico permite um início rápido do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9268a-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="9268a-135">Carregar de entrega de pacote de arquivo</span><span class="sxs-lookup"><span data-stu-id="9268a-135">Load from File Package Delivery</span></span>

<span data-ttu-id="9268a-136">Para carregar a entrega de pacotes de arquivos, o servidor entrega todo o pacote de aplicativos virtualizados para um computador cliente antes de o usuário iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9268a-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="9268a-137">Nesse cenário, os aplicativos virtualizados são entregues como um pacote completo, em vez de usar o método dinâmico e incremental usado pelo modelo de entrega dinâmico.</span><span class="sxs-lookup"><span data-stu-id="9268a-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="9268a-138">**Observação**  Para cada método de entrega, o processo inicial de entrega do aplicativo virtual e o processo de atualização de aplicativo virtual são iguais. o pacote de aplicativo virtual atualizado substitui o pacote do aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="9268a-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="9268a-139">A tabela a seguir compara as vantagens e desvantagens de cada método de entrega de pacote.</span><span class="sxs-lookup"><span data-stu-id="9268a-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9268a-140">Método</span><span class="sxs-lookup"><span data-stu-id="9268a-140">Method</span></span></th>
<th align="left"><span data-ttu-id="9268a-141">Vantagens</span><span class="sxs-lookup"><span data-stu-id="9268a-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="9268a-142">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="9268a-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="9268a-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="9268a-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9268a-144">Entrega de pacote dinâmico</span><span class="sxs-lookup"><span data-stu-id="9268a-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-145">Os aplicativos são entregues e atualizados sob demanda.</span><span class="sxs-lookup"><span data-stu-id="9268a-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="9268a-146">Os aplicativos são entregues e atualizados de forma incremental para otimizar o tempo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9268a-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="9268a-147">As atualizações são entregues automaticamente na área de trabalho do cliente.</span><span class="sxs-lookup"><span data-stu-id="9268a-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-148">Maior base na topologia empresarial devido aos requisitos do servidor.</span><span class="sxs-lookup"><span data-stu-id="9268a-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="9268a-149">O streaming de aplicativos deve ser de uma LAN; cenários de implantação em uma WAN ou que usam uma conexão não confiável ou intermitente entre o servidor e o cliente podem ser inutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="9268a-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-150">Requer uma infraestrutura de streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="9268a-151">Windows Installer usado para implantar o software cliente da área de trabalho do Application Virtualization em computadores de usuários finais.</span><span class="sxs-lookup"><span data-stu-id="9268a-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="9268a-152">Grandes empresas devem usar os servidores de streaming do Application Virtualization como pontos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="9268a-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9268a-153">Carregar de entrega de pacote de arquivo</span><span class="sxs-lookup"><span data-stu-id="9268a-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-154">Consistente com práticas comuns de gerenciamento corporativo.</span><span class="sxs-lookup"><span data-stu-id="9268a-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="9268a-155">Compatível com o cenário de configuração autônomo.</span><span class="sxs-lookup"><span data-stu-id="9268a-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="9268a-156">Fornece a solução para o micro – problema com o Branch Office.</span><span class="sxs-lookup"><span data-stu-id="9268a-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-157">A entrega e a atualização de aplicativos não é possível sob demanda.</span><span class="sxs-lookup"><span data-stu-id="9268a-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="9268a-158">A entrega e a atualização de aplicativos não é incremental; Ele aumenta o consumo de recursos em relação à entrega dinâmica.</span><span class="sxs-lookup"><span data-stu-id="9268a-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-159">A organização de ti geralmente é responsável por gerenciar licenças de aplicativos, autorização de usuário e autenticação.</span><span class="sxs-lookup"><span data-stu-id="9268a-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9268a-160">Protocolos relacionados a servidor e componentes externos</span><span class="sxs-lookup"><span data-stu-id="9268a-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="9268a-161">A tabela a seguir lista os tipos de servidor que podem ser usados em cenários baseados em servidor do Application Virtualization, juntamente com seus protocolos de transmissão correspondentes e os componentes externos necessários para dar suporte à configuração do servidor específico.</span><span class="sxs-lookup"><span data-stu-id="9268a-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="9268a-162">A tabela também inclui o mecanismo de relatório e o mecanismo de atualização ativa para cada tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="9268a-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="9268a-163">Como esses cenários usam o servidor de gerenciamento do Application Virtualization, você pode usar a funcionalidade de relatório interna interna do sistema.</span><span class="sxs-lookup"><span data-stu-id="9268a-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="9268a-164">Se você usa um servidor de gerenciamento do Application Virtualization ou um servidor de streaming do Application Virtualization para entregar pacotes ao cliente, os pacotes no servidor são atualizados automaticamente quando um usuário faz logon no cliente; Se você usar servidores IIS ou um arquivo para entregar os pacotes ao cliente, os pacotes no cliente deverão ser atualizados manualmente.</span><span class="sxs-lookup"><span data-stu-id="9268a-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

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
<th align="left"><span data-ttu-id="9268a-165">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="9268a-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="9268a-166">Protocolos</span><span class="sxs-lookup"><span data-stu-id="9268a-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="9268a-167">Componentes externos necessários</span><span class="sxs-lookup"><span data-stu-id="9268a-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="9268a-168">Relatórios</span><span class="sxs-lookup"><span data-stu-id="9268a-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="9268a-169">Atualização ativa</span><span class="sxs-lookup"><span data-stu-id="9268a-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9268a-170">Servidor de gerenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9268a-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-171">RTSP</span><span class="sxs-lookup"><span data-stu-id="9268a-171">RTSP</span></span></p>
<p><span data-ttu-id="9268a-172">RTSPs</span><span class="sxs-lookup"><span data-stu-id="9268a-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-173">Ao usar HTTPS, use um servidor IIS para baixar arquivos ICO e OSD e um firewall para proteger o servidor de exposição à Internet.</span><span class="sxs-lookup"><span data-stu-id="9268a-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-174">Interna</span><span class="sxs-lookup"><span data-stu-id="9268a-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-175">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9268a-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9268a-176">Servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9268a-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-177">RTSP</span><span class="sxs-lookup"><span data-stu-id="9268a-177">RTSP</span></span></p>
<p><span data-ttu-id="9268a-178">RTSPs</span><span class="sxs-lookup"><span data-stu-id="9268a-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-179">Use um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="9268a-180">Ao usar HTTPS, use um servidor IIS para baixar arquivos ICO e OSD e use um firewall para proteger o servidor de exposição à Internet.</span><span class="sxs-lookup"><span data-stu-id="9268a-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-181">Interna</span><span class="sxs-lookup"><span data-stu-id="9268a-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-182">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9268a-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9268a-183">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="9268a-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="9268a-184">HTTP</span></span></p>
<p><span data-ttu-id="9268a-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9268a-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-186">Use um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="9268a-187">Ao usar HTTP ou HTTPS, use um servidor IIS para baixar arquivos ICO e OSD e um firewall para proteger o servidor de exposição à Internet.</span><span class="sxs-lookup"><span data-stu-id="9268a-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-188">Interna</span><span class="sxs-lookup"><span data-stu-id="9268a-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-189">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="9268a-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9268a-190">Arquivo</span><span class="sxs-lookup"><span data-stu-id="9268a-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-191">SMB</span><span class="sxs-lookup"><span data-stu-id="9268a-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-192">Você precisa de uma maneira de sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="9268a-193">Você precisa de um computador cliente com compartilhamento de arquivos ou recurso de streaming.</span><span class="sxs-lookup"><span data-stu-id="9268a-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-194">Interna</span><span class="sxs-lookup"><span data-stu-id="9268a-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="9268a-195">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="9268a-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9268a-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9268a-196">Related topics</span></span>


[<span data-ttu-id="9268a-197">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="9268a-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="9268a-198">Como configurar os servidores para a implantação baseada em servidor</span><span class="sxs-lookup"><span data-stu-id="9268a-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="9268a-199">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="9268a-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





