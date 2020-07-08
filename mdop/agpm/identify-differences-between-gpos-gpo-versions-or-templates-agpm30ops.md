---
title: Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos
description: Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos
author: dansimp
ms.assetid: e391fa91-3956-4150-9d43-900cfc88d543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88c37a3723c31fb110e731084237a8d89350a4ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797792"
---
# Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos


Você pode gerar relatórios de diferença baseados em HTML ou baseados em XML para analisar as diferenças entre objetos de política de grupo (GPOs), modelos ou versões diferentes de um GPO.

Uma conta de usuário com a função revisor, editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

## Identificar diferenças entre GPOs, versões de GPO ou modelos


-   [Entre dois GPOs ou modelos](#bkmk-two-gpos)

-   [Entre um GPO e um modelo](#bkmk-gpo-and-template)

-   [Entre duas versões de um GPO](#bkmk-two-versions)

-   [Entre uma versão de GPO e um modelo](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**Para identificar as diferenças entre dois GPOs ou modelos**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).

3.  Selecione os dois GPOs ou modelos.

4.  Clique com o botão direito do mouse em um dos GPOs ou modelos, clique em **diferenças**e, em seguida, clique em **relatório HTML** ou **relatório XML** para exibir um relatório de diferença Resumindo as configurações dos GPOs ou modelos.

### <a href="" id="bkmk-gpo-and-template"></a>

**Para identificar as diferenças entre um GPO e um modelo**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).

3.  Clique com o botão direito do mouse no GPO, clique em **diferenças**e, em seguida, clique em **modelo**.

4.  Selecione o modelo e o tipo de relatório e, em seguida, clique em **OK** para exibir um relatório de diferença Resumindo as configurações do GPO e do modelo.

### <a href="" id="bkmk-two-versions"></a>

**Para identificar as diferenças entre duas versões de um GPO**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).

3.  Clique duas vezes no GPO para exibir o histórico e, em seguida, realce as versões a serem comparadas.

4.  Clique com o botão direito do mouse em uma das versões, clique em **diferenças**e, em seguida, clique em **relatório HTML** ou **relatório XML** para exibir um relatório de diferença Resumindo as configurações dos GPOs.

### <a href="" id="bkmk-gpo-version-and-template"></a>

**Para identificar as diferenças entre uma versão de GPO e um modelo**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs (ou modelos, se for comparar dois modelos).

3.  Clique duas vezes no GPO para exibir seu histórico.

4.  Clique com o botão direito do mouse na versão do GPO do interesse, clique em **diferenças**e, em seguida, clique em **modelo**.

5.  Selecione o modelo e o tipo de relatório e, em seguida, clique em **OK** para exibir um relatório de diferença Resumindo as configurações da versão e do modelo do GPO.

## Chave para relatórios de diferença


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Símbolo</th>
<th align="left">Significado</th>
<th align="left">Cor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>O item existe com configurações idênticas nos dois GPOs</p></td>
<td align="left"><p>Varia de acordo com o nível</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>O item existe nos dois GPOs, mas com configurações alteradas</p></td>
<td align="left"><p>Chuva</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>O item existe somente no primeiro GPO</p></td>
<td align="left"><p>Vermelho</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>O item existe somente no segundo GPO</p></td>
<td align="left"><p>Verde</p></td>
</tr>
</tbody>
</table>

 

-   Para itens com configurações alteradas, as configurações alteradas são identificadas quando o item é expandido. O valor do atributo em cada GPO é exibido na mesma ordem em que os GPOs são exibidos no relatório.

-   Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens diferentes (um presente somente no primeiro GPO, um presente somente no segundo) em vez de um item alterado.

### Considerações adicionais

-   Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o GPO. Além disso, para exibir a lista de GPOs, você deve ter permissão de **lista de conteúdo** para o domínio.

### Referências adicionais

-   [Execução de tarefas do revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





