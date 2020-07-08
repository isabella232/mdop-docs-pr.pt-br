---
title: Lista de verificação criar, editar e implantar um GPO
description: Lista de verificação criar, editar e implantar um GPO
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797458"
---
# Lista de verificação: Criar, editar e implantar um GPO


Em um ambiente em que várias pessoas alteram objetos de política de grupo (GPOs) usando o gerenciamento avançado de política de grupo (AGPM), um administrador do AGPM (controle total) delega permissão para editores, Aprovadores e revisores como grupos ou como indivíduos. Veja a seguir um processo típico de desenvolvimento de GPOs para um editor e um Aprovador.

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
<td align="left"><p>O editor solicita que um novo GPO seja criado ou um Aprovador cria um novo GPO.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">Solicitar a criação de um novo GPO controlado</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">Criar um novo GPO controlado</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>O aprovador aprova a criação do GPO se ele foi solicitado por um editor.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Aprovar ou rejeitar uma ação pendente</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>O editor verifica uma cópia do GPO do arquivo morto para que ninguém mais possa modificar o GPO. O editor faz alterações no GPO e, em seguida, verifica o GPO modificado no arquivo morto.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">Editar um GPO offline</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Se estiver desenvolvendo em uma floresta de teste, o editor exportará o GPO para um arquivo, transferirá o arquivo para a floresta de produção e importará o arquivo. Além disso, um editor pode vincular o GPO a uma unidade organizacional que contém computadores de teste e usuários.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">Como usar um ambiente de teste</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>O editor solicita a implantação do GPO no ambiente de produção do domínio.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">Solicitar a implantação de um GPO</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Revisores, como aprovadores ou editores, analise o GPO.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">Execução de tarefas do revisor</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>O aprovador aprova e implanta o GPO no ambiente de produção do domínio ou rejeita o GPO.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Aprovar ou rejeitar uma ação pendente</a></p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

[Gerenciamento Avançado de Política de Grupo 4.0](advanced-group-policy-management-40.md)

 

 





