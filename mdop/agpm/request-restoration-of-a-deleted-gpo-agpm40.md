---
title: Solicitar a restauração de um GPO excluído
description: Solicitar a restauração de um GPO excluído
author: dansimp
ms.assetid: bac5ca3b-be47-49b5-bf1b-96280625fda8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 606690554ca1f813e1c20787bca59cfe2de6432d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797712"
---
# Solicitar a restauração de um GPO excluído


A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar a restauração de um objeto de política de grupo (GPO) excluído da lixeira para devolvê-lo ao arquivo morto.

Uma conta de usuário com a função de editor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para solicitar a restauração de um GPO excluído**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.

3.  Clique com o botão direito do mouse no GPO que você deseja restaurar e clique em **restaurar**.

4.  A menos que você tenha permissão especial para restaurar GPOs, você deve enviar uma solicitação para restauração do GPO excluído. Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** . Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **Enviar**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .

**Observação**  Se um GPO foi excluído do ambiente de produção, restaurá-lo para o arquivo não o reimplantará automaticamente no ambiente de produção. Para retornar o GPO ao ambiente de produção, implante o GPO. Para obter informações, consulte [solicitar a implantação de um GPO](request-deployment-of-a-gpo-agpm40.md).

 

### Considerações adicionais

-   Por padrão, você deve ser um editor para executar esse procedimento. Especificamente, você deve ter a permissão **listar conteúdo** e **Editar configurações** para o GPO.

-   Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**. O GPO será retornado para a guia da **Lixeira** .

### Referências adicionais

-   [Excluir ou restaurar um GPO](deleting-or-restoring-a-gpo-agpm40.md)

 

 





