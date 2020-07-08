---
title: Recursos da guia Conteúdo
description: Recursos da guia Conteúdo
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797416"
---
# Recursos da guia Conteúdo


Cada guia secundária na guia **conteúdo** tem duas seções: objetos e **grupos e usuários**da**política de grupo** .

## Seção objetos de política de grupo


A seção **objetos de política de grupo** exibe uma lista filtrada dos objetos de política de grupo (GPOs) e identifica os atributos a seguir para cada GPO. Você pode usar a caixa de **pesquisa** para pesquisar GPOs com atributos específicos. Para obter mais informações, consulte [Pesquisar e filtrar a lista de GPOs](search-and-filter-the-list-of-gpos.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Atributo GPO</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nome do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>O estado do GPO selecionado</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Alterado por</strong></p></td>
<td align="left"><p>O editor que fez check-in ou o aprovador que implantou o GPO selecionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Alterar Data</strong></p></td>
<td align="left"><p>Para um GPO controlado, a data mais recente em que foi feito o check-out após a modificação ou check-out para ser modificado. Para um GPO não controlado, a data em que ele foi modificado pela última vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comentário</strong></p></td>
<td align="left"><p>Um comentário inserido pela pessoa que fez check-in ou implantou um GPO no momento em que ele foi modificado. Útil para identificar as especificidades da versão em caso de necessidade de reverter para uma versão anterior.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versão do computador</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do computador do GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Versão do usuário</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do usuário do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Status do GPO</strong></p></td>
<td align="left"><p>A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente. O status do GPO indica quais partes do GPO estão habilitadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Exiba os filtros WMI aplicados a esse GPO. Os filtros WMI são gerenciados na <strong> pasta filtros WMI </strong> do domínio na árvore de console do GPMC.</p></td>
</tr>
</tbody>
</table>

 

## Seção grupos e usuários


Quando um GPO é selecionado, a seção **grupos e usuários** exibe uma lista dos grupos e usuários com acesso a esse GPO. As permissões e herança permitidas são exibidas para cada grupo ou usuário. Um administrador do AGPM pode configurar permissões usando as funções padrão do AGPM (editor, Aprovador, revisor e administrador do AGPM) ou uma combinação personalizada de permissões.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Botão</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Adicionar</strong></p></td>
<td align="left"><p>Adicione uma nova entrada ao descritor de segurança. Qualquer usuário ou grupo no Active Directory pode ser adicionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Remover</strong></p></td>
<td align="left"><p>Remover a entrada selecionada da lista de controle de acesso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propriedades</strong></p></td>
<td align="left"><p>Exibir as propriedades do objeto selecionado. A página Propriedades é a mesma exibida para um objeto em <strong> usuários e computadores do Active Directory </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avançado</strong></p></td>
<td align="left"><p>Abrir o <strong> Editor de lista de controle de acesso </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Considerações adicionais

-   Para obter informações sobre funções e permissões relacionadas a tarefas específicas, consulte as tarefas em [executando tarefas do administrador do AGPM](performing-agpm-administrator-tasks-agpm40.md), [executando tarefas do editor](performing-editor-tasks-agpm40.md), [executando tarefas do aprovador](performing-approver-tasks-agpm40.md)e [executando tarefas do revisor](performing-reviewer-tasks-agpm40.md).

### Referências adicionais

-   [Guia Conteúdo](contents-tab-agpm40.md)

 

 





