---
title: Configurações com suporte ao App-V 5.1
description: Configurações com suporte ao App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796571"
---
# <span data-ttu-id="4dae7-103">Configurações com suporte ao App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4dae7-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="4dae7-104">Aplica-se a: Windows 10, versão 1607; Servidor de janelas 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (atualização de segurança estendida)</span><span class="sxs-lookup"><span data-stu-id="4dae7-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="4dae7-105">Este tópico especifica os requisitos para instalar e executar o Microsoft Application Virtualization (App-V) 5,1 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="4dae7-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="4dae7-106">Requisitos do sistema do App-V Server</span><span class="sxs-lookup"><span data-stu-id="4dae7-106">App-V Server system requirements</span></span>

<span data-ttu-id="4dae7-107">Esta seção lista os requisitos de sistema operacional e de hardware para todos os componentes do App-V Server.</span><span class="sxs-lookup"><span data-stu-id="4dae7-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="4dae7-108">Cenários de servidor sem suporte do 5,1 do App-V</span><span class="sxs-lookup"><span data-stu-id="4dae7-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="4dae7-109">O servidor do App-V 5,1 não é compatível com os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="4dae7-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="4dae7-110">Implantação em um computador que executa o Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="4dae7-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="4dae7-111">Implantação em um computador que executa uma versão anterior dos componentes do App-V 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="4dae7-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="4dae7-112">Você pode instalar o App-V 5,1 lado a lado com o servidor do App-V 4.5 Lightweight Streaming Server (LWS) apenas.</span><span class="sxs-lookup"><span data-stu-id="4dae7-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="4dae7-113">A implantação do App-V lado a lado com o serviço de gerenciamento de virtualização do aplicativo (HWS) do App-V 4,5 não é suportada.</span><span class="sxs-lookup"><span data-stu-id="4dae7-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="4dae7-114">Implantação em um computador que executa o Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="4dae7-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="4dae7-115">Implantação em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="4dae7-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="4dae7-116">Caminhos curtos.</span><span class="sxs-lookup"><span data-stu-id="4dae7-116">Short paths.</span></span> <span data-ttu-id="4dae7-117">Se você pretende usar um caminho curto, deve criar um novo volume.</span><span class="sxs-lookup"><span data-stu-id="4dae7-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="4dae7-118">Requisitos do sistema operacional do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4dae7-118">Management server operating system requirements</span></span>

