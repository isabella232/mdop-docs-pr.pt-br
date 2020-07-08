---
title: Implantar um GPO
description: Implantar um GPO
author: dansimp
ms.assetid: a0a3f292-e3ab-46ae-a0fd-d7b2b4ad8883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a98bdd758937d86cf8c30c5abf0b49302d377360
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797377"
---
# Implantar um GPO


O gerenciamento avançado de política de grupo (AGPM) permite que um Aprovador implante um objeto de política de grupo (GPO) novo ou editado para o ambiente de produção. Para obter informações sobre como reimplantar uma versão anterior de um GPO, consulte [reverter para uma versão anterior de um GPO](roll-back-to-a-previous-version-of-a-gpo.md).

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para implantar um GPO no ambiente de produção**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO a ser implantado e clique em **implantar**.

4.  Para revisar os links para o GPO, clique em **avançado**. Pause o ponteiro do mouse sobre um nó na árvore para exibir detalhes.

    -   Por padrão, todos os links para o GPO serão restaurados.

    -   Para impedir que um link seja restaurado, desmarque a caixa de seleção desse link.

    -   Para impedir que todos os links sejam restaurados, desmarque a caixa de seleção **restaurar vínculos** na caixa de diálogo **implantar GPO** .

5.  Clique em **Sim**. Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.

**Observação**  Para verificar se a versão mais recente de um GPO foi implantada, na guia **controlado** , clique duas vezes no GPO para exibir seu **histórico**. No **histórico** do GPO, a coluna **estado** indica se um GPO foi implantado.

 

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter a **lista de conteúdo** e as permissões de GPO de **implantação** para o GPO.

### Referências adicionais

-   [Execução de tarefas do aprovador](performing-approver-tasks.md)

 

 





