---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797930"
---
# HELP


Exibe informações sobre os vários comandos SFTMIME que podem ser usados na virtualização do aplicativo (App-V).

## HELP


`SFTMIME [/? | /HELP [VERB:<verb>]]`

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
<td align="left"><p>/?,/HELP</p></td>
<td align="left"><p>Exibe informações de uso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>verba</p></td>
<td align="left"><p>O comando a ser executado, como adicionar, atualizar, ajuda ou remover.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>object</p></td>
<td align="left"><p>A que se aplica o comando, como APP: &quot; aplicativo padrão.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>os</p></td>
<td align="left"><p>Parâmetros opcionais do verbo e do objeto especificado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Log de saída para o nome do caminho especificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Exibe a saída na janela ativa do console (padrão).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Exibe erros em uma caixa de diálogo (não é válido para consultas).</p></td>
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

 

Os verbos descritos na tabela a seguir são suportados.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>ADD</p></td>
<td align="left"><p>Adiciona um novo aplicativo, pacote, associação de tipo de arquivo ou servidor de publicação ao cliente App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CONFIGURAÇÃO</p></td>
<td align="left"><p>Altera a configuração de um aplicativo, um pacote, uma associação de tipo de arquivo ou um servidor de publicação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>Remove aplicativos, pacotes, associações de tipo de arquivo ou servidores.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CARREGÁ</p></td>
<td align="left"><p>Carrega um pacote no cache do sistema de arquivos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CONSERTO</p></td>
<td align="left"><p>Redefine suas configurações pessoais para um aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Atualize</p></td>
<td align="left"><p>Dispara uma atualização do Publishing Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PUBLICADO</p></td>
<td align="left"><p>Publica um atalho de aplicativo no menu Iniciar, na área de trabalho ou em outro local especificado do usuário, ou pode ser usado para publicar o conteúdo de um pacote inteiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CANCELAR</p></td>
<td align="left"><p>Remove os atalhos e tipos de arquivo de um pacote inteiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PESQUISA</p></td>
<td align="left"><p>Obtém uma lista atual de aplicativos, pacotes, associações de tipo de arquivo ou servidores de publicação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ELIMINA</p></td>
<td align="left"><p>Remove suas configurações pessoais e configurações da área de trabalho de um ou mais aplicativos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CARREGADO</p></td>
<td align="left"><p>Descarrega um pacote do cache do sistema de arquivos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NumLock</p></td>
<td align="left"><p>Bloqueia o aplicativo especificado no cache do sistema de arquivos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REVELAR</p></td>
<td align="left"><p>Desbloqueia o aplicativo especificado no cache do sistema de arquivos.</p></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre as ações anteriores, use o seguinte comando:

`SFTMIME /HELP VERB:verb`

Por exemplo, o comando a seguir exibirá informações sobre o verbo adicionar:

`SFTMIME /HELP VERB:ADD`

## Tópicos relacionados


[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





