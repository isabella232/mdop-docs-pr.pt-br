---
title: Comandos de modelo
description: Comandos de modelo
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797674"
---
# Comandos de modelo


A guia **modelos** :

-   Exibe uma lista de modelos disponíveis que você pode usar para criar novos objetos de política de grupo (GPOs).

-   Fornece um menu de atalho com comandos para criar um GPO com base em um modelo selecionado, gerenciar modelos e exibir relatórios para modelos.

-   Exibe uma lista dos grupos e usuários que têm permissão para acessar um modelo selecionado.

Como um modelo não pode ser alterado, os modelos não têm histórico. No entanto, como qualquer versão do GPO, as configurações de um modelo podem ser exibidas com um relatório de configurações ou comparadas a outro GPO com um relatório de diferença.

**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.

 

Clicar com o botão direito do mouse na lista **objetos de política de grupo** nessa guia exibe um menu de atalho, incluindo qualquer uma das opções a seguir, que se aplicam.

## Controle


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
<td align="left"><p>Criar um novo GPO com base no modelo selecionado. É fornecida a opção para implantar o novo GPO no ambiente de produção. Se você não tiver permissão para criar um GPO, será solicitado a enviar uma solicitação. (Esta opção será exibida se nenhum GPO for selecionado ao clicar com o <strong> botão direito do mouse na Lista de objetos de política de grupo </strong> .)</p></td>
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
<td align="left"><p>Gerar um relatório baseado em HTML ou baseado em XML exibindo as configurações dentro do GPO selecionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Existentes</strong></p></td>
<td align="left"><p>Gerar um relatório baseado em HTML ou baseado em XML para comparar as configurações dentro de dois modelos de GPO selecionados.</p></td>
</tr>
</tbody>
</table>

 

## Gerenciamento de modelos


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
<td align="left"><p><strong>Definir como padrão</strong></p></td>
<td align="left"><p>Defina o modelo selecionado como o padrão a ser usado automaticamente ao criar um novo GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Excluir</strong></p></td>
<td align="left"><p>Mover o modelo selecionado para a <strong> Lixeira </strong> . Se você não tiver permissão para excluir um GPO, será solicitado a enviar uma solicitação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Renomear</strong></p></td>
<td align="left"><p>Alterar o nome do modelo selecionado.</p></td>
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
<td align="left"><p>Exibir ajuda para o gerenciamento avançado de política de grupo (AGPM).</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Guia Conteúdo](contents-tab-agpm30ops.md)

-   [Como executar tarefas de editor](performing-editor-tasks-agpm30ops.md)

-   [Execução de tarefas do revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





