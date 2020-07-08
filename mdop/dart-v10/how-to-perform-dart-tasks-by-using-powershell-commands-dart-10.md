---
title: Como realizar tarefas do DaRT usando comandos do PowerShell
description: Como realizar tarefas do DaRT usando comandos do PowerShell
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799104"
---
# Como realizar tarefas do DaRT usando comandos do PowerShell


O Microsoft Diagnostics and Recovery Toolset (DaRT) 10 fornece o conjunto de cmdlets do Windows PowerShell listados a seguir. Os administradores podem usar esses cmdlets do PowerShell para executar várias tarefas do servidor DaRT 10 a partir do prompt de comando, e não do assistente de imagem de recuperação do DaRT.

## Para administrar o DaRT usando comandos do PowerShell


Use os cmdlets do PowerShell descritos aqui para administrar o DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copy-DartImage</p></td>
<td align="left"><p>Grava uma ISO em um CD, DVD ou unidade USB.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Export-DartImage</p></td>
<td align="left"><p>Permite que o arquivo WIM de origem, que contém uma imagem DaRT, seja convertido em um arquivo ISO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>New-DartConfiguration</p></td>
<td align="left"><p>Cria um objeto de configuração DaRT que é necessário para aplicar um conjunto de ferramentas DaRT a uma imagem do Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-DartImage</p></td>
<td align="left"><p>Aplica um objeto DartConfiguration a uma imagem montada do Windows. Isso inclui a adição de todos os arquivos, configuração e dependências do pacote.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Administrar o DaRT 10 usando o PowerShell](administering-dart-10-using-powershell.md)

 

 





