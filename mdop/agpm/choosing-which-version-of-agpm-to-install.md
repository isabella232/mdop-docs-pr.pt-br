---
title: Como escolher qual versão do AGPM a ser instalada
description: Como escolher qual versão do AGPM a ser instalada
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905598"
---
# Como escolher qual versão do AGPM a ser instalada


Cada lançamento do gerenciamento de política de grupo (AGPM) do MicrosoftAdvanced oferece suporte a versões específicas do sistema operacional Windows. É altamente recomendável que você execute o cliente do AGPM e o servidor do AGPM na mesma linha de sistemas operacionais. Por exemplo, Windows 10 com Windows Server 2016, Windows 8.1 com Windows Server2012 R2 e assim por diante.

Recomendamos que você instale o servidor do AGPM na versão mais recente do sistema operacional do domínio. O AGPM usa o GPMC (console de gerenciamento de política de grupo) para fazer backup e restaurar objetos de política de grupo (GPOs). Como as versões mais recentes do GPMC fornecem configurações de política adicionais que não estão disponíveis em versões anteriores, você pode gerenciar mais configurações de política usando a versão mais recente do sistema operacional.

Todas as versões do AGPM podem gerenciar apenas as configurações de política que foram introduzidas na mesma versão ou em uma versão anterior do sistema operacional em que o AGPM está em execução. Por exemplo, se você instalar o AGPM 4.0 SP2 no Windows Server 2012, poderá gerenciar as configurações de política que foram introduzidas no Windows Server 2012 ou anterior, mas não poderá gerenciar as configurações de política que foram introduzidas mais tarde, no Windows 8.1 ou no Windows Server2012 R2.

Se a versão do GPMC em seu servidor do AGPM for mais antiga do que a versão nos computadores que os administradores usam para gerenciar a política de grupo, o servidor do AGPM não poderá armazenar nenhuma configuração de política que não esteja disponível na versão anterior do GPMC. Consulte a planilha de configurações de Política de Grupo incluídas no Windows na [Referência de configurações de Política de Grupo para Windows e Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).

## AGPM 4.0 SP3


Se você estiver usando computadores que executam o Windows 10 para gerenciar GPOs, deverá usar o AGPM 4,0 SP3. Não é possível instalar versões anteriores do AGPM em computadores que executam o sistema operacional Windows 10.

A tabela 1 lista os sistemas operacionais nos quais você pode instalar o AGPM 4.0 SP3 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP3.

**Tabela 1: sistemas operacionais compatíveis com o AGPM 4,0 SP3 e configurações de política**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurações com suporte para o servidor do AGPM</strong></th>
<th align="left"><strong>Configurações com suporte para o cliente do AGPM</strong></th>
<th align="left"><strong>Suporte do AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2019 ou Windows 10</p></td>
<td align="left"><p>Windows Server 2019 ou Windows 10</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
 <tr class="even">
<td align="left"><p>Windows Server 2019 ou Windows 10</p></td>
<td align="left"><p>Windows Server 2019 ou Windows 10</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="edd">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Compatível com as advertências descritas em <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 ou Windows 8,1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP2


Se estiver usando computadores que executam o Windows Server2012 R2 ou o Windows 8.1 para gerenciar GPOs, você deve usar o AGPM 4.0 SP2. Não é possível instalar versões anteriores do AGPM em computadores que executam esses sistemas operacionais.

A tabela 1 lista os sistemas operacionais nos quais você pode instalar o AGPM 4.0 SP2 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP2.

**Tabela 2: sistemas operacionais com suporte do AGPM 4.0 SP2 e configurações de política**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurações com suporte para o servidor do AGPM</strong></th>
<th align="left"><strong>Configurações com suporte para o cliente do AGPM</strong></th>
<th align="left"><strong>Suporte do AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 ou Windows 8,1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP1


A tabela 2 lista os sistemas operacionais nos quais você pode instalar o AGPM 4,0 SP1 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP1.

**Tabela 3: sistemas operacionais com suporte do AGPM 4.0 SP1 e configurações de política**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurações com suporte para o servidor do AGPM</strong></th>
<th align="left"><strong>Configurações com suporte para o cliente do AGPM</strong></th>
<th align="left"><strong>Suporte do AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0


A tabela 3 lista os sistemas operacionais nos quais você pode instalar o AGPM 4,0 e as configurações de política que você pode gerenciar usando o AGPM 4.0.

**Tabela 4: sistemas operacionais com suporte do AGPM 4.0 e configurações de política**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistemas operacionais com suporte para o servidor do AGPM</th>
<th align="left">Sistemas operacionais com suporte para o cliente do AGPM</th>
<th align="left">Suporte do AGPM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</p></td>
</tr>
</tbody>
</table>

 

## Versões do AGPM que precedem o AGPM 4.0


A tabela 4 lista os sistemas operacionais em que você pode instalar as versões do AGPM que precedem o AGPM 4.0. Se um sistema operacional não estiver listado, não será possível instalar o AGPM nesse sistema operacional.

**Tabela 5: sistemas operacionais com suporte para versões do AGPM que precedem o AGPM 4.0**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Versão do AGPM que pode ser instalada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista com SP1</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsVista sem Service Pack instalado (32 bits)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 (32 bits)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
</tbody>
</table>

 

## Como obter tecnologias do MDOP


O AGPM 4,0 SP2 faz parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Tópicos relacionados


[Gerenciamento Avançado de Política de Grupo](index.md)

 

 





