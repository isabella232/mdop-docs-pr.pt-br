---
title: Como planejar a implantação do MBAM com o Configuration Manager
description: Como planejar a implantação do MBAM com o Configuration Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799710"
---
# Como planejar a implantação do MBAM com o Configuration Manager


Para implantar o MBAM com a topologia do Configuration Manager, é recomendável uma arquitetura de três servidores, que dá suporte a clientes do 200.000. Use um servidor separado para executar o Configuration Manager e instale os recursos básicos de administração e monitoramento em dois servidores, como mostrado na imagem de arquitetura em [introdução-usando o MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).

**Importante**  
Não há suporte para o Windows to go ao instalar a topologia integrada do MBAM com o Configuration Manager 2007.



## Pré-requisitos de implantação para instalar o MBAM com o Configuration Manager


Verifique se você atendeu aos seguintes pré-requisitos antes de instalar o MBAM com o Configuration Manager:

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
<td align="left"><p>Verifique se o servidor do Configuration Manager é um site primário no sistema do Configuration Manager.</p></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="even">
<td align="left"><p>Habilite o agente cliente do inventário de hardware no servidor do Configuration Manager.</p></td>
<td align="left"><p>Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> como configurar o inventário de hardware para um site </a> .</p>
<p>Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> como configurar o inventário de hardware no Configuration Manager </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Habilite o agente DCM (gerenciamento de configuração) ou as configurações de conformidade, dependendo da versão do Configuration Manager que você está usando.</p></td>
<td align="left"><p>Para o Configuration Manager 2007, habilite as <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Propriedades do agente do cliente de gerenciamento de configuração desejado </a> .</p>
<p>Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> definindo configurações de conformidade no Configuration Manager </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Defina um ponto do Reporting Services no Configuration Manager. Obrigatório para SQL Reporting Services.</p></td>
<td align="left"><p>Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> como criar um ponto do Reporting Services para SQL Reporting Services </a> .</p>
<p>Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> pré-requisitos para relatórios no Configuration Manager </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Versões compatíveis do Configuration Manager


O MBAM dá suporte para as seguintes versões do Configuration Manager:

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
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 ou posterior</p></td>
<td align="left"><p>64 bits</p>
<div class="alert">
<strong>Observação</strong><br/><p>Embora o Configuration Manager 2007 seja 32 bits, você deve instalá-lo e SQL Server em um sistema operacional de 64 bits para corresponder ao software MBAM de 64 bits.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Gerenciador de configuração do Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



Para obter uma lista de configurações compatíveis com o Configuration Manager Server, consulte a página da Web apropriada para a versão do Configuration Manager que você está usando. O MBAM não tem requisitos de sistema adicionais para o servidor do Configuration Manager.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> Requisitos de sistema do MBAM e do SQL Server


As configurações compatíveis e os requisitos de sistema para os servidores MBAM e SQL Server para a topologia do Configuration Manager são iguais aos da topologia autônoma. Para obter os requisitos de sistema autônomos, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Para os requisitos do servidor do SQL Server e do processador do SQL Server, da RAM e do espaço em disco para a topologia do Configuration Manager, consulte as seções a seguir.

## Processador de servidor MBAM, RAM e requisitos de espaço em disco para MBAM


A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco para servidores MBAM quando você estiver usando a topologia de integração do Configuration Manager.

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



## Requisitos de processador, RAM e espaço em disco do SQL Server


A tabela a seguir lista os requisitos do processador do servidor, da RAM e do espaço em disco do computador SQL Server quando você estiver usando a topologia de integração do Configuration Manager.

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
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço livre em disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB ou mais</p></td>
</tr>
</tbody>
</table>



## Permissões necessárias para instalar o servidor MBAM


Para instalar o MBAM com o Configuration Manager, você deve ter um usuário administrativo no Configuration Manager que tenha um direito de acesso com as permissões mínimas listadas na tabela a seguir. A tabela também mostra os direitos que você deve ter, além dos direitos de administrador do computador básico, para instalar o MBAM Server.

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
<td align="left"><p>Funções do servidor de logon da instância SQL:-dbcreator-processadmin</p></td>
<td align="left"><p>- Banco de dados de recuperação-banco de dados de auditoria</p></td>
</tr>
<tr class="even">
<td align="left"><p>Direitos de instância do SQL Server Reporting Services:-criar pastas-publicar relatórios</p></td>
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



## Ordem de implantação de recursos de MBAM para a topologia do Configuration Manager


Ao implantar o MBAM no servidor do Configuration Manager, você deve concluir as tarefas de implantação na seguinte ordem:

1.  Edite o arquivo Configuration. mof no servidor do Configuration Manager.

2.  Crie ou edite o servidor do Gerenciador de arquivos do SMS \ _def. mof.

3.  Instale o MBAM no servidor do Configuration Manager.

4.  Instale o banco de dados de recuperação e o banco de dados de auditoria no servidor de banco de dados.

5.  Instale os recursos do MBAM no servidor de administração e monitoramento.

## Lista de verificação de planejamento para a instalação do MBAM com o Configuration Manager


Esta lista de verificação descreve as etapas recomendadas e uma lista de alto nível de itens a serem considerados ao planejar uma implantação do Microsoft BitLocker Administration and Monitoring with Configuration Manager. É recomendável que você copie esta lista de verificação para um programa de planilha e personalize-a para seu uso.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tarefa</th>
<th align="left">Referências</th>
<th align="left">Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de introdução, que descrevem como o Configuration Manager funciona com o MBAM e mostra a arquitetura de alto nível recomendada.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">Introdução – Como usar o MBAM com o Configuration Manager</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de planejamento, que descrevem os pré-requisitos de implantação, configurações com suporte, permissões necessárias e ordem de implantação para cada recurso.</p></td>
<td align="left"><p>Como planejar a implantação do MBAM com o Configuration Manager</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje e configure MBAM requisitos da política de grupo.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planejar Requisitos de Política de Grupo do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje e crie os grupos de segurança dos serviços de domínio Active Directory necessários e planeje os requisitos de associação do grupo de segurança local do MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planejamento para Funções de Administrador do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plano para implantar a implantação do cliente MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planejar implantação de cliente MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md)