<span data-ttu-id="4dae7-119">A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="4dae7-120">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="4dae7-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="4dae7-121">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="4dae7-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="4dae7-122">Consulte [perguntas frequentes sobre política de suporte do ciclo de vida do suporte Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="4dae7-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="4dae7-123">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4dae7-123">Operating System</span></span>                 | <span data-ttu-id="4dae7-124">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-124">Service Pack</span></span> | <span data-ttu-id="4dae7-125">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="4dae7-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="4dae7-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="4dae7-127">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-127">64-bit</span></span>       |
| <span data-ttu-id="4dae7-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="4dae7-129">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-129">64-bit</span></span>       |
| <span data-ttu-id="4dae7-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="4dae7-131">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-131">64-bit</span></span>       |
| <span data-ttu-id="4dae7-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="4dae7-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-133">64-bit</span></span>       |
| <span data-ttu-id="4dae7-134">[Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="4dae7-135">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-135">SP1</span></span>     |        <span data-ttu-id="4dae7-136">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-136">64-bit</span></span>       |
 

<span data-ttu-id="4dae7-137">**Importante**  Não há suporte para a implantação da função de servidor de gerenciamento em um computador com o compartilhamento de área de trabalho remota (RDS) habilitada.</span><span class="sxs-lookup"><span data-stu-id="4dae7-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="4dae7-138">Requisitos de hardware do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4dae7-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="4dae7-139">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="4dae7-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="4dae7-140">RAM — 1 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="4dae7-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="4dae7-141">Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo</span><span class="sxs-lookup"><span data-stu-id="4dae7-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="4dae7-142">Requisitos de banco de dados do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4dae7-142">Management server database requirements</span></span>

<span data-ttu-id="4dae7-143">A tabela a seguir lista as versões do SQL Server que têm suporte para a instalação do banco de dados de gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4dae7-144">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4dae7-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="4dae7-145">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="4dae7-146">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="4dae7-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="4dae7-148">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="4dae7-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="4dae7-150">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-151">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-152">SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-153">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-154">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="4dae7-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-155">SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-156">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-157">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-158">SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-159">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-161">SP3</span><span class="sxs-lookup"><span data-stu-id="4dae7-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-162">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4dae7-163">Para obter mais informações sobre arquivos de configuração do usuário com o SQL Server 2016 ou posterior, consulte o [artigo de suporte](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span><span class="sxs-lookup"><span data-stu-id="4dae7-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="4dae7-164">Requisitos do sistema operacional do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="4dae7-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="4dae7-165">A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de publicação do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="4dae7-166">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4dae7-166">Operating System</span></span>                 | <span data-ttu-id="4dae7-167">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-167">Service Pack</span></span> | <span data-ttu-id="4dae7-168">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="4dae7-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="4dae7-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="4dae7-170">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-170">64-bit</span></span>       |
| <span data-ttu-id="4dae7-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="4dae7-172">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-172">64-bit</span></span>       |
| <span data-ttu-id="4dae7-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="4dae7-174">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-174">64-bit</span></span>       |
| <span data-ttu-id="4dae7-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="4dae7-176">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-176">64-bit</span></span>       |
| <span data-ttu-id="4dae7-177">[Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="4dae7-178">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-178">SP1</span></span>     |        <span data-ttu-id="4dae7-179">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="4dae7-180">Requisitos de hardware do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="4dae7-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="4dae7-181">O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4dae7-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="4dae7-182">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="4dae7-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="4dae7-183">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="4dae7-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="4dae7-184">Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo</span><span class="sxs-lookup"><span data-stu-id="4dae7-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="4dae7-185">Requisitos do sistema operacional do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="4dae7-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="4dae7-186">A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,1 Reporting Server.</span><span class="sxs-lookup"><span data-stu-id="4dae7-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="4dae7-187">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4dae7-187">Operating System</span></span>                 | <span data-ttu-id="4dae7-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-188">Service Pack</span></span> | <span data-ttu-id="4dae7-189">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="4dae7-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="4dae7-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="4dae7-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-191">64-bit</span></span>       |
| <span data-ttu-id="4dae7-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="4dae7-193">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-193">64-bit</span></span>       |
| <span data-ttu-id="4dae7-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="4dae7-195">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-195">64-bit</span></span>       |
| <span data-ttu-id="4dae7-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="4dae7-197">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-197">64-bit</span></span>       |
| <span data-ttu-id="4dae7-198">[Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="4dae7-199">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-199">SP1</span></span>     |        <span data-ttu-id="4dae7-200">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="4dae7-201">Requisitos de hardware do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="4dae7-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="4dae7-202">O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4dae7-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="4dae7-203">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="4dae7-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="4dae7-204">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="4dae7-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="4dae7-205">Espaço em disco — 200 MB de espaço disponível no disco rígido</span><span class="sxs-lookup"><span data-stu-id="4dae7-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="4dae7-206">Requisitos de banco de dados do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="4dae7-206">Reporting server database requirements</span></span>

<span data-ttu-id="4dae7-207">A tabela a seguir lista as versões do SQL Server que têm suporte para a instalação do banco de dados de relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4dae7-208">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4dae7-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="4dae7-209">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="4dae7-210">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="4dae7-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="4dae7-212">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-213">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-214">SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-215">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-216">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="4dae7-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-217">SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-218">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-219">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-220">SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-221">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-223">SP3</span><span class="sxs-lookup"><span data-stu-id="4dae7-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-224">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="4dae7-225">Requisitos do sistema do cliente App-V</span><span class="sxs-lookup"><span data-stu-id="4dae7-225">App-V client system requirements</span></span>

<span data-ttu-id="4dae7-226">A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="4dae7-227">Com a versão de aniversário do Windows 10 (aka versão 1607), o cliente App-V está em uma caixa e bloqueará a instalação de qualquer versão anterior do cliente App-V</span><span class="sxs-lookup"><span data-stu-id="4dae7-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4dae7-228">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4dae7-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="4dae7-229">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="4dae7-230">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-231">Microsoft Windows10 (versão anterior ao 1607)</span><span class="sxs-lookup"><span data-stu-id="4dae7-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="4dae7-232">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4dae7-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="4dae7-234">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-235">7</span><span class="sxs-lookup"><span data-stu-id="4dae7-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-236">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-237">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4dae7-238">Não há suporte para os seguintes cenários de instalação do cliente do App-V, exceto conforme observado:</span><span class="sxs-lookup"><span data-stu-id="4dae7-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="4dae7-239">Computadores que executam o Windows Server</span><span class="sxs-lookup"><span data-stu-id="4dae7-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="4dae7-240">Computadores que executam o App-V 4.6 SP1 ou versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4dae7-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="4dae7-241">O cliente de serviços de área de trabalho remota do App-V 5,1 tem suporte apenas para servidores habilitados para RDS</span><span class="sxs-lookup"><span data-stu-id="4dae7-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="4dae7-242">Requisitos de hardware do aplicativo cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="4dae7-242">App-V client hardware requirements</span></span>

<span data-ttu-id="4dae7-243">A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="4dae7-244">Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="4dae7-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="4dae7-245">RAM – 1 GB (32 bits) ou 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="4dae7-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="4dae7-246">Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="4dae7-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="4dae7-247">Requisitos do sistema do cliente dos serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="4dae7-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="4dae7-248">A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,1 Remote Desktop Services (RDS).</span><span class="sxs-lookup"><span data-stu-id="4dae7-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="4dae7-249">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4dae7-249">Operating System</span></span>                 | <span data-ttu-id="4dae7-250">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-250">Service Pack</span></span> | <span data-ttu-id="4dae7-251">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="4dae7-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="4dae7-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="4dae7-253">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-253">64-bit</span></span>       |
| <span data-ttu-id="4dae7-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="4dae7-255">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-255">64-bit</span></span>       |
| <span data-ttu-id="4dae7-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="4dae7-257">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-257">64-bit</span></span>       |
| <span data-ttu-id="4dae7-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="4dae7-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-259">64-bit</span></span>       |
| <span data-ttu-id="4dae7-260">[Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="4dae7-261">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-261">SP1</span></span>     |        <span data-ttu-id="4dae7-262">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-262">64-bit</span></span>       |

### <span data-ttu-id="4dae7-263">Requisitos de hardware do cliente dos serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="4dae7-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="4dae7-264">O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4dae7-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="4dae7-265">Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="4dae7-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="4dae7-266">RAM – 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="4dae7-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="4dae7-267">Espaço em disco — 200 MB de espaço disponível no disco rígido</span><span class="sxs-lookup"><span data-stu-id="4dae7-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="4dae7-268">Requisitos do sistema do sequenciador</span><span class="sxs-lookup"><span data-stu-id="4dae7-268">Sequencer system requirements</span></span>

<span data-ttu-id="4dae7-269">A tabela a seguir lista os sistemas operacionais suportados para a instalação do sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4dae7-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="4dae7-270">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4dae7-270">Operating System</span></span>                 | <span data-ttu-id="4dae7-271">Service Pack</span><span class="sxs-lookup"><span data-stu-id="4dae7-271">Service Pack</span></span> | <span data-ttu-id="4dae7-272">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="4dae7-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="4dae7-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="4dae7-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="4dae7-274">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-274">64-bit</span></span>       |
| <span data-ttu-id="4dae7-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4dae7-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="4dae7-276">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-276">64-bit</span></span>       |
| <span data-ttu-id="4dae7-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="4dae7-278">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-278">64-bit</span></span>       |
| <span data-ttu-id="4dae7-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dae7-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="4dae7-280">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-280">64-bit</span></span>       |
| <span data-ttu-id="4dae7-281">[Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dae7-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="4dae7-282">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-282">SP1</span></span>     |        <span data-ttu-id="4dae7-283">64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-283">64-bit</span></span>       |
| <span data-ttu-id="4dae7-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="4dae7-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="4dae7-285">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="4dae7-286">Microsoft Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="4dae7-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="4dae7-287">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="4dae7-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="4dae7-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="4dae7-289">SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-289">SP1</span></span>     | <span data-ttu-id="4dae7-290">32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="4dae7-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="4dae7-291">Requisitos de hardware do sequenciador</span><span class="sxs-lookup"><span data-stu-id="4dae7-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="4dae7-292">Consulte a documentação do Windows ou Windows Server para saber quais são os requisitos de hardware.</span><span class="sxs-lookup"><span data-stu-id="4dae7-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="4dae7-293">O App-V adiciona nenhum requisito de hardware adicional.</span><span class="sxs-lookup"><span data-stu-id="4dae7-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="4dae7-294">Versões com suporte do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4dae7-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="4dae7-295">O cliente App-V dá suporte às seguintes versões do System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="4dae7-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="4dae7-296">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="4dae7-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="4dae7-297">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4dae7-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="4dae7-298">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="4dae7-299">A seguinte matriz de versão do App-V e do System Center Configuration Manager mostra todas as combinações suportadas oficialmente do App-V e do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4dae7-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="4dae7-300">O App-V 4,5 e o 4,6 saíram do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="4dae7-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

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
<th align="left"><span data-ttu-id="4dae7-301">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="4dae7-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="4dae7-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="4dae7-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="4dae7-303">Systems Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4dae7-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="4dae7-304">System Center 2012 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="4dae7-305">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4dae7-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="4dae7-306">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="4dae7-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="4dae7-307">System Center 2012 Configuration Manager SP2</span><span class="sxs-lookup"><span data-stu-id="4dae7-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="4dae7-308">System Center Configuration Manager versão 1511</span><span class="sxs-lookup"><span data-stu-id="4dae7-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4dae7-309">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="4dae7-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-310">MSI-wrapper somente</span><span class="sxs-lookup"><span data-stu-id="4dae7-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-311">Não</span><span class="sxs-lookup"><span data-stu-id="4dae7-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-312">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="4dae7-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="4dae7-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-314">Sim</span><span class="sxs-lookup"><span data-stu-id="4dae7-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-315">Sim</span><span class="sxs-lookup"><span data-stu-id="4dae7-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-316">Sim</span><span class="sxs-lookup"><span data-stu-id="4dae7-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4dae7-317">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4dae7-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-318">MSI-wrapper somente</span><span class="sxs-lookup"><span data-stu-id="4dae7-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-319">Não</span><span class="sxs-lookup"><span data-stu-id="4dae7-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-320">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="4dae7-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="4dae7-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-322">Sim</span><span class="sxs-lookup"><span data-stu-id="4dae7-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-323">Sim</span><span class="sxs-lookup"><span data-stu-id="4dae7-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4dae7-324">Sim</span><span class="sxs-lookup"><span data-stu-id="4dae7-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4dae7-325">Para obter mais informações sobre como o Configuration Manager integra-se ao App-V, consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="4dae7-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="4dae7-326">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4dae7-326">Related topics</span></span>

[<span data-ttu-id="4dae7-327">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="4dae7-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="4dae7-328">Pré-requisitos do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4dae7-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
