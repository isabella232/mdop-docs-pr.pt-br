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
# Como configurar os bancos de dados do MBAM 2.5


Este tópico explica como configurar o banco de dados de auditoria e a conformidade do 2,5 do Microsoft BitLocker (MBAM) e o banco de dados de recuperação usando:

-   Um cmdlet do Windows PowerShell

-   O assistente de configuração do servidor do MBAM

As instruções se baseiam na arquitetura recomendada na [arquitetura de alto nível do MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Antes de iniciar a configuração:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Onde obter instruções</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Examine a arquitetura recomendada para MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitetura de alto nível do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Examine as configurações com suporte para MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complete os pré-requisitos obrigatórios em cada servidor.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2,5-pré-requisitos do servidor que se aplicam somente à topologia de integração do Configuration Manager </a> (se aplicável)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Instale o software do servidor MBAM em cada servidor em que você planeja configurar um recurso do servidor MBAM.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Você pode instalar os bancos de dados em um computador remoto do SQL Server usando o Windows PowerShell ou um pacote de aplicativo da camada de dados (DAC) exportado. Para obter mais informações sobre pacotes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicativos da camada de dados </a> .</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar cmdlets do Windows PowerShell para configurar os recursos do MBAM Server.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar os bancos de dados usando o Windows PowerShell**

1.  Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.

2.  Use o cmdlet **Enable-MbamDatabase** do Windows PowerShell para configurar os bancos de dados. Para obter informações sobre esse cmdlet do Windows PowerShell, digite **Get-Help Enable-MbamDatabase**.

**Para configurar o banco de dados de auditoria e conformidade usando o assistente**

1. No servidor em que você deseja configurar os bancos de dados, inicie o assistente de **configuração do servidor do MBAM** . Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.

2. Clique em **Adicionar novos recursos**, selecione **conformidade e auditoria** e banco de dados de **recuperação**e clique em **Avançar**. O assistente verifica se todos os pré-requisitos dos bancos de dados foram atendidos.

3. Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.

4. Usando as descrições a seguir, insira os valores de campo no assistente:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Nome do SQL Server</strong></p></td>
   <td align="left"><p>Nome do servidor no qual você está configurando o banco de dados de conformidade e auditoria.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Você deve adicionar uma exceção no computador de banco de dados de conformidade e auditoria para habilitar o tráfego de entrada na porta do Microsoft SQL Server. O número da porta padrão é 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instância de banco de dados do SQL Server</strong></p></td>
   <td align="left"><p>Nome da instância do banco de dados em que os dados de conformidade e auditoria serão armazenados. Você também deve especificar onde as informações do banco de dados serão localizadas.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nome do banco de dados</strong></p></td>
   <td align="left"><p>Nome do banco de dados que armazenará os dados de conformidade.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Se você estiver atualizando de uma versão anterior do MBAM, deverá usar o mesmo nome de banco de dados que o nome que foi usado na implantação anterior.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Usuário ou grupo de domínio de acesso de leitura/gravação</strong></p></td>
   <td align="left"><p>Usuário ou grupo de domínio que tem permissão de leitura/gravação para esse banco de dados para habilitar os aplicativos Web para acessar os dados e relatórios nesse banco de dados.</p>
   <p>Se você inserir um usuário nesse campo, ele deve ter o mesmo valor que o valor no <strong> campo conta de domínio do pool de aplicativos de serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> .</p>
   <p>Se você inserir um grupo nesse campo, o valor no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> deve ser um membro do grupo que você inserir nesse campo.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Usuário ou grupo de domínio de acesso somente leitura</strong></p></td>
   <td align="left"><p>Nome do usuário ou grupo que terá permissão somente leitura para esse banco de dados para permitir que os relatórios acessem os dados de conformidade nesse banco de dados.</p>
   <p>Se você inserir um usuário nesse campo, ele deverá ser o mesmo usuário que você especificou no <strong> campo conta de domínio de banco de dados de conformidade e auditoria </strong> na <strong> página Configurar relatórios </strong> .</p>
   <p>Se você inserir um grupo nesse campo, o valor especificado no <strong> campo conta do domínio do banco de dados de auditoria e de auditoria </strong> na <strong> página Configurar relatórios </strong> deve ser um membro do grupo especificado nesse campo.</p></td>
   </tr>
   </tbody>
   </table>



5. Vá para a próxima seção para configurar o banco de dados de recuperação.

**Para configurar o banco de dados de recuperação usando o assistente**

1. Usando as descrições a seguir, insira os valores de campo no assistente:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Nome do SQL Server</strong></p></td>
   <td align="left"><p>Nome do servidor no qual você está configurando o banco de dados de recuperação.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Você deve adicionar uma exceção no computador do banco de dados de recuperação para habilitar o tráfego de entrada na porta do Microsoft SQL Server. O número da porta padrão é 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instância de banco de dados do SQL Server</strong></p></td>
   <td align="left"><p>Nome da instância de banco de dados na qual os dados de recuperação serão armazenados. Você também deve especificar onde as informações do banco de dados serão localizadas.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nome do banco de dados</strong></p></td>
   <td align="left"><p>Nome do banco de dados que armazenará os dados de recuperação.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Se você estiver atualizando de uma versão anterior do MBAM, deverá usar o mesmo nome de banco de dados que o nome que foi usado na implantação anterior.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Usuário ou grupo de domínio de acesso de leitura/gravação</strong></p></td>
   <td align="left"><p>Usuário ou grupo de domínio que tem permissão de leitura/gravação para esse banco de dados para habilitar os aplicativos Web para acessar os dados e relatórios nesse banco de dados.</p>
   <p>Se você inserir um usuário nesse campo, ele deve ter o mesmo valor que o valor no <strong> campo conta de domínio do pool de aplicativos de serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> .</p>
   <p>Se você inserir um grupo nesse campo, o valor no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> deve ser um membro do grupo que você inserir nesse campo.</p></td>
   </tr>
   </tbody>
   </table>



2. Quando terminar as entradas, clique em **Avançar**.

   O assistente verifica se todos os pré-requisitos dos bancos de dados foram atendidos.

3. Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e, em seguida, clique em **Avançar** novamente.

4. Na página **Resumo** , examine os recursos que serão adicionados.

   **Observação**  
   Para criar um script do Windows PowerShell das entradas que você acabou de fazer, clique em **Exportar script do PowerShell**e salve o script.



5. Clique em **Adicionar** para adicionar os bancos de dados do MBAM no servidor e, em seguida, clique em **fechar**.



## Tópicos relacionados


[Logs de eventos do servidor](server-event-logs.md)

[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Como configurar os relatórios do MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Como configurar os aplicativos Web do MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Validando a configuração de recursos de servidor do MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





