---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799064"
---
# ADD PACKAGE


Adiciona um registro de pacote. Se o pacote já existir, esse comando atualizará a configuração do pacote existente.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>PACKAGE: &lt; Package-Name&gt;</p></td>
<td align="left"><p>Nome de usuário e de usuário visível para o pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Manifesto/manifest-caminho&gt;</p></td>
<td align="left"><p>O caminho do arquivo de manifesto que lista os aplicativos incluídos no pacote e todas as informações de publicação deles.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>URL do/OVERRIDEURL &lt;&gt;</p></td>
<td align="left"><p>O local do arquivo SFT do pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>O carregamento em segundo plano é executado após uma atualização de publicação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>O carregamento em segundo plano é executado quando um usuário faz logon.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>O carregamento em segundo plano é executado após um usuário iniciar um aplicativo do pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADTARGET alvo</p></td>
<td align="left"><p>Indica quais aplicativos do pacote serão carregados de forma carregada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NENHUMA</p></td>
<td align="left"><p>Nenhuma sobrecarga será realizada, apesar da presença de qualquer sinalizador/AUTOLOADONxxx.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TODO</p></td>
<td align="left"><p>Se um gatilho de autocarregamento estiver habilitado, todos os aplicativos do pacote serão carregados no cache, independentemente de terem sido iniciados anteriormente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Se um gatilho de autocarregamento estiver habilitado, o pacote será carregado se qualquer aplicativo deste pacote tiver sido iniciado anteriormente por um usuário.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Se estiver presente, o pacote estará disponível para todos os usuários neste computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Se especificado, a saída será registrada no nome do caminho especificado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Se especificado, a saída será apresentada na janela ativa do console (padrão).</p></td>
</tr>
<tr class="even">
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

 

 





