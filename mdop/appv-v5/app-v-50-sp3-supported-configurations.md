---
title: Configurações com suporte ao App-V 5.0 SP3
description: Configurações com suporte ao App-V 5.0 SP3
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796588"
---
# <span data-ttu-id="12d1c-103">Configurações com suporte ao App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="12d1c-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="12d1c-104">Este tópico especifica os requisitos para instalar e executar o Microsoft Application Virtualization (App-V) 5,0 SP3 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="12d1c-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="12d1c-105">Requisitos do sistema do App-V Server</span><span class="sxs-lookup"><span data-stu-id="12d1c-105">App-V Server system requirements</span></span>


<span data-ttu-id="12d1c-106">Esta seção lista os requisitos de sistema operacional e de hardware para todos os componentes do App-V Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="12d1c-107">Cenários de servidor do App-V 5,0 SP3 sem suporte</span><span class="sxs-lookup"><span data-stu-id="12d1c-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="12d1c-108">O servidor App-V 5,0 SP3 não é compatível com os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="12d1c-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="12d1c-109">Implantação em um computador que executa o Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="12d1c-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="12d1c-110">Implantação em um computador que executa uma versão anterior dos componentes do App-V 5,0 SP3 Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="12d1c-111">Você pode instalar o App-V 5,0 SP3 lado a lado com o servidor do App-V 4.5 (LWS Stream Server) apenas.</span><span class="sxs-lookup"><span data-stu-id="12d1c-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="12d1c-112">A implantação do App-V lado a lado com o serviço de gerenciamento de virtualização do aplicativo (HWS) do App-V 4,5 não é suportada.</span><span class="sxs-lookup"><span data-stu-id="12d1c-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="12d1c-113">Implantação em um computador que executa o Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="12d1c-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="12d1c-114">Implantação remota do banco de dados do servidor de gerenciamento ou do banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="12d1c-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="12d1c-115">Você deve executar o instalador diretamente no computador que está executando o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="12d1c-116">Implantação em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="12d1c-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="12d1c-117">Caminhos curtos.</span><span class="sxs-lookup"><span data-stu-id="12d1c-117">Short paths.</span></span> <span data-ttu-id="12d1c-118">Se você pretende usar um caminho curto, deve criar um novo volume.</span><span class="sxs-lookup"><span data-stu-id="12d1c-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="12d1c-119">Requisitos do sistema operacional do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="12d1c-119">Management server operating system requirements</span></span>

