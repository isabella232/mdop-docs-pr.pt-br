---
title: Pré-requisitos para implantação do MBAM 1.0
description: Pré-requisitos para implantação do MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799117"
---
# <span data-ttu-id="fdd39-103">Pré-requisitos para implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="fdd39-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="fdd39-104">Antes de começar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), verifique se você atende aos pré-requisitos necessários para instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="fdd39-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="fdd39-105">Esta seção contém informações para ajudá-lo a preparar com êxito o ambiente de computação antes de implantar os recursos de clientes e servidores do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdd39-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="fdd39-106">Pré-requisitos de instalação para recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="fdd39-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="fdd39-107">Cada um dos recursos do servidor MBAM tem pré-requisitos específicos que devem ser atendidos para que possam ser instalados com êxito.</span><span class="sxs-lookup"><span data-stu-id="fdd39-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="fdd39-108">A instalação do MBAM verifica se todos os pré-requisitos são atendidos antes do início da instalação.</span><span class="sxs-lookup"><span data-stu-id="fdd39-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="fdd39-109">Pré-requisitos de instalação do servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="fdd39-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="fdd39-110">A tabela a seguir contém os pré-requisitos de instalação do MBAM Administration and Monitoring Server:</span><span class="sxs-lookup"><span data-stu-id="fdd39-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdd39-111">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="fdd39-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fdd39-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="fdd39-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fdd39-113">Função do Windows ServerWeb Server</span><span class="sxs-lookup"><span data-stu-id="fdd39-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fdd39-114">Esta função deve ser adicionada a um sistema operacional de servidor compatível com o recurso de servidor administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdd39-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fdd39-115">Ferramentas de gerenciamento do servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="fdd39-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fdd39-116">Ferramentas e scripts de gerenciamento do IIS</span><span class="sxs-lookup"><span data-stu-id="fdd39-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fdd39-117">Serviços de função de servidor Web</span><span class="sxs-lookup"><span data-stu-id="fdd39-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fdd39-118">Recursos comuns de HTTP:</span><span class="sxs-lookup"><span data-stu-id="fdd39-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fdd39-119">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="fdd39-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="fdd39-120">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="fdd39-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="fdd39-121">Desenvolvimento de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="fdd39-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fdd39-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="fdd39-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="fdd39-123">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="fdd39-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="fdd39-124">Extensões ISAPI</span><span class="sxs-lookup"><span data-stu-id="fdd39-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="fdd39-125">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="fdd39-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="fdd39-126">Segurança</span><span class="sxs-lookup"><span data-stu-id="fdd39-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fdd39-127">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="fdd39-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="fdd39-128">Filtragem de solicitações</span><span class="sxs-lookup"><span data-stu-id="fdd39-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fdd39-129">Recursos do Windows Server</span><span class="sxs-lookup"><span data-stu-id="fdd39-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fdd39-130">Recursos do Microsoft .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="fdd39-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fdd39-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="fdd39-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="fdd39-132">Ativação do WCF</span><span class="sxs-lookup"><span data-stu-id="fdd39-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="fdd39-133">Ativação de HTTP</span><span class="sxs-lookup"><span data-stu-id="fdd39-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="fdd39-134">Ativação não HTTP</span><span class="sxs-lookup"><span data-stu-id="fdd39-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="fdd39-135">Serviço de Ativação de Processos do Windows</span><span class="sxs-lookup"><span data-stu-id="fdd39-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fdd39-136">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="fdd39-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="fdd39-137">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="fdd39-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="fdd39-138">APIs de configuração</span><span class="sxs-lookup"><span data-stu-id="fdd39-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fdd39-139">**Observação**  Para obter uma lista dos sistemas operacionais compatíveis, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fdd39-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="fdd39-140">Pré-requisitos de instalação dos relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="fdd39-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="fdd39-141">Os relatórios de conformidade e auditoria devem ser instalados em uma versão com suporte do SQLServer.</span><span class="sxs-lookup"><span data-stu-id="fdd39-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="fdd39-142">Os pré-requisitos de instalação para esse recurso incluem SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="fdd39-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="fdd39-143">O SSRS deve ser instalado e executado durante a instalação do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="fdd39-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="fdd39-144">O SSRS também deve ser configurado no modo "nativo", não no modo "não configurado" ou "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="fdd39-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="fdd39-145">**Observação**  Para obter uma lista dos sistemas operacionais compatíveis e das versões do SQLServer, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fdd39-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="fdd39-146">Pré-requisitos de instalação para o banco de dados de recuperação e hardware</span><span class="sxs-lookup"><span data-stu-id="fdd39-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="fdd39-147">O banco de dados de recuperação e de hardware deve ser instalado em uma versão com suporte do SQLServer.</span><span class="sxs-lookup"><span data-stu-id="fdd39-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="fdd39-148">O SQL Server deve ter serviços de mecanismo de banco de dados instalados e em execução durante a instalação do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdd39-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="fdd39-149">O recurso de criptografia de dados transparente (TDE) deve estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="fdd39-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="fdd39-150">**Observação**  Para obter uma lista dos sistemas operacionais compatíveis e das versões do SQLServer, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fdd39-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="fdd39-151">O recurso TDE SQLServer executa a criptografia e a descriptografia de entrada/saída (e/s) em tempo real dos arquivos de dados e log.</span><span class="sxs-lookup"><span data-stu-id="fdd39-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="fdd39-152">O TDE protege os dados que são "em repouso", que incluem os dados e os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="fdd39-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="fdd39-153">Ele fornece a capacidade de obedecer a várias leis, regulamentações e diretrizes estabelecidas em diversos setores.</span><span class="sxs-lookup"><span data-stu-id="fdd39-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="fdd39-154">**Observação**  Como o TDE executa a descriptografia em tempo real das informações do banco de dados, as informações da chave de recuperação ficarão visíveis se a conta na qual você está conectado tiver permissões para o banco de dados quando você exibir as tabelas de informações de chave de recuperação do SQL.</span><span class="sxs-lookup"><span data-stu-id="fdd39-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="fdd39-155">Pré-requisitos de instalação para o banco de dados de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="fdd39-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="fdd39-156">O banco de dados de auditoria e conformidade deve ser instalado em uma versão com suporte do SQLServer.</span><span class="sxs-lookup"><span data-stu-id="fdd39-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="fdd39-157">O SQL Server deve ter serviços de mecanismo de banco de dados instalados e em execução durante a instalação do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="fdd39-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="fdd39-158">**Observação**  Para obter uma lista dos sistemas operacionais compatíveis e das versões do SQLServer, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fdd39-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="fdd39-159">Pré-requisitos de instalação para clientes MBAM</span><span class="sxs-lookup"><span data-stu-id="fdd39-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="fdd39-160">Os pré-requisitos necessários que você precisa atender antes de iniciar a instalação do cliente do MBAM são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="fdd39-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="fdd39-161">Recurso de TPM (Trusted Platform Module) v 1.2</span><span class="sxs-lookup"><span data-stu-id="fdd39-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="fdd39-162">O chip TPM deve estar ativado no BIOS e deve ser redefinido do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fdd39-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="fdd39-163">Para obter mais informações, consulte a documentação do BIOS.</span><span class="sxs-lookup"><span data-stu-id="fdd39-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="fdd39-164">**Aviso**  Verifique se o teclado, o mouse e o vídeo estão conectados diretamente ao computador, em vez de a um botão de teclado, vídeo, mouse (KVM).</span><span class="sxs-lookup"><span data-stu-id="fdd39-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="fdd39-165">Um comutador KVM pode interferir na capacidade do computador de detectar a presença física do hardware.</span><span class="sxs-lookup"><span data-stu-id="fdd39-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="fdd39-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdd39-166">Related topics</span></span>


[<span data-ttu-id="fdd39-167">Planejar a implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="fdd39-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="fdd39-168">Configurações com suporte no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="fdd39-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





