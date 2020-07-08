---
title: Criar um novo GPO controlado
description: Criar um novo GPO controlado
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797856"
---
# Criar um novo GPO controlado


Novos objetos de política de grupo (GPOs) criados por meio do nó de **controle de alteração** serão automaticamente controlados, permitindo que você o gerencie com o gerenciamento avançado de política de grupo (AGPM).

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para criar um novo GPO com controle de alterações gerenciado por meio do AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.

3.  Na caixa de diálogo **novo GPO controlado** :

    1.  Digite um nome para o novo GPO.

    2.  Opcional: digite um comentário para o novo GPO a ser exibido no **histórico** do GPO.

    3.  Para implantar imediatamente o novo GPO no ambiente de produção, clique em **criar ao vivo**. Para criar o novo GPO offline sem implantá-lo imediatamente, clique em **criar offline**.

    4.  Selecione o modelo de GPO a ser usado como ponto de partida para o novo GPO.

    5.  Clique em **OK**.

4.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O novo GPO é exibido na lista de GPOs na guia **controlado** .

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo de lista** e criar permissões de **GPO** para o domínio.

### Referências adicionais

-   [Criação, controle ou importação de um GPO](creating-controlling-or-importing-a-gpo-approver.md)

 

 





