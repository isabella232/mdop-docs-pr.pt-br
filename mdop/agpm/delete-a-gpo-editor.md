---
title: Excluir um GPO
description: Excluir um GPO
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797832"
---
# Excluir um GPO


Como um editor, talvez você não tenha permissão para concluir a exclusão de um objeto de política de grupo (GPO), mas tem a permissão necessária para iniciar o processo e enviar sua solicitação a um Aprovador.

Uma conta de usuário com a função de editor ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para solicitar a exclusão de um GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO a ser excluído e, em seguida, clique em **excluir**.

    -   Para excluir o GPO do arquivo morto, deixando a versão implantada do GPO intocado no ambiente de produção, clique em **excluir GPO de somente arquivo morto (não controlar)**.

    -   Para excluir o GPO do ambiente de arquivamento e de produção, clique em **excluir GPO do arquivamento e da produção**.

        A menos que você tenha permissão especial para excluir GPOs, você deve enviar uma solicitação de exclusão do GPO implantado. Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** . Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **Enviar**.

4.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado a sua solicitação, o GPO será movido da guia **pendente** para a guia **Lixeira** , onde poderá ser restaurado ou destruído.

### Considerações adicionais

-   Por padrão, você deve ser um editor para solicitar a exclusão de um GPO implantado. Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO.

-   Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para excluir um GPO do arquivo morto. Especificamente, você deve ter **conteúdo da lista** e **Editar as** permissões do **GPO ou excluir** as permissões do GPO.

-   Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**. O GPO será retornado para a guia **controlado** .

-   Para excluir um GPO não controlado do ambiente de produção sem primeiro controlá-lo, no **console de gerenciamento de política de grupo**, clique em **floresta**, clique em **domínios**, clique em ** &lt; &gt; mydomain**e, em seguida, clique em objetos de política de **grupo**. Clique com o botão direito do mouse no GPO não controlado e clique em **excluir**.

### Referências adicionais

-   [Como executar tarefas de editor](performing-editor-tasks.md)

 

 





