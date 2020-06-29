---
title: Delegar acesso a um GPO individual
description: Delegar acesso a um GPO individual
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797384"
---
# Delegar acesso a um GPO individual


Como administrador do AGPM (controle total), você pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado, para que os grupos selecionados e editores possam editá-lo, os revisores podem revisá-lo e os aprovadores podem aprová-lo.

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para delegar o gerenciamento de um GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado.

3.  Clique no botão **Adicionar** , selecione os usuários ou grupos para os quais você tem permissão de acesso e, em seguida, clique em **OK**.

4.  Para personalizar as permissões para cada usuário ou grupo, clique no botão **avançado** na guia **conteúdo** e marque permissões de função para permitir ou recusar. (Para obter controle mais detalhado, clique em **avançado** na caixa de diálogo **permissões** .)

5.  Clique em **aplicar**e, em seguida, clique em **OK** na caixa de diálogo **permissões** .

### Considerações adicionais

-   Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.

-   Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** . Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM. Defina a permissão para aplicar a **esse objeto e a objetos aninhados**. Outras permissões devem ser explicitamente delegadas.

-   Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.

-   A associação no grupo proprietários criadores de política de grupo deve ser restrita para que não seja usada para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

### Referências adicionais

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks.md)

 

 





