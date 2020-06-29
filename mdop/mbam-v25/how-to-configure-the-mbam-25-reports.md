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
# Como configurar os relatórios do MBAM 2.5


Este tópico explica como configurar o recurso de relatórios do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando:

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
<td align="left"><p>Instale o software do servidor MBAM em cada servidor em que você planeja configurar um recurso do servidor MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar cmdlets do Windows PowerShell para configurar os recursos do MBAM Server.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar os relatórios usando o Windows PowerShell**

1.  Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.

2.  Use o cmdlet **Enable-MbamReport** do Windows PowerShell para configurar os relatórios. Para obter informações sobre esse cmdlet do Windows PowerShell, digite **Get-Help Enable-MbamReport**.

**Para configurar os relatórios usando o assistente**

1. No servidor em que você deseja configurar os relatórios, inicie o assistente de **configuração do MBAM Server** . Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.

2. Clique em **Adicionar novos recursos**, selecione **relatórios**e, em seguida, clique em **Avançar**. O assistente verifica se todos os pré-requisitos dos relatórios foram atendidos.

3. Clique em **Avançar** para continuar.

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
   <td align="left"><p><strong>Instância do SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>Instância do SQL Server Reporting Services em que os relatórios serão configurados.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Grupo de domínio da função de relatório</strong></p></td>
   <td align="left"><p>Nome do grupo usuários do domínio cujos membros têm direitos para acessar os relatórios no servidor de administração e monitoramento.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nome do SQL Server</strong></p></td>
   <td align="left"><p>Nome do servidor em que o banco de dados de conformidade e auditoria está configurado.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instância de banco de dados do SQL Server</strong></p></td>
   <td align="left"><p>Nome da instância do SQL Server (por exemplo, <em> MSSQLSERVER </em> ) em que o banco de dados de conformidade e auditoria está configurado.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Você deve adicionar uma exceção no computador relatórios para habilitar o tráfego de entrada na porta do servidor de relatório (a porta padrão é 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nome do banco de dados</strong></p></td>
   <td align="left"><p>Nome do banco de dados de conformidade e auditoria. Por padrão, o nome do banco de dados é <strong> MBAM status de conformidade </strong> , embora você possa alterar o nome ao configurar o banco de dados de auditoria e conformidade.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Se você estiver atualizando de uma versão anterior do MBAM, deverá usar o mesmo nome de banco de dados que o nome usado em sua implantação anterior.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Conta de domínio de banco de dados de auditoria e conformidade</strong></p></td>
   <td align="left"><p>Conta de usuário do domínio e senha para acessar o banco de dados de conformidade e auditoria.</p>
   <p>Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um usuário, você deverá digitar esse mesmo valor neste campo.</p>
   <p>Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um grupo, o valor que você inserir nesse campo deve ser um membro desse grupo.</p>
   <p>Configure a senha desta conta para nunca expirar. A conta de usuário deve ser capaz de acessar todos os dados que estão disponíveis para o grupo de usuários do MBAM Reports.</p></td>
   </tr>
   </tbody>
   </table>



5. Quando terminar as entradas, clique em **Avançar**.

   O assistente verifica se todos os pré-requisitos do recurso relatórios foram atendidos.

6. Clique em **Avançar** para continuar.

7. Na página **Resumo** , examine os recursos que serão adicionados.

   **Observação**  
   Para criar um script do Windows PowerShell das entradas que você acabou de fazer, clique em **Exportar script do PowerShell**e salve o script.



8. Clique em **Adicionar** para adicionar os relatórios no servidor e, em seguida, clique em **fechar**.



## Tópicos relacionados


[Logs de eventos do servidor](server-event-logs.md)

[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Como configurar os aplicativos Web do MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Validando a configuração de recursos de servidor do MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






