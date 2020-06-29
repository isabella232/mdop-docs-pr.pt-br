---
title: Como configurar os bancos de dados do MBAM 2.5
description: Como configurar os bancos de dados do MBAM 2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799909"
---
# <span data-ttu-id="1281d-103">Como configurar os bancos de dados do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="1281d-104">Este tópico explica como configurar o banco de dados de auditoria e a conformidade do 2,5 do Microsoft BitLocker (MBAM) e o banco de dados de recuperação usando:</span><span class="sxs-lookup"><span data-stu-id="1281d-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="1281d-105">Um cmdlet do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1281d-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="1281d-106">O assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="1281d-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="1281d-107">As instruções se baseiam na arquitetura recomendada na [arquitetura de alto nível do MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="1281d-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="1281d-108">Antes de iniciar a configuração:</span><span class="sxs-lookup"><span data-stu-id="1281d-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1281d-109">Etapa</span><span class="sxs-lookup"><span data-stu-id="1281d-109">Step</span></span></th>
<th align="left"><span data-ttu-id="1281d-110">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="1281d-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1281d-111">Examine a arquitetura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="1281d-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="1281d-112">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1281d-113">Examine as configurações com suporte para MBAM.</span><span class="sxs-lookup"><span data-stu-id="1281d-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="1281d-114">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1281d-115">Complete os pré-requisitos obrigatórios em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="1281d-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="1281d-116">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1281d-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="1281d-117">MBAM 2,5-pré-requisitos do servidor que se aplicam somente à topologia de integração do Configuration Manager </a> (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="1281d-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1281d-118">Instale o software do servidor MBAM em cada servidor em que você planeja configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="1281d-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1281d-119">Observação</span><span class="sxs-lookup"><span data-stu-id="1281d-119">Note</span></span></strong><br/><p><span data-ttu-id="1281d-120">Você pode instalar os bancos de dados em um computador remoto do SQL Server usando o Windows PowerShell ou um pacote de aplicativo da camada de dados (DAC) exportado.</span><span class="sxs-lookup"><span data-stu-id="1281d-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="1281d-121">Para obter mais informações sobre pacotes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicativos da camada de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="1281d-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="1281d-122">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1281d-123">Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar cmdlets do Windows PowerShell para configurar os recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="1281d-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="1281d-124">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1281d-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="1281d-125">Para configurar os bancos de dados usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1281d-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="1281d-126">Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1281d-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="1281d-127">Use o cmdlet **Enable-MbamDatabase** do Windows PowerShell para configurar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="1281d-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="1281d-128">Para obter informações sobre esse cmdlet do Windows PowerShell, digite **Get-Help Enable-MbamDatabase**.</span><span class="sxs-lookup"><span data-stu-id="1281d-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="1281d-129">Para configurar o banco de dados de auditoria e conformidade usando o assistente</span><span class="sxs-lookup"><span data-stu-id="1281d-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="1281d-130">No servidor em que você deseja configurar os bancos de dados, inicie o assistente de **configuração do servidor do MBAM** .</span><span class="sxs-lookup"><span data-stu-id="1281d-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="1281d-131">Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.</span><span class="sxs-lookup"><span data-stu-id="1281d-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="1281d-132">Clique em **Adicionar novos recursos**, selecione **conformidade e auditoria** e banco de dados de **recuperação**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1281d-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="1281d-133">O assistente verifica se todos os pré-requisitos dos bancos de dados foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="1281d-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="1281d-134">Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1281d-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="1281d-135">Caso contrário, resolva todos os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="1281d-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="1281d-136">Usando as descrições a seguir, insira os valores de campo no assistente:</span><span class="sxs-lookup"><span data-stu-id="1281d-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1281d-137">Campo</span><span class="sxs-lookup"><span data-stu-id="1281d-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="1281d-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="1281d-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1281d-139">Nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="1281d-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-140">Nome do servidor no qual você está configurando o banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="1281d-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1281d-141">Observação</span><span class="sxs-lookup"><span data-stu-id="1281d-141">Note</span></span></strong><br/><p><span data-ttu-id="1281d-142">Você deve adicionar uma exceção no computador de banco de dados de conformidade e auditoria para habilitar o tráfego de entrada na porta do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1281d-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="1281d-143">O número da porta padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="1281d-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1281d-144">Instância de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="1281d-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-145">Nome da instância do banco de dados em que os dados de conformidade e auditoria serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="1281d-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="1281d-146">Você também deve especificar onde as informações do banco de dados serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="1281d-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1281d-147">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="1281d-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-148">Nome do banco de dados que armazenará os dados de conformidade.</span><span class="sxs-lookup"><span data-stu-id="1281d-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1281d-149">Observação</span><span class="sxs-lookup"><span data-stu-id="1281d-149">Note</span></span></strong><br/><p><span data-ttu-id="1281d-150">Se você estiver atualizando de uma versão anterior do MBAM, deverá usar o mesmo nome de banco de dados que o nome que foi usado na implantação anterior.</span><span class="sxs-lookup"><span data-stu-id="1281d-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1281d-151">Usuário ou grupo de domínio de acesso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1281d-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-152">Usuário ou grupo de domínio que tem permissão de leitura/gravação para esse banco de dados para habilitar os aplicativos Web para acessar os dados e relatórios nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1281d-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="1281d-153">Se você inserir um usuário nesse campo, ele deve ter o mesmo valor que o valor no <strong> campo conta de domínio do pool de aplicativos de serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="1281d-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="1281d-154">Se você inserir um grupo nesse campo, o valor no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> deve ser um membro do grupo que você inserir nesse campo.</span><span class="sxs-lookup"><span data-stu-id="1281d-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1281d-155">Usuário ou grupo de domínio de acesso somente leitura</span><span class="sxs-lookup"><span data-stu-id="1281d-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-156">Nome do usuário ou grupo que terá permissão somente leitura para esse banco de dados para permitir que os relatórios acessem os dados de conformidade nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1281d-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="1281d-157">Se você inserir um usuário nesse campo, ele deverá ser o mesmo usuário que você especificou no <strong> campo conta de domínio de banco de dados de conformidade e auditoria </strong> na <strong> página Configurar relatórios </strong> .</span><span class="sxs-lookup"><span data-stu-id="1281d-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="1281d-158">Se você inserir um grupo nesse campo, o valor especificado no <strong> campo conta do domínio do banco de dados de auditoria e de auditoria </strong> na <strong> página Configurar relatórios </strong> deve ser um membro do grupo especificado nesse campo.</span><span class="sxs-lookup"><span data-stu-id="1281d-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="1281d-159">Vá para a próxima seção para configurar o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1281d-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="1281d-160">Para configurar o banco de dados de recuperação usando o assistente</span><span class="sxs-lookup"><span data-stu-id="1281d-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="1281d-161">Usando as descrições a seguir, insira os valores de campo no assistente:</span><span class="sxs-lookup"><span data-stu-id="1281d-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1281d-162">Campo</span><span class="sxs-lookup"><span data-stu-id="1281d-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="1281d-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="1281d-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1281d-164">Nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="1281d-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-165">Nome do servidor no qual você está configurando o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1281d-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1281d-166">Observação</span><span class="sxs-lookup"><span data-stu-id="1281d-166">Note</span></span></strong><br/><p><span data-ttu-id="1281d-167">Você deve adicionar uma exceção no computador do banco de dados de recuperação para habilitar o tráfego de entrada na porta do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1281d-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="1281d-168">O número da porta padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="1281d-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1281d-169">Instância de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="1281d-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-170">Nome da instância de banco de dados na qual os dados de recuperação serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="1281d-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="1281d-171">Você também deve especificar onde as informações do banco de dados serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="1281d-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1281d-172">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="1281d-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-173">Nome do banco de dados que armazenará os dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1281d-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1281d-174">Observação</span><span class="sxs-lookup"><span data-stu-id="1281d-174">Note</span></span></strong><br/><p><span data-ttu-id="1281d-175">Se você estiver atualizando de uma versão anterior do MBAM, deverá usar o mesmo nome de banco de dados que o nome que foi usado na implantação anterior.</span><span class="sxs-lookup"><span data-stu-id="1281d-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1281d-176">Usuário ou grupo de domínio de acesso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1281d-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1281d-177">Usuário ou grupo de domínio que tem permissão de leitura/gravação para esse banco de dados para habilitar os aplicativos Web para acessar os dados e relatórios nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1281d-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="1281d-178">Se você inserir um usuário nesse campo, ele deve ter o mesmo valor que o valor no <strong> campo conta de domínio do pool de aplicativos de serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="1281d-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="1281d-179">Se você inserir um grupo nesse campo, o valor no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> deve ser um membro do grupo que você inserir nesse campo.</span><span class="sxs-lookup"><span data-stu-id="1281d-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="1281d-180">Quando terminar as entradas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1281d-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="1281d-181">O assistente verifica se todos os pré-requisitos dos bancos de dados foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="1281d-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="1281d-182">Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1281d-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="1281d-183">Caso contrário, resolva todos os pré-requisitos ausentes e, em seguida, clique em **Avançar** novamente.</span><span class="sxs-lookup"><span data-stu-id="1281d-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="1281d-184">Na página **Resumo** , examine os recursos que serão adicionados.</span><span class="sxs-lookup"><span data-stu-id="1281d-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="1281d-185">Observação</span><span class="sxs-lookup"><span data-stu-id="1281d-185">Note</span></span>**  
   <span data-ttu-id="1281d-186">Para criar um script do Windows PowerShell das entradas que você acabou de fazer, clique em **Exportar script do PowerShell**e salve o script.</span><span class="sxs-lookup"><span data-stu-id="1281d-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="1281d-187">Clique em **Adicionar** para adicionar os bancos de dados do MBAM no servidor e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="1281d-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="1281d-188">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1281d-188">Related topics</span></span>


[<span data-ttu-id="1281d-189">Logs de eventos do servidor</span><span class="sxs-lookup"><span data-stu-id="1281d-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="1281d-190">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="1281d-191">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="1281d-192">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="1281d-193">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1281d-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="1281d-194">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="1281d-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1281d-195">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1281d-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="1281d-196">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1281d-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





