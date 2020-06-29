---
title: Pré-requisitos para implantação do MBAM 2.0
description: Pré-requisitos para implantação do MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799787"
---
# <span data-ttu-id="33e8e-103">Pré-requisitos para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="33e8e-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="33e8e-104">Antes de iniciar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), você deve certificar-se de que você atendeu aos pré-requisitos para instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="33e8e-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="33e8e-105">Esta seção contém informações para ajudá-lo a planejar com êxito o ambiente computacional antes de implantar os recursos e os clientes do Microsoft BitLocker Administration and Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="33e8e-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="33e8e-106">Se você estiver instalando o MBAM com o Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) para obter pré-requisitos adicionais.</span><span class="sxs-lookup"><span data-stu-id="33e8e-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="33e8e-107">Pré-requisitos de instalação para recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="33e8e-108">Cada um dos recursos do MBAM Server tem pré-requisitos específicos que devem ser atendidos para que os recursos do MBAM possam ser instalados com êxito.</span><span class="sxs-lookup"><span data-stu-id="33e8e-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="33e8e-109">MBAM a instalação verifica se todos os pré-requisitos são atendidos antes do início da instalação.</span><span class="sxs-lookup"><span data-stu-id="33e8e-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="33e8e-110">Pré-requisitos para o servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="33e8e-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33e8e-111">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="33e8e-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="33e8e-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="33e8e-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="33e8e-113">Função de servidor Web do Windows Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="33e8e-114">Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o recurso de servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="33e8e-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="33e8e-115">Ferramentas de gerenciamento do servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="33e8e-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="33e8e-116">Selecione <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="33e8e-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="33e8e-117">Certificado SSL</span><span class="sxs-lookup"><span data-stu-id="33e8e-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="33e8e-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="33e8e-118">Optional.</span></span> <span data-ttu-id="33e8e-119">Para proteger a comunicação entre os clientes e os serviços Web, você precisa obter e instalar um certificado assinado por uma autoridade de segurança confiável.</span><span class="sxs-lookup"><span data-stu-id="33e8e-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="33e8e-120">Serviços de função de servidor Web</span><span class="sxs-lookup"><span data-stu-id="33e8e-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="33e8e-121">Recursos comuns de HTTP:</span><span class="sxs-lookup"><span data-stu-id="33e8e-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="33e8e-122">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="33e8e-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="33e8e-123">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="33e8e-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="33e8e-124">Desenvolvimento de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="33e8e-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="33e8e-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="33e8e-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="33e8e-126">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="33e8e-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="33e8e-127">Extensões ISAPI</span><span class="sxs-lookup"><span data-stu-id="33e8e-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="33e8e-128">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="33e8e-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="33e8e-129">Segurança</span><span class="sxs-lookup"><span data-stu-id="33e8e-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="33e8e-130">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="33e8e-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="33e8e-131">Filtragem de solicitações</span><span class="sxs-lookup"><span data-stu-id="33e8e-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="33e8e-132">Recursos do Windows Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="33e8e-133">Recursos do .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="33e8e-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="33e8e-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="33e8e-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="33e8e-135">Ativação do WCF</span><span class="sxs-lookup"><span data-stu-id="33e8e-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-136">Ativação de HTTP</span><span class="sxs-lookup"><span data-stu-id="33e8e-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="33e8e-137">Ativação não HTTP</span><span class="sxs-lookup"><span data-stu-id="33e8e-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="33e8e-138">Serviço de ativação de processos do Windows:</span><span class="sxs-lookup"><span data-stu-id="33e8e-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="33e8e-139">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="33e8e-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="33e8e-140">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="33e8e-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="33e8e-141">APIs de configuração</span><span class="sxs-lookup"><span data-stu-id="33e8e-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="33e8e-142">Observação</span><span class="sxs-lookup"><span data-stu-id="33e8e-142">Note</span></span>**  
<span data-ttu-id="33e8e-143">Para obter uma lista dos sistemas operacionais compatíveis, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="33e8e-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="33e8e-144">Pré-requisitos para os relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="33e8e-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33e8e-145">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="33e8e-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="33e8e-146">Detalhes</span><span class="sxs-lookup"><span data-stu-id="33e8e-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-147">Versão com suporte do SQL Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="33e8e-148">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="33e8e-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-149">Instale o SQL Server com:</span><span class="sxs-lookup"><span data-stu-id="33e8e-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-150">Agrupamento SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="33e8e-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33e8e-151">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="33e8e-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-152">Direitos de instância do SSRS – necessários para a instalação de relatórios apenas se você estiver instalando bancos de dados em um servidor separado dos relatórios.</span><span class="sxs-lookup"><span data-stu-id="33e8e-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-153">Direitos de instância obrigatórios:</span><span class="sxs-lookup"><span data-stu-id="33e8e-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-154">Criar pastas</span><span class="sxs-lookup"><span data-stu-id="33e8e-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="33e8e-155">Publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="33e8e-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="33e8e-156">O SSRS deve ser instalado e executado durante a instalação do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="33e8e-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="33e8e-157">Configurar o SSRS no modo "nativo" e não no modo não configurado ou "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="33e8e-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="33e8e-158">Pré-requisitos para o banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="33e8e-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33e8e-159">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="33e8e-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="33e8e-160">Detalhes</span><span class="sxs-lookup"><span data-stu-id="33e8e-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-161">Versão com suporte do SQL Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="33e8e-162">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="33e8e-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-163">Instale o SQL Server com:</span><span class="sxs-lookup"><span data-stu-id="33e8e-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-164">Agrupamento SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="33e8e-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="33e8e-165">Ferramentas de gerenciamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33e8e-166">Permissões do SQL Server necessárias</span><span class="sxs-lookup"><span data-stu-id="33e8e-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-167">Permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="33e8e-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-168">Funções de servidor de logon da instância SQL:</span><span class="sxs-lookup"><span data-stu-id="33e8e-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-169">dbcreator</span><span class="sxs-lookup"><span data-stu-id="33e8e-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="33e8e-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="33e8e-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="33e8e-171">Direitos de instância do SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="33e8e-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-172">Criar pastas</span><span class="sxs-lookup"><span data-stu-id="33e8e-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="33e8e-173">Publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="33e8e-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-174">Opcional-instalar o recurso de criptografia transparente de dados (TDE) disponível no SQL Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-175">O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a várias leis, regulamentações e diretrizes estabelecidas em diversos setores.</span><span class="sxs-lookup"><span data-stu-id="33e8e-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="33e8e-176">Observação</span><span class="sxs-lookup"><span data-stu-id="33e8e-176">Note</span></span></strong><br/><p><span data-ttu-id="33e8e-177">O TDE executa a descriptografia em tempo real das informações do banco de dados, o que significa que, se a conta na qual você está conectado tiver permissões para o banco de dados enquanto você estiver exibindo as informações da chave de recuperação nas tabelas do SQL Server, as informações da chave de recuperação estarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="33e8e-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="33e8e-178">Saiba mais sobre o TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerações de segurança </a> .</span><span class="sxs-lookup"><span data-stu-id="33e8e-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="33e8e-179">Pré-requisitos para o banco de dados de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="33e8e-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33e8e-180">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="33e8e-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="33e8e-181">Detalhes</span><span class="sxs-lookup"><span data-stu-id="33e8e-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-182">Versão com suporte do SQL Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="33e8e-183">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="33e8e-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-184">Instale o SQL Server com:</span><span class="sxs-lookup"><span data-stu-id="33e8e-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-185">Agrupamento SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="33e8e-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="33e8e-186">Ferramentas de gerenciamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33e8e-187">Permissões do SQL Server necessárias</span><span class="sxs-lookup"><span data-stu-id="33e8e-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-188">Permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="33e8e-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-189">Funções de servidor de logon da instância SQL:</span><span class="sxs-lookup"><span data-stu-id="33e8e-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-190">dbcreator</span><span class="sxs-lookup"><span data-stu-id="33e8e-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="33e8e-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="33e8e-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="33e8e-192">Direitos de instância do SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="33e8e-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-193">Criar pastas</span><span class="sxs-lookup"><span data-stu-id="33e8e-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="33e8e-194">Publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="33e8e-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-195">Opcional – Instale o recurso de criptografia transparente de dados (TDE) no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="33e8e-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-196">O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a várias leis, regulamentações e diretrizes estabelecidas em diversos setores.</span><span class="sxs-lookup"><span data-stu-id="33e8e-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="33e8e-197">Observação</span><span class="sxs-lookup"><span data-stu-id="33e8e-197">Note</span></span></strong><br/><p><span data-ttu-id="33e8e-198">O TDE executa a descriptografia em tempo real das informações do banco de dados, o que significa que, se a conta na qual você está conectado tiver permissões para o banco de dados enquanto você estiver exibindo as informações da chave de recuperação nas tabelas do SQL Server, as informações da chave de recuperação estarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="33e8e-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="33e8e-199">Saiba mais sobre o TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="33e8e-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33e8e-200">O SQL Server deve ter serviços de mecanismo de banco de dados instalados e em execução durante a instalação do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="33e8e-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-201">O serviço do SQL Server Agent deve estar em execução e definido para inicialização automática nas instâncias selecionadas do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="33e8e-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="33e8e-202">Pré-requisitos para o portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="33e8e-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33e8e-203">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="33e8e-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="33e8e-204">Detalhes</span><span class="sxs-lookup"><span data-stu-id="33e8e-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-205">Versão com suporte do Windows Server</span><span class="sxs-lookup"><span data-stu-id="33e8e-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="33e8e-206">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</span><span class="sxs-lookup"><span data-stu-id="33e8e-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33e8e-207">ASP.NET MVC 2,0</span><span class="sxs-lookup"><span data-stu-id="33e8e-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="33e8e-208">Download do ASP.NET MVC 2</span><span class="sxs-lookup"><span data-stu-id="33e8e-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33e8e-209">Ferramentas de gerenciamento do IIS do serviço Web</span><span class="sxs-lookup"><span data-stu-id="33e8e-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="33e8e-210">Pré-requisitos para clientes MBAM</span><span class="sxs-lookup"><span data-stu-id="33e8e-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33e8e-211">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="33e8e-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="33e8e-212">Detalhes</span><span class="sxs-lookup"><span data-stu-id="33e8e-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="33e8e-213">Os clientes do Windows 7 </strong> - devem ter a funcionalidade TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="33e8e-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-214">A versão do TPM deve ser 1,2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="33e8e-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33e8e-215">O chip TPM deve estar ativado no BIOS e ser redefinido do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="33e8e-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="33e8e-216">Para obter mais informações, consulte a documentação do BIOS.</span><span class="sxs-lookup"><span data-stu-id="33e8e-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="33e8e-217">Clientes do Windows 8 somente </strong> : para ter o MBAM Store e gerenciar as chaves de recuperação do TPM: o provisionamento automático do TPM deve ser desativado e MBAM deve ser definido como o proprietário do TPM antes de implantar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="33e8e-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="33e8e-218">Para desativar o provisionamento automático do TPM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="33e8e-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="33e8e-219">O provisionamento automático de TPM deve ser desativado.</span><span class="sxs-lookup"><span data-stu-id="33e8e-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="33e8e-220">MBAM deve ser definido como o proprietário do TPM antes de implantar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="33e8e-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="33e8e-221">Para desativar o provisionamento automático do TPM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="33e8e-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="33e8e-222">Observação</span><span class="sxs-lookup"><span data-stu-id="33e8e-222">Note</span></span></strong><br/><p><span data-ttu-id="33e8e-223">Verifique se o teclado, o vídeo ou o mouse estão diretamente conectados e não são gerenciados por meio de um botão de teclado, vídeo ou mouse (KVM).</span><span class="sxs-lookup"><span data-stu-id="33e8e-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="33e8e-224">Um comutador KVM pode interferir na capacidade do computador de detectar a presença física do hardware.</span><span class="sxs-lookup"><span data-stu-id="33e8e-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="33e8e-225">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33e8e-225">Related topics</span></span>


[<span data-ttu-id="33e8e-226">Planejar a implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="33e8e-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="33e8e-227">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="33e8e-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









