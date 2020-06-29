---
title: Pré-requisitos para o recurso de integração do Configuration Manager
description: Pré-requisitos para o recurso de integração do Configuration Manager
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799587"
---
# Pré-requisitos para o recurso de integração do Configuration Manager


Se você implantar o MBAM com a topologia de integração do System Center Configuration Manager, recomendamos uma arquitetura de três servidores, conforme descrito em [arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md). Essa arquitetura pode dar suporte a 500.000 computadores cliente.

**Importante**  
Não há suporte para o Windows to go para a instalação de topologia de integração do Configuration Manager quando você está usando o Configuration Manager 2007.



## Pré-requisitos gerais do recurso de integração do Configuration Manager


Quando você instala o MBAM com o Configuration Manager, os seguintes pré-requisitos adicionais são necessários, além dos pré-requisitos para a topologia autônoma.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Informações adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O servidor do Configuration Manager é um site primário no sistema do Configuration Manager.</p></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="even">
<td align="left"><p>O agente cliente do inventário de hardware está no servidor do Configuration Manager.</p></td>
<td align="left"><p>Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> como configurar o inventário de hardware no Configuration Manager </a> .</p>
<p>Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> como configurar o inventário de hardware para um site </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Um dos seguintes itens está habilitado, dependendo da versão do Configuration Manager que você está usando:</p>
<ul>
<li><p>Configurações de conformidade-(System Center 2012 Configuration Manager)</p></li>
<li><p>Agente cliente do gerenciamento de configuração desejado (DCM) – (Configuration Manager 2007)</p></li>
</ul></td>
<td align="left"><p>Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> definindo configurações de conformidade no Configuration Manager </a> .</p>
<p>Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> as propriedades do agente cliente de gerenciamento de configuração desejadas </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Um ponto do Reporting Services é definido no Configuration Manager. Obrigatório para SQL Server Reporting Services (SSRS).</p></td>
<td align="left"><p>Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> pré-requisitos para relatórios no Configuration Manager </a> .</p>
<p>Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> como criar um ponto do Reporting Services para SQL Reporting Services </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>O Configuration Manager 2007 requer o Microsoft .NET Framework 2,0</p></td>
<td align="left"><p>O agente do cliente DCM (gerenciamento de configuração desejado) no Configuration Manager 2007 requer que o .NET Framework 2,0 para denunciar a conformidade.</p>
<div class="alert">
<strong>Observação</strong><br/><p>A instalação do .NET Framework 3,5 instala automaticamente o .NET Framework 2,0.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Permissões necessárias para instalar o MBAM com o Configuration Manager


Para instalar o MBAM com o Configuration Manager, você deve ter um usuário administrativo no Configuration Manager que tenha um direito de acesso com as permissões mínimas listadas na tabela a seguir. A tabela também mostra os direitos que você deve ter, além dos direitos de administrador do computador básico, para instalar o MBAM Server.

**As permissões na tabela a seguir se aplicam a ambas as versões do Configuration Manager.**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permissões</th>
<th align="left">Recurso do servidor MBAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Funções do servidor de logon da instância do SQL Server:-dbcreator-processadmin</p></td>
<td align="left"><p>- Banco de dados de recuperação-banco de dados de auditoria</p></td>
</tr>
<tr class="even">
<td align="left"><p>Direitos de instância do SSRS:-criar pastas – publicar relatórios</p></td>
<td align="left"><p>- Integração do System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Systems Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permissões</th>
<th align="left">Recurso do servidor do Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Direitos de site do Configuration Manager:-ler</p></td>
<td align="left"><p>Integração do System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Direitos de coleção do Configuration Manager:-criar-excluir-ler-modificar-implantar itens de configuração</p></td>
<td align="left"><p>Integração do System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Direitos de item de configuração do Configuration Manager:-Create-Delete-Read</p></td>
<td align="left"><p>Integração do System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Configuration Manager 2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permissões</th>
<th align="left">Recurso do servidor do Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Direitos de site do Configuration Manager:-ler</p></td>
<td align="left"><p>Integração do System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Direitos de coleção do Configuration Manager:-Create-Delete-Read-ReadResource</p></td>
<td align="left"><p>Integração do System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Direitos de item de configuração do Configuration Manager:-criar-excluir-ler-distribuir</p></td>
<td align="left"><p>Integração do System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Alterações necessárias para os arquivos. mof


Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo. mof de configuração e o arquivo SMS \ _def. MOF para o System Center 2012 Configuration Manager e o Microsoft System Center Configuration Manager 2007. Para obter instruções, consulte [pré-requisitos do servidor do MBAM 2,5 que se aplicam apenas à topologia de integração do Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).



## Tópicos relacionados


[Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





