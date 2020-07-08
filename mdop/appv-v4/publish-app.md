---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796801"
---
# PUBLISH APP


Publica um atalho de aplicativo no menu Iniciar, na área de trabalho ou em outro local especificado do usuário.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>APLICATIVO: &lt; aplicativo&gt;</p></td>
<td align="left"><p>O nome e a versão (opcional) do aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESKTOP</p></td>
<td align="left"><p>Publica um atalho para a área de trabalho do usuário.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/START</p></td>
<td align="left"><p>Publica um atalho para a pasta aplicativos de virtualização de aplicativos na pasta programas do menu iniciar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TARGET &lt; target-Path&gt;</p></td>
<td align="left"><p>O caminho absoluto onde o atalho deve ser publicado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ícone do/ICON &lt; -PathName&gt;</p></td>
<td align="left"><p>O caminho ou a URL do arquivo de ícone.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Nome de exibição de/display&gt;</p></td>
<td align="left"><p>O nome de exibição do atalho.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/ARGS &lt; Command-args&gt;</p></td>
<td align="left"><p>Parâmetros a serem passados para o aplicativo.</p></td>
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

 

 





