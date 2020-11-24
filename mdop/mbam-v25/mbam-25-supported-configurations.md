---
title: Configurações com suporte no MBAM 2.5
description: Configurações com suporte no MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182923"
---
# Configurações com suporte no MBAM 2.5


Você pode executar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 em uma topologia autônoma ou em uma topologia de integração do Configuration Manager que integre o MBAM com o System Center Configuration Manager. Se você usar a configuração recomendada para a topologia em um ambiente de produção, o MBAM oferece suporte a até 500.000 clientes do MBAM. Para obter informações sobre a arquitetura e os recursos recomendados que são configurados em cada servidor para cada topologia, consulte [arquitetura de alto nível para MBAM 2,5](high-level-architecture-for-mbam-25.md).

Para configurações adicionais específicas para a topologia de integração do Configuration Manager, confira [versões do Configuration Manager às quais o MBAM oferece suporte](#bkmk-cm-ramreqs).

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



## Idiomas com suporte do MBAM


As tabelas a seguir mostram os idiomas com suporte para o cliente MBAM (incluindo o portal Self-Service) e o servidor MBAM no MBAM 2,5 e MBAM 2,5 SP1.

**Idiomas com suporte no MBAM 2,5 SP1:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Idiomas do cliente</th>
<th align="left">Idiomas do servidor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tcheco (República Tcheca) CS-CZ</p>
<p>Dinamarquês (Dinamarca) da-DK</p>
<p>Holandês (Holanda) nl-NL</p>
<p>Inglês (Estados Unidos) en-US</p>
<p>Finlandês (Finlândia) fi-FI</p>
<p>Francês (França) fr-FR</p>
<p>Alemão (Alemanha) de-DE</p>
<p>Grego (Grécia) El-GA</p>
<p>Húngaro (Hungria) hu-HU</p>
<p>Italiano (Itália) it-IT</p>
<p>Japonês (Japão) ja-JP</p>
<p>Coreano (Coréia) ko-KR</p>
<p>Norueguês, Bokmål (Noruega) NB-não</p>
<p>Polonês (Polônia) pl-PL</p>
<p>Português (Brasil) pt-BR</p>
<p>Português (Portugal) pt-PT</p>
<p>Russo (Rússia) ru-RU</p>
<p>Eslovaco (Eslováquia) SK-SK</p>
<p>Espanhol (Espanha) es-ES</p>
<p>Sueco (Suécia) VA-SE</p>
<p>Turco (Turquia) TR-TR</p>
<p>Esloveno (Eslovênia) SL-SI</p>
<p>Chinês simplificado (República Popular da China) zh-CN</p>
<p>Chinês tradicional (Taiwan) zh-TW</p></td>
<td align="left"><ul>
<li><p>Inglês (Estados Unidos) en-US</p></li>
<li><p>Francês (França) fr-FR</p></li>
<li><p>Alemão (Alemanha) de-DE</p></li>
<li><p>Italiano (Itália) it-IT</p></li>
<li><p>Japonês (Japão) ja-JP</p></li>
<li><p>Coreano (Coréia) ko-KR</p></li>
<li><p>Português (Brasil) pt-BR</p></li>
<li><p>Russo (Rússia) ru-RU</p></li>
<li><p>Espanhol (Espanha) es-ES</p></li>
<li><p>Chinês simplificado (República Popular da China) zh-CN</p></li>
<li><p>Chinês tradicional (Taiwan) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Idiomas com suporte no MBAM 2,5:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Idiomas do cliente</th>
<th align="left">Idiomas do servidor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Inglês (Estados Unidos) en-US</p></li>
<li><p>Francês (França) fr-FR</p></li>
<li><p>Alemão (Alemanha) de-DE</p></li>
<li><p>Italiano (Itália) it-IT</p></li>
<li><p>Japonês (Japão) ja-JP</p></li>
<li><p>Coreano (Coréia) ko-KR</p></li>
<li><p>Português (Brasil) pt-BR</p></li>
<li><p>Russo (Rússia) ru-RU</p></li>
<li><p>Espanhol (Espanha) es-ES</p></li>
<li><p>Chinês simplificado (República Popular da China) zh-CN</p></li>
<li><p>Chinês tradicional (Taiwan) zh-TW</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Inglês (Estados Unidos) en-US</p></li>
<li><p>Francês (França) fr-FR</p></li>
<li><p>Alemão (Alemanha) de-DE</p></li>
<li><p>Italiano (Itália) it-IT</p></li>
<li><p>Japonês (Japão) ja-JP</p></li>
<li><p>Coreano (Coréia) ko-KR</p></li>
<li><p>Português (Brasil) pt-BR</p></li>
<li><p>Russo (Rússia) ru-RU</p></li>
<li><p>Espanhol (Espanha) es-ES</p></li>
<li><p>Chinês simplificado (República Popular da China) zh-CN</p></li>
<li><p>Chinês tradicional (Taiwan) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> Requisitos do sistema do MBAM Server


### Requisitos do sistema operacional do MBAM Server

É altamente recomendável que você execute o cliente MBAM e o MBAM Server na mesma linha de sistemas operacionais. Por exemplo, Windows 10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.

A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor do MBAM.

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
<td align="left"><p>Windows Server 2019</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



O domínio da empresa deve conter pelo menos um controlador de domínio do Windows Server 2008 (ou posterior).

### <a href="" id="bkmk-stand-alone-ramreqs"></a>MBAM do processador do servidor, RAM e requisitos de espaço em disco – topologia autônoma

Esses requisitos são para a topologia autônoma do MBAM. Para obter os requisitos para a topologia de integração do Configuration Manager, consulte [topologia do processador do servidor MBAM, RAM e requisitos de espaço em disco – topologia de integração do Configuration Manager](#bkmk-cm-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item de hardware</th>
<th align="left">Necessidade mínima</th>
<th align="left">Necessidade recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processor</p></td>
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



### <a href="" id="bkmk-cm-ramreqs"></a>Processador de servidor MBAM, RAM e requisitos de espaço em disco – topologia de integração do Configuration Manager

A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para servidores MBAM quando você estiver usando a topologia de integração do Configuration Manager. Para obter os requisitos para a topologia autônoma, consulte [processador do MBAM Server, RAM e requisitos de espaço em disco – topologia](#bkmk-stand-alone-ramreqs)autônoma.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item de hardware</th>
<th align="left">Necessidade mínima</th>
<th align="left">Necessidade recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processor</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou mais</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço livre em disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>Versões do Configuration Manager com suporte no MBAM

O MBAM dá suporte para as seguintes versões do Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão com suporte</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (ramificação atual), versões de até 1902</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (corporativo-versão 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gerenciador de configuração do Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 ou posterior</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p>

&gt;<strong>Observação </strong> embora o Configuration Manager 2007 R2 seja 32 bits, você deve instalá-lo e SQL Server em um sistema operacional de 64 bits para corresponder ao software MBAM de 64 bits.
</td>
</tr>
</tbody>
</table>



Para obter uma lista de configurações compatíveis com o Configuration Manager Server, consulte a documentação apropriada do TechNet para a versão do Configuration Manager que você está usando. O MBAM não tem requisitos de sistema adicionais para o servidor do Configuration Manager.

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de banco de dados do SQL Server

A tabela a seguir lista as versões do Microsoft SQL Server com suporte para os recursos do servidor do MBAM, que incluem o banco de dados de recuperação, o banco de dados de auditoria e a conformidade e o recurso relatórios. As versões necessárias se aplicam às topologias autônomas ou de integração do Configuration Manager.

Você deve instalar o SQL Server com o agrupamento do **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** .

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
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64 bits</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bits</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64 bits</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard ou Enterprise</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

**Observação**  
O MBAM tem um nível de compatibilidade máximo com suporte de 140. O nível de compatibilidade padrão para novos bancos de dados criados no SQL Server 2019 é 150 que precisará ser alterado para 140 ou inferior, usando o comando ALTER DATABASE, após a criação do banco de dados. Bancos de dados existentes migrados do SQL Server 2017 ou inferior permanecerão em seu nível de compatibilidade anterior e não precisarão ser alterados.

Para dar suporte ao SQL 2016, você deve instalar a versão de manutenção do 2017 de março do MDOP https://www.microsoft.com/download/details.aspx?id=54967  e para dar suporte ao sql 2017, instale o lançamento de serviços de julho de 2018 para o MDOP https://www.microsoft.com/download/details.aspx?id=57157 . Em geral, mantenha-se atualizado sempre usando a atualização de manutenção mais recente, pois também inclui todos os recursos correções e novos.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>Requisitos de processador, RAM e espaço em disco do SQL Server – topologia autônoma

A tabela a seguir lista os requisitos de processador do servidor, RAM e espaço em disco recomendados para o computador SQL Server quando você estiver usando a topologia autônoma. Use estes requisitos como guia. Seus requisitos específicos variam de acordo com o número de computadores cliente que você tem suporte na sua empresa. Para ver os requisitos da topologia de integração do Configuration Manager, consulte [topologia do processador do SQL Server, da RAM e dos requisitos de espaço em disco – topologia de integração do Configuration Manager](#bkmk-cm-sql-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item de hardware</th>
<th align="left">Necessidade mínima</th>
<th align="left">Necessidade recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processor</p></td>
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



### <a href="" id="bkmk-cm-sql-ramreqs"></a>Requisitos de processador, RAM e espaço em disco do SQL Server-topologia de integração do Configuration Manager

A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para o computador Microsoft SQL Server quando você estiver usando a topologia de integração do Configuration Manager, consulte o [processador do SQL Server, a RAM e requisitos de espaço em disco – topologia autônoma](#bkmk-sql-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item de hardware</th>
<th align="left">Necessidade mínima</th>
<th align="left">Necessidade recomendada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processor</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou mais</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço livre em disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Requisitos do sistema do cliente MBAM


### Requisitos do sistema operacional do cliente

É altamente recomendável que você execute o cliente MBAM e o MBAM Server na mesma linha de sistemas operacionais. Por exemplo, Windows 10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.

A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MBAM. Os mesmos requisitos se aplicam às topologias autônomas e de integração do Configuration Manager.

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
<tr class="even">
    <td align="left"><p>Windows 10 IoT</p></td>
    <td align="left"><p>Enterprise</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32 bits ou 64 bits</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Empresa ou Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8,1 e Windows 10 Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Requisitos de RAM do cliente

Não há requisitos de RAM específicos para a instalação do cliente do MBAM.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Requisitos do sistema da política de grupo do MBAM


A tabela a seguir lista os sistemas operacionais suportados para a instalação de modelos de política de grupo do MBAM.

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
 <tr class="even">
      <td align="left"><p>Windows 10 IoT</p></td>
      <td align="left"><p>Enterprise</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32 bits ou 64 bits</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise ou Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

## MBAM no Azure IaaS

O servidor MBAM pode ser implantado no Azure infraestrutura como serviço (IaaS) em qualquer uma das versões de sistema operacional compatíveis listadas acima, conectando-se a um Active Directory hospedado em um local ou a um Active Directory também hospedado no Azure IaaS.  A documentação para configurar e configurar o Active Directory no Azure IaaS está [aqui](https://msdn.microsoft.com/library/azure/jj156090.aspx).

O cliente MBAM não tem suporte em máquinas virtuais e também não é compatível com o Azure IaaS.


## Lançamentos de serviço 

- [Hotfix de abril de 2016](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [Setembro de 2016](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [Dezembro de 2016](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [Março de 2017](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [Junho de 2017](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [Setembro de 2017](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [Março de 2018](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [De julho de 2018](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [Maio de 2019](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## Tópicos relacionados


[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

[Preparando seu ambiente para o MBAM 2.5](preparing-your-environment-for-mbam-25.md)




## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




