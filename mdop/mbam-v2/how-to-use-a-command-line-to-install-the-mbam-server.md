---
title: Como usar uma linha de comando para instalar o Servidor do MBAM
description: Como usar uma linha de comando para instalar o Servidor do MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799713"
---
# <span data-ttu-id="067a5-103">Como usar uma linha de comando para instalar o Servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="067a5-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="067a5-104">Você pode usar uma linha de comando para instalar o servidor MBAM com a topologia autônoma ou do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="067a5-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="067a5-105">O exemplo de linha de comando a seguir é para implantar MBAM em um único servidor, que é uma arquitetura que deve ser usada somente em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="067a5-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="067a5-106">Você precisará alterar a linha de comando adequadamente ao implantar o MBAM em um ambiente de produção, que deve ter vários servidores.</span><span class="sxs-lookup"><span data-stu-id="067a5-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="067a5-107">Linha de comando para a implantação do servidor do MBAM 2.0 com a topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="067a5-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="067a5-108">Você pode usar uma linha de comando semelhante à seguinte para instalar o servidor MBAM com a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="067a5-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="067a5-109">A tabela a seguir descreve os parâmetros de linha de comando para a implantação do servidor MBAM com a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="067a5-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="067a5-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="067a5-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="067a5-111">Valor do parâmetro</span><span class="sxs-lookup"><span data-stu-id="067a5-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="067a5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="067a5-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-113">TOPOLOGIA</span><span class="sxs-lookup"><span data-stu-id="067a5-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-114">0</span><span class="sxs-lookup"><span data-stu-id="067a5-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-115">0 – topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="067a5-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="067a5-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-117">Dezembro</span><span class="sxs-lookup"><span data-stu-id="067a5-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-118">0 – não aceitar o contrato de licença agreement1-aceitar o contrato de licença</span><span class="sxs-lookup"><span data-stu-id="067a5-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="067a5-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-120">Recursos a serem instalados no servidor</span><span class="sxs-lookup"><span data-stu-id="067a5-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-121">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="067a5-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-122">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="067a5-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="067a5-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-124">Banco de dados de relatórios de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="067a5-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-125">Relatórios</span><span class="sxs-lookup"><span data-stu-id="067a5-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-126">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="067a5-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="067a5-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-128">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="067a5-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="067a5-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-130">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="067a5-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="067a5-131">Políticatemplate</span><span class="sxs-lookup"><span data-stu-id="067a5-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-132">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="067a5-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="067a5-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-134">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="067a5-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-135">Conta de domínio e de usuário da conta de serviço do Reporting Services que irá acessar o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="067a5-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="067a5-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="067a5-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-138">Senha da conta de serviço do Reporting Services que vai acessar o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="067a5-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="067a5-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-140">% ComputerName%</span><span class="sxs-lookup"><span data-stu-id="067a5-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-141">Nome da instância do SQL Server para o banco de dados de conformidade e auditoria – substituir <strong> % ComputerName% </strong> pelo nome do computador</span><span class="sxs-lookup"><span data-stu-id="067a5-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="067a5-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-143">% ComputerName%</span><span class="sxs-lookup"><span data-stu-id="067a5-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-144">Nome da instância do SQL Server para o banco de dados de recuperação – substituir <strong> % ComputerName% </strong> pelo nome do computador</span><span class="sxs-lookup"><span data-stu-id="067a5-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="067a5-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-146">% ComputerName%</span><span class="sxs-lookup"><span data-stu-id="067a5-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-147">Instância do servidor de relatórios do SQL Server na qual os relatórios de conformidade e auditoria serão instalados – substitua <strong> % ComputerName% </strong> pelo nome do computador</span><span class="sxs-lookup"><span data-stu-id="067a5-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="067a5-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-149">83</span><span class="sxs-lookup"><span data-stu-id="067a5-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-150">Porta para o site de administração e monitoramento; "83" é apenas um exemplo</span><span class="sxs-lookup"><span data-stu-id="067a5-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="067a5-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-152">83</span><span class="sxs-lookup"><span data-stu-id="067a5-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-153">Porta para o site do portal de autoatendimento; "83" é apenas um exemplo</span><span class="sxs-lookup"><span data-stu-id="067a5-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="067a5-154">Linha de comando para a implantação do servidor do MBAM 2.0 com a topologia do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="067a5-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="067a5-155">Você pode usar uma linha de comando semelhante à seguinte para instalar o servidor MBAM com a topologia do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="067a5-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="067a5-156">A tabela a seguir descreve os parâmetros de linha de comando para instalar o MBAM 2.0 Server com a topologia do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="067a5-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="067a5-157">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="067a5-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="067a5-158">Valor do parâmetro</span><span class="sxs-lookup"><span data-stu-id="067a5-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="067a5-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="067a5-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-160">TOPOLOGIA</span><span class="sxs-lookup"><span data-stu-id="067a5-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-161">um</span><span class="sxs-lookup"><span data-stu-id="067a5-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-162">1 – topologia do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="067a5-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="067a5-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-164">Dezembro</span><span class="sxs-lookup"><span data-stu-id="067a5-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-165">0 – não aceitar o contrato de licença agreement1-aceitar o contrato de licença</span><span class="sxs-lookup"><span data-stu-id="067a5-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="067a5-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-167">% ComputerName%</span><span class="sxs-lookup"><span data-stu-id="067a5-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-168">Nome da instância do SQL Server para o banco de dados de auditoria – substituir <strong> % ComputerName% </strong> pelo nome do computador</span><span class="sxs-lookup"><span data-stu-id="067a5-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="067a5-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-170">% ComputerName%</span><span class="sxs-lookup"><span data-stu-id="067a5-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-171">Nome da instância do SQL Server para o banco de dados de recuperação: substituir <strong> % ComputerName% </strong> pelo nome do computador</span><span class="sxs-lookup"><span data-stu-id="067a5-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="067a5-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-173">% ComputerName%</span><span class="sxs-lookup"><span data-stu-id="067a5-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-174">Instância do servidor de relatórios do SQL Server na qual os relatórios de auditoria serão instalados – substitua% ComputerName% pelo nome do computador</span><span class="sxs-lookup"><span data-stu-id="067a5-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="067a5-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-176">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="067a5-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-177">Conta de domínio e de usuário da conta de serviço do Reporting Services que irá acessar o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="067a5-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="067a5-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="067a5-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-180">Senha da conta de serviço do Reporting Services que vai acessar o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="067a5-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="067a5-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="067a5-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-182">83</span><span class="sxs-lookup"><span data-stu-id="067a5-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-183">Porta para o site de administração e monitoramento; "83" é apenas um exemplo</span><span class="sxs-lookup"><span data-stu-id="067a5-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="067a5-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="067a5-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-185">83</span><span class="sxs-lookup"><span data-stu-id="067a5-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="067a5-186">Porta para o site do portal de autoatendimento; "83" é apenas um exemplo</span><span class="sxs-lookup"><span data-stu-id="067a5-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="067a5-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="067a5-187">Related topics</span></span>


[<span data-ttu-id="067a5-188">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="067a5-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





