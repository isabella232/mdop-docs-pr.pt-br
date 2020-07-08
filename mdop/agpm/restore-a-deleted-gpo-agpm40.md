---
title: Restaurar um GPO excluído
description: Restaurar um GPO excluído
author: dansimp
ms.assetid: 0a131d26-a741-4a51-b612-c0bc7dbba06b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14fdf2f74f2d3db4be0db1aab7c185f5c1ab2cd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797322"
---
# Restaurar um GPO excluído


Os aprovadores podem restaurar um objeto de política de grupo (GPO) excluído da lixeira, retornando-o ao arquivo morto.

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para restaurar um GPO excluído**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.

3.  Clique com o botão direito do mouse no GPO para restaurar e clique em **restaurar**.

4.  Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .

**Observação**  Se um GPO foi excluído do ambiente de produção, restaurá-lo para o arquivo não o reimplantará automaticamente no ambiente de produção. Para retornar o GPO ao ambiente de produção, implante o GPO. Para obter informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).

 

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo da lista** e **implantar** permissões de GPO ou **excluir** GPO para o GPO.

### Referências adicionais

-   [Excluir, restaurar ou destruir um GPO](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





