---
title: Fazer check-in de um GPO
description: Fazer check-in de um GPO
author: dansimp
ms.assetid: b838c8a2-eb9e-4e5b-8740-d7701a4294ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 27924e57e7430cdf992a7730e5cd141ed4fb52ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797474"
---
# Fazer check-in de um GPO


Normalmente, os editores devem verificar objetos de política de grupo (GPOs) que foram editados quando suas modificações são concluídas. (Para obter detalhes, consulte [Editar um GPO offline](edit-a-gpo-offline-agpm40.md).) No entanto, se o editor estiver indisponível, um Aprovador também pode fazer check-in de um GPO.

Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para fazer check-in de um GPO que foi verificado por um editor**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

    -   Para descartar alterações feitas pelo editor, clique com o botão direito do mouse no GPO, clique em **desfazer check-out**e, em seguida, clique em **Sim** para confirmar.

    -   Para reter as alterações feitas pelo editor, clique com o botão direito do mouse no GPO e, em seguida, clique em **check-in**.

3.  Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.

4.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. Na guia **controlado** , o estado do GPO é identificado como **checked-in**.

### Considerações adicionais

-   Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter o **conteúdo da lista** e **Editar as** permissões do **GPO** para o GPO. Se você não for um Aprovador ou administrador do AGPM (ou outro administrador da política de grupo com a permissão **implantar GPO** ), você deve ser o editor que fez check-out do GPO.

### Referências adicionais

-   [Execução de tarefas do aprovador](performing-approver-tasks-agpm40.md)

-   [Editar um GPO offline](edit-a-gpo-offline-agpm40.md)

 

 





