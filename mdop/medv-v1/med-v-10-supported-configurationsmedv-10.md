---
title: Configurações com suporte no MED-V 1.0
description: Configurações com suporte no MED-V 1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796042"
---
# <span data-ttu-id="87f23-103">Configurações com suporte no MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="87f23-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="87f23-104">Este tópico especifica os requisitos necessários para instalar e executar o Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="87f23-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="87f23-105">Requisitos do sistema do cliente do MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="87f23-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="87f23-106">Requisitos do sistema operacional do cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="87f23-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="87f23-107">A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="87f23-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87f23-108">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="87f23-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="87f23-109">Edição</span><span class="sxs-lookup"><span data-stu-id="87f23-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="87f23-110">Service Pack</span><span class="sxs-lookup"><span data-stu-id="87f23-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="87f23-111">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="87f23-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87f23-112">Windows XP</span><span class="sxs-lookup"><span data-stu-id="87f23-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-113">Edição Professional</span><span class="sxs-lookup"><span data-stu-id="87f23-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-114">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="87f23-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-115">x86</span><span class="sxs-lookup"><span data-stu-id="87f23-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87f23-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87f23-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-117">Business, Enterprise ou Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="87f23-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-118">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="87f23-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-119">x86</span><span class="sxs-lookup"><span data-stu-id="87f23-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="87f23-120">Observação</span><span class="sxs-lookup"><span data-stu-id="87f23-120">Note</span></span>**  
<span data-ttu-id="87f23-121">O cliente MED-V não é executado no modo x64 nativo.</span><span class="sxs-lookup"><span data-stu-id="87f23-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="87f23-122">Em vez disso, o MED-V funciona no modo WOW64 (Windows 64-bit) em computadores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="87f23-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="87f23-123">Configuração do cliente do MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="87f23-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="87f23-124">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="87f23-124">.NET Framework Version</span></span>**

<span data-ttu-id="87f23-125">As seguintes versões do Microsoft .NET Framework têm suporte para a instalação do cliente do MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="87f23-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="87f23-126">.NET Framework 2,0 ou .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="87f23-127">.NET Framework 3,0 ou .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="87f23-128">.NET Framework 3,5 ou .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="87f23-129">Mecanismo de virtualização</span><span class="sxs-lookup"><span data-stu-id="87f23-129">Virtualization Engine</span></span>**

<span data-ttu-id="87f23-130">O Microsoft Virtual PC 2007 SP1 com o hotfix descrito no artigo 974918 da base de dados de conhecimento Microsoft tem suporte para a instalação do cliente MED-V 1,0 nas seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="87f23-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="87f23-131">Arquivo de disco rígido virtual estático (VHD)</span><span class="sxs-lookup"><span data-stu-id="87f23-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="87f23-132">Vários arquivos VHD localizados no mesmo diretório</span><span class="sxs-lookup"><span data-stu-id="87f23-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="87f23-133">Arquivo VHD dinâmico</span><span class="sxs-lookup"><span data-stu-id="87f23-133">Dynamic VHD file</span></span>

**<span data-ttu-id="87f23-134">Navegador da Internet</span><span class="sxs-lookup"><span data-stu-id="87f23-134">Internet Browser</span></span>**

<span data-ttu-id="87f23-135">O Windows Internet Explorer 7 e o Windows Internet Explorer 8 têm suporte para a instalação do cliente do MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="87f23-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="87f23-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="87f23-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="87f23-137">O cliente MED-V não é compatível com um ambiente do Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="87f23-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="87f23-138">Requisitos do sistema do espaço de trabalho do MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="87f23-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="87f23-139">Requisitos do sistema operacional do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="87f23-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="87f23-140">A tabela a seguir lista os sistemas operacionais suportados para os espaços de trabalho do MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="87f23-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87f23-141">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="87f23-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="87f23-142">Edição</span><span class="sxs-lookup"><span data-stu-id="87f23-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="87f23-143">Service Pack</span><span class="sxs-lookup"><span data-stu-id="87f23-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="87f23-144">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="87f23-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87f23-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="87f23-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-146">Professional</span><span class="sxs-lookup"><span data-stu-id="87f23-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-147">4</span><span class="sxs-lookup"><span data-stu-id="87f23-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-148">X86</span><span class="sxs-lookup"><span data-stu-id="87f23-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87f23-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="87f23-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-150">Edição Professional</span><span class="sxs-lookup"><span data-stu-id="87f23-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-151">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="87f23-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87f23-152">Observação</span><span class="sxs-lookup"><span data-stu-id="87f23-152">Note</span></span></strong><br/><p><span data-ttu-id="87f23-153">O SP3 é recomendado para garantir que o espaço de trabalho do MED-V seja compatível com futuras versões do MED-V.</span><span class="sxs-lookup"><span data-stu-id="87f23-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="87f23-154">x86</span><span class="sxs-lookup"><span data-stu-id="87f23-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="87f23-155">Configuração do espaço de trabalho do MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="87f23-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="87f23-156">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="87f23-156">.NET Framework Version</span></span>**

