---
title: Configurar segurança de email para o AGPM
description: Configurar segurança de email para o AGPM
author: dansimp
ms.assetid: b9c48894-0a10-4d03-8027-50ed3b02485a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a384c2a21f912ca7ec55a5e4c74ca7062bfe864c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797436"
---
# Configurar segurança de email para o AGPM


Por padrão, as notificações por email enviadas devido a ações no AGPM (gerenciamento avançado de política de grupo) não são criptografadas e são enviadas por meio da porta 25 SMTP. No entanto, você pode configurar a segurança de email para o AGPM usando configurações do registro para especificar se deseja usar a criptografia SSL (Secure Sockets Layer) e qual porta SMTP usar.

Ao criptografar notificações por email do AGPM, você pode proteger melhor as pessoas que podem revelar informações confidenciais sobre a segurança da sua organização. As notificações de criptografia de email são recomendadas quando elas são retransmitidas por servidores de email remotos e podem ser necessárias para alguns regulamentos sobre conformidade.

**Cuidado**  A edição incorreta do registro pode danificar seriamente seu sistema. Antes de fazer alterações no registro, você deve fazer backup de todos os dados importantes do computador.

 

Uma conta de usuário que tem a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o objeto de política de grupo (GPO) usado nesses procedimentos ou uma conta de usuário que tenha as permissões necessárias no AGPM é necessária para concluir estes procedimentos. Examine os detalhes em "considerações adicionais" neste tópico.

**Para configurar a segurança de email para o AGPM usando as preferências de política de grupo**

1.  Na árvore do **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os servidores do AGPM para os quais você deseja configurar a segurança de email. (Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)

2.  Na janela **Editor de gerenciamento de política de grupo** , expanda a **configuração do computador**, **preferências**, **configurações do Windows**e pastas **do registro** .

3.  Na árvore do console, clique com o botão direito do mouse em **registro**, aponte para **novo**, clique em **item da coleção**e digite segurança de email do **AGPM**.

4.  Crie um item de preferência Registry para ativar a criptografia:

    1.  Na árvore de console, clique com o botão direito do mouse em **segurança de email do AGPM**, aponte para **novo**e clique em **item do registro**.

    2.  Na caixa de diálogo **novas propriedades do registro** , selecione a ação **Atualizar** .

    3.  Para **Hive**, selecione **HKEY \ _LOCAL \ _MACHINE**.

    4.  Para o **caminho da chave**, digite **SOFTWARE\\Microsoft\\AGPM**.

    5.  Para **nome do valor**, digite **EncryptSmtp**.

    6.  Para **tipo de valor**, selecione **reg \ _DWORD**.

    7.  Para **base**, selecione **decimal**e para **dados de valor**, digite **1** para usar a criptografia SSL ou **0** para permitir que o email seja enviado sem criptografia. Por padrão, o email é enviado sem criptografia. Clique em **OK**.

5.  Crie um item de preferência Registry para especificar a porta SMTP:

    1.  Na árvore de console, clique com o botão direito do mouse em **segurança de email do AGPM**, aponte para **novo**e clique em **item do registro**.

    2.  Na caixa de diálogo **novas propriedades do registro** , selecione a ação **Atualizar** .

    3.  Para **Hive**, selecione **HKEY \ _LOCAL \ _MACHINE**.

    4.  Para a caixa de diálogo **caminho da chave** , digite **SOFTWARE\\Microsoft\\AGPM**.

    5.  Para **nome do valor**, digite **SMTPPORT**.

    6.  Para **tipo de valor**, selecione **reg \ _DWORD**.

    7.  Para **base**, selecione **decimal**e para **dados de valor**, digite um número de porta para a porta SMTP. Por padrão, a porta SMTP é a porta 25 se a criptografia não estiver habilitada ou porta 587 se a criptografia SSL estiver habilitada. Clique em **OK**.

6.  Feche a janela do **Editor de gerenciamento de política de grupo** e, em seguida, faça check-in e implante o GPO. Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).

### Considerações adicionais

-   Você deve ser capaz de editar e implantar um GPO para definir as configurações do registro usando as preferências de política de grupo. Consulte [editando um GPO](editing-a-gpo-agpm40.md) e [implante um GPO](deploy-a-gpo-agpm40.md) para obter detalhes adicionais.

### Referências adicionais

-   [Configuração do Gerenciamento Avançado de Política de Grupo](configuring-advanced-group-policy-management-agpm40.md)

 

 





