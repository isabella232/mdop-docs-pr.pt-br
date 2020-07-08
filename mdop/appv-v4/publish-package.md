---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796800"
---
# PUBLISH PACKAGE


Publica o conteúdo de um pacote inteiro.

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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

 

**Importante**  O pacote já deve ter sido adicionado ao cliente do Application Virtualization e o arquivo de manifesto é necessário.

Para usar o parâmetro **global** , o comando publicar pacote deve ser executado como administrador local; caso contrário, somente as permissões **ManageTypes** e **PublishShortcut** são necessárias.

Publicar sem o parâmetro **global** concede ao usuário acesso aos aplicativos no pacote e publica os tipos de arquivo e atalhos listados no manifesto para o perfil do usuário.

A publicação com o parâmetro **global** adiciona os tipos de arquivo e atalhos listados no manifesto ao perfil "todos os usuários".

Se o pacote não for global antes de a chamada e o parâmetro **global** ser usado, o pacote será tornado global e estará disponível para todos os usuários.

 

## Tópicos relacionados


[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





