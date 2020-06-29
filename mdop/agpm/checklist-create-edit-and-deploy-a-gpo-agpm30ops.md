---
title: Lista de verificação criar, editar e implantar um GPO
description: Lista de verificação criar, editar e implantar um GPO
author: dansimp
ms.assetid: a7a17706-304a-4455-9ada-52508ec620f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35255926ba2384e2942900fc30eae06a30049a15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797459"
---
# Lista de verificação: Criar, editar e implantar um GPO


Em um ambiente onde várias pessoas fazem alterações nos objetos de política de grupo (GPOs) usando o gerenciamento avançado de política de grupo (AGPM), um administrador do AGPM (controle total) delega permissão para editores, Aprovadores e revisores, como grupos ou como indivíduos. Veja a seguir um processo típico de desenvolvimento de GPOs para um editor e um Aprovador.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Referência</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O editor solicita a criação de um novo GPO ou um Aprovador cria um novo GPO.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm30ops.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)">Solicitar a criação de um novo GPO controlado</a></p>
<p><a href="create-a-new-controlled-gpo-agpm30ops.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm30ops.md)">Criar um novo GPO controlado</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>O aprovador aprova a criação do GPO se ele foi solicitado por um editor.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm30ops.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm30ops.md)">Aprovar ou rejeitar uma ação pendente</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>O editor faz check-out de uma cópia do GPO do arquivamento, para que ninguém mais possa modificar o GPO. O editor faz alterações no GPO e, em seguida, verifica o GPO modificado no arquivo morto.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm30ops.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm30ops.md)">Editar um GPO offline</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>O editor solicita a implantação do GPO no ambiente de produção.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm30ops.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm30ops.md)">Solicitar a implantação de um GPO</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revisores, como aprovadores ou editores, analise o GPO.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm30ops.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md)">Execução de tarefas do revisor</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>O aprovador aprova e implanta o GPO no ambiente de produção ou rejeita o GPO.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm30ops.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm30ops.md)">Aprovar ou rejeitar uma ação pendente</a></p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

[Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





