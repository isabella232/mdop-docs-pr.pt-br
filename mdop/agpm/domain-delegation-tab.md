---
title: Guia Delegação de Domínio
description: Guia Delegação de Domínio
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797363"
---
# Guia Delegação de Domínio


A guia de **delegação de domínio** no painel de **controle alterar** fornece uma lista de administradores de política de grupo que têm acesso ao arquivo no nível do domínio e indicam as funções de cada um. Além disso, esta guia habilita os administradores do AGPM (controle total) a configurar permissões no nível do domínio para editores, Aprovadores, revisores e outros administradores do AGPM. Há duas seções na guia de **delegação de domínio** – configuração de notificação por email e delegação baseada em função para gerenciamento avançado de política de grupo (AGPM) no nível do domínio.

## Configuração de notificação por email


A seção de notificação por email desta guia identifica os aprovadores que receberão notificações quando as operações estiverem pendentes no AGPM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuração</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>De</strong></p></td>
<td align="left"><p>O alias do AGPM do qual a notificação é enviada aos aprovadores. Em um ambiente com vários domínios, isso pode ser o mesmo alias em todo o ambiente ou um alias diferente para cada domínio.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Para</strong></p></td>
<td align="left"><p>Uma lista delimitada por vírgulas de endereços de email de aprovadores para quem a notificação deve ser enviada</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Servidor SMTP</strong></p></td>
<td align="left"><p>O nome do servidor de email, como mail.contoso.com</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nome de usuário</strong></p></td>
<td align="left"><p>Um usuário com acesso ao servidor SMTP</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Senha</strong></p></td>
<td align="left"><p>Senha do usuário para autenticação para o servidor SMTP</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Confirmar senha</strong></p></td>
<td align="left"><p>Confirmar senha do usuário</p></td>
</tr>
</tbody>
</table>

 

## Delegação baseada em função no nível de domínio


A seção delegação baseada em função desta guia exibe e permite que um administrador do AGPM delegue permissões permitidas, negadas e herdadas para cada grupo e usuário no domínio com acesso ao arquivo morto. Um administrador do AGPM pode configurar permissões de todo o domínio usando funções de AGPM padrão (editor, Aprovador, revisor e administrador do AGPM) ou uma combinação personalizada de permissões para cada administrador de política de grupo.

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
<td align="left"><p>Adicione uma nova entrada ao descritor de segurança. Qualquer usuário ou grupo no Active Directory pode ser adicionado como administradores de política de grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Remover</strong></p></td>
<td align="left"><p>Remover os administradores de política de grupo selecionados da lista controle de acesso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propriedades</strong></p></td>
<td align="left"><p>Exibir as propriedades dos administradores de política de grupo selecionados. A página Propriedades é a mesma exibida para um objeto em <strong> usuários e computadores do Active Directory </strong> .</p></td>
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

-   [Interface do usuário: Gerenciamento Avançado de Política de Grupo](user-interface-advanced-group-policy-management.md)

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks.md)

 

 





