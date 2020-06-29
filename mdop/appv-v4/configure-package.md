---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797507"
---
# CONFIGURE PACKAGE


Permite que o usuário altere um arquivo de manifesto de pacote, origem do pacote, tipos de gatilho de carga ou destino de carga para um pacote.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>O caminho ou a URL do arquivo de manifesto que lista os aplicativos incluídos no pacote e todas as informações de publicação deles.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>URL do/OVERRIDEURL &lt;&gt;</p></td>
<td align="left"><p>O local do arquivo SFT do pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>O carregamento em segundo plano está desativado para o pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>O carregamento em segundo plano é executado após uma atualização de publicação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>O carregamento em segundo plano é executado quando um usuário faz logon.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>O carregamento em segundo plano é executado após um usuário iniciar um aplicativo do pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADTARGET &lt; alvo&gt;</p></td>
<td align="left"><p>Indica quais aplicativos do pacote serão carregados de forma carregada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NENHUMA</p></td>
<td align="left"><p>Nenhuma sobrecarga será realizada, apesar da presença de qualquer sinalizador/AUTOLOADONxxx.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TODO</p></td>
<td align="left"><p>Se um gatilho de autocarregamento estiver habilitado, todos os aplicativos do pacote serão carregados no cache independentemente de terem sido iniciados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Se um gatilho de autocarregamento estiver habilitado, o pacote será carregado se qualquer aplicativo deste pacote tiver sido iniciado anteriormente por um usuário.</p></td>
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

 

Para a versão 4.6 SP2, a seguinte opção foi adicionada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</p></td>
<td align="left"><p>Se definido como TRUE, um valor do registro será criado para o pacote, seja por usuário ou globalmente se o sinalizador/GLOBAL for especificado.</p>
<p>Se definido como FALSE, o valor do registro será removido e as associações de tipo de arquivo (FTA) do pacote serão reinstaladas.</p>
<p>Se não for especificado, ocorrerá a FTA normal e o comportamento de publicação de atalhos. Se você executar qualquer operação de atualização de publicação subsequente no cliente do App-V 4,6 SP2, os atalhos e FTAs para pacotes que possuem esse valor de registro definido não serão alterados, e os atalhos e FTAs não serão registrados na inicialização do sistema ou no logon do usuário, a menos que você redefina o sinalizador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Funciona em conjunto com o sinalizador/NO-UPDATE-FTA-SHORTCUT. Se o sinalizador/GLOBAL estiver presente, isso indicará que um valor do registro será criado para esse pacote para todos os usuários. Por padrão, o valor do registro é criado apenas para esse usuário.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





