---
title: Configurações com suporte no MBAM 2.0
description: Configurações com suporte no MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799366"
---
# <span data-ttu-id="697f0-103">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="697f0-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="697f0-104">Este tópico especifica os requisitos para instalar e executar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 em seu ambiente usando a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="697f0-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="697f0-105">Para configurações compatíveis que se aplicam a versões posteriores, consulte a documentação da versão aplicável.</span><span class="sxs-lookup"><span data-stu-id="697f0-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="697f0-106">Se você planeja instalar o MBAM 2,0 usando a topologia do Configuration Manager e deseja revisar uma lista dos requisitos do sistema, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="697f0-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="697f0-107">A configuração recomendada para executar o MBAM em um ambiente de produção é com dois servidores, dependendo dos requisitos de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="697f0-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="697f0-108">Essa configuração dá suporte a até 200.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="697f0-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="697f0-109">Para obter uma imagem e descrições da infraestrutura autônoma do servidor MBAM, consulte [arquitetura de alto nível para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="697f0-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="697f0-110">**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="697f0-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="697f0-111">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="697f0-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="697f0-112">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="697f0-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="697f0-113">Requisitos do sistema do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="697f0-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="697f0-114">Requisitos do sistema operacional do servidor</span><span class="sxs-lookup"><span data-stu-id="697f0-114">Server Operating System Requirements</span></span>

<span data-ttu-id="697f0-115">A tabela a seguir lista os sistemas operacionais suportados para a instalação do Microsoft BitLocker Administration and Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="697f0-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="697f0-116">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="697f0-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="697f0-117">Edição</span><span class="sxs-lookup"><span data-stu-id="697f0-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="697f0-118">Service Pack</span><span class="sxs-lookup"><span data-stu-id="697f0-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="697f0-119">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="697f0-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="697f0-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-121">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="697f0-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-122">SP1</span><span class="sxs-lookup"><span data-stu-id="697f0-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-123">64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="697f0-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-125">Edição padrão ou de datacenter</span><span class="sxs-lookup"><span data-stu-id="697f0-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="697f0-126">64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="697f0-127">**Observação**  Não há suporte para a instalação de serviços, relatórios ou bancos de dados do MBAM em um computador controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="697f0-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="697f0-128">Requisitos do processador do servidor, da RAM e do espaço em disco</span><span class="sxs-lookup"><span data-stu-id="697f0-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="697f0-129">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="697f0-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="697f0-130">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="697f0-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="697f0-131">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="697f0-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-132">Processador</span><span class="sxs-lookup"><span data-stu-id="697f0-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-133">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="697f0-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-134">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="697f0-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-135">RAM</span><span class="sxs-lookup"><span data-stu-id="697f0-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-136">8 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-137">12 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-138">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="697f0-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-139">1 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-140">2 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="697f0-141">Requisitos do banco de dados do SQLServer</span><span class="sxs-lookup"><span data-stu-id="697f0-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="697f0-142">A tabela a seguir lista as versões do SQLServer com suporte para a instalação de recursos do servidor de administração e monitoramento, que inclui o banco de dados de recuperação, o banco de dados de auditoria e conformidade e os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="697f0-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="697f0-143">Os bancos de dados também exigem a instalação das ferramentas de gerenciamento do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="697f0-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="697f0-144">**Observação**  O MBAM não oferece suporte nativo a grupos de clusters, espelhamento ou clusters de SQL.</span><span class="sxs-lookup"><span data-stu-id="697f0-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="697f0-145">Para instalar os bancos de dados, você deve executar a instalação do servidor do MBAM em um SQL Server autônomo.</span><span class="sxs-lookup"><span data-stu-id="697f0-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="697f0-146">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="697f0-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="697f0-147">Edição</span><span class="sxs-lookup"><span data-stu-id="697f0-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="697f0-148">Service Pack</span><span class="sxs-lookup"><span data-stu-id="697f0-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="697f0-149">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="697f0-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="697f0-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-151">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="697f0-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-152">SP1</span><span class="sxs-lookup"><span data-stu-id="697f0-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-153">64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="697f0-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-155">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="697f0-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-156">SP1</span><span class="sxs-lookup"><span data-stu-id="697f0-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="697f0-158">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="697f0-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="697f0-159">Necessidade mínima</span><span class="sxs-lookup"><span data-stu-id="697f0-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="697f0-160">Necessidade recomendada</span><span class="sxs-lookup"><span data-stu-id="697f0-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-161">Processador</span><span class="sxs-lookup"><span data-stu-id="697f0-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-162">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="697f0-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-163">2,33 GHz ou mais</span><span class="sxs-lookup"><span data-stu-id="697f0-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-164">RAM</span><span class="sxs-lookup"><span data-stu-id="697f0-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-165">8 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-166">12 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-167">Espaço livre em disco</span><span class="sxs-lookup"><span data-stu-id="697f0-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-168">5 GB</span><span class="sxs-lookup"><span data-stu-id="697f0-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-169">5 GB ou mais</span><span class="sxs-lookup"><span data-stu-id="697f0-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="697f0-170">Requisitos do sistema do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="697f0-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="697f0-171">Requisitos do sistema operacional do cliente</span><span class="sxs-lookup"><span data-stu-id="697f0-171">Client Operating System Requirements</span></span>

