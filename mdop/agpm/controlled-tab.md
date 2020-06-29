---
title: Guia Controlados
description: Guia Controlados
author: dansimp
ms.assetid: 8995a9e1-ace4-40b7-a47b-e1e9924541ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71668555dd0b5d5ff42b5a4a49ecaaa5edec52e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797863"
---
# Guia Controlados


A guia **controlado** :

-   Exibe uma lista de objetos de política de grupo (GPOs) gerenciados pelo gerenciamento avançado de política de grupo (AGPM).

-   Fornece um menu de atalho com comandos para gerenciar GPOs e para exibir o histórico e relatórios de GPOs.

-   Exibe uma lista dos grupos e usuários que têm permissão para acessar um GPO selecionado.

Clicar com o botão direito do mouse na lista **objetos de política de grupo** nessa guia exibe um menu de atalho, incluindo qualquer uma das opções a seguir, que se aplicam.

## Controle e histórico


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Novo GPO controlado</strong></p></td>
<td align="left"><p>Crie um novo GPO com controle de alterações gerenciado por meio do AGPM e implante-o no ambiente de produção. Se você não tiver permissão para criar um GPO, será solicitado a enviar uma solicitação. (Esta opção será exibida se nenhum GPO for selecionado ao clicar com o <strong> botão direito do mouse na Lista de objetos de política de grupo </strong> .)</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Histórico</strong></p></td>
<td align="left"><p>Abrir uma janela listando todas as versões do GPO selecionado salvas no arquivo morto. No histórico, você pode obter um relatório das configurações em um GPO, comparar duas versões de um GPO, comparar um GPO a um modelo ou retornar a uma versão anterior de um GPO.</p></td>
</tr>
</tbody>
</table>

 

## Relatórios


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurações</strong></p></td>
<td align="left"><p>Gerar um relatório baseado em HTML ou baseado em XML exibindo as configurações no GPO selecionado ou exibir links para o (s) GPO (s) selecionado (s) de unidades organizacionais a partir de quando o (s) GPO (s) foi (m) mais recentemente controlado, importado ou check-in.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Existentes</strong></p></td>
<td align="left"><p>Gerar um relatório baseado em HTML ou baseado em XML para comparar as configurações dentro de dois GPOs selecionados ou no GPO selecionado e um modelo.</p></td>
</tr>
</tbody>
</table>

 

## Edição


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Editar</strong></p></td>
<td align="left"><p>Abrir o <strong> Editor de objeto de política </strong> de grupo para fazer alterações no GPO selecionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Fazer Check-out</strong></p></td>
<td align="left"><p>Obtenha uma cópia do GPO selecionado do arquivo para edição offline e proíba a qualquer pessoa de editá-lo até que ele seja novamente verificado no arquivo. (Check-out pode ser substituído por um administrador do AGPM (controle total).)</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Fazer Check-in</strong></p></td>
<td align="left"><p>Verifique a versão editada do GPO selecionado no arquivo morto para que outros editores autorizados possam fazer alterações ou um Aprovador possa implantá-lo no ambiente de produção.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Desfazer check-out</strong></p></td>
<td align="left"><p>Retorne um GPO com check-out para o arquivo sem alterações.</p></td>
</tr>
</tbody>
</table>

 

## Gerenciamento de versão


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Importar da produção</strong></p></td>
<td align="left"><p>Para o GPO selecionado, copie a versão no ambiente de produção para o arquivo morto.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Excluir</strong></p></td>
<td align="left"><p>Mova o GPO selecionado para a lixeira e indique se deseja sair da versão implantada (se houver) em produção ou excluí-la, bem como a versão no arquivo. Se você não tiver permissão para excluir um GPO, será solicitado a enviar uma solicitação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Implantar</strong></p></td>
<td align="left"><p>Mova o GPO selecionado que está marcado para o arquivo morto para o ambiente de produção. Essa ação faz com que ela seja ativada na rede e substitui a versão ativa anteriormente do GPO, se houver uma existente. Se você não tiver permissão para implantar um GPO, será solicitado a enviar uma solicitação.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Rótulo</strong></p></td>
<td align="left"><p>Marque o GPO selecionado com um rótulo descritivo (como &quot; conhecido como satisfatório &quot; ) e faça um comentário para a manutenção de registros. Os rótulos são exibidos <strong> na </strong> coluna Estado e nos comentários <strong> na </strong> coluna comentário da <strong> janela do histórico </strong> , permitindo que você identifique facilmente as versões anteriores de um GPO identificada com um rótulo específico, para que possa reverter se ocorrer um problema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Renomear</strong></p></td>
<td align="left"><p>Alterar o nome do GPO selecionado. Se o GPO já tiver sido implantado, o nome será atualizado no ambiente de produção quando o GPO for reimplantado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Salvar como modelo</strong></p></td>
<td align="left"><p>Criar um novo modelo com base nas configurações do GPO selecionado.</p></td>
</tr>
</tbody>
</table>

 

## Diversos


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Atualizar</strong></p></td>
<td align="left"><p>Atualize a exibição do console de gerenciamento de política de grupo para incorporar alterações. Algumas alterações não ficam visíveis até que a exibição seja atualizada.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ajuda</strong></p></td>
<td align="left"><p>Exibir a ajuda do AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Guia Conteúdo](contents-tab.md)

-   [Como executar tarefas de editor](performing-editor-tasks.md)

-   [Execução de tarefas do aprovador](performing-approver-tasks.md)

-   [Execução de tarefas do revisor](performing-reviewer-tasks.md)

 

 





