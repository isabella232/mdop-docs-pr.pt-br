---
title: Delegar acesso no nível do domínio ao arquivo morto
description: Delegar acesso no nível do domínio ao arquivo morto
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797382"
---
# Delegar acesso no nível do domínio ao arquivo morto


Configure a delegação do seu ambiente para que os administradores de política de grupo tenham o acesso e o controle apropriados em GPOs (objetos de política de grupo) no arquivo morto. Há permissões de linha de base que você pode aplicar para fazer a operação ser mais eficiente. Você pode conceder permissões de qualquer maneira que atenda às necessidades da sua organização.

Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para delegar o acesso para que os usuários e grupos tenham permissões apropriadas para todos os GPOs em todo o domínio**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Clique na guia **delegação de domínio** e configure o acesso a todos os GPOs no domínio:

    1.  Para adicionar acesso para um usuário ou grupo, clique no botão **Adicionar** , selecione o usuário ou grupo e clique em **OK**. Na caixa de diálogo **Adicionar grupo ou usuário** , selecione uma função e clique em **OK**.

    2.  Para remover o acesso de um usuário ou grupo, selecione o usuário ou grupo e clique no botão **remover** .

    3.  Para modificar as funções e permissões delegadas a um usuário ou grupo, selecione clique no botão **avançado** . Na caixa de diálogo **permissões** , selecione o usuário ou grupo, marque a caixa de seleção de cada função a ser atribuída a esse usuário ou grupo e, em seguida, clique em **OK**.

        **Observação**  O editor e o aprovador incluem permissões do revisor.

         

### Considerações adicionais

-   Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **modificação de segurança** para o domínio.

-   Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** . Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM. Outras permissões devem ser explicitamente delegadas.

-   Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.

-   A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

### Referências adicionais

-   [Gerenciamento do arquivo morto](managing-the-archive-agpm40.md)

 

 





