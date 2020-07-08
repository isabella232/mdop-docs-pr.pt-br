---
title: Delegar acesso a um GPO
description: Delegar acesso a um GPO
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797394"
---
# Delegar acesso a um GPO


Um Aprovador pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado **criado pelo aprovador**. Como um administrador do AGPM (controle total), o aprovador pode delegar o acesso a tal GPO, para que os editores selecionados possam editá-lo, os Revisores possam examiná-lo e outros Aprovadores possam aprová-lo. Por padrão, um aprovador não pode delegar o acesso a GPOs criados por outro administrador de política de grupo.

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para delegar o gerenciamento de um GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado.

3.  Clique no botão **Adicionar** , selecione os usuários ou grupos para os quais você tem permissão de acesso e, em seguida, clique em **OK**.

4.  Para personalizar as permissões para cada um, clique no botão **avançado** na guia **conteúdo** e marque as permissões de função para permitir ou recusar. (Para obter controle mais detalhado, clique em **avançado** na caixa de diálogo **permissões** .)

5.  Clique em **aplicar**e, em seguida, clique em **OK** na caixa de diálogo **permissões** .

### Considerações adicionais

-   Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.

### Referências adicionais

-   [Criação, controle ou importação de um GPO](creating-controlling-or-importing-a-gpo-approver.md)

 

 





