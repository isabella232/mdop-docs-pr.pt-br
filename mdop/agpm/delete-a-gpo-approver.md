---
title: Excluir um GPO
description: Excluir um GPO
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797834"
---
# Excluir um GPO


O gerenciamento avançado de política de grupo (AGPM) permite que os aprovadores excluam um GPO (objeto de política de grupo) controlado, movendo-o para a lixeira.

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para excluir um GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO a ser excluído e, em seguida, clique em **excluir**.

    -   Para excluir o GPO do arquivo morto, deixando a versão implantada do GPO intocado no ambiente de produção, clique em **excluir GPO de somente arquivo morto (não controlar)**.

    -   Para excluir o GPO do ambiente de arquivamento e de produção, clique em **excluir GPO do arquivamento e da produção**.

4.  Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO é removido da guia **controlado** e é exibido na guia **Lixeira** , onde ele pode ser restaurado ou destruído. Se o GPO tiver sido excluído somente do arquivo morto, ele também será exibido na guia não **controlado** .

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para excluir um GPO implantado. Especificamente, você deve ter permissões **list Content** e **delete GPO** para o GPO.

-   Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para excluir um GPO do arquivo morto. Especificamente, você deve ter **conteúdo da lista** e **Editar as** permissões do **GPO ou excluir** as permissões do GPO.

-   Para excluir um GPO não controlado do ambiente de produção sem primeiro controlá-lo, no **console de gerenciamento de política de grupo**, clique em **floresta**, clique em **domínios**, clique em ** &lt; &gt; mydomain**e, em seguida, clique em objetos de política de **grupo**. Clique com o botão direito do mouse no GPO não controlado e clique em **excluir**.

### Referências adicionais

-   [Excluir, restaurar ou destruir um GPO](deleting-restoring-or-destroying-a-gpo.md)

 

 





