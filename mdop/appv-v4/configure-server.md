---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798979"
---
# CONFIGURE SERVER


Permite que um usuário altere a configuração de um servidor; qualquer configuração não especificada não será modificada.

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
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
<td align="left"><p>SERVIDOR: &lt; nome do servidor&gt;</p></td>
<td align="left"><p>O nome de exibição do servidor de publicação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Nome de exibição/Name&gt;</p></td>
<td align="left"><p>Novo nome para exibição do servidor.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Nome do host/host&gt;</p></td>
<td align="left"><p>O nome do host ou o endereço IP do servidor de publicação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PORT &lt; porta&gt;</p></td>
<td align="left"><p>A porta na qual o servidor de publicação escuta. O padrão é o 80 para servidores HTTP normais, 443 para servidores HTTP usando a segurança aprimorada, 554 para servidores de virtualização de aplicativos normais e 322 para servidores que usam segurança aprimorada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Caminho/Path&gt;</p></td>
<td align="left"><p>A parte do caminho da URL usada em uma solicitação de publicação. Se o parâmetro TYPE estiver definido como RTSP, o caminho será opcional e padrão &quot; / &quot; .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TYPE</p></td>
<td align="left"><p>Indica se o servidor de publicação é um servidor Web ( &quot; http &quot; ) ou um servidor de virtualização de aplicativos ( &quot; RTSP &quot; ).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/REFRESH</p></td>
<td align="left"><p>Se definido como ativado, as informações de publicação serão atualizadas quando o usuário fizer logon. O padrão é ativado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SECURE</p></td>
<td align="left"><p>Se presente, indica que uma conexão com a segurança reforçada deve ser estabelecida com o servidor de publicação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Se especificado, a saída será registrada no nome do caminho especificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Se especificado, a saída será apresentada na janela ativa do console (padrão).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</p></td>
</tr>
</tbody>
</table>

 

Para a versão 4.6, a seguinte opção foi adicionada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





