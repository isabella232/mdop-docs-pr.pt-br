---
title: Solicitar a implantação de um GPO
description: Solicitar a implantação de um GPO
author: dansimp
ms.assetid: 5783cfd0-bd93-46b4-8fa0-684bd39aa8fc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e9cc0fc12962dbdd7758c429a20fdd7c55b3cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797714"
---
# Solicitar a implantação de um GPO


Depois de modificar e verificar um GPO (objeto de política de grupo), implante o GPO para que ele entre em vigor no ambiente de produção.

Uma conta de usuário com a função de editor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para solicitar a implantação de um GPO para o ambiente de produção do domínio**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO a ser implantado e, em seguida, clique em **implantar**.

4.  A menos que você seja um Aprovador ou administrador do AGPM ou tenha permissão especial para implantar GPOs, você deve enviar uma solicitação de implantação. Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** . Digite um comentário a ser exibido no **histórico** do GPO e, em seguida, clique em **Enviar**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido da guia **pendente** para a guia **controlado** e será implantado.

### Considerações adicionais

-   Por padrão, você deve ser um editor para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e de **edição de configurações** para o GPO.

-   Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**. O GPO será retornado para a guia **controlado** .

### Referências adicionais

-   [Como executar tarefas de editor](performing-editor-tasks-agpm40.md)

 

 





