---
title: Destruir um GPO
description: Destruir um GPO
author: dansimp
ms.assetid: 09bce8c4-f75b-4633-b80b-d894bbec95c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d93b95fceda99a5840705c33e8919d6d7414fe8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797368"
---
# Destruir um GPO


Os aprovadores podem destruir um objeto de política de grupo (GPO), removê-lo da lixeira e excluí-lo permanentemente para que ele não possa mais ser restaurado.

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para excluir permanentemente um GPO para que ele não possa mais ser restaurado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.

3.  Clique com o botão direito do mouse no GPO a ser destruído e, em seguida, clique em **destruir**.

4.  Clique em **Sim** para confirmar que você deseja excluir permanentemente o GPO selecionado e todos os backups do arquivo morto.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO é removido da guia **Lixeira** e é excluído permanentemente.

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissões **list Content** e **delete GPO** para o GPO.

### Referências adicionais

-   [Excluir, restaurar ou destruir um GPO](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





