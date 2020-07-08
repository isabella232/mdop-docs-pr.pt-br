---
title: Controlar um GPO não controlado
description: Controlar um GPO não controlado
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797418"
---
# Controlar um GPO não controlado


Para fornecer controle de alterações para um objeto de política de grupo (GPO), você deve primeiro controlar o GPO.

Uma conta de usuário com a função Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para controlar um GPO não controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia não **controlado** para exibir os GPOs não controlados.

3.  Clique com o botão direito do mouse no GPO para ser controlado com o AGPM e, em seguida, clique em **controle**.

4.  Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO é removido da lista na guia não **controlado** e adicionado à guia **controlado** .

### Considerações adicionais

-   Por padrão, você deve ser um Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo de lista** e criar permissões de **GPO** para o domínio.

### Referências adicionais

-   [Criar ou controlar um GPO](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





