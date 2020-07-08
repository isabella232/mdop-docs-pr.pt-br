---
title: Arquivos de log do Application Virtualization Sequencer
description: Arquivos de log do Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796881"
---
# Arquivos de log do Application Virtualization Sequencer


Os arquivos de log do sequenciador do Application Virtualization (App-V) fornecem informações detalhadas sobre o sequenciamento de aplicativos, e eles podem ser úteis quando você está verificando a funcionalidade ou durante a solução de problemas.

A tabela a seguir fornece informações sobre os arquivos de log e seus locais padrão, que são criados ao usar o sequenciador.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome do arquivo de log</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>sft-seq-log.txt</strong></p></td>
<td align="left"><p>Fornece informações gerais sobre a sequenciagem de um aplicativo. Use este log como ponto de partida para solucionar erros de sequenciador.</p>
<p>Local do arquivo de log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valor do token do modelo] Local do arquivo de log do App-V 4.6: <em> %windir%\Program Comuns\microsoft Application Virtualization Sequencer\Logs </em> [valor de token do modelo]</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>sftbt.txt</strong></p></td>
<td align="left"><p>Fornece informações sobre as tarefas de reinicialização do computador que ocorrem durante a reinicialização simulada do sequenciador.</p>
<p>Local do arquivo de log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valor do token do modelo] Local do arquivo de log do App-V 4.6: <em> %windir%\Program Comuns\microsoft Application Virtualization Sequencer\Logs </em> [valor de token do modelo]</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SftCallBack.txt</strong></p></td>
<td align="left"><p>Fornece informações gerais sobre os processos usados durante o sequenciamento.</p>
<p>Local do arquivo de log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valor do token do modelo] Local do arquivo de log do App-V 4.6: <em> %windir%\Program Comuns\microsoft Application Virtualization Sequencer\Logs </em> [valor de token do modelo]</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Referência do Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

 

 





