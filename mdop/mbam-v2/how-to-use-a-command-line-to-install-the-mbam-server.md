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
# Como usar uma linha de comando para instalar o Servidor do MBAM


Você pode usar uma linha de comando para instalar o servidor MBAM com a topologia autônoma ou do Configuration Manager. O exemplo de linha de comando a seguir é para implantar MBAM em um único servidor, que é uma arquitetura que deve ser usada somente em um ambiente de teste. Você precisará alterar a linha de comando adequadamente ao implantar o MBAM em um ambiente de produção, que deve ter vários servidores.

## Linha de comando para a implantação do servidor do MBAM 2.0 com a topologia autônoma


Você pode usar uma linha de comando semelhante à seguinte para instalar o servidor MBAM com a topologia autônoma.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

A tabela a seguir descreve os parâmetros de linha de comando para a implantação do servidor MBAM com a topologia autônoma.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Valor do parâmetro</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGIA</p></td>
<td align="left"><p>0</p></td>
<td align="left"><p>0 – topologia autônoma</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>Dezembro</p></td>
<td align="left"><p>0 – não aceitar o contrato de licença agreement1-aceitar o contrato de licença</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Recursos a serem instalados no servidor</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Banco de dados</p></td>
<td align="left"><p>Banco de dados de recuperação</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>Banco de dados de relatórios de auditoria e conformidade</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Relatórios</p></td>
<td align="left"><p>Relatórios de conformidade e auditoria</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>Site de administração e monitoramento</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>Portal de autoatendimento</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Políticatemplate</p></td>
<td align="left"><p>Modelo de política de grupo MBAM</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>Conta de domínio e de usuário da conta de serviço do Reporting Services que irá acessar o banco de dados de auditoria e conformidade</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Senha da conta de serviço do Reporting Services que vai acessar o banco de dados de auditoria e conformidade</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>% ComputerName%</p></td>
<td align="left"><p>Nome da instância do SQL Server para o banco de dados de conformidade e auditoria – substituir <strong> % ComputerName% </strong> pelo nome do computador</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>% ComputerName%</p></td>
<td align="left"><p>Nome da instância do SQL Server para o banco de dados de recuperação – substituir <strong> % ComputerName% </strong> pelo nome do computador</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>% ComputerName%</p></td>
<td align="left"><p>Instância do servidor de relatórios do SQL Server na qual os relatórios de conformidade e auditoria serão instalados – substitua <strong> % ComputerName% </strong> pelo nome do computador</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta para o site de administração e monitoramento; "83" é apenas um exemplo</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta para o site do portal de autoatendimento; "83" é apenas um exemplo</p></td>
</tr>
</tbody>
</table>

 

## Linha de comando para a implantação do servidor do MBAM 2.0 com a topologia do Configuration Manager


Você pode usar uma linha de comando semelhante à seguinte para instalar o servidor MBAM com a topologia do Configuration Manager.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

A tabela a seguir descreve os parâmetros de linha de comando para instalar o MBAM 2.0 Server com a topologia do Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Valor do parâmetro</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGIA</p></td>
<td align="left"><p>um</p></td>
<td align="left"><p>1 – topologia do Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>Dezembro</p></td>
<td align="left"><p>0 – não aceitar o contrato de licença agreement1-aceitar o contrato de licença</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>% ComputerName%</p></td>
<td align="left"><p>Nome da instância do SQL Server para o banco de dados de auditoria – substituir <strong> % ComputerName% </strong> pelo nome do computador</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>% ComputerName%</p></td>
<td align="left"><p>Nome da instância do SQL Server para o banco de dados de recuperação: substituir <strong> % ComputerName% </strong> pelo nome do computador</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>% ComputerName%</p></td>
<td align="left"><p>Instância do servidor de relatórios do SQL Server na qual os relatórios de auditoria serão instalados – substitua% ComputerName% pelo nome do computador</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>Conta de domínio e de usuário da conta de serviço do Reporting Services que irá acessar o banco de dados de auditoria e conformidade</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Senha da conta de serviço do Reporting Services que vai acessar o banco de dados de auditoria e conformidade</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta para o site de administração e monitoramento; "83" é apenas um exemplo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Porta para o site do portal de autoatendimento; "83" é apenas um exemplo</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Implantação da infraestrutura de servidor do MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





