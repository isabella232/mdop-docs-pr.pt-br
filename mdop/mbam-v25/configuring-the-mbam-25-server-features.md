---
title: Configurando os recursos de servidor do MBAM 2.5
description: Configurando os recursos de servidor do MBAM 2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799196"
---
# Configurando os recursos de servidor do MBAM 2.5


Use estas informações como um local inicial para configurar os recursos do servidor do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 após [a instalação do software do MBAM 2,5 Server](installing-the-mbam-25-server-software.md). Há dois métodos que você pode usar para configurar o MBAM:

-   Assistente de configuração do servidor do MBAM

-   Cmdlets do Windows PowerShell

## Antes de começar a configurar os recursos do MBAM Server


Examine e conclua as etapas a seguir antes de começar a configurar os recursos do servidor do MBAM:

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
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Instale o software do servidor MBAM em cada servidor em que você irá configurar um recurso do servidor MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Examine os pré-requisitos para usar o Windows PowerShell para configurar os recursos do MBAM Server (se você estiver usando esse método para configurar os recursos do MBAM Server).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>

 

## Etapas para configurar os recursos do MBAM Server


Cada linha na tabela a seguir descreve os recursos que você irá configurar em um servidor separado, de acordo com a [arquitetura de alto nível recomendada para o MBAM 2,5](high-level-architecture-for-mbam-25.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Recursos para instalar</th>
<th align="left">Onde obter instruções</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurar os bancos de dados.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Como configurar os bancos de dados do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar os relatórios.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Como configurar os relatórios do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar os aplicativos Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Como configurar os aplicativos Web do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar a integração do System Center Configuration Manager (se aplicável).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>

 

Para obter uma lista de eventos sobre a configuração de recursos do servidor do MBAM, consulte [logs de eventos do servidor](server-event-logs.md).



## Tópicos relacionados


Configurando os recursos de servidor do MBAM 2.5
 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




