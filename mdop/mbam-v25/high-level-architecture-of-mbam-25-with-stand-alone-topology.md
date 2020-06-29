---
title: Arquitetura de alto nível do MBAM 2.5 com topologia autônoma
description: Arquitetura de alto nível do MBAM 2.5 com topologia autônoma
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799896"
---
# <span data-ttu-id="08a01-103">Arquitetura de alto nível do MBAM 2.5 com topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="08a01-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="08a01-104">Este tópico descreve a arquitetura recomendada para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia autônoma do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="08a01-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="08a01-105">Nessa topologia, o MBAM é implantado como um produto autônomo.</span><span class="sxs-lookup"><span data-stu-id="08a01-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="08a01-106">Você também pode implantar o MBAM com a topologia de integração do Configuration Manager, que integra o MBAM com o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="08a01-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="08a01-107">Para obter mais informações, consulte [arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="08a01-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="08a01-108">Para obter uma lista das versões com suporte do software mencionadas neste tópico, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="08a01-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="08a01-109">**Observação**  Recomendamos que você use uma arquitetura de servidor único somente em ambientes de teste.</span><span class="sxs-lookup"><span data-stu-id="08a01-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="08a01-110">Número recomendado de servidores e número de clientes com suporte</span><span class="sxs-lookup"><span data-stu-id="08a01-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="08a01-111">O número recomendado de servidores e o número de clientes com suporte em um ambiente de produção é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="08a01-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08a01-112">Arquitetura recomendada em um ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="08a01-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="08a01-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="08a01-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08a01-114">Número de servidores e outros computadores</span><span class="sxs-lookup"><span data-stu-id="08a01-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="08a01-115">Dois servidores</span><span class="sxs-lookup"><span data-stu-id="08a01-115">Two servers</span></span></p>
<p><span data-ttu-id="08a01-116">Uma estação de trabalho</span><span class="sxs-lookup"><span data-stu-id="08a01-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08a01-117">Número de computadores cliente com suporte</span><span class="sxs-lookup"><span data-stu-id="08a01-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="08a01-118">500.000</span><span class="sxs-lookup"><span data-stu-id="08a01-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="08a01-119">Arquitetura de alto nível MBAM recomendada com a topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="08a01-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="08a01-120">O diagrama e a tabela a seguir descrevem a arquitetura recomendada de dois níveis e dois servidores para o MBAM com a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="08a01-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="08a01-121">MBAM implantações de várias florestas exigem confiança unidirecional ou bidirecional.</span><span class="sxs-lookup"><span data-stu-id="08a01-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="08a01-122">As relações de confiança unidirecionais exigem que o domínio do servidor confie no domínio do cliente.</span><span class="sxs-lookup"><span data-stu-id="08a01-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="08a01-124">Recursos de servidor a serem configurados neste servidor de banco de dados de descrição do servidor</span><span class="sxs-lookup"><span data-stu-id="08a01-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="08a01-125">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="08a01-125">Compliance and Audit Database</span></span>

<span data-ttu-id="08a01-126">Esse recurso está configurado em um servidor que executa o Windows Server e a instância do SQL Server com suporte.</span><span class="sxs-lookup"><span data-stu-id="08a01-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="08a01-127">O banco de dados de **conformidade e auditoria** armazena dados de conformidade, que são usados principalmente para relatórios que o SQL Server Reporting Services hospeda.</span><span class="sxs-lookup"><span data-stu-id="08a01-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="08a01-128">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="08a01-128">Recovery Database</span></span>

<span data-ttu-id="08a01-129">Esse recurso está configurado em um servidor que executa o Windows Server e a instância do SQL Server com suporte.</span><span class="sxs-lookup"><span data-stu-id="08a01-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="08a01-130">O **banco** de dados de recuperação armazena dados de recuperação coletados de computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="08a01-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="08a01-131">Relatórios</span><span class="sxs-lookup"><span data-stu-id="08a01-131">Reports</span></span>

