---
title: Solicitar o controle de um GPO não controlado
description: Solicitar o controle de um GPO não controlado
author: dansimp
ms.assetid: b668a67a-5a2c-4f6a-8b1c-efa3ca0794d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8cf1ede496a54d6d3d211c2e3cfc23c506217ca7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797328"
---
# Solicitar o controle de um GPO não controlado


Para fornecer controle de alterações para um objeto de política de grupo (GPO) existente, o GPO deve ser controlado. A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar que o GPO seja controlado.

Uma conta de usuário com a função de editor ou de revisor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para controlar um GPO não controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia não **controlado** para exibir os GPOs não controlados.

3.  Clique com o botão direito do mouse no GPO para ser controlado com o AGPM e, em seguida, clique em **controle**.

4.  A menos que você tenha permissão especial para controlar os GPOs, você deve enviar uma solicitação de controle. Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** . Digite um comentário a ser exibido no **histórico** do GPO e, em seguida, clique em **Enviar**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO é removido da lista na guia não **controlado** e adicionado à guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido para a guia **controlado** .

### Considerações adicionais

-   Por padrão, você deve ser um editor ou um revisor para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o domínio.

-   Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**. O GPO será retornado para a guia não **controlado** .

### Referências adicionais

-   [Criação, controle ou importação de um GPO](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





