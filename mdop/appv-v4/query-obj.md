---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796785"
---
# QUERY OBJ


Retorna uma lista delimitada por tabulação de aplicativos, pacotes, associações de tipo de arquivo ou servidores de publicação atuais.

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

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
<td align="left"><p>APPV</p></td>
<td align="left"><p>Retorna uma lista de aplicativos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PACOTE</p></td>
<td align="left"><p>Retorna uma lista de pacotes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TYPE</p></td>
<td align="left"><p>Retorna uma lista de associações de tipo de arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVIDOR</p></td>
<td align="left"><p>Retorna uma lista de servidores de publicação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SHORT</p></td>
<td align="left"><p>Sem exibir as propriedades completas de cada um, retorna uma lista de nomes de aplicativos, pacotes, associações ou nomes de servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Para aplicativos, retorna todos os aplicativos conhecidos, em vez de apenas aqueles que o usuário atual tem acesso. Para pacotes, retorna todos os pacotes conhecidos, em vez de apenas aqueles que o usuário atual tem acesso. Para associações, retorna somente associações que se aplicam a todos os usuários, não àqueles específicos do usuário. Não é válido para servidores.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Se especificado, a saída será registrada no nome do caminho especificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Se especificado, a saída será apresentada na janela ativa do console (padrão).</p></td>
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

 

**Observação**  Na versão 4,6, uma nova coluna foi adicionada à saída de SFTMIME QUERY OBJ: APP \ [/GLOBAL\]. A última coluna da saída é um valor numérico que indica se um aplicativo foi publicado ou não.

PUBLISHed = 1 significa que o aplicativo foi publicado por uma atualização do Publishing Server, instalando o aplicativo usando um arquivo do Windows Installer (. MSI) ou executando um comando adicionar pacote SFTMIME, configurar pacote ou publicar pacote usando um manifesto do pacote.

PUBLISHed = 0 significa que o aplicativo não foi publicado ou não está mais publicado como resultado da realização de uma operação clara ou da execução de um comando de cancelamento de publicação do SFTMIME.

Se você usar o parâmetro/GLOBAL, o estado PUBLISHed será 1 para aplicativos que foram publicados globalmente e 0 para os aplicativos que foram publicados em contextos do usuário. Sem o parâmetro/GLOBAL, um estado publicado de 1 é retornado para aplicativos publicados no contexto do usuário que está executando o comando, e um estado de 0 é retornado para os aplicativos que são publicados globalmente.

 

O comando SFTMIME QUERY OBJ pode ser usado para consultar informações sobre todos os objetos mostrados acima — aplicativos, pacotes, associações de tipo de arquivo e servidores.Para mostrar como você pode usar o comando SFTMIME QUERY OBJ em suas tarefas normais de operações, o exemplo a seguir demonstra o processo que você seguiria se quisesse definir o valor do parâmetro OVERRIDEURL para um pacote específico para especificar um novo caminho para o conteúdo do pacote. 

1.  Para localizar o pacote que você deseja configurar, execute o seguinte comando:

    `SFTMIME QUERY OBJ:PACKAGE`

    Esse comando retorna cada nome de pacote descoberto como um GUID na primeira coluna de saída — por exemplo, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.

2.  Para definir o valor do parâmetro OVERRIDEURL, use o comando [Configurar pacote](configure-package.md) do SFTMIME. Por exemplo, para definir o valor OVERRIDEURL para esse pacote como um valor de *\\\\server\\share\\mypackage.sft*, use o comando Set Package do SFTMIME e dê a ele o GUID do pacote selecionado da saída do comando SFTMIME QUERY OBJ na etapa 1, seguido do parâmetro OVERRIDEURL e seu novo valor, da seguinte maneira:

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

Para a versão 4.6 SP2, a seguinte opção foi adicionada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT</p></td>
<td align="left"><p>Indica o estado atual do sinalizador/NO-UPDATE-FTA-SHORTCUT.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





