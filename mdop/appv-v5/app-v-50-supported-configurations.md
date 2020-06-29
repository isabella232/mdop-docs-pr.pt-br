---
title: Configurações com suporte ao App-V 5.0
description: Configurações com suporte ao App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796587"
---
# <span data-ttu-id="17581-103">Configurações com suporte ao App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="17581-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="17581-104">Este tópico especifica os requisitos necessários para instalar e executar o Microsoft Application Virtualization (App-V) 5,0 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="17581-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="17581-105">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-105">Important</span></span>**  
<span data-ttu-id="17581-106">**As configurações com suporte neste artigo se aplicam apenas ao App-V 5,0**.</span><span class="sxs-lookup"><span data-stu-id="17581-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="17581-107">Para configurações compatíveis que se aplicam aos pacotes de serviço do App-V 5,0, consulte as seguintes páginas da Web:</span><span class="sxs-lookup"><span data-stu-id="17581-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="17581-108">Quais são as novidades no App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="17581-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="17581-109">Sobre o App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="17581-110">Configurações com suporte ao App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="17581-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="17581-111">Requisitos do sistema do App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="17581-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="17581-112">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-112">Important</span></span>**  
<span data-ttu-id="17581-113">O servidor do App-V 5,0 não é compatível com os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="17581-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="17581-114">Implantação em um computador que executa o Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="17581-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="17581-115">Implantação em um computador que executa uma versão anterior dos componentes do App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="17581-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="17581-116">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-116">Note</span></span>**  
    <span data-ttu-id="17581-117">Você pode instalar o App-V 5,0 lado a lado com o servidor do App-V 4,5 Lightweight Streaming Server (LWS) apenas.</span><span class="sxs-lookup"><span data-stu-id="17581-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="17581-118">Não há suporte para a implantação do App-V 5,0 lado a lado com o servidor HWS do App-V 4,5 Application Virtualization Management Service (HWS).</span><span class="sxs-lookup"><span data-stu-id="17581-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="17581-119">Implantação em um computador que executa o Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="17581-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="17581-120">Implantação remota do banco de dados do servidor de gerenciamento ou do banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="17581-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="17581-121">O instalador deve ser executado diretamente no computador executando o Microsoft SQL para que a instalação do banco de dados seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="17581-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="17581-122">Implantação em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="17581-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="17581-123">Não há suporte para caminhos curtos.</span><span class="sxs-lookup"><span data-stu-id="17581-123">Short paths are not supported.</span></span> <span data-ttu-id="17581-124">Se você pretende usar um caminho curto, você deve criar um novo volume.</span><span class="sxs-lookup"><span data-stu-id="17581-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="17581-125">Requisitos do sistema operacional do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="17581-125">Management Server operating system requirements</span></span>

<span data-ttu-id="17581-126">A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="17581-127">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-127">Note</span></span>**  
<span data-ttu-id="17581-128">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17581-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17581-129">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17581-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17581-130">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17581-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17581-131">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17581-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17581-132">Edição</span><span class="sxs-lookup"><span data-stu-id="17581-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="17581-133">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17581-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17581-134">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17581-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-135">Microsoft Windows Server 2008 (padrão, Enterprise, Datacenter ou servidor Web)</span><span class="sxs-lookup"><span data-stu-id="17581-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-136">R2</span><span class="sxs-lookup"><span data-stu-id="17581-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-137">SP1 e versões mais recentes</span><span class="sxs-lookup"><span data-stu-id="17581-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-138">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-139">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-140">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-141">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-142">R2</span><span class="sxs-lookup"><span data-stu-id="17581-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-143">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="17581-144">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-144">Important</span></span>**  
<span data-ttu-id="17581-145">Não há suporte para a implantação da função de servidor de gerenciamento em um computador com o compartilhamento de área de trabalho remota (RDS) habilitada.</span><span class="sxs-lookup"><span data-stu-id="17581-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="17581-146">Requisitos de hardware do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="17581-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="17581-147">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="17581-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="17581-148">RAM — 1 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="17581-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="17581-149">Espaço em disco – 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="17581-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="17581-150">Requisitos do sistema operacional do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="17581-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="17581-151">A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de publicação do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="17581-152">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-152">Note</span></span>**  
<span data-ttu-id="17581-153">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17581-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17581-154">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17581-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17581-155">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17581-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17581-156">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17581-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17581-157">Edição</span><span class="sxs-lookup"><span data-stu-id="17581-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="17581-158">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17581-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17581-159">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17581-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-160">Microsoft Windows Server 2008 (padrão, Enterprise, Datacenter ou servidor Web)</span><span class="sxs-lookup"><span data-stu-id="17581-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-161">R2</span><span class="sxs-lookup"><span data-stu-id="17581-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-162">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-163">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-164">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-165">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-166">R2</span><span class="sxs-lookup"><span data-stu-id="17581-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-167">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="17581-168">Requisitos de hardware do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="17581-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="17581-169">Processador – 1,4 GHz ou mais veloz.</span><span class="sxs-lookup"><span data-stu-id="17581-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="17581-170">processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="17581-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="17581-171">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="17581-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="17581-172">Espaço em disco — 200 MB de espaço disponível no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="17581-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="17581-173">Não inclui o diretório de conteúdo</span><span class="sxs-lookup"><span data-stu-id="17581-173">not including content directory</span></span>

