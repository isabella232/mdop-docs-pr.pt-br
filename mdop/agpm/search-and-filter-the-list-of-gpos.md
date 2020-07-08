---
title: Pesquisar e filtrar a lista de GPOs
description: Pesquisar e filtrar a lista de GPOs
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797690"
---
# Pesquisar e filtrar a lista de GPOs


No gerenciamento avançado de política de grupo (AGPM), você pode pesquisar a lista de objetos de política de grupo (GPOs) e seus atributos para filtrar a lista de GPOs exibida. Por exemplo, você pode pesquisar GPOs com um nome, estado ou comentário específico. Você também pode pesquisar os GPOs que foram alterados pela última vez por um determinado administrador de política de grupo ou em uma data específica.

## Executar uma pesquisa complexa


Você pode realizar uma pesquisa complexa usando o atributo Format *GPO 1: Pesquisar Cadeia de caracteres 1 do atributo GPO 2: Pesquisar Cadeia de caracteres 2... cadeias de caracteres de pesquisa de todas as colunas*. A pesquisa não diferencia maiúsculas de minúsculas.

-   **Atributo GPO:** Qualquer título de coluna na lista de GPOs em AGPM diferente da **versão do computador** ou da **versão do usuário**. Os atributos de GPO incluem o nome do GPO, o estado, o usuário que alterou mais recentemente o GPO, a data e a hora em que o GPO foi alterado mais recentemente, comentário, status do GPO e filtro WMI aplicado ao GPO.

-   **Cadeia de pesquisa:** Texto a ser pesquisado na coluna especificada. Se uma cadeia de caracteres incluir espaços, você deve colocar a cadeia de caracteres entre aspas.

-   **Cadeias de caracteres de pesquisa de todas as colunas:** Texto no qual Pesquisar em todas as colunas da lista de GPOs em AGPM diferente da **versão do computador** e da **versão do usuário**. Você pode incluir várias cadeias de caracteres separadas por espaços. Se uma cadeia de caracteres incluir espaços, você deve colocar a cadeia de caracteres entre aspas.

Cada par de atributos de objeto de objeto e de cadeia de caracteres de pesquisa e cada cadeia de caracteres de pesquisa de todas as colunas são combinados usando uma operação e lógica. O resultado é uma lista de todos os GPOs para os quais cada atributo especificado inclui a cadeia de caracteres de pesquisa especificada e para a qual todas as cadeias de caracteres de pesquisa de todas as colunas aparecem em pelo menos uma coluna. A pesquisa retorna quaisquer correspondências parciais para cadeias de caracteres para que você possa inserir parte de um nome de GPO ou nome de usuário e exibir uma lista de todos os GPOs que incluam esse texto no nome.

Veja a seguir exemplos de pesquisas:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrição do resultado da pesquisa</th>
<th align="left">Consulta de pesquisa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Todos os GPOs com nomes que incluem a <strong> segurança de texto </strong> e a <strong> América do Norte </strong> .</p></td>
<td align="left"><p><strong>Nome: </strong><strong> nome de segurança </strong><strong> : </strong> &quot; <strong> América do Norte</strong>&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>Todos os GPOs com check-out.</p></td>
<td align="left"><p><strong>Estado: </strong> &quot; <strong> com check-out</strong>&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Todos os GPOs alterados mais recentemente pelo usuário chamado <strong> administrador </strong> e alterados recentemente no mês anterior.</p></td>
<td align="left"><p><strong>alterado por: </strong><strong> data de alteração do administrador </strong><strong> : </strong><strong> lastmonth</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Todos os GPOs nos quais o <strong> Firewall do Word </strong> está incluído no comentário mais recente e no qual a palavra <strong> segurança é </strong> exibida em qualquer coluna.</p></td>
<td align="left"><p><strong>Comentário: </strong><strong> segurança do firewall </strong><strong></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Todos os GPOs que têm um status de <strong> todas as configurações desabilitadas </strong> .</p></td>
<td align="left"><p><strong>status do GPO: </strong><strong> todos</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Todos os GPOs que têm um filtro WMI chamado <strong> meu filtro WMI </strong> foram aplicados e que têm um status de <strong> configuração do usuário desabilitado </strong> .</p></td>
<td align="left"><p><strong>filtro WMI: </strong> &quot; <strong> status do GPO do meu filtro WMI </strong> &quot; <strong> : </strong><strong> usuário</strong></p></td>
</tr>
</tbody>
</table>

 

## Especificando datas


Você pode pesquisar os GPOs alterados em uma data específica, em um horário específico ou durante um período de tempo usando os mesmos termos especiais disponíveis quando você pesquisa no Windows. Ao inserir uma data ou hora específica, você deve usar o formato usado na coluna **alterar Data** . Veja a seguir exemplos de pesquisas da coluna **data de alteração** :

-   **alterar Data:****10/10/2009**

-   **alterar Data:****10/10/2009 9:00:00 am**

-   **alterar Data:****thisweek**

Você pode usar os seguintes termos especiais, que não diferenciam maiúsculas de minúsculas, quando você pesquisa a coluna **alterar Data** :

-   **Hoje**

-   **Ontem**

-   **ThisWeek**

-   **LastWeek**

-   **ThisMonth**

-   **LastMonth**

-   **TwoMonths**

-   **ThreeMonths**

-   **ThisYear**

-   **LastYear**

### Considerações adicionais

-   Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **listar conteúdo** para o domínio.

-   Para obter mais informações sobre atributos de GPO, consulte [recursos da guia conteúdo](contents-tab-features-agpm40.md).

### Referências adicionais

-   [Gerenciamento Avançado de Política de Grupo 4.0](advanced-group-policy-management-40.md)

 

 





