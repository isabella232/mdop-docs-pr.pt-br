---
title: Editar um GPO offline
description: Editar um GPO offline
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797815"
---
# Editar um GPO offline


Para fazer alterações em um GPO (objeto de política de grupo) controlado, você deve primeiro fazer o check-out de uma cópia do GPO do arquivo. Ninguém mais conseguirá modificar o GPO até que ele seja novamente verificado, evitando a introdução de alterações conflitantes por vários administradores de política de grupo. Quando terminar de modificar o GPO, verifique-o no arquivo morto para que ele possa ser revisado e implantado no ambiente de produção.

Uma conta de usuário com a função de editor ou administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

## Editando um GPO offline


Para editar um GPO, você pode fazer o check-out do GPO, editar o GPO offline e, em seguida, verificar o GPO no arquivo morto para que ele possa ser revisado e implantado (ou modificado por outros editores).

-   [Fazer check-out de um GPO](#bkmk-checkout)

-   [Editar um GPO](#bkmk-edit)

-   [Fazer check-in de um GPO](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**Para fazer check-out de um GPO do arquivo para edição**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO a ser editado e, em seguida, clique em **check-out**.

4.  Digite um comentário a ser exibido no histórico do GPO durante o check-out e clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. Na guia **controlado** , o estado do GPO agora está identificado como Checked- **out**.

### <a href="" id="bkmk-edit"></a>

**Para editar um GPO offline**

1.  Na guia **controlado** , clique com o botão direito do mouse no GPO a ser editado e, em seguida, clique em **Editar**.

2.  No **Editor de objeto de política de grupo**, faça alterações em uma cópia offline do GPO.

3.  Quando terminar de modificar o GPO, feche o **Editor de objeto de política de grupo**.

### <a href="" id="bkmk-checkin"></a>

**Para verificar um GPO no arquivo morto**

1.  Na guia **controlado** :

    -   Se você não fez alterações no GPO, clique com o botão direito do mouse no GPO e clique em **desfazer check-out**e, em seguida, clique em **Sim** para confirmar.

    -   Se você fez alterações no GPO, clique com o botão direito do mouse no GPO e clique em **fazer check-in**.

2.  Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.

3.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. Na guia **controlado** , o estado do GPO é identificado como **checked-in**.

### Considerações adicionais

-   Para fazer check-out e editar um GPO, por padrão, você deve ser o aprovador que criou ou controlado o GPO, um editor ou um administrador do AGPM (controle total). Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO. Além disso, para editar o GPO, você deve ser a pessoa que fez check-out do GPO.

-   Para fazer check-in de um GPO, por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total). Especificamente, você deve ter o **conteúdo da lista** e **Editar as** permissões do **GPO** para o GPO. Se você não for um Aprovador ou administrador do AGPM (ou outro administrador da política de grupo com a permissão **implantar GPO** ), você deve ser o editor que fez check-out do GPO.

-   Ao editar um GPO, qualquer atualização de instalação de software de política de grupo de um pacote em outro GPO deve referenciar o GPO implantado, não a cópia com check-out.

### Referências adicionais

-   [Editando um GPO](editing-a-gpo.md)

-   Revisando um GPO

    -   [Analisar configurações do GPO](review-gpo-settings.md)

    -   [Analisar links do GPO](review-gpo-links.md)

    -   [Identificar as diferenças entre os GPOs, as versões de GPO ou os modelos](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   Implantando um GPO

    -   [Solicitar a implantação de um GPO](request-deployment-of-a-gpo.md)

    -   [Implantar um GPO](deploy-a-gpo.md)

 

 





