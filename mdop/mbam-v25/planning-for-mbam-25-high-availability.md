---
title: Planejando a alta disponibilidade do MBAM 2.5
description: Planejando a alta disponibilidade do MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799973"
---
# <span data-ttu-id="abdc4-103">Planejando a alta disponibilidade do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="abdc4-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="abdc4-104">A administração e o monitoramento do Microsoft BitLocker (MBAM) podem manter a alta disponibilidade por meio de uma ou mais das seguintes tecnologias, que estão descritas nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="abdc4-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="abdc4-105">Grupos de disponibilidade do SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="abdc4-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="abdc4-106">Clustering do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="abdc4-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="abdc4-107">Balanceamento de carga de rede do IIS</span><span class="sxs-lookup"><span data-stu-id="abdc4-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="abdc4-108">Espelhamento de banco de dados no SQL Server</span><span class="sxs-lookup"><span data-stu-id="abdc4-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="abdc4-109">Fazendo backup de bancos de dados do MBAM usando o serviço de cópias de sombra de volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="abdc4-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="abdc4-110">Use as informações das seções a seguir para ajudá-lo a entender as opções de implantação do MBAM em uma configuração altamente disponível.</span><span class="sxs-lookup"><span data-stu-id="abdc4-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="abdc4-111">Suporte para os grupos de disponibilidade do SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="abdc4-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="abdc4-112">O MBAM permite que você configure e gerencie grupos de disponibilidade para bancos de dados no Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abdc4-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="abdc4-113">Um grupo de disponibilidade para MBAM dá suporte a um ambiente de failover em que o banco de dados de conformidade e auditoria e o banco de dados de recuperação falham juntos em vez de separadamente.</span><span class="sxs-lookup"><span data-stu-id="abdc4-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="abdc4-114">Um grupo de disponibilidade dá suporte a um conjunto de bancos de dados primários de leitura/gravação e a um a quatro conjuntos de bancos de dados secundários correspondentes.</span><span class="sxs-lookup"><span data-stu-id="abdc4-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="abdc4-115">Opcionalmente, bancos de dados secundários podem ser disponibilizados para permissão somente leitura, algumas operações de backup ou para ambos.</span><span class="sxs-lookup"><span data-stu-id="abdc4-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="abdc4-116">Para obter informações sobre como configurar grupos de disponibilidade, consulte [grupos de disponibilidade de AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).</span><span class="sxs-lookup"><span data-stu-id="abdc4-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="abdc4-117">Clustering do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="abdc4-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="abdc4-118">Você pode executar o banco de dados de auditoria e conformidade do MBAM 2,5 e o banco de dados de recuperação em computadores que executam clusters do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abdc4-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="abdc4-119">Balanceamento de carga de rede do IIS</span><span class="sxs-lookup"><span data-stu-id="abdc4-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="abdc4-120">Você pode usar o balanceamento de carga de rede para configurar um ambiente altamente disponível para computadores que executam o site de administração e monitoramento (também conhecido como suporte técnico), o portal de autoatendimento e os serviços Web, que são implantados através dos serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="abdc4-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="abdc4-121">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="abdc4-121">Prerequisites</span></span>

