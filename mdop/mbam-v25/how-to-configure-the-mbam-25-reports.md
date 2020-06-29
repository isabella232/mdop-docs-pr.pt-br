---
title: Como configurar os relatórios do MBAM 2.5
description: Como configurar os relatórios do MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799908"
---
# <span data-ttu-id="c5e83-103">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="c5e83-104">Este tópico explica como configurar o recurso de relatórios do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando:</span><span class="sxs-lookup"><span data-stu-id="c5e83-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="c5e83-105">Um cmdlet do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5e83-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="c5e83-106">O assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="c5e83-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="c5e83-107">As instruções se baseiam na arquitetura recomendada na [arquitetura de alto nível do MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="c5e83-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="c5e83-108">Antes de iniciar a configuração:</span><span class="sxs-lookup"><span data-stu-id="c5e83-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5e83-109">Etapa</span><span class="sxs-lookup"><span data-stu-id="c5e83-109">Step</span></span></th>
<th align="left"><span data-ttu-id="c5e83-110">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="c5e83-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5e83-111">Examine a arquitetura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="c5e83-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="c5e83-112">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5e83-113">Examine as configurações com suporte para MBAM.</span><span class="sxs-lookup"><span data-stu-id="c5e83-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="c5e83-114">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5e83-115">Complete os pré-requisitos obrigatórios em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="c5e83-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="c5e83-116">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c5e83-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="c5e83-117">MBAM 2,5-pré-requisitos do servidor que se aplicam somente à topologia de integração do Configuration Manager </a> (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="c5e83-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5e83-118">Instale o software do servidor MBAM em cada servidor em que você planeja configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="c5e83-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="c5e83-119">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5e83-120">Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar cmdlets do Windows PowerShell para configurar os recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="c5e83-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="c5e83-121">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5e83-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c5e83-122">Para configurar os relatórios usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5e83-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c5e83-123">Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5e83-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="c5e83-124">Use o cmdlet **Enable-MbamReport** do Windows PowerShell para configurar os relatórios.</span><span class="sxs-lookup"><span data-stu-id="c5e83-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="c5e83-125">Para obter informações sobre esse cmdlet do Windows PowerShell, digite **Get-Help Enable-MbamReport**.</span><span class="sxs-lookup"><span data-stu-id="c5e83-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="c5e83-126">Para configurar os relatórios usando o assistente</span><span class="sxs-lookup"><span data-stu-id="c5e83-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="c5e83-127">No servidor em que você deseja configurar os relatórios, inicie o assistente de **configuração do MBAM Server** .</span><span class="sxs-lookup"><span data-stu-id="c5e83-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="c5e83-128">Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.</span><span class="sxs-lookup"><span data-stu-id="c5e83-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="c5e83-129">Clique em **Adicionar novos recursos**, selecione **relatórios**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c5e83-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="c5e83-130">O assistente verifica se todos os pré-requisitos dos relatórios foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="c5e83-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="c5e83-131">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="c5e83-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="c5e83-132">Usando as descrições a seguir, insira os valores de campo no assistente:</span><span class="sxs-lookup"><span data-stu-id="c5e83-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c5e83-133">Campo</span><span class="sxs-lookup"><span data-stu-id="c5e83-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="c5e83-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5e83-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c5e83-135">Instância do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="c5e83-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c5e83-136">Instância do SQL Server Reporting Services em que os relatórios serão configurados.</span><span class="sxs-lookup"><span data-stu-id="c5e83-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c5e83-137">Grupo de domínio da função de relatório</span><span class="sxs-lookup"><span data-stu-id="c5e83-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c5e83-138">Nome do grupo usuários do domínio cujos membros têm direitos para acessar os relatórios no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="c5e83-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c5e83-139">Nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="c5e83-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c5e83-140">Nome do servidor em que o banco de dados de conformidade e auditoria está configurado.</span><span class="sxs-lookup"><span data-stu-id="c5e83-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c5e83-141">Instância de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="c5e83-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c5e83-142">Nome da instância do SQL Server (por exemplo, <em> MSSQLSERVER </em> ) em que o banco de dados de conformidade e auditoria está configurado.</span><span class="sxs-lookup"><span data-stu-id="c5e83-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="c5e83-143">Observação</span><span class="sxs-lookup"><span data-stu-id="c5e83-143">Note</span></span></strong><br/><p><span data-ttu-id="c5e83-144">Você deve adicionar uma exceção no computador relatórios para habilitar o tráfego de entrada na porta do servidor de relatório (a porta padrão é 80).</span><span class="sxs-lookup"><span data-stu-id="c5e83-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c5e83-145">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="c5e83-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c5e83-146">Nome do banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="c5e83-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="c5e83-147">Por padrão, o nome do banco de dados é <strong> MBAM status de conformidade </strong> , embora você possa alterar o nome ao configurar o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="c5e83-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="c5e83-148">Observação</span><span class="sxs-lookup"><span data-stu-id="c5e83-148">Note</span></span></strong><br/><p><span data-ttu-id="c5e83-149">Se você estiver atualizando de uma versão anterior do MBAM, deverá usar o mesmo nome de banco de dados que o nome usado em sua implantação anterior.</span><span class="sxs-lookup"><span data-stu-id="c5e83-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c5e83-150">Conta de domínio de banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="c5e83-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c5e83-151">Conta de usuário do domínio e senha para acessar o banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="c5e83-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="c5e83-152">Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um usuário, você deverá digitar esse mesmo valor neste campo.</span><span class="sxs-lookup"><span data-stu-id="c5e83-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="c5e83-153">Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um grupo, o valor que você inserir nesse campo deve ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="c5e83-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="c5e83-154">Configure a senha desta conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="c5e83-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="c5e83-155">A conta de usuário deve ser capaz de acessar todos os dados que estão disponíveis para o grupo de usuários do MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="c5e83-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="c5e83-156">Quando terminar as entradas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c5e83-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="c5e83-157">O assistente verifica se todos os pré-requisitos do recurso relatórios foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="c5e83-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="c5e83-158">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="c5e83-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="c5e83-159">Na página **Resumo** , examine os recursos que serão adicionados.</span><span class="sxs-lookup"><span data-stu-id="c5e83-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="c5e83-160">Observação</span><span class="sxs-lookup"><span data-stu-id="c5e83-160">Note</span></span>**  
   <span data-ttu-id="c5e83-161">Para criar um script do Windows PowerShell das entradas que você acabou de fazer, clique em **Exportar script do PowerShell**e salve o script.</span><span class="sxs-lookup"><span data-stu-id="c5e83-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="c5e83-162">Clique em **Adicionar** para adicionar os relatórios no servidor e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="c5e83-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="c5e83-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5e83-163">Related topics</span></span>


[<span data-ttu-id="c5e83-164">Logs de eventos do servidor</span><span class="sxs-lookup"><span data-stu-id="c5e83-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="c5e83-165">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="c5e83-166">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="c5e83-167">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c5e83-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="c5e83-168">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="c5e83-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c5e83-169">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c5e83-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c5e83-170">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c5e83-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






