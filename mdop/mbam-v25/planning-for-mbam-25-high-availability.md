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
# Planejando a alta disponibilidade do MBAM 2.5


A administração e o monitoramento do Microsoft BitLocker (MBAM) podem manter a alta disponibilidade por meio de uma ou mais das seguintes tecnologias, que estão descritas nas seguintes seções:

-   [Grupos de disponibilidade do SQL Server AlwaysOn](#bkmk-alwayson)

-   [Clustering do Microsoft SQL Server](#bkmk-sql-clustering)

-   [Balanceamento de carga de rede do IIS](#bkmk-load-balance)

-   [Espelhamento de banco de dados no SQL Server](#bkmk-db-mirroring)

-   [Fazendo backup de bancos de dados do MBAM usando o serviço de cópias de sombra de volume (VSS)](#bkmk-vss)

Use as informações das seções a seguir para ajudá-lo a entender as opções de implantação do MBAM em uma configuração altamente disponível.

## <a href="" id="bkmk-alwayson"></a>Suporte para os grupos de disponibilidade do SQL Server AlwaysOn


O MBAM permite que você configure e gerencie grupos de disponibilidade para bancos de dados no Microsoft SQL Server. Um grupo de disponibilidade para MBAM dá suporte a um ambiente de failover em que o banco de dados de conformidade e auditoria e o banco de dados de recuperação falham juntos em vez de separadamente.

Um grupo de disponibilidade dá suporte a um conjunto de bancos de dados primários de leitura/gravação e a um a quatro conjuntos de bancos de dados secundários correspondentes. Opcionalmente, bancos de dados secundários podem ser disponibilizados para permissão somente leitura, algumas operações de backup ou para ambos.

Para obter informações sobre como configurar grupos de disponibilidade, consulte [grupos de disponibilidade de AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).

## <a href="" id="bkmk-sql-clustering"></a>Clustering do Microsoft SQL Server


Você pode executar o banco de dados de auditoria e conformidade do MBAM 2,5 e o banco de dados de recuperação em computadores que executam clusters do SQL Server.

## <a href="" id="bkmk-load-balance"></a>Balanceamento de carga de rede do IIS


Você pode usar o balanceamento de carga de rede para configurar um ambiente altamente disponível para computadores que executam o site de administração e monitoramento (também conhecido como suporte técnico), o portal de autoatendimento e os serviços Web, que são implantados através dos serviços de informações da Internet (IIS).

### Pré-requisitos

Antes de configurar o balanceamento de carga, verifique se você atendeu aos seguintes pré-requisitos:

-   Um balanceador de carga deve estar disponível. Você pode usar balanceadores de carga da Microsoft ou de outra empresa. Para obter mais informações sobre a tecnologia de balanceador de carga da Microsoft, consulte [compilar um Web farm com servidores IIS](https://go.microsoft.com/fwlink/?LinkId=393326).

-   Pelo menos dois servidores estão executando o IIS e atingiram todos os pré-requisitos do MBAM para dar suporte a seus recursos da Web, incluindo o ASP.NET MVC 4.

-   Os bancos de dados e relatórios do MBAM são executados em um servidor.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> MBAM: alterações específicas necessárias para habilitar o balanceamento de carga

Conclua as seguintes tarefas:

1.  Registre um SPN (nome da entidade de serviço) para o nome do host virtual na conta de domínio que você está usando para os pools de aplicativos Web. Por exemplo, se o nome do host virtual for mbamvirtual.contoso.com e a conta de domínio usada para os pools de aplicativos Web for contoso\\mbamapppooluser, o comando a seguir registrará adequadamente o SPN.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  Configure os seguintes recursos da Web do MBAM:

    -   Em cada servidor que hospedará os recursos da Web do MBAM, use a mesma conta de domínio para as credenciais administrativas do pool de aplicativos.

    -   Especifique um nome de host que corresponda ao nome de host virtual (nome DNS) do cluster de balanceamento de carga. Por exemplo, quando você instala o MBAM em um servidor chamado "NLB1" com um nome de host virtual de **mbamvirtual.contoso.com**, certifique-se de que o nome do host especificado no cmdlet do Windows PowerShell é **mbamvirtual.contoso.com**.

3.  Se você estiver configurando os sites em um farm da Web com um balanceador de carga, será necessário configurar os websites para usar a mesma chave de máquina.

    Para obter mais informações, consulte as seções a seguir no [elemento machineKey (esquema de configurações do ASP.net)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):

    -   Chave do computador explicada

    -   Considerações sobre a implantação do Web farm

    Para obter instruções sobre como gerar uma chave automaticamente, consulte [gerar uma chave do computador (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).

As informações sobre balanceamento de carga também se aplicam aos clusters de balanceamento de carga de rede (NLB) do IIS no Windows Server 2012 ou no Windows Server2008R2. A funcionalidade de balanceamento de carga de rede do IIS no Windows Server 2012 geralmente é a mesma que no Windows Server2008R2. No entanto, alguns detalhes da tarefa são diferentes no Windows Server 2012. Para obter informações sobre novas maneiras de realizar tarefas, consulte [tarefas comuns de gerenciamento e navegação no Windows server 2012 R2 Preview e no Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).

## <a href="" id="bkmk-db-mirroring"></a>Espelhamento de banco de dados no SQL Server


O MBAM dá suporte ao uso do espelhamento do SQL Server, em que o banco de dados de conformidade e auditoria e o banco de dados de recuperação são espelhados usando duas instâncias do SQL Server para cada banco de dados. Antes de implementar o espelhamento, lembre-se de que o espelhamento está lento, em favor dos grupos de disponibilidade, que são discutidos anteriormente neste tópico.

Para implementar o espelhamento para MBAM, você deve especificar as cadeias de caracteres de conexão adequadas para a configuração do banco de dados espelhado usando o cmdlet **Enable-MbamWebApplication** do Windows PowerShell. Para obter mais informações sobre os cmdlets do Windows PowerShell do MBAM 2,5, consulte [configurando recursos do MBAM do 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

### Exemplos de implementação de espelhamento do SQL Server usando o Windows PowerShell

Os exemplos a seguir mostram como você pode implementar o espelhamento do SQL Server usando cmdlets do Windows PowerShell.

**Exemplo 1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**Exemplo 2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### Mais informações sobre o espelhamento do SQL Server

Os links a seguir fornecem mais informações sobre como configurar o espelhamento do SQL Server:

-   [Como: preparar um banco de dados espelho para espelhamento (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Estabelecer uma sessão de espelhamento de banco de dados usando a autenticação do Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>Fazendo backup de bancos de dados do MBAM usando o serviço de cópias de sombra de volume (VSS)


O MBAM fornece um gravador de Volume Shadow Copy Service (VSS), chamado de Microsoft BitLocker Administration and Management Writer. Esse gravador VSS facilita o backup do banco de dados de conformidade e auditoria e do banco de dados de recuperação.

O gravador VSS é registrado em todos os servidores em que você habilita um aplicativo Web MBAM. O gravador VSS do MBAM depende do gravador VSS do SQL Server, que é registrado como parte da instalação do Microsoft SQL Server. Qualquer tecnologia de backup que usa gravadores VSS para executar o backup pode descobrir o gravador VSS do MBAM.



## Tópicos relacionados


[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




