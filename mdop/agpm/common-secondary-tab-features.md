---
title: Recursos comuns da guia secundária
description: Recursos comuns da guia secundária
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797455"
---
# Recursos comuns da guia secundária


Cada guia secundária tem duas seções:**objetos** e **grupos e usuários**da política de grupo.

## Seção objetos de política de grupo


A seção **objetos de política de grupo** exibe uma lista filtrada dos objetos de política de grupo (GPOs) e identifica as características a seguir para cada GPO:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica do GPO</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nome do objeto de política de grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Computador (comp.)</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do computador do GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Usuário</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do usuário do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>O estado do GPO selecionado:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Não controlado: </strong> não gerenciado pelo AGPM.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Check-in: </strong> disponível para editores autorizados para fazer check-out para edição ou para a implantação de um administrador de política de grupo.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Check-out: </strong> atualmente sendo editado. Não disponível para outros editores fazer check-out até o editor que o fez check-out ou um administrador do AGPM fazer o check-in.</p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong>Pendente: </strong> aguardando aprovação de um administrador de política de grupo antes de ser criado, controlado, implantado ou excluído.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Excluído: </strong> excluído do arquivo morto, mas ainda pode ser restaurado.</p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong>Modelo: </strong> uma versão estática de um GPO para ser usada como ponto de partida ao criar novos GPOs.</p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong>Modelo (padrão): </strong> por padrão, esse modelo é o ponto de partida usado durante a criação de um novo GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Status do GPO</strong></p></td>
<td align="left"><p>A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente. O status do GPO indica quais partes do GPO estão habilitadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Exiba os filtros WMI aplicados a esse GPO. Os filtros WMI são gerenciados no <strong> nó filtros WMI </strong> do domínio na árvore de console do GPMC.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificação em</strong></p></td>
<td align="left"><p>Para um GPO controlado, a data mais recente em que foi feito o check-in após a modificação ou check-out para ser modificado. Para um GPO não controlado, a data em que ele foi modificado pela última vez.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Proprietário</strong></p></td>
<td align="left"><p>O editor que fez check-in ou o aprovador que implantou o GPO selecionado.</p></td>
</tr>
</tbody>
</table>

 

## Seção grupos e usuários


Quando um GPO é selecionado, a seção **grupos e usuários** exibe uma lista dos grupos e usuários com acesso a esse GPO. As permissões e herança permitidas são exibidas para cada grupo ou usuário. Um administrador do AGPM pode configurar permissões usando as funções padrão do AGPM (editor, Aprovador e revisor) ou uma combinação personalizada de permissões.

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

-   Para obter informações sobre funções e permissões relacionadas a tarefas específicas, consulte as tarefas em [executando tarefas do administrador do AGPM](performing-agpm-administrator-tasks.md), [executando tarefas do editor](performing-editor-tasks.md), [executando tarefas do aprovador](performing-approver-tasks.md)e [executando tarefas do revisor](performing-reviewer-tasks.md).

### Referências adicionais

-   [Guia Conteúdo](contents-tab.md)

 

 





