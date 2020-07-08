---
title: Restaurar um GPO excluído
description: Restaurar um GPO excluído
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797320"
---
# Restaurar um GPO excluído


O gerenciamento avançado de política de grupo (AGPM) permite que os aprovadores restaurem um objeto de política de grupo (GPO) excluído da lixeira, retornando-o ao arquivo morto.

Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para restaurar um GPO excluído**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.

3.  Clique com o botão direito do mouse no GPO para restaurar e clique em **restaurar**.

4.  Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .

**Observação**  Se um GPO foi excluído do ambiente de produção, restaurá-lo para o arquivo não o reimplantará automaticamente no ambiente de produção. Para retornar o GPO ao ambiente de produção, implante o GPO. Para obter informações, consulte [implantar um GPO](deploy-a-gpo.md).

 

### Considerações adicionais

-   Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo da lista** e **Editar as configurações**, **implantar o GPO**ou excluir permissões de **GPO** para o GPO.

### Referências adicionais

-   [Excluir, restaurar ou destruir um GPO](deleting-restoring-or-destroying-a-gpo.md)

 

 