<span data-ttu-id="12d1c-120">A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,0 SP3 Management Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="12d1c-121">**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="12d1c-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="12d1c-122">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="12d1c-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="12d1c-123">Consulte [perguntas frequentes sobre política de suporte do ciclo de vida do suporte Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="12d1c-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-124">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="12d1c-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="12d1c-125">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-126">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-128">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-130">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-132">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="12d1c-134">**Importante**  Não há suporte para a implantação da função de servidor de gerenciamento em um computador com o compartilhamento de área de trabalho remota (RDS) habilitada.</span><span class="sxs-lookup"><span data-stu-id="12d1c-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="12d1c-135">Requisitos de hardware do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="12d1c-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="12d1c-136">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="12d1c-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="12d1c-137">RAM — 1 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="12d1c-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="12d1c-138">Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo</span><span class="sxs-lookup"><span data-stu-id="12d1c-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="12d1c-139">Requisitos de banco de dados do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="12d1c-139">Management server database requirements</span></span>

<span data-ttu-id="12d1c-140">A tabela a seguir lista as versões do SQL Server que têm suporte para a instalação do banco de dados de gerenciamento do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="12d1c-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-141">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="12d1c-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="12d1c-142">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-143">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-144">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="12d1c-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-145">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-146">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-147">SP2</span><span class="sxs-lookup"><span data-stu-id="12d1c-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-148">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-150">SP3</span><span class="sxs-lookup"><span data-stu-id="12d1c-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-151">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="12d1c-152">Requisitos do sistema operacional do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="12d1c-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="12d1c-153">A tabela a seguir lista os sistemas operacionais com suporte para a instalação do App-V 5,0 SP3 Publishing Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-154">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="12d1c-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="12d1c-155">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-156">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-158">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-160">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-162">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-163">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="12d1c-164">Requisitos de hardware do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="12d1c-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="12d1c-165">O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="12d1c-166">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="12d1c-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="12d1c-167">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="12d1c-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="12d1c-168">Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo</span><span class="sxs-lookup"><span data-stu-id="12d1c-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="12d1c-169">Requisitos do sistema operacional do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="12d1c-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="12d1c-170">A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,0 SP3 Reporting Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-171">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="12d1c-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="12d1c-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-173">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-175">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-177">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-179">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-180">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="12d1c-181">Requisitos de hardware do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="12d1c-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="12d1c-182">O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="12d1c-183">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="12d1c-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="12d1c-184">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="12d1c-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="12d1c-185">Espaço em disco — 200 MB de espaço disponível no disco rígido</span><span class="sxs-lookup"><span data-stu-id="12d1c-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="12d1c-186">Requisitos de banco de dados do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="12d1c-186">Reporting server database requirements</span></span>

<span data-ttu-id="12d1c-187">A tabela a seguir lista as versões do SQL Server que têm suporte para a instalação do banco de dados de relatórios do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="12d1c-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-188">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="12d1c-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="12d1c-189">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-190">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-191">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="12d1c-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-192">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-193">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-194">SP2</span><span class="sxs-lookup"><span data-stu-id="12d1c-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-195">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-197">SP3</span><span class="sxs-lookup"><span data-stu-id="12d1c-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-198">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="12d1c-199">Requisitos do sistema do cliente App-V</span><span class="sxs-lookup"><span data-stu-id="12d1c-199">App-V client system requirements</span></span>


<span data-ttu-id="12d1c-200">A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="12d1c-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-201">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="12d1c-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="12d1c-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-203">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="12d1c-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-205">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-206">Microsoft windows8</span><span class="sxs-lookup"><span data-stu-id="12d1c-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-207">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-208">7</span><span class="sxs-lookup"><span data-stu-id="12d1c-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-209">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-210">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="12d1c-211">Não há suporte para os seguintes cenários de instalação do cliente do App-V, exceto conforme observado:</span><span class="sxs-lookup"><span data-stu-id="12d1c-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="12d1c-212">Computadores que executam o Windows Server</span><span class="sxs-lookup"><span data-stu-id="12d1c-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="12d1c-213">Computadores que executam o App-V 4.6 SP1 ou versões anteriores</span><span class="sxs-lookup"><span data-stu-id="12d1c-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="12d1c-214">O cliente de serviços de área de trabalho remota do App-V 5,0 SP3 só tem suporte para servidores habilitados para RDS</span><span class="sxs-lookup"><span data-stu-id="12d1c-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="12d1c-215">Requisitos de hardware do aplicativo cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="12d1c-215">App-V client hardware requirements</span></span>

<span data-ttu-id="12d1c-216">A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="12d1c-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="12d1c-217">Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="12d1c-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="12d1c-218">RAM – 1 GB (32 bits) ou 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="12d1c-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="12d1c-219">Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="12d1c-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="12d1c-220">Requisitos do sistema do cliente dos serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="12d1c-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="12d1c-221">A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente dos serviços de área de trabalho remota do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="12d1c-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-222">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="12d1c-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="12d1c-223">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-224">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-226">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-228">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-230">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-231">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="12d1c-232">Requisitos de hardware do cliente dos serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="12d1c-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="12d1c-233">O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="12d1c-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="12d1c-234">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="12d1c-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="12d1c-235">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="12d1c-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="12d1c-236">Espaço em disco — 200 MB de espaço disponível no disco rígido</span><span class="sxs-lookup"><span data-stu-id="12d1c-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="12d1c-237">Requisitos do sistema do sequenciador</span><span class="sxs-lookup"><span data-stu-id="12d1c-237">Sequencer system requirements</span></span>


<span data-ttu-id="12d1c-238">A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,0 SP3 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="12d1c-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12d1c-239">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="12d1c-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="12d1c-240">Service Pack</span><span class="sxs-lookup"><span data-stu-id="12d1c-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="12d1c-241">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="12d1c-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="12d1c-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="12d1c-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-245">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-246">Microsoft Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="12d1c-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-247">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-248">64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="12d1c-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-250">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="12d1c-251">Microsoft windows8</span><span class="sxs-lookup"><span data-stu-id="12d1c-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="12d1c-252">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="12d1c-253">Microsoft Windows7</span><span class="sxs-lookup"><span data-stu-id="12d1c-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-254">SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="12d1c-255">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="12d1c-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="12d1c-256">Requisitos de hardware do sequenciador</span><span class="sxs-lookup"><span data-stu-id="12d1c-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="12d1c-257">Consulte a documentação do Windows ou Windows Server para saber quais são os requisitos de hardware.</span><span class="sxs-lookup"><span data-stu-id="12d1c-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="12d1c-258">O App-V adiciona nenhum requisito de hardware adicional.</span><span class="sxs-lookup"><span data-stu-id="12d1c-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="12d1c-259">Versões com suporte do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="12d1c-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="12d1c-260">O cliente App-V dá suporte às seguintes versões do System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="12d1c-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="12d1c-261">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="12d1c-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="12d1c-262">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="12d1c-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="12d1c-263">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="12d1c-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="12d1c-264">Para obter mais informações sobre como o Configuration Manager integra-se ao App-V, consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="12d1c-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="12d1c-265">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12d1c-265">Related topics</span></span>


[<span data-ttu-id="12d1c-266">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="12d1c-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="12d1c-267">Pré-requisitos do App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="12d1c-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