<span data-ttu-id="08a01-132">Esse recurso está configurado em um servidor que executa o Windows Server e a instância do SQL Server com suporte.</span><span class="sxs-lookup"><span data-stu-id="08a01-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="08a01-133">Os **relatórios** fornecem dados de status de conformidade e auditoria de recuperação sobre os computadores cliente da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="08a01-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="08a01-134">Você pode acessar os relatórios do site Administração e monitoramento ou diretamente do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="08a01-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="08a01-135">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="08a01-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="08a01-136">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="08a01-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="08a01-137">Esse recurso é configurado em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="08a01-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="08a01-138">O **site de administração e monitoramento** é usado para:</span><span class="sxs-lookup"><span data-stu-id="08a01-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="08a01-139">Ajude os usuários finais a recuperarem o acesso aos seus computadores quando estiverem bloqueados. (Essa área do site geralmente é chamada de suporte técnico).</span><span class="sxs-lookup"><span data-stu-id="08a01-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="08a01-140">Exiba relatórios que mostram o status de conformidade e a atividade de recuperação para computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="08a01-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="08a01-141">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="08a01-141">Self-Service Portal</span></span>

<span data-ttu-id="08a01-142">Esse recurso é configurado em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="08a01-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="08a01-143">O **portal de autoatendimento** é um site que permite aos usuários finais nos computadores cliente fazerem logon independentemente em um site para obter uma chave de recuperação caso percam ou esqueçam a senha do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="08a01-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="08a01-144">Monitorando serviços Web para este site</span><span class="sxs-lookup"><span data-stu-id="08a01-144">Monitoring web services for this website</span></span>

<span data-ttu-id="08a01-145">Esse recurso é configurado em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="08a01-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="08a01-146">Os **Serviços Web de monitoramento** são usados pelo cliente MBAM e pelos websites para se comunicar ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08a01-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="08a01-147">**Importante**  O serviço Web de monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, pois os sites do MBAM se comunicam diretamente com o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="08a01-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="08a01-148">Estação de trabalho de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="08a01-148">Management workstation</span></span>

<span data-ttu-id="08a01-149">Modelos de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="08a01-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="08a01-150">Os modelos de política de grupo do MBAM são configurações de política de grupo que definem configurações de implementação para MBAM, que permitem que você gerencie a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="08a01-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="08a01-151">Antes de executar o MBAM, você deve baixar os modelos de política de grupo de [como obter modelos de política de grupo do MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou estação de trabalho que esteja executando um servidor Windows ou sistema operacional Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="08a01-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="08a01-152">A estação de trabalho não precisa ser um computador dedicado.</span><span class="sxs-lookup"><span data-stu-id="08a01-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="08a01-153">Cliente MBAM e computador cliente do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="08a01-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="08a01-154">Software cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="08a01-154">MBAM Client software</span></span>

<span data-ttu-id="08a01-155">O cliente MBAM:</span><span class="sxs-lookup"><span data-stu-id="08a01-155">The MBAM Client:</span></span>

-   <span data-ttu-id="08a01-156">Usa objetos de política de grupo para impor a criptografia de unidade de disco BitLocker em computadores cliente da empresa.</span><span class="sxs-lookup"><span data-stu-id="08a01-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="08a01-157">Coleta a chave de recuperação do BitLocker para três tipos de unidade de dados: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).</span><span class="sxs-lookup"><span data-stu-id="08a01-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="08a01-158">Coleta informações de recuperação e informações do computador dos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="08a01-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="08a01-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08a01-159">Related topics</span></span>


[<span data-ttu-id="08a01-160">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="08a01-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="08a01-161">Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="08a01-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="08a01-162">Recursos ilustrados de uma implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="08a01-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="08a01-163">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="08a01-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="08a01-164">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="08a01-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="08a01-165">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="08a01-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





