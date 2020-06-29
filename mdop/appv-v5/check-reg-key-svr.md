---
title: Verificar as chaves do Registro antes de instalar o servidor do App-V 5.x
description: Verificar as chaves do Registro antes de instalar o servidor do App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796567"
---
# <span data-ttu-id="f82e4-103">Verificar as chaves do Registro antes de instalar o servidor do App-V 5.x</span><span class="sxs-lookup"><span data-stu-id="f82e4-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="f82e4-104">Se você estiver atualizando o pacote do pacote do aplicativo App-V do App-V 5,0 SP1 3 ou posterior, conclua as etapas desta seção antes de instalar o App-V 5. x Server</span><span class="sxs-lookup"><span data-stu-id="f82e4-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f82e4-105">Quando essa etapa é necessária</span><span class="sxs-lookup"><span data-stu-id="f82e4-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f82e4-106">Você está atualizando do App-V 5,0 SP1 com qualquer pacote de hotfix subsequente que você instalou usando um arquivo. msp.</span><span class="sxs-lookup"><span data-stu-id="f82e4-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f82e4-107">Quais componentes exigem que você siga esta etapa</span><span class="sxs-lookup"><span data-stu-id="f82e4-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f82e4-108">Somente os componentes do App-V Server que você está atualizando.</span><span class="sxs-lookup"><span data-stu-id="f82e4-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f82e4-109">Quando precisar fazer esta etapa</span><span class="sxs-lookup"><span data-stu-id="f82e4-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f82e4-110">Antes de atualizar o servidor do App-V para o App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="f82e4-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f82e4-111">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="f82e4-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f82e4-112">Usando as informações nas tabelas a seguir, atualize cada valor de chave do registro sob <code>HKLM\Software\Microsoft\AppV\Server</code> o valor que você forneceu na instalação do servidor original.</span><span class="sxs-lookup"><span data-stu-id="f82e4-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="f82e4-113">Concluir esta etapa restaura os valores do registro que podem ter sido removidos quando os pacotes de hotfix do App-V 5,0 SP1 foram instalados.</span><span class="sxs-lookup"><span data-stu-id="f82e4-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f82e4-114">Chave ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="f82e4-114">ManagementDatabase key</span></span>**

<span data-ttu-id="f82e4-115">Se você estiver instalando o banco de dados de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="f82e4-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f82e4-116">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f82e4-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="f82e4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f82e4-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="f82e4-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-119">Descreve se uma conta de acesso público é necessária para acessar bancos de dados de gerenciamento não locais.</span><span class="sxs-lookup"><span data-stu-id="f82e4-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="f82e4-120">Valor é definido como "1" se for necessário.</span><span class="sxs-lookup"><span data-stu-id="f82e4-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f82e4-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-122">Nome do banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-124">Conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="f82e4-125">Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="f82e4-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="f82e4-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-127">Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="f82e4-128">Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="f82e4-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f82e4-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-130">Instância do SQL Server para o banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="f82e4-131">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="f82e4-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-133">Conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="f82e4-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-135">Identificador seguro (SID) da conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-137">Conta de computador remoto do servidor de gerenciamento (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="f82e4-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-139">Logon de administrador de instalação para o servidor de gerenciamento (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="f82e4-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f82e4-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-141">Valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f82e4-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="f82e4-142">1 </strong> – o serviço de gerenciamento está no computador local, ou seja, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</span><span class="sxs-lookup"><span data-stu-id="f82e4-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="f82e4-143">0 </strong> - o serviço de gerenciamento está em um computador diferente do computador local.</span><span class="sxs-lookup"><span data-stu-id="f82e4-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f82e4-144">Chave ManagementService</span><span class="sxs-lookup"><span data-stu-id="f82e4-144">ManagementService key</span></span>**

<span data-ttu-id="f82e4-145">Se você estiver instalando o servidor de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="f82e4-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f82e4-146">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f82e4-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="f82e4-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="f82e4-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-149">Conta ou grupo dos serviços de domínio Active Directory (AD DS) que está autorizado a gerenciar o App-V (domínio de domínio).</span><span class="sxs-lookup"><span data-stu-id="f82e4-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f82e4-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-151">Instância do SQL Server que contém o banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="f82e4-152">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="f82e4-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f82e4-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-154">Nome do SQL Server remoto com o banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f82e4-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="f82e4-155">Se o valor estiver em branco, o computador local será usado.</span><span class="sxs-lookup"><span data-stu-id="f82e4-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f82e4-156">Chave ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="f82e4-156">ReportingDatabase key</span></span>**

<span data-ttu-id="f82e4-157">Se você estiver instalando o banco de dados de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="f82e4-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f82e4-158">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f82e4-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="f82e4-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="f82e4-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="f82e4-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-161">Descreve se uma conta de acesso público é necessária para acessar bancos de dados de relatório não locais.</span><span class="sxs-lookup"><span data-stu-id="f82e4-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="f82e4-162">Valor é definido como "1" se for necessário.</span><span class="sxs-lookup"><span data-stu-id="f82e4-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f82e4-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-164">Nome do banco de dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="f82e4-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-166">Conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="f82e4-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="f82e4-167">Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="f82e4-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="f82e4-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-169">Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="f82e4-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="f82e4-170">Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="f82e4-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f82e4-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-172">Instância do SQL Server para o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="f82e4-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="f82e4-173">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="f82e4-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="f82e4-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-177">Conta de computador remoto do servidor de relatório (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="f82e4-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f82e4-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-179">Login de administrador de instalação para o servidor de relatórios (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="f82e4-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f82e4-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-181">Valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f82e4-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="f82e4-182">1 </strong> – o serviço de relatório está no computador local, ou seja, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</span><span class="sxs-lookup"><span data-stu-id="f82e4-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="f82e4-183">0 </strong> - o serviço de relatório está em um computador diferente do computador local.</span><span class="sxs-lookup"><span data-stu-id="f82e4-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f82e4-184">Chave ReportingService</span><span class="sxs-lookup"><span data-stu-id="f82e4-184">ReportingService key</span></span>**

<span data-ttu-id="f82e4-185">Se você estiver instalando o servidor de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="f82e4-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f82e4-186">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f82e4-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="f82e4-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="f82e4-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82e4-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f82e4-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-189">Instância do SQL Server para o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="f82e4-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="f82e4-190">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="f82e4-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82e4-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f82e4-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82e4-192">Nome do SQL Server remoto com o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="f82e4-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="f82e4-193">Se o valor estiver em branco, o computador local será usado.</span><span class="sxs-lookup"><span data-stu-id="f82e4-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