<span data-ttu-id="87f23-157">O MED-V requer uma das seguintes versões compatíveis do Microsoft .NET Framework para a instalação do espaço de trabalho do MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="87f23-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="87f23-158">.NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="87f23-159">.NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="87f23-160">.NET Framework 3,5 ou .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="87f23-161">Observação</span><span class="sxs-lookup"><span data-stu-id="87f23-161">Note</span></span>**  
<span data-ttu-id="87f23-162">O .NET Framework 3,5 SP1 é recomendado para garantir que o espaço de trabalho do MED-V seja compatível com futuras versões do MED-V.</span><span class="sxs-lookup"><span data-stu-id="87f23-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="87f23-163">Navegador da Internet</span><span class="sxs-lookup"><span data-stu-id="87f23-163">Internet Browser</span></span>**

<span data-ttu-id="87f23-164">O Windows Internet Explorer 6 SP2 e o Windows Internet Explorer 7 têm suporte para a instalação do espaço de trabalho do MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="87f23-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="87f23-165">Imagens do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="87f23-165">MED-V Workspace Images</span></span>

<span data-ttu-id="87f23-166">As imagens do espaço de trabalho do MED-V devem ser criadas usando o Virtual PC 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="87f23-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="87f23-167">Requisitos do sistema do MED-V 1,0 Server</span><span class="sxs-lookup"><span data-stu-id="87f23-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="87f23-168">Requisitos do sistema operacional do MED-V 1,0 Server</span><span class="sxs-lookup"><span data-stu-id="87f23-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="87f23-169">A tabela a seguir lista os sistemas operacionais com suporte para instalações do servidor MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="87f23-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87f23-170">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="87f23-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="87f23-171">Edição</span><span class="sxs-lookup"><span data-stu-id="87f23-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="87f23-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="87f23-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="87f23-173">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="87f23-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87f23-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87f23-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-175">Standard ou Enterprise</span><span class="sxs-lookup"><span data-stu-id="87f23-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-176">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="87f23-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-177">X86 ou x64</span><span class="sxs-lookup"><span data-stu-id="87f23-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="87f23-178">Configuração do servidor do MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="87f23-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="87f23-179">Versão do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="87f23-179">.NET Framework Version</span></span>**

<span data-ttu-id="87f23-180">O MED-V requer uma das seguintes versões compatíveis do Microsoft .NET Framework para a instalação do espaço de trabalho do MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="87f23-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="87f23-181">.NET Framework 2,0 ou .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="87f23-182">.NET Framework 3,0 ou .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="87f23-183">.NET Framework 3,5 ou .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="87f23-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="87f23-184">Microsoft SQL Server versão</span><span class="sxs-lookup"><span data-stu-id="87f23-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="87f23-185">As seguintes versões do Microsoft SQL Server são compatíveis com o MED-V 1,0 quando o SQL Server é instalado localmente ou remotamente do servidor MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="87f23-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87f23-186">Versão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="87f23-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="87f23-187">Edição</span><span class="sxs-lookup"><span data-stu-id="87f23-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="87f23-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="87f23-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="87f23-189">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="87f23-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87f23-190">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="87f23-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-191">Edição expressa, padrão ou Enterprise</span><span class="sxs-lookup"><span data-stu-id="87f23-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-192">SP2</span><span class="sxs-lookup"><span data-stu-id="87f23-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-193">X86 ou x64</span><span class="sxs-lookup"><span data-stu-id="87f23-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87f23-194">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="87f23-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-195">Express, Standard ou Enterprise</span><span class="sxs-lookup"><span data-stu-id="87f23-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-196">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="87f23-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="87f23-197">X86 ou x64</span><span class="sxs-lookup"><span data-stu-id="87f23-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="87f23-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="87f23-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="87f23-199">O servidor MED-V é compatível com um ambiente do Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="87f23-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="87f23-200">Informações de globalização do MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="87f23-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="87f23-201">Embora o MED-V não seja liberado em idiomas diferentes do inglês, as seguintes versões do idioma do sistema operacional Windows são suportadas para as instalações do cliente, do espaço de trabalho e do cliente do MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="87f23-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="87f23-202">Inglês</span><span class="sxs-lookup"><span data-stu-id="87f23-202">English</span></span>

-   <span data-ttu-id="87f23-203">Francês</span><span class="sxs-lookup"><span data-stu-id="87f23-203">French</span></span>

-   <span data-ttu-id="87f23-204">Alemão</span><span class="sxs-lookup"><span data-stu-id="87f23-204">German</span></span>

-   <span data-ttu-id="87f23-205">Italiano</span><span class="sxs-lookup"><span data-stu-id="87f23-205">Italian</span></span>

-   <span data-ttu-id="87f23-206">Espanhol</span><span class="sxs-lookup"><span data-stu-id="87f23-206">Spanish</span></span>

-   <span data-ttu-id="87f23-207">Português (Brasil)</span><span class="sxs-lookup"><span data-stu-id="87f23-207">Portuguese (Brazil)</span></span>









