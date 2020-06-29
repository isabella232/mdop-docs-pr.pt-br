---
title: Permissões de acesso de usuário no Application Virtualization Client
description: Permissões de acesso de usuário no Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796661"
---
# Permissões de acesso de usuário no Application Virtualization Client


Na guia **permissões** , na caixa de diálogo **Propriedades** , acessível ao clicar com o botão direito do mouse no nó **virtualização do aplicativo** no console de gerenciamento do aplicativo virtualização de aplicativos, os administradores podem conceder permissões aos usuários para usar as várias funções de cliente.

**Observação**  Antes de alterar as permissões de usuários, certifique-se de que as alterações de permissões sejam consistentes com as diretrizes da organização para conceder permissões de usuário.

 

A tabela a seguir lista e descreve as permissões que podem ser concedidas aos usuários.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da permissão</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Adicionar aplicativos</p></td>
<td align="left"><p>Registre novos aplicativos passando um novo arquivo OSD para o cliente usando sfttray.exe, sftmime.exe ou o MMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Alterar o tamanho do cache do sistema de arquivos</p></td>
<td align="left"><p>Aumente o tamanho do cache do sistema de arquivos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alterar unidade do sistema de arquivos</p></td>
<td align="left"><p>Selecione uma letra de unidade preferida diferente para o sistema de arquivos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Alterar configurações de log</p></td>
<td align="left"><p>Altere o nível de log ou o caminho do log para o arquivo de log do cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alterar arquivos OSD</p></td>
<td align="left"><p>Modifique arquivos OSD para aplicativos registrados e passe-os para o cliente. Isso não afeta a publicação de atualização.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Limpar configurações do aplicativo</p></td>
<td align="left"><p>Exclua tipos de arquivo, atalhos e todas as configurações do usuário atual.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Excluir aplicativos</p></td>
<td align="left"><p>Remova todas as referências a um aplicativo do sistema de arquivos e do cache do OSD para todos os usuários do computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Importar aplicativos para o cache</p></td>
<td align="left"><p>Carregar dados de aplicativo diretamente de um arquivo SFT especificado no cache do sistema de arquivos. Isso afeta todos os usuários.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Carregar aplicativos no cache</p></td>
<td align="left"><p>Inicie uma carga do arquivo SFT para um aplicativo da fonte configurada, como um servidor de streaming App-V. Isso carrega o aplicativo para todos os usuários do computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bloquear e desbloquear aplicativos no cache</p></td>
<td align="left"><p>Impedir ou permitir que os aplicativos sejam descarregados do cache do sistema de arquivos. Isso afetará todos os usuários do computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gerenciar associações de tipo de arquivo</p></td>
<td align="left"><p>Adicionar, modificar ou excluir associações de tipo de arquivo somente para o usuário atual.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gerenciar configurações de atualização de publicação</p></td>
<td align="left"><p>Altere as configurações que controlam o tempo de publicação de atualizações para todos os usuários do computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gerenciar servidores de publicação</p></td>
<td align="left"><p>Adicionar, modificar ou excluir servidores de publicação para todos os usuários do computador. Essa permissão implicitamente inclui permissão para gerenciar as configurações de atualização da publicação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar atalhos</p></td>
<td align="left"><p>Crie novos atalhos para aplicativos registrados. O usuário também deve ter permissão para criar arquivos no sistema de arquivos local.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reparar aplicativos</p></td>
<td align="left"><p>Remover configurações específicas do aplicativo para o usuário atual sem remover atalhos ou associações de tipo de arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Iniciar uma atualização de publicação</p></td>
<td align="left"><p>Iniciar uma atualização de publicação não agendada para o usuário atual.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alternar o modo offline</p></td>
<td align="left"><p>Altere o cliente inteiro de online para o modo offline para todos os usuários.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descarregar aplicativos do cache</p></td>
<td align="left"><p>Limpar dados de aplicativo do cache do sistema de arquivos para todos os usuários sem remover configurações específicas do usuário, atalhos ou associações de tipo de arquivo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exibir todos os aplicativos</p></td>
<td align="left"><p>Permita que o usuário veja os aplicativos virtuais para todos os usuários registrados no computador.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Como alterar permissões de acesso de usuário](how-to-change-user-access-permissions.md)

 

 