<span data-ttu-id="abdc4-122">Antes de configurar o balanceamento de carga, verifique se você atendeu aos seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="abdc4-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="abdc4-123">Um balanceador de carga deve estar disponível.</span><span class="sxs-lookup"><span data-stu-id="abdc4-123">A load balancer must be available.</span></span> <span data-ttu-id="abdc4-124">Você pode usar balanceadores de carga da Microsoft ou de outra empresa.</span><span class="sxs-lookup"><span data-stu-id="abdc4-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="abdc4-125">Para obter mais informações sobre a tecnologia de balanceador de carga da Microsoft, consulte [compilar um Web farm com servidores IIS](https://go.microsoft.com/fwlink/?LinkId=393326).</span><span class="sxs-lookup"><span data-stu-id="abdc4-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="abdc4-126">Pelo menos dois servidores estão executando o IIS e atingiram todos os pré-requisitos do MBAM para dar suporte a seus recursos da Web, incluindo o ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="abdc4-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="abdc4-127">Os bancos de dados e relatórios do MBAM são executados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="abdc4-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="abdc4-128">MBAM: alterações específicas necessárias para habilitar o balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="abdc4-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="abdc4-129">Conclua as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="abdc4-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="abdc4-130">Registre um SPN (nome da entidade de serviço) para o nome do host virtual na conta de domínio que você está usando para os pools de aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="abdc4-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="abdc4-131">Por exemplo, se o nome do host virtual for mbamvirtual.contoso.com e a conta de domínio usada para os pools de aplicativos Web for contoso\\mbamapppooluser, o comando a seguir registrará adequadamente o SPN.</span><span class="sxs-lookup"><span data-stu-id="abdc4-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="abdc4-132">Configure os seguintes recursos da Web do MBAM:</span><span class="sxs-lookup"><span data-stu-id="abdc4-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="abdc4-133">Em cada servidor que hospedará os recursos da Web do MBAM, use a mesma conta de domínio para as credenciais administrativas do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="abdc4-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="abdc4-134">Especifique um nome de host que corresponda ao nome de host virtual (nome DNS) do cluster de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="abdc4-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="abdc4-135">Por exemplo, quando você instala o MBAM em um servidor chamado "NLB1" com um nome de host virtual de **mbamvirtual.contoso.com**, certifique-se de que o nome do host especificado no cmdlet do Windows PowerShell é **mbamvirtual.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="abdc4-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="abdc4-136">Se você estiver configurando os sites em um farm da Web com um balanceador de carga, será necessário configurar os websites para usar a mesma chave de máquina.</span><span class="sxs-lookup"><span data-stu-id="abdc4-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="abdc4-137">Para obter mais informações, consulte as seções a seguir no [elemento machineKey (esquema de configurações do ASP.net)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span><span class="sxs-lookup"><span data-stu-id="abdc4-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="abdc4-138">Chave do computador explicada</span><span class="sxs-lookup"><span data-stu-id="abdc4-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="abdc4-139">Considerações sobre a implantação do Web farm</span><span class="sxs-lookup"><span data-stu-id="abdc4-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="abdc4-140">Para obter instruções sobre como gerar uma chave automaticamente, consulte [gerar uma chave do computador (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span><span class="sxs-lookup"><span data-stu-id="abdc4-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="abdc4-141">As informações sobre balanceamento de carga também se aplicam aos clusters de balanceamento de carga de rede (NLB) do IIS no Windows Server 2012 ou no Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="abdc4-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="abdc4-142">A funcionalidade de balanceamento de carga de rede do IIS no Windows Server 2012 geralmente é a mesma que no Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="abdc4-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="abdc4-143">No entanto, alguns detalhes da tarefa são diferentes no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="abdc4-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="abdc4-144">Para obter informações sobre novas maneiras de realizar tarefas, consulte [tarefas comuns de gerenciamento e navegação no Windows server 2012 R2 Preview e no Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span><span class="sxs-lookup"><span data-stu-id="abdc4-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="abdc4-145">Espelhamento de banco de dados no SQL Server</span><span class="sxs-lookup"><span data-stu-id="abdc4-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="abdc4-146">O MBAM dá suporte ao uso do espelhamento do SQL Server, em que o banco de dados de conformidade e auditoria e o banco de dados de recuperação são espelhados usando duas instâncias do SQL Server para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="abdc4-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="abdc4-147">Antes de implementar o espelhamento, lembre-se de que o espelhamento está lento, em favor dos grupos de disponibilidade, que são discutidos anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="abdc4-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="abdc4-148">Para implementar o espelhamento para MBAM, você deve especificar as cadeias de caracteres de conexão adequadas para a configuração do banco de dados espelhado usando o cmdlet **Enable-MbamWebApplication** do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="abdc4-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="abdc4-149">Para obter mais informações sobre os cmdlets do Windows PowerShell do MBAM 2,5, consulte [configurando recursos do MBAM do 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="abdc4-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="abdc4-150">Exemplos de implementação de espelhamento do SQL Server usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="abdc4-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="abdc4-151">Os exemplos a seguir mostram como você pode implementar o espelhamento do SQL Server usando cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="abdc4-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="abdc4-152">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="abdc4-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="abdc4-153">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="abdc4-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="abdc4-154">Mais informações sobre o espelhamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="abdc4-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="abdc4-155">Os links a seguir fornecem mais informações sobre como configurar o espelhamento do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="abdc4-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="abdc4-156">Como: preparar um banco de dados espelho para espelhamento (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="abdc4-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="abdc4-157">Estabelecer uma sessão de espelhamento de banco de dados usando a autenticação do Windows (SQL Server Management Studio)</span><span class="sxs-lookup"><span data-stu-id="abdc4-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="abdc4-158">Fazendo backup de bancos de dados do MBAM usando o serviço de cópias de sombra de volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="abdc4-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="abdc4-159">O MBAM fornece um gravador de Volume Shadow Copy Service (VSS), chamado de Microsoft BitLocker Administration and Management Writer.</span><span class="sxs-lookup"><span data-stu-id="abdc4-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="abdc4-160">Esse gravador VSS facilita o backup do banco de dados de conformidade e auditoria e do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="abdc4-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="abdc4-161">O gravador VSS é registrado em todos os servidores em que você habilita um aplicativo Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="abdc4-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="abdc4-162">O gravador VSS do MBAM depende do gravador VSS do SQL Server, que é registrado como parte da instalação do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abdc4-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="abdc4-163">Qualquer tecnologia de backup que usa gravadores VSS para executar o backup pode descobrir o gravador VSS do MBAM.</span><span class="sxs-lookup"><span data-stu-id="abdc4-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="abdc4-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abdc4-164">Related topics</span></span>


[<span data-ttu-id="abdc4-165">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="abdc4-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="abdc4-166">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="abdc4-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="abdc4-167">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="abdc4-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="abdc4-168">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="abdc4-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




