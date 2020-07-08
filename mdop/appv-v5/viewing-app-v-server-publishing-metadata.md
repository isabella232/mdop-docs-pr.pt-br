---
title: Exibindo os metadados de publicação do servidor do App-V
description: Exibindo os metadados de publicação do servidor do App-V
author: dansimp
ms.assetid: 048dd42a-24d4-4cc4-81f6-7a919aadd9b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 304aa656de98a0c9d59f0a6166811ead911033ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796206"
---
# Exibindo os metadados de publicação do servidor do App-V


Use este procedimento para exibir metadados de publicação, que podem ajudar você a solucionar problemas relacionados à publicação. Você deve usar o servidor de gerenciamento do App-V para usar este procedimento.

Este artigo contém as seguintes informações:

-   [Requisitos do App-V 5,0 SP3 para visualização de metadados de publicação](#bkmk-50sp3-reqs-pub-meta)

-   [Sintaxe a ser usada para exibir metadados de publicação](#bkmk-syntax-view-pub-meta)

-   [Consultar valores para a versão e o sistema operacional do cliente](#bkmk-values-query-pub-meta)

-   [Definição de metadados de publicação](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-50sp3-reqs-pub-meta"></a>Requisitos do App-V 5,0 SP3 para visualização de metadados de publicação


No App-V 5,0 SP3, você deve fornecer os seguintes valores no endereço quando consulta o servidor de publicação App-V para metadados:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor</th>
<th align="left">Detalhes adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Se você omitir <strong> o </strong> parâmetro ClientVersion da consulta, os metadados excluirão os novos recursos do App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ClientOS</strong></p></td>
<td align="left"><p>Você deve fornecer esse valor apenas se selecionar sistemas operacionais específicos do cliente quando você sequenciar o pacote. Se você selecionar o padrão (todos os sistemas operacionais), não especifique esse valor na consulta.</p>
<p>Se você omitir <strong> o </strong> parâmetro ClientOS da consulta, somente os pacotes que foram sequenciados para dar suporte a qualquer sistema operacional aparecem nos metadados.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>Sintaxe de consulta para exibir metadados de publicação


A tabela a seguir fornece os exemplos de sintaxe e consulta.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do App-V</th>
<th align="left">Sintaxe da consulta</th>
<th align="left">Descrições de parâmetro</th>
<th align="left">Exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;PubServer&gt;</p></td>
<td align="left"><p>Nome do servidor de publicação App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Porta de publicação #&gt;</p></td>
<td align="left"><p>Porta para o servidor de publicação App-V, que você definiu quando configurou o Publishing Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClientVersion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>Versão do cliente App-V. Veja a tabela a seguir para obter o valor correto a ser usado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ClientOS = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>Sistema operacional do computador que está executando o cliente App-V. Veja a tabela a seguir para obter o valor correto a ser usado.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>Para obter o nome do servidor de publicação e o número da porta (http:// &lt; PubServer &gt; : &lt; Publishing Port # &gt; ) do cliente App-V, examine a configuração de URL do <strong> cmdlet Get-AppvPublishingServer do </strong> PowerShell.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>No exemplo:</p>
<ul>
<li><p>Um Windows Server 2012 R2 chamado "pubsvr01" hospeda o serviço de publicação.</p></li>
<li><p>O cliente Windows é o Windows 8,1 64 bits.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 até App-V 5,0 SP2</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>Observação</strong><br/><p><strong></strong> <strong> </strong> Só há suporte para ClientVersion e ClientOS no App-V 5,0 SP3.</p>
</div>
<div>

</div></td>
<td align="left"><p>Consulte as informações para o App-V 5,0 SP3.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>No exemplo, um Windows Server 2012 R2 chamado "pubsvr01" hospeda os serviços de gerenciamento e publicação.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>Consultar valores para a versão e o sistema operacional do cliente


Na consulta de metadados de publicação, insira os valores de cadeia de caracteres que correspondem ao sistema operacional do cliente e à versão que você está usando.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Arquitetura</th>
<th align="left">Valor String da cadeia de caracteres operacional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>Definição de metadados de publicação


Quando pacotes são publicados em um computador que está executando o cliente App-V, os metadados são enviados para esse computador indicando quais pacotes e grupos de conexão estão sendo publicados. O cliente App-V faz duas solicitações separadas para o seguinte:

-   Pacotes e grupos de conexão que são habilitados para o computador cliente.

-   Pacotes e grupos de conexão que são habilitados para o usuário atual.

O servidor de publicação se comunica com o servidor de gerenciamento para determinar quais pacotes e grupos de conexão estão disponíveis para o solicitante. O servidor de publicação deve ser registrado com o servidor de gerenciamento para que os metadados sejam gerados.

Você pode exibir os metadados de cada solicitação em um navegador da Internet usando uma consulta que se encontra no contexto do usuário ou computador específico.






## Tópicos relacionados


[Referência técnica para o App-V 5.0](technical-reference-for-app-v-50.md)









