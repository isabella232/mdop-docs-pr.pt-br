---
title: Como planejar a implantação do MBAM com o Configuration Manager
description: Como planejar a implantação do MBAM com o Configuration Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799710"
---
# <span data-ttu-id="d1850-103">Como planejar a implantação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="d1850-104">Para implantar o MBAM com a topologia do Configuration Manager, é recomendável uma arquitetura de três servidores, que dá suporte a clientes do 200.000.</span><span class="sxs-lookup"><span data-stu-id="d1850-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="d1850-105">Use um servidor separado para executar o Configuration Manager e instale os recursos básicos de administração e monitoramento em dois servidores, como mostrado na imagem de arquitetura em [introdução-usando o MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="d1850-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="d1850-106">Importante</span><span class="sxs-lookup"><span data-stu-id="d1850-106">Important</span></span>**  
<span data-ttu-id="d1850-107">Não há suporte para o Windows to go ao instalar a topologia integrada do MBAM com o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="d1850-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="d1850-108">Pré-requisitos de implantação para instalar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="d1850-109">Verifique se você atendeu aos seguintes pré-requisitos antes de instalar o MBAM com o Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="d1850-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-110">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="d1850-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="d1850-111">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="d1850-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-112">Verifique se o servidor do Configuration Manager é um site primário no sistema do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-113">N/A</span><span class="sxs-lookup"><span data-stu-id="d1850-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-114">Habilite o agente cliente do inventário de hardware no servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-115">Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> como configurar o inventário de hardware para um site </a> .</span><span class="sxs-lookup"><span data-stu-id="d1850-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="d1850-116">Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> como configurar o inventário de hardware no Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="d1850-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-117">Habilite o agente DCM (gerenciamento de configuração) ou as configurações de conformidade, dependendo da versão do Configuration Manager que você está usando.</span><span class="sxs-lookup"><span data-stu-id="d1850-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-118">Para o Configuration Manager 2007, habilite as <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Propriedades do agente do cliente de gerenciamento de configuração desejado </a> .</span><span class="sxs-lookup"><span data-stu-id="d1850-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="d1850-119">Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> definindo configurações de conformidade no Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="d1850-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-120">Defina um ponto do Reporting Services no Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="d1850-121">Obrigatório para SQL Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="d1850-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-122">Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> como criar um ponto do Reporting Services para SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="d1850-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="d1850-123">Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> pré-requisitos para relatórios no Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="d1850-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="d1850-124">Versões compatíveis do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="d1850-125">O MBAM dá suporte para as seguintes versões do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="d1850-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-126">Versão com suporte</span><span class="sxs-lookup"><span data-stu-id="d1850-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="d1850-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="d1850-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="d1850-128">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="d1850-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d1850-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-130">SP1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d1850-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-131">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1850-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d1850-132">Observação</span><span class="sxs-lookup"><span data-stu-id="d1850-132">Note</span></span></strong><br/><p><span data-ttu-id="d1850-133">Embora o Configuration Manager 2007 seja 32 bits, você deve instalá-lo e SQL Server em um sistema operacional de 64 bits para corresponder ao software MBAM de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1850-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-134">Gerenciador de configuração do Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="d1850-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-135">SP1</span><span class="sxs-lookup"><span data-stu-id="d1850-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-136">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1850-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="d1850-137">Para obter uma lista de configurações compatíveis com o Configuration Manager Server, consulte a página da Web apropriada para a versão do Configuration Manager que você está usando.</span><span class="sxs-lookup"><span data-stu-id="d1850-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="d1850-138">O MBAM não tem requisitos de sistema adicionais para o servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="d1850-139">Requisitos de sistema do MBAM e do SQL Server</span><span class="sxs-lookup"><span data-stu-id="d1850-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="d1850-140">As configurações compatíveis e os requisitos de sistema para os servidores MBAM e SQL Server para a topologia do Configuration Manager são iguais aos da topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="d1850-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="d1850-141">Para obter os requisitos de sistema autônomos, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d1850-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="d1850-142">Para os requisitos do servidor do SQL Server e do processador do SQL Server, da RAM e do espaço em disco para a topologia do Configuration Manager, consulte as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1850-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="d1850-143">Processador de servidor MBAM, RAM e requisitos de espaço em disco para MBAM</span><span class="sxs-lookup"><span data-stu-id="d1850-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="d1850-144">A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para servidores MBAM quando você estiver usando a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-145">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="d1850-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="d1850-146">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="d1850-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="d1850-147">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="d1850-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-148">Processador</span><span class="sxs-lookup"><span data-stu-id="d1850-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-149">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="d1850-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-150">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="d1850-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-151">RAM</span><span class="sxs-lookup"><span data-stu-id="d1850-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-152">4 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-153">8 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-154">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="d1850-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-155">1 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-156">2 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1850-157">Requisitos de processador, RAM e espaço em disco do SQL Server</span><span class="sxs-lookup"><span data-stu-id="d1850-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="d1850-158">A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco do computador SQL Server quando você estiver usando a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-159">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="d1850-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="d1850-160">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="d1850-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="d1850-161">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="d1850-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-162">Processador</span><span class="sxs-lookup"><span data-stu-id="d1850-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-163">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="d1850-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-164">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="d1850-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-165">RAM</span><span class="sxs-lookup"><span data-stu-id="d1850-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-166">4 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-167">8 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-168">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="d1850-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-169">5 GB</span><span class="sxs-lookup"><span data-stu-id="d1850-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-170">5 GB ou mais</span><span class="sxs-lookup"><span data-stu-id="d1850-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1850-171">Permissões necessárias para instalar o servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="d1850-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="d1850-172">Para instalar o MBAM com o Configuration Manager, você deve ter um usuário administrativo no Configuration Manager que tenha um direito de acesso com as permissões mínimas listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1850-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="d1850-173">A tabela também mostra os direitos que você deve ter, além dos direitos de administrador do computador básico, para instalar o MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="d1850-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-174">Permissões</span><span class="sxs-lookup"><span data-stu-id="d1850-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="d1850-175">Recurso do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="d1850-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-176">Funções do servidor de logon da instância SQL:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="d1850-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="d1850-177">Banco de dados de recuperação-banco de dados de auditoria</span><span class="sxs-lookup"><span data-stu-id="d1850-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-178">Direitos de instância do SQL Server Reporting Services:-criar pastas-publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="d1850-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="d1850-179">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d1850-180">Systems Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-181">Permissões</span><span class="sxs-lookup"><span data-stu-id="d1850-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="d1850-182">Recurso do servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-183">Direitos de site do Configuration Manager:-ler</span><span class="sxs-lookup"><span data-stu-id="d1850-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-184">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-185">Direitos de coleção do Configuration Manager:-criar-excluir-ler-modificar-implantar itens de configuração</span><span class="sxs-lookup"><span data-stu-id="d1850-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-186">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-187">Direitos de item de configuração do Configuration Manager:-Create-Delete-Read</span><span class="sxs-lookup"><span data-stu-id="d1850-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-188">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d1850-189">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="d1850-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1850-190">Permissões</span><span class="sxs-lookup"><span data-stu-id="d1850-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="d1850-191">Recurso do servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-192">Direitos de site do Configuration Manager:-ler</span><span class="sxs-lookup"><span data-stu-id="d1850-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-193">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1850-194">Direitos de coleção do Configuration Manager:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="d1850-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-195">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1850-196">Direitos de item de configuração do Configuration Manager:-criar-excluir-ler-distribuir</span><span class="sxs-lookup"><span data-stu-id="d1850-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-197">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1850-198">Ordem de implantação de recursos de MBAM para a topologia do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="d1850-199">Ao implantar o MBAM no servidor do Configuration Manager, você deve concluir as tarefas de implantação na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="d1850-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="d1850-200">Edite o arquivo Configuration. mof no servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="d1850-201">Crie ou edite o servidor do Gerenciador de arquivos do SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="d1850-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="d1850-202">Instale o MBAM no servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="d1850-203">Instale o banco de dados de recuperação e o banco de dados de auditoria no servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d1850-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="d1850-204">Instale os recursos do MBAM no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d1850-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="d1850-205">Lista de verificação de planejamento para a instalação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="d1850-206">Esta lista de verificação descreve as etapas recomendadas e uma lista de alto nível de itens a serem considerados ao planejar uma implantação do Microsoft BitLocker Administration and Monitoring with Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d1850-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="d1850-207">É recomendável que você copie esta lista de verificação para um programa de planilha e personalize-a para seu uso.</span><span class="sxs-lookup"><span data-stu-id="d1850-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="d1850-208">Tarefa</span><span class="sxs-lookup"><span data-stu-id="d1850-208">Task</span></span></th>
<th align="left"><span data-ttu-id="d1850-209">Referências</span><span class="sxs-lookup"><span data-stu-id="d1850-209">References</span></span></th>
<th align="left"><span data-ttu-id="d1850-210">Observações</span><span class="sxs-lookup"><span data-stu-id="d1850-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d1850-211">Examine as informações de introdução, que descrevem como o Configuration Manager funciona com o MBAM e mostra a arquitetura de alto nível recomendada.</span><span class="sxs-lookup"><span data-stu-id="d1850-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="d1850-212">Introdução – Como usar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d1850-213">Examine as informações de planejamento, que descrevem os pré-requisitos de implantação, configurações com suporte, permissões necessárias e ordem de implantação para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="d1850-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1850-214">Como planejar a implantação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d1850-215">Planeje e configure MBAM requisitos da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="d1850-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="d1850-216">Planejar Requisitos de Política de Grupo do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d1850-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d1850-217">Planeje e crie os grupos de segurança dos serviços de domínio Active Directory necessários e planeje os requisitos de associação do grupo de segurança local do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d1850-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="d1850-218">Planejamento para Funções de Administrador do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d1850-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d1850-219">Plano para implantar a implantação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="d1850-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="d1850-220">Planejar implantação de cliente MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d1850-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1850-221">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1850-221">Related topics</span></span>


[<span data-ttu-id="d1850-222">Usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1850-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









