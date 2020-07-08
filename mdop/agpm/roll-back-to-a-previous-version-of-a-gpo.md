---
title: Reverter a uma versão anterior de um GPO
description: Reverter a uma versão anterior de um GPO
author: dansimp
ms.assetid: 028631c0-4cb9-4642-90ad-04cd813051b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a71740eaa60a4b1292e47ca8aa57d4657231ab57
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797694"
---
# Reverter a uma versão anterior de um GPO


O gerenciamento avançado de política de grupo (AGPM) permite que um Aprovador reverta alterações para um objeto de política de grupo (GPO) implantando novamente uma versão anterior do GPO em seu histórico. Implantar uma versão anterior de um GPO substitui a versão do GPO atualmente em produção.

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Implantar uma versão anterior de um GPO no ambiente de produção**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique duas vezes no GPO a ser implantado para exibir seu **histórico**.

4.  Clique com o botão direito do mouse na versão a ser implantada, clique em **implantar**e, em seguida, clique em **Sim**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. Na janela do **histórico** , clique em **fechar**.

**Observação**  Para verificar se a versão que foi reimplementada corresponde à versão pretendida, examine um relatório de diferença para as duas versões. Na janela do **histórico** do GPO, realce as duas versões e clique com o botão direito do mouse e selecione **diferença** e relatório **HTML** ou **relatório XML**.

 

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter a **lista de conteúdo** e as permissões de GPO de **implantação** para o GPO.

### Referências adicionais

-   [Execução de tarefas do aprovador](performing-approver-tasks.md)

 

 





