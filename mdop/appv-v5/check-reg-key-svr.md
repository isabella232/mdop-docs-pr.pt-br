---
title: Verificar as chaves do Registro antes de instalar o servidor do App-V 5.x
description: Verificar as chaves do Registro antes de instalar o servidor do App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796567"
---
# Verificar as chaves do Registro antes de instalar o servidor do App-V 5.x

Se você estiver atualizando o pacote do pacote do aplicativo App-V do App-V 5,0 SP1 3 ou posterior, conclua as etapas desta seção antes de instalar o App-V 5. x Server

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quando essa etapa é necessária</strong></p></td>
<td align="left"><p>Você está atualizando do App-V 5,0 SP1 com qualquer pacote de hotfix subsequente que você instalou usando um arquivo. msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Quais componentes exigem que você siga esta etapa</strong></p></td>
<td align="left"><p>Somente os componentes do App-V Server que você está atualizando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Quando precisar fazer esta etapa</strong></p></td>
<td align="left"><p>Antes de atualizar o servidor do App-V para o App-V 5. x</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>O que você precisa fazer</strong></p></td>
<td align="left"><p>Usando as informações nas tabelas a seguir, atualize cada valor de chave do registro sob <code>HKLM\Software\Microsoft\AppV\Server</code> o valor que você forneceu na instalação do servidor original. Concluir esta etapa restaura os valores do registro que podem ter sido removidos quando os pacotes de hotfix do App-V 5,0 SP1 foram instalados.</p></td>
</tr>
</tbody>
</table>

 

**Chave ManagementDatabase**

Se você estiver instalando o banco de dados de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Descreve se uma conta de acesso público é necessária para acessar bancos de dados de gerenciamento não locais. Valor é definido como "1" se for necessário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Nome do banco de dados de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</p>
<p>Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</p>
<p>Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server para o banco de dados de gerenciamento.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) da conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Conta de computador remoto do servidor de gerenciamento (domínio \ conta).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Logon de administrador de instalação para o servidor de gerenciamento (domínio \ conta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valores válidos são:</p>
<ul>
<li><p><strong>1 </strong> – o serviço de gerenciamento está no computador local, ou seja, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</p></li>
<li><p><strong>0 </strong> - o serviço de gerenciamento está em um computador diferente do computador local.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Chave ManagementService**

Se você estiver instalando o servidor de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Conta ou grupo dos serviços de domínio Active Directory (AD DS) que está autorizado a gerenciar o App-V (domínio de domínio).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server que contém o banco de dados de gerenciamento.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nome do SQL Server remoto com o banco de dados de gerenciamento.</p>
<p>Se o valor estiver em branco, o computador local será usado.</p></td>
</tr>
</tbody>
</table>

 

**Chave ReportingDatabase**

Se você estiver instalando o banco de dados de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Descreve se uma conta de acesso público é necessária para acessar bancos de dados de relatório não locais. Valor é definido como "1" se for necessário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Nome do banco de dados de relatório.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</p>
<p>Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</p>
<p>Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server para o banco de dados de relatórios.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Conta de computador remoto do servidor de relatório (domínio \ conta).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Login de administrador de instalação para o servidor de relatórios (domínio \ conta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valores válidos são:</p>
<ul>
<li><p><strong>1 </strong> – o serviço de relatório está no computador local, ou seja, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</p></li>
<li><p><strong>0 </strong> - o serviço de relatório está em um computador diferente do computador local.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Chave ReportingService**

Se você estiver instalando o servidor de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server para o banco de dados de relatórios.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nome do SQL Server remoto com o banco de dados de relatórios.</p>
<p>Se o valor estiver em branco, o computador local será usado.</p></td>
</tr>
</tbody>
</table>

