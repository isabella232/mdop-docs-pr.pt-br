---
title: Aprovar ou rejeitar uma ação pendente
description: Aprovar ou rejeitar uma ação pendente
author: dansimp
ms.assetid: 22921a51-50fb-4a47-bec1-4f563f523675
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 508df2766b7d480f8ba4d6e13c97ed880ef6939e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797481"
---
# Aprovar ou rejeitar uma ação pendente


A principal responsabilidade de um Aprovador é avaliar e aprovar ou rejeitar solicitações de criação, implantação e exclusão de objetos de política de grupo (GPO) de editores ou revisores que não têm permissão para completar essas ações. Os recursos de relatório do recurso gerenciamento avançado de política de grupo (AGPM) podem ajudar um Aprovador a avaliar uma nova versão de um GPO.

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para aprovar ou rejeitar uma solicitação pendente**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.

3.  Clique com o botão direito do mouse em um GPO pendente e, em seguida, clique em **aprovar** ou **rejeitar**.

4.  Se estiver aprovando a implantação, clique em **avançado** na caixa de diálogo **aprovar operação pendente** para revisar os links para o GPO. Pause o ponteiro do mouse sobre um nó na árvore para exibir detalhes.

    -   Por padrão, todos os links para o GPO serão restaurados.

    -   Para impedir que um link seja restaurado, desmarque a caixa de seleção desse link.

    -   Para impedir que todos os links sejam restaurados, desmarque a caixa de seleção **restaurar vínculos** na caixa de diálogo **implantar GPO** .

5.  Clique em **Sim** ou **OK** para confirmar a aprovação ou rejeição da ação pendente. Se você tiver aprovado a solicitação, o GPO será movido para a guia apropriada para a ação executada.

    **Observação**  Se o endereço de email de um Aprovador estiver incluído no campo **para** na guia de **delegação** de **domínio** , o aprovador receberá o email do alias do AGPM quando um editor ou revisor enviar uma solicitação.

     

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter as permissões necessárias para executar a solicitação que está aprovando.

### Referências adicionais

-   [Execução de tarefas do aprovador](performing-approver-tasks.md)

 

 





