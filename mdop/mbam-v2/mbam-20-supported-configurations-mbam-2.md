---
title: Configurações com suporte no MBAM 2.0
description: Configurações com suporte no MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799366"
---
# Configurações com suporte no MBAM 2.0


Este tópico especifica os requisitos para instalar e executar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 em seu ambiente usando a topologia autônoma. Para configurações compatíveis que se aplicam a versões posteriores, consulte a documentação da versão aplicável.

Se você planeja instalar o MBAM 2,0 usando a topologia do Configuration Manager e deseja revisar uma lista dos requisitos do sistema, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

A configuração recomendada para executar o MBAM em um ambiente de produção é com dois servidores, dependendo dos requisitos de redimensionamento. Essa configuração dá suporte a até 200.000 clientes MBAM. Para obter uma imagem e descrições da infraestrutura autônoma do servidor MBAM, consulte [arquitetura de alto nível para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

## <a href="" id="---------mbam-server-system-requirements"></a> Requisitos do sistema do MBAM Server


### Requisitos do sistema operacional do servidor

A tabela a seguir lista os sistemas operacionais suportados para a instalação do Microsoft BitLocker Administration and Monitoring Server.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Edição padrão ou de datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

**Observação**  Não há suporte para a instalação de serviços, relatórios ou bancos de dados do MBAM em um computador controlador de domínio.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>Requisitos do processador do servidor, da RAM e do espaço em disco

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de hardware</th>
<th align="left">Necessidade mínima</th>
<th align="left">Necessidade recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processador</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou mais</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço livre em disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a>Requisitos do banco de dados do SQLServer

A tabela a seguir lista as versões do SQLServer com suporte para a instalação de recursos do servidor de administração e monitoramento, que inclui o banco de dados de recuperação, o banco de dados de auditoria e conformidade e os relatórios de conformidade e auditoria. Os bancos de dados também exigem a instalação das ferramentas de gerenciamento do SQL Server.

**Observação**  O MBAM não oferece suporte nativo a grupos de clusters, espelhamento ou clusters de SQL. Para instalar os bancos de dados, você deve executar a instalação do servidor do MBAM em um SQL Server autônomo.

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do SQL Server</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de hardware</th>
<th align="left">Necessidade mínima</th>
<th align="left">Necessidade recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processador</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou mais</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço livre em disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB ou mais</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> Requisitos do sistema do cliente MBAM


### Requisitos do sistema operacional do cliente

A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente de administração e monitoramento do Microsoft BitLocker.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Edição Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Edição do Windows 8 Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>Requisitos de RAM do cliente

Não há nenhuma necessidade de RAM específica para a instalação do cliente de administração e monitoramento do Microsoft BitLocker.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Requisitos do sistema da política de grupo do MBAM


A tabela a seguir lista os sistemas operacionais suportados para a instalação do modelo de política de grupo do Microsoft BitLocker Administration and Monitoring.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Edição Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Edição padrão ou de datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Planejar a implantação do MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Pré-requisitos para implantação do MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





