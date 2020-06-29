---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798025"
---
# CONFIGURE TYPE


Permite que o usuário altere as configurações de uma associação de tipo de arquivo.

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>A extensão de nome de arquivo a ser configurada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Aplicativo/App&gt;</p></td>
<td align="left"><p>O nome e a versão (opcional) do aplicativo ao qual associar esse tipo de arquivo. Não pode ser especificado com PROGID.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ícone do/ICON &lt; -PathName&gt;</p></td>
<td align="left"><p>O caminho ou a URL do arquivo de ícone.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Tipo de/Description-desc&gt;</p></td>
<td align="left"><p>O nome amigável do tipo de arquivo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Tipo de conteúdo/Content-Type&gt;</p></td>
<td align="left"><p>O tipo de conteúdo do arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Se presente, indica que a associação que se aplica a todos os usuários deve ser editada, não a específica do usuário.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Tipo percebido/PERCEIVED-Type&gt;</p></td>
<td align="left"><p>O tipo percebido do arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ProgID/ProgId&gt;</p></td>
<td align="left"><p>Indica que a extensão deve ser associada a um tipo de arquivo diferente. O tipo de arquivo anterior não é excluído. Não pode ser especificado com APP, ICON, DESCRIPTION, CONFIRMOPEN ou SHOWEXT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indica se os usuários que baixam um arquivo desse tipo devem ser solicitados a abrir ou salvar o arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indica se a extensão do arquivo sempre deve ser mostrada, mesmo se o usuário tiver solicitado que todas as extensões fiquem ocultas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indica se uma entrada deve ser adicionada ao <strong> menu novo do Shell </strong> .</p></td>
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

 

 