### <span data-ttu-id="17581-174">Requisitos do sistema operacional do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="17581-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="17581-175">A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,0 Reporting Server.</span><span class="sxs-lookup"><span data-stu-id="17581-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="17581-176">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-176">Note</span></span>**  
<span data-ttu-id="17581-177">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17581-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17581-178">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17581-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17581-179">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17581-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17581-180">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17581-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17581-181">Edição</span><span class="sxs-lookup"><span data-stu-id="17581-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="17581-182">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17581-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="17581-183">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17581-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-184">Microsoft Windows Server 2008 (padrão, Enterprise, Datacenter ou servidor Web)</span><span class="sxs-lookup"><span data-stu-id="17581-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-185">R2</span><span class="sxs-lookup"><span data-stu-id="17581-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-186">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-187">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-189">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-190">R2</span><span class="sxs-lookup"><span data-stu-id="17581-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="17581-192">Requisitos de hardware do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="17581-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="17581-193">Processador – 1,4 GHz ou mais veloz.</span><span class="sxs-lookup"><span data-stu-id="17581-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="17581-194">processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="17581-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="17581-195">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="17581-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="17581-196">Espaço em disco — 200 MB de espaço disponível no disco rígido</span><span class="sxs-lookup"><span data-stu-id="17581-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="17581-197">Requisitos de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="17581-197">SQL Server database requirements</span></span>

<span data-ttu-id="17581-198">A tabela a seguir lista as versões do SQL Server com suporte para o banco de dados do App-V 5,0 e para a instalação do servidor.</span><span class="sxs-lookup"><span data-stu-id="17581-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

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
<th align="left"><span data-ttu-id="17581-199">Tipo de servidor do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="17581-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="17581-200">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="17581-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="17581-201">Edição</span><span class="sxs-lookup"><span data-stu-id="17581-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="17581-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17581-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17581-203">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17581-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-204">Gerenciamento/relatórios</span><span class="sxs-lookup"><span data-stu-id="17581-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="17581-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="17581-206">(Standard, Enterprise, Datacenter ou a edição para desenvolvedores com o seguinte recurso: <strong> Serviços de mecanismo de banco de dados </strong> .)</span><span class="sxs-lookup"><span data-stu-id="17581-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-207">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-208">Gerenciamento/relatórios</span><span class="sxs-lookup"><span data-stu-id="17581-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="17581-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="17581-210">(Standard, Enterprise, Datacenter ou a edição para desenvolvedores com o seguinte recurso: <strong> Serviços de mecanismo de banco de dados </strong> .)</span><span class="sxs-lookup"><span data-stu-id="17581-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-211">R2</span><span class="sxs-lookup"><span data-stu-id="17581-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-212">SP2</span><span class="sxs-lookup"><span data-stu-id="17581-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-213">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-214">Gerenciamento/relatórios</span><span class="sxs-lookup"><span data-stu-id="17581-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-215">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="17581-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="17581-216">(Standard, Enterprise, Datacenter ou a edição para desenvolvedores com o seguinte recurso: <strong> Serviços de mecanismo de banco de dados </strong> .)</span><span class="sxs-lookup"><span data-stu-id="17581-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-217">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="17581-218">Requisitos do sistema do cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="17581-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="17581-219">A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="17581-220">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-220">Note</span></span>**  
<span data-ttu-id="17581-221">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17581-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17581-222">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17581-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17581-223">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17581-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17581-224">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17581-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17581-225">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17581-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17581-226">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17581-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="17581-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-228">SP1</span><span class="sxs-lookup"><span data-stu-id="17581-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-229">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="17581-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-231">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="17581-232">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-232">Important</span></span></strong><br/><p><span data-ttu-id="17581-233">O Windows 8,1 só tem suporte do App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="17581-234">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="17581-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-235">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="17581-236">Não há suporte para os seguintes cenários de instalação do cliente do App-V, exceto conforme observado:</span><span class="sxs-lookup"><span data-stu-id="17581-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="17581-237">Computadores que executam o Windows Server</span><span class="sxs-lookup"><span data-stu-id="17581-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="17581-238">Computadores que executam o App-V 4,6 SP1 ou versões anteriores</span><span class="sxs-lookup"><span data-stu-id="17581-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="17581-239">O cliente de serviços de área de trabalho remota do App-V 5,0 tem suporte apenas para servidores habilitados para RDS</span><span class="sxs-lookup"><span data-stu-id="17581-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="17581-240">Requisitos de hardware do cliente</span><span class="sxs-lookup"><span data-stu-id="17581-240">Client hardware requirements</span></span>

