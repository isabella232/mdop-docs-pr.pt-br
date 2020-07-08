---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796664"
---
# UNPUBLISH PACKAGE


Permite remover os atalhos e tipos de arquivo para um pacote inteiro.

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>O nome do pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CLEAR</p></td>
<td align="left"><p>Se houver, as configurações do usuário também serão removidas. (Para obter mais informações, consulte a observação importante posteriormente neste tópico.)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Se estiver presente, o pacote será cancelado para todos os usuários neste computador.</p></td>
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

 

**Importante**  Antes de poder executar o comando **Cancelar publicação do pacote** , o pacote já deve ter sido adicionado ao cliente do Application Virtualization.

Para usar o pacote **global**de **cancelamento de publicação** deve ser executado como administrador local; caso contrário, somente a permissão **ClearApp** é necessária.

Usar o **pacote não publicar** com **global** remove todos os tipos de arquivo e atalhos globais do pacote. **Clear** não é aplicável.

Usar o **pacote não publicar** sem a **global** remove os atalhos de usuário e os tipos de arquivo do pacote e, se **limpar** estiver definido, também removerá as configurações do usuário e interromperá as cargas em segundo plano sob o contexto do usuário.

O **CANcelamento de publicação do pacote** funciona em aplicativos do mesmo nome ou GUID do pacote que foi usado como a ID da fonte para **Adicionar**, **Editar**e **publicar pacote**.

A opção **Cancelar publicação do pacote** sempre limpa todas as configurações do usuário, atalhos e tipos de arquivo, independentemente do uso da opção/Clear

 

## Tópicos relacionados


[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





