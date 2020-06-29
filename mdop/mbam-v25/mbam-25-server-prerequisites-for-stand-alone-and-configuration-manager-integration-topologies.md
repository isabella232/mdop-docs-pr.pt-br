---
title: Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager
description: Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799784"
---
# <span data-ttu-id="aa8b4-103">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="aa8b4-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="aa8b4-104">Antes de iniciar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), você deve concluir os pré-requisitos listados neste tópico.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="aa8b4-105">Esses pré-requisitos se aplicam à topologia autônoma do MBAM e à topologia de integração do System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="aa8b4-106">Se você estiver implantando o MBAM com o System Center Configuration Manager, será necessário concluir pré-requisitos adicionais, listados em [pré-requisitos de servidor MBAM 2,5 que se aplicam somente à topologia de integração do Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="aa8b4-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="aa8b4-107">Para obter uma lista dos hardwares e sistemas operacionais compatíveis com o MBAM, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="aa8b4-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="aa8b4-108">Importante</span><span class="sxs-lookup"><span data-stu-id="aa8b4-108">Important</span></span>**  
<span data-ttu-id="aa8b4-109">Se o BitLocker tiver sido usado sem MBAM, você deverá descriptografar a unidade e limpar o TPM usando TPM. msc.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="aa8b4-110">MBAM não pode apropriar-se do TPM se o computador cliente já estiver criptografado e a senha de proprietário do TPM criada.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="aa8b4-111">Funções e contas MBAM necessárias</span><span class="sxs-lookup"><span data-stu-id="aa8b4-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-112">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-114">Grupos criados nos serviços de domínio Active Directory (AD DS)</span><span class="sxs-lookup"><span data-stu-id="aa8b4-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-115">Consulte <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> planejando os grupos e contas do MBAM 2,5 </a> para obter uma descrição desses grupos e contas.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="aa8b4-116">Pré-requisitos para o banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="aa8b4-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-117">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-119">Versão com suporte do SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-120">Instale o Microsoft SQL Server com SQL_Latin1_General_CP1_CI_AS agrupamento.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="aa8b4-121">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-122">Permissões do SQL Server necessárias</span><span class="sxs-lookup"><span data-stu-id="aa8b4-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-123">Permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-124">Funções do servidor de logon da instância do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-125">dbcreator</span><span class="sxs-lookup"><span data-stu-id="aa8b4-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="aa8b4-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="aa8b4-127">Direitos de instância do SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-128">Criar pastas</span><span class="sxs-lookup"><span data-stu-id="aa8b4-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-129">Publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="aa8b4-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-130">Opcional – Instale o recurso de criptografia de dados transparente (TDE) disponível no SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-131">O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a leis, regulamentos e diretrizes aplicáveis a diversos setores.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="aa8b4-132">Observação</span><span class="sxs-lookup"><span data-stu-id="aa8b4-132">Note</span></span></strong><br/><p><span data-ttu-id="aa8b4-133">O TDE executa a descriptografia em tempo real das informações do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="aa8b4-134">Isso significa que, se você estiver exibindo as informações da chave de recuperação no banco de dados do SQL Server e estiver conectado em uma conta que tenha permissões para o banco de dados, as informações da chave de recuperação serão visíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="aa8b4-135">Para ler mais sobre o TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerações de segurança do MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="aa8b4-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-136">Serviços de mecanismo de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-137">Os serviços de mecanismo de banco de dados do SQL Server devem ser instalados e executados durante a instalação do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-138">Windows PowerShell 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="aa8b4-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-139">O Windows PowerShell não precisa ser instalado no servidor de banco de dados de recuperação se você estiver usando o Windows PowerShell para configurar o banco de dados de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="aa8b4-140">Pré-requisitos para o banco de dados de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="aa8b4-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-141">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-142">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-143">Versão com suporte do SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-144">Instale o SQL Server com SQL_Latin1_General_CP1_CI_AS agrupamento.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="aa8b4-145">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-146">Permissões do SQL Server necessárias</span><span class="sxs-lookup"><span data-stu-id="aa8b4-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-147">Permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-148">Funções do servidor de logon da instância do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-149">dbcreator</span><span class="sxs-lookup"><span data-stu-id="aa8b4-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="aa8b4-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="aa8b4-151">Direitos de instância do SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-152">Criar pastas</span><span class="sxs-lookup"><span data-stu-id="aa8b4-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-153">Publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="aa8b4-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-154">Opcional-instalar o recurso de criptografia de dados transparente (TDE) no SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-155">O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a leis, regulamentos e diretrizes aplicáveis a diversos setores.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="aa8b4-156">O TDE executa a descriptografia em tempo real das informações do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="aa8b4-157">Isso significa que, se você estiver exibindo as informações da chave de recuperação no banco de dados do SQL Server e estiver conectado em uma conta que tenha permissões para o banco de dados, as informações da chave de recuperação serão visíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="aa8b4-158">Para ler mais sobre o TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerações de segurança do MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="aa8b4-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-159">Serviços de mecanismo de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-160">Os serviços de mecanismo de banco de dados do SQL Server devem ser instalados e executados durante a instalação do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="aa8b4-161">No entanto, o SQL Server pode ser executado remotamente; Não precisa estar no mesmo servidor em que você está instalando o software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-162">Windows PowerShell 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="aa8b4-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-163">O Windows PowerShell não precisa ser instalado no servidor de banco de dados de conformidade e auditoria se você estiver usando o Windows PowerShell para configurar o banco de dados de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="aa8b4-164">Pré-requisitos dos relatórios</span><span class="sxs-lookup"><span data-stu-id="aa8b4-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-165">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-166">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-167">Versão com suporte do SQL Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-168">Instale o SQL Server com SQL_Latin1_General_CP1_CI_AS agrupamento.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="aa8b4-169">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-170">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="aa8b4-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-171">O SSRS deve ser instalado e executado durante a instalação do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="aa8b4-172">Configurar o SSRS &quot; no &quot; modo nativo e não no modo não configurado ou &quot; SharePoint &quot; .</span><span class="sxs-lookup"><span data-stu-id="aa8b4-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-173">Direitos de instância do SSRS – necessários para configurar relatórios apenas se você estiver instalando bancos de dados em um servidor separado do servidor em que os relatórios estiverem configurados.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-174">Direitos de instância obrigatórios:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="aa8b4-175">Criar pastas</span><span class="sxs-lookup"><span data-stu-id="aa8b4-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-176">Publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="aa8b4-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-177">Windows PowerShell 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="aa8b4-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-178">O Windows PowerShell não precisa ser instalado neste servidor de banco de dados se você estiver usando o Windows PowerShell para configurar o banco de dados de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="aa8b4-179">Pré-requisitos para o servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="aa8b4-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="aa8b4-180">A tabela a seguir lista os pré-requisitos de instalação do MBAM Administration and Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-181">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-182">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-183">Função de servidor Web do Windows Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-184">Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o recurso de servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-185">Ferramentas de gerenciamento do servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="aa8b4-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-186">Clique em <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="aa8b4-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aa8b4-187">Certificado SSL</span><span class="sxs-lookup"><span data-stu-id="aa8b4-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-188">Opcional.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-188">Optional.</span></span> <span data-ttu-id="aa8b4-189">Para proteger a comunicação entre os computadores cliente e os serviços Web, você deve obter e instalar um certificado assinado por uma autoridade de segurança confiável.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-190">Serviços de função de servidor Web</span><span class="sxs-lookup"><span data-stu-id="aa8b4-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="aa8b4-191">Recursos comuns de HTTP:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="aa8b4-192">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="aa8b4-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-193">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="aa8b4-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="aa8b4-194">Desenvolvimento de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="aa8b4-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="aa8b4-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-196">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="aa8b4-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-197">Extensões ISAPI</span><span class="sxs-lookup"><span data-stu-id="aa8b4-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-198">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="aa8b4-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="aa8b4-199">Segurança</span><span class="sxs-lookup"><span data-stu-id="aa8b4-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="aa8b4-200">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="aa8b4-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-201">Filtragem de solicitações</span><span class="sxs-lookup"><span data-stu-id="aa8b4-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-202">Recursos do Windows Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="aa8b4-203">Recursos do .NET Framework 4,5:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="aa8b4-204">.NET Framework 4,5 ou 4,6</span><span class="sxs-lookup"><span data-stu-id="aa8b4-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="aa8b4-205">O Windows Server 2016 </strong> - .net Framework 4,6 já está instalado para essas versões do Windows Server, mas você deve habilitá-la.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="aa8b4-206">O Windows Server 2012 ou o Windows Server 2012 R2 </strong> - .net Framework 4,5 já está instalado para essas versões do Windows Server, mas você deve habilitá-la.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="aa8b4-207">O Windows Server 2008 R2 </strong> - .net Framework 4,5 não está incluído no windows Server 2008 R2, portanto, você deve <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> baixar o Microsoft .NET Framework 4,5 </a> e instalá-lo separadamente.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="aa8b4-208">Observação</span><span class="sxs-lookup"><span data-stu-id="aa8b4-208">Note</span></span></strong><br/><p><span data-ttu-id="aa8b4-209">Se você estiver atualizando do MBAM 2,0 ou do MBAM 2,0 SP1 e precisar instalar o .NET Framework 4,5, consulte as <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> notas de versão do MBAM 2,5 </a> para obter uma etapa adicional necessária para fazer com que os sites funcionem.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="aa8b4-210">Ativação do WCF</span><span class="sxs-lookup"><span data-stu-id="aa8b4-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="aa8b4-211">Ativação de HTTP</span><span class="sxs-lookup"><span data-stu-id="aa8b4-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-212">Ativação não HTTP (somente para Windows Server 2008, 2012 e 2012 R2)</span><span class="sxs-lookup"><span data-stu-id="aa8b4-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="aa8b4-213">Ativação de TCP</span><span class="sxs-lookup"><span data-stu-id="aa8b4-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="aa8b4-214">Serviço de ativação de processos do Windows:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="aa8b4-215">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="aa8b4-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-216">Ambiente do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="aa8b4-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="aa8b4-217">APIs de configuração</span><span class="sxs-lookup"><span data-stu-id="aa8b4-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-218">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="aa8b4-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="aa8b4-219">Download do ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="aa8b4-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-220">SPN (nome da entidade de serviço)</span><span class="sxs-lookup"><span data-stu-id="aa8b4-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-221">Os aplicativos Web exigem um SPN para o nome do host virtual na conta de domínio que você usa para os pools de aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="aa8b4-222">Se seus direitos administrativos permitirem que você crie SPNs nos serviços de domínio Active Directory, o MBAM criará o SPN para você.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="aa8b4-223">Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obter informações sobre os direitos necessários para criar SPNs.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="aa8b4-224">Se você não tiver direitos administrativos para criar SPNs, você deve solicitar que os administradores do Active Directory em sua organização criem o SPN para você usando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="aa8b4-225">No exemplo de código, o nome do host virtual é mbamvirtual.contoso.com e a conta de domínio usada para os pools de aplicativos Web é contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="aa8b4-226">Observação</span><span class="sxs-lookup"><span data-stu-id="aa8b4-226">Note</span></span></strong><br/><p><span data-ttu-id="aa8b4-227">Se você estiver configurando o balanceamento de carga, use a mesma conta de pool de aplicativos em todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="aa8b4-228">Para obter mais informações sobre como registrar SPNs para nomes de host totalmente qualificados, NetBIOS e nomes de host, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planejando como proteger os sites do MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="aa8b4-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="aa8b4-229">Pré-requisitos para o portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="aa8b4-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-230">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-231">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-232">Versão com suporte do Windows Server</span><span class="sxs-lookup"><span data-stu-id="aa8b4-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-233">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-234">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="aa8b4-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="aa8b4-235">Download do ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="aa8b4-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-236">Ferramentas de gerenciamento do IIS do serviço Web</span><span class="sxs-lookup"><span data-stu-id="aa8b4-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-237">SPN (nome da entidade de serviço)</span><span class="sxs-lookup"><span data-stu-id="aa8b4-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-238">Os aplicativos Web exigem um SPN para o nome do host virtual na conta de domínio que você usa para os pools de aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="aa8b4-239">Se seus direitos administrativos permitirem que você crie SPNs nos serviços de domínio Active Directory, o MBAM criará o SPN para você.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="aa8b4-240">Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obter informações sobre os direitos necessários para criar SPNs.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="aa8b4-241">Se você não tiver direitos administrativos para criar SPNs, você deve perguntar aos administradores do Active Directory em seus administradores de organização em sua organização para criar o SPN para você usando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="aa8b4-242">No exemplo de código, o nome do host virtual é mbamvirtual.contoso.com e a conta de domínio usada para os pools de aplicativos Web é contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="aa8b4-243">Observação</span><span class="sxs-lookup"><span data-stu-id="aa8b4-243">Note</span></span></strong><br/><p><span data-ttu-id="aa8b4-244">Se você estiver configurando o balanceamento de carga, use a mesma conta de pool de aplicativos em todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="aa8b4-245">Para obter mais informações sobre como registrar SPNs para nomes de host totalmente qualificados, NetBIOS e nomes de host, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planejando como proteger os sites do MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="aa8b4-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="aa8b4-246">Pré-requisitos para a estação de trabalho de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="aa8b4-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-247">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="aa8b4-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-248">Detalhes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-249">Antes de instalar o cliente do MBAM, baixe os modelos de política de grupo do MBAM em <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> como obter modelos de política de grupo do MDOP (. admx) </a> e configure-os com as configurações que você deseja implementar na sua empresa para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa8b4-250">Antes de instalar o cliente do MBAM, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa8b4-251">O que fazer</span><span class="sxs-lookup"><span data-stu-id="aa8b4-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="aa8b4-252">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="aa8b4-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa8b4-253">Copiar os modelos de política de grupo do MBAM</span><span class="sxs-lookup"><span data-stu-id="aa8b4-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="aa8b4-254">Copiando os modelos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa8b4-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa8b4-255">Editar as configurações de política de grupo</span><span class="sxs-lookup"><span data-stu-id="aa8b4-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="aa8b4-256">Editando as configurações de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa8b4-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="aa8b4-257">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa8b4-257">Related topics</span></span>


[<span data-ttu-id="aa8b4-258">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa8b4-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="aa8b4-259">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa8b4-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="aa8b4-260">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="aa8b4-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="aa8b4-261">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="aa8b4-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="aa8b4-262">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="aa8b4-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="aa8b4-263">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="aa8b4-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




