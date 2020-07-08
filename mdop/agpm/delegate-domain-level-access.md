---
title: Delegar acesso no nível do domínio
description: Delegar acesso no nível do domínio
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797837"
---
# Delegar acesso no nível do domínio


Configurar a delegação do seu ambiente para que os administradores de política de grupo tenham acesso e controle apropriados em GPOs (objetos de política de grupo). Há permissões de linha de base que você pode aplicar para fazer com que a operação do gerenciamento avançado de política de grupo (AGPM) seja mais eficiente. Você pode conceder permissões de qualquer maneira que atenda às necessidades da sua organização.

Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para delegar o acesso para que os usuários e grupos tenham permissões adequadas para todos os GPOs em todo o domínio**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Clique na guia **delegação de domínio** e, em seguida, clique no botão **avançado** .

3.  Na caixa de diálogo **permissões** , clique na caixa de seleção de cada função a ser atribuída a um indivíduo e, em seguida, clique no botão **avançado** .

    **Observação**  O editor e o aprovador incluem permissões do revisor.

     

4.  Na caixa de diálogo **configurações de segurança avançadas** , selecione um administrador de política de grupo e, em seguida, clique em **Editar**.

5.  Para **aplicar em**, selecione **este objeto e objetos aninhados**, configure todas as permissões especiais além das funções padrão do AGPM e, em seguida, clique em **OK** na caixa de diálogo **entrada** de **permissão** .

6.  Na caixa de diálogo **configurações de segurança avançadas** , clique em **OK**.

7.  Na caixa de diálogo **permissões** , clique em **OK**.

### Considerações adicionais

-   Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **modificação de segurança** para o domínio.

-   Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** . Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM. Defina a permissão para aplicar a **esse objeto e a objetos aninhados**. Outras permissões devem ser explicitamente delegadas.

-   Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.

-   A associação no grupo proprietários criadores de política de grupo deve ser restrita para que não seja usada para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

### Referências adicionais

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks.md)

 

 





