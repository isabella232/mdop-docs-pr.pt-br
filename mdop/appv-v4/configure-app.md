---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797513"
---
# CONFIGURE APP


Permite que o usuário altere o ícone associado a um aplicativo, mas não atualiza o ícone em atalhos existentes ou associações de tipo de arquivo.

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Aplicativo: &lt; aplicativo&gt;</p></td>
<td align="left"><p>O nome e a versão (opcional) do aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ícone do/ICON &lt; -PathName&gt;</p></td>
<td align="left"><p>O caminho ou a URL do arquivo de ícone.</p></td>
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

 

 





