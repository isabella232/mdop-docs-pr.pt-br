---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799061"
---
# ADD TYPE


Adiciona a associação de tipo de arquivo especificada.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>TIPO: &lt; extensão de arquivo&gt;</p></td>
<td align="left"><p>A extensão de nome de arquivo que será associada ao aplicativo especificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Aplicativo/App&gt;</p></td>
<td align="left"><p>O nome e a versão (opcional) do aplicativo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ícone do/ICON &lt; -PathName&gt;</p></td>
<td align="left"><p>O caminho ou a URL do arquivo de ícone.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Tipo de/Description-desc&gt;</p></td>
<td align="left"><p>O nome amigável do tipo de arquivo. O padrão é o &quot; arquivo de extensão.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Tipo de conteúdo/Content-Type&gt;</p></td>
<td align="left"><p>O tipo de conteúdo do arquivo. O padrão é &quot; Application/Softricity-Extension.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Se estiver presente, o pacote estará disponível para todos os usuários neste computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Tipo percebido/PERCEIVED-Type&gt;</p></td>
<td align="left"><p>O tipo percebido do arquivo. O padrão é Nothing.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ProgID/ProgId&gt;</p></td>
<td align="left"><p>O identificador programático para o tipo de arquivo. Padrão para App Virt. Extension. File.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indica se os usuários que baixam um arquivo desse tipo devem ser solicitados a abrir ou salvar o arquivo. Padrão para Sim.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indica se a extensão do arquivo sempre deve ser mostrada, mesmo se o usuário tiver solicitado que todas as extensões fiquem ocultas. Padrão para não.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indica se uma entrada deve ser adicionada ao <strong> menu novo do Shell </strong> . Padrão para não.</p></td>
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

 

 