<span data-ttu-id="697f0-172">A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="697f0-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="697f0-173">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="697f0-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="697f0-174">Edição</span><span class="sxs-lookup"><span data-stu-id="697f0-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="697f0-175">Service Pack</span><span class="sxs-lookup"><span data-stu-id="697f0-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="697f0-176">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="697f0-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-177">7</span><span class="sxs-lookup"><span data-stu-id="697f0-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-178">Enterprise ou Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="697f0-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-179">SP1</span><span class="sxs-lookup"><span data-stu-id="697f0-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-180">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-181">Windows 8</span><span class="sxs-lookup"><span data-stu-id="697f0-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-182">Edição Enterprise</span><span class="sxs-lookup"><span data-stu-id="697f0-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="697f0-183">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-184">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="697f0-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-185">Edição do Windows 8 Enterprise</span><span class="sxs-lookup"><span data-stu-id="697f0-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="697f0-186">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="697f0-187">Requisitos de RAM do cliente</span><span class="sxs-lookup"><span data-stu-id="697f0-187">Client RAM Requirements</span></span>

<span data-ttu-id="697f0-188">Não há nenhuma necessidade de RAM específica para a instalação do cliente de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="697f0-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="697f0-189">Requisitos do sistema da política de grupo do MBAM</span><span class="sxs-lookup"><span data-stu-id="697f0-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="697f0-190">A tabela a seguir lista os sistemas operacionais suportados para a instalação do modelo de política de grupo do Microsoft BitLocker Administration and Monitoring.</span><span class="sxs-lookup"><span data-stu-id="697f0-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="697f0-191">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="697f0-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="697f0-192">Edição</span><span class="sxs-lookup"><span data-stu-id="697f0-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="697f0-193">Service Pack</span><span class="sxs-lookup"><span data-stu-id="697f0-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="697f0-194">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="697f0-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-195">7</span><span class="sxs-lookup"><span data-stu-id="697f0-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-196">Enterprise ou Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="697f0-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-197">SP1</span><span class="sxs-lookup"><span data-stu-id="697f0-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-198">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-199">Windows 8</span><span class="sxs-lookup"><span data-stu-id="697f0-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-200">Edição Enterprise</span><span class="sxs-lookup"><span data-stu-id="697f0-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="697f0-201">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="697f0-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="697f0-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-203">Standard, Enterprise ou Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="697f0-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-204">SP1</span><span class="sxs-lookup"><span data-stu-id="697f0-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-205">64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="697f0-206">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="697f0-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="697f0-207">Edição padrão ou de datacenter</span><span class="sxs-lookup"><span data-stu-id="697f0-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="697f0-208">64 bits</span><span class="sxs-lookup"><span data-stu-id="697f0-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="697f0-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="697f0-209">Related topics</span></span>


[<span data-ttu-id="697f0-210">Planejar a implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="697f0-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="697f0-211">Pré-requisitos para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="697f0-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