<span data-ttu-id="17581-241">A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="17581-242">Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="17581-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="17581-243">RAM – 1 GB (32 bits) ou 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="17581-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="17581-244">Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="17581-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="17581-245">Requisitos do sistema do cliente de área de trabalho remota do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="17581-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="17581-246">A tabela a seguir lista os sistemas operacionais com suporte para a instalação de cliente de área de trabalho remota do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="17581-247">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-247">Note</span></span>**  
<span data-ttu-id="17581-248">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17581-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17581-249">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17581-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17581-250">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17581-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="17581-251">Service Pack da edição do sistema operacional Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17581-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="17581-252">R2</span><span class="sxs-lookup"><span data-stu-id="17581-252">R2</span></span>

<span data-ttu-id="17581-253">SP1</span><span class="sxs-lookup"><span data-stu-id="17581-253">SP1</span></span>

<span data-ttu-id="17581-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17581-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="17581-255">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-255">Important</span></span>**  
<span data-ttu-id="17581-256">O Windows Server 2012 R2 só tem suporte do App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="17581-257">Microsoft Windows Server 2012 (padrão, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="17581-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="17581-258">R2</span><span class="sxs-lookup"><span data-stu-id="17581-258">R2</span></span>

<span data-ttu-id="17581-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="17581-260">Requisitos de hardware do cliente da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="17581-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="17581-261">A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="17581-262">Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="17581-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="17581-263">RAM – 1 GB (32 bits) ou 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="17581-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="17581-264">Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="17581-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="17581-265">Requisitos do sistema do App-V 5,0 Sequencer</span><span class="sxs-lookup"><span data-stu-id="17581-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="17581-266">A tabela a seguir lista os sistemas operacionais suportados para a instalação do sequenciador do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="17581-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="17581-267">Observação</span><span class="sxs-lookup"><span data-stu-id="17581-267">Note</span></span>**  
<span data-ttu-id="17581-268">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17581-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="17581-269">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="17581-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="17581-270">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="17581-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17581-271">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="17581-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="17581-272">Edição</span><span class="sxs-lookup"><span data-stu-id="17581-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="17581-273">Service Pack</span><span class="sxs-lookup"><span data-stu-id="17581-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="17581-274">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="17581-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="17581-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-276">SP1</span><span class="sxs-lookup"><span data-stu-id="17581-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-277">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="17581-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-279">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="17581-280">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-280">Important</span></span></strong><br/><p><span data-ttu-id="17581-281">O Windows 8,1 só tem suporte do App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="17581-282">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="17581-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-283">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17581-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-285">R2</span><span class="sxs-lookup"><span data-stu-id="17581-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-286">SP1</span><span class="sxs-lookup"><span data-stu-id="17581-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-287">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17581-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="17581-289">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="17581-290">Importante</span><span class="sxs-lookup"><span data-stu-id="17581-290">Important</span></span></strong><br/><p><span data-ttu-id="17581-291">O Windows Server 2012 R2 só tem suporte do App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="17581-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17581-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="17581-293">R2</span><span class="sxs-lookup"><span data-stu-id="17581-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="17581-294">64 bits</span><span class="sxs-lookup"><span data-stu-id="17581-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="17581-295">Versões com suporte do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="17581-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="17581-296">Você pode usar o Gerenciador de configuração do Microsoft System Center 2012 ou o Gerenciador de configuração do System Center 2012 R2 para gerenciar aplicativos virtuais do App-V, relatórios e outras funções.</span><span class="sxs-lookup"><span data-stu-id="17581-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="17581-297">A tabela a seguir lista as versões com suporte do Configuration Manager para cada versão aplicável do App-V.</span><span class="sxs-lookup"><span data-stu-id="17581-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17581-298">Versão do Configuration Manager compatível</span><span class="sxs-lookup"><span data-stu-id="17581-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="17581-299">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="17581-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17581-300">Gerenciador de configuração do Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="17581-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="17581-301">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="17581-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="17581-302">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="17581-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="17581-303">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17581-304">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="17581-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="17581-305">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="17581-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="17581-306">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="17581-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="17581-307">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="17581-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="17581-308">Para obter mais informações sobre como o Configuration Manager integra-se ao App-V, consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="17581-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="17581-309">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17581-309">Related topics</span></span>


[<span data-ttu-id="17581-310">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="17581-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="17581-311">Pré-requisitos do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="17581-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









