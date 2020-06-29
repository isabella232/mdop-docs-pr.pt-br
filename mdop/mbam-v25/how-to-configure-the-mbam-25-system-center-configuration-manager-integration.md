---
title: Como configurar a integração do System Center Configuration Manager do MBAM 2.5
description: Como configurar a integração do System Center Configuration Manager do MBAM 2.5
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796001"
---
# Como configurar a integração do System Center Configuration Manager do MBAM 2.5


Este tópico explica como configurar o Microsoft BitLocker Administration and Monitoring (MBAM) para usar a topologia de integração do System Center Configuration Manager, que integra o MBAM com o Configuration Manager.

As instruções explicam como configurar a integração do Configuration Manager usando:

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
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Examine as configurações com suporte para MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complete os pré-requisitos obrigatórios em cada servidor.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Instale o software do servidor MBAM em cada servidor em que você irá configurar um recurso do servidor MBAM.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Para essa topologia, você deve instalar o console do Configuration Manager no computador em que está instalando o software MBAM Server.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Examine os pré-requisitos do Windows PowerShell (aplicável somente se você pretende usar cmdlets do Windows PowerShell para configurar o MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar a integração do Configuration Manager usando o Windows PowerShell**

1.  Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.

2.  Use o cmdlet **Enable-MbamCMIntegration** do Windows PowerShell para configurar os relatórios. Para obter informações sobre esse cmdlet, digite **Get-Help Enable-MbamCMIntegration**.

**Para configurar a integração do System Center Configuration Manager usando o assistente**

1.  No servidor em que você deseja configurar o recurso de integração do System Center Configuration Manager, inicie o assistente de configuração do MBAM Server. Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.

2.  Clique em **Adicionar novos recursos**, selecione **integração com o System Center Configuration Manager**e, em seguida, clique em **Avançar**.

    O assistente verifica se todos os pré-requisitos para a integração do Configuration Manager foram atendidos.

3.  Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.

4.  Use as descrições a seguir para inserir os valores de campo no assistente:

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
    <td align="left"><p><strong>Servidor do SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>FQDN (nome de domínio totalmente qualificado) do servidor com a função de ponto de serviço de relatório. Esse é o servidor ao qual os relatórios do Gerenciador de configuração do MBAM são implantados.</p>
    <p>Se você não especificar um servidor, os relatórios do Configuration Manager serão implantados no servidor local.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instância do SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nome da instância do SQL Server Reporting Services (SSRS) em que os relatórios do Configuration Manager são implantados.</p>
    <p>Se você não especificar uma instância, os relatórios do Configuration Manager serão implantados para o nome da instância padrão do SSRS. O valor que você inserir será ignorado se o servidor tiver o System Center 2012 Configuration Manager instalado.</p></td>
    </tr>
    </tbody>
    </table>



5.  Na página **Resumo** , examine os recursos que serão adicionados.

    **Observação**  
    Para criar um script do Windows PowerShell das entradas que você acabou de fazer, clique em **Exportar script do PowerShell** e salve o script.



6.  Clique em **Adicionar** para adicionar o recurso integração com o Gerenciador de configurações ao servidor e, em seguida, clique em **fechar**.



## Tópicos relacionados


[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Validando a configuração de recursos de servidor do MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






