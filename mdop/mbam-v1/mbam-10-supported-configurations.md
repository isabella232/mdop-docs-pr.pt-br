---
title: Configurações com suporte no MBAM 1.0
description: Configurações com suporte no MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799772"
---
# <span data-ttu-id="13712-103">Configurações com suporte no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="13712-103">MBAM 1.0 Supported Configurations</span></span>


<span data-ttu-id="13712-104">Este tópico especifica os requisitos necessários para instalar e executar o Microsoft BitLocker Administration and Monitoring (MBAM) em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="13712-104">This topic specifies the necessary requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) in your environment.</span></span>

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="13712-105">Requisitos do sistema do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="13712-105">MBAM server system Requirements</span></span>


### <span data-ttu-id="13712-106">Requisitos do sistema operacional do servidor</span><span class="sxs-lookup"><span data-stu-id="13712-106">Server operating system requirements</span></span>

<span data-ttu-id="13712-107">A tabela a seguir lista os sistemas operacionais suportados para a instalação do Microsoft BitLocker Administration and Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="13712-107">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

**<span data-ttu-id="13712-108">Observação</span><span class="sxs-lookup"><span data-stu-id="13712-108">Note</span></span>**  
<span data-ttu-id="13712-109">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="13712-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="13712-110">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="13712-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="13712-111">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="13712-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13712-112">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="13712-112">Operating System</span></span></th>
<th align="left"><span data-ttu-id="13712-113">Edição</span><span class="sxs-lookup"><span data-stu-id="13712-113">Edition</span></span></th>
<th align="left"><span data-ttu-id="13712-114">Service Pack</span><span class="sxs-lookup"><span data-stu-id="13712-114">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="13712-115">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="13712-115">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13712-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13712-116">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-117">Standard, Enterprise, Datacenter ou servidor Web</span><span class="sxs-lookup"><span data-stu-id="13712-117">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-118">SP2 somente</span><span class="sxs-lookup"><span data-stu-id="13712-118">SP2 only</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-119">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-119">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13712-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13712-120">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-121">Standard, Enterprise, Datacenter ou servidor Web</span><span class="sxs-lookup"><span data-stu-id="13712-121">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="13712-122">64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-122">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="13712-123">Aviso</span><span class="sxs-lookup"><span data-stu-id="13712-123">Warning</span></span>**  
<span data-ttu-id="13712-124">Não há suporte para a instalação de serviços, relatórios ou bancos de dados do MBAM em um computador controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="13712-124">There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>



### <a href="" id="server-random-access-memory--ram--requirements-"></a><span data-ttu-id="13712-125">Requisitos de memória de acesso randômico (RAM) do servidor</span><span class="sxs-lookup"><span data-stu-id="13712-125">Server random access memory (RAM) requirements</span></span>

<span data-ttu-id="13712-126">Não há nenhuma necessidade de RAM específica para a instalação do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="13712-126">There are no RAM requirements that are specific to MBAM Server installation.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="13712-127">Requisitos de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="13712-127">SQL Server Database requirements</span></span>

<span data-ttu-id="13712-128">A tabela a seguir lista as versões do SQL Server com suporte para a instalação do recurso MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="13712-128">The following table lists the SQL Server versions that are supported for the MBAM Server feature installation.</span></span>

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
<th align="left"><span data-ttu-id="13712-129">Recurso do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="13712-129">MBAM Server Feature</span></span></th>
<th align="left"><span data-ttu-id="13712-130">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="13712-130">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="13712-131">Edição</span><span class="sxs-lookup"><span data-stu-id="13712-131">Edition</span></span></th>
<th align="left"><span data-ttu-id="13712-132">Service Pack</span><span class="sxs-lookup"><span data-stu-id="13712-132">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="13712-133">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="13712-133">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13712-134">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="13712-134">Compliance and Audit Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-135">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="13712-135">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="13712-136">R2, Standard, Enterprise, Datacenter ou edição para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="13712-136">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-137">SP2</span><span class="sxs-lookup"><span data-stu-id="13712-137">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-138">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-138">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13712-139">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="13712-139">Recovery and Hardware Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-140">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="13712-140">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="13712-141">R2, Enterprise, Datacenter ou edição para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="13712-141">R2, Enterprise, Datacenter, or Developer Edition</span></span></p>
<div class="alert">
<strong><span data-ttu-id="13712-142">Importante</span><span class="sxs-lookup"><span data-stu-id="13712-142">Important</span></span></strong><br/><p><span data-ttu-id="13712-143">Não há suporte para as edições padrão do SQL Server para a recuperação de MBAM e instalação de recursos do servidor de banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="13712-143">SQL Server Standard Editions are not supported for MBAM Recovery and Hardware Database Server feature installation.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="13712-144">SP2</span><span class="sxs-lookup"><span data-stu-id="13712-144">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-145">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13712-146">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="13712-146">Compliance and Audit Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-147">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="13712-147">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="13712-148">R2, Standard, Enterprise, Datacenter ou edição para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="13712-148">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-149">SP2</span><span class="sxs-lookup"><span data-stu-id="13712-149">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-150">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-150">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="13712-151">Requisitos do sistema do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="13712-151">MBAM Client system requirements</span></span>


### <span data-ttu-id="13712-152">Requisitos do sistema operacional do cliente</span><span class="sxs-lookup"><span data-stu-id="13712-152">Client operating system requirements</span></span>

<span data-ttu-id="13712-153">A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="13712-153">The following table lists the operating systems that are supported for MBAM Client installation.</span></span>

**<span data-ttu-id="13712-154">Observação</span><span class="sxs-lookup"><span data-stu-id="13712-154">Note</span></span>**  
<span data-ttu-id="13712-155">A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="13712-155">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="13712-156">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="13712-156">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="13712-157">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="13712-157">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13712-158">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="13712-158">Operating System</span></span></th>
<th align="left"><span data-ttu-id="13712-159">Edição</span><span class="sxs-lookup"><span data-stu-id="13712-159">Edition</span></span></th>
<th align="left"><span data-ttu-id="13712-160">Service Pack</span><span class="sxs-lookup"><span data-stu-id="13712-160">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="13712-161">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="13712-161">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13712-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13712-162">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-163">Edição Enterprise</span><span class="sxs-lookup"><span data-stu-id="13712-163">Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-164">Nenhum, SP1</span><span class="sxs-lookup"><span data-stu-id="13712-164">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-165">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-165">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13712-166">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13712-166">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-167">Última edição</span><span class="sxs-lookup"><span data-stu-id="13712-167">Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-168">Nenhum, SP1</span><span class="sxs-lookup"><span data-stu-id="13712-168">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13712-169">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="13712-169">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="13712-170">Requisitos de RAM do cliente</span><span class="sxs-lookup"><span data-stu-id="13712-170">Client RAM requirements</span></span>

<span data-ttu-id="13712-171">Não há requisitos de RAM específicos para a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="13712-171">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <span data-ttu-id="13712-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13712-172">Related topics</span></span>


[<span data-ttu-id="13712-173">Planejar a implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="13712-173">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="13712-174">Pré-requisitos para implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="13712-174">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)









