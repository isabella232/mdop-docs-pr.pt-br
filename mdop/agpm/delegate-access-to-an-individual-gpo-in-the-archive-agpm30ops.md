---
title: Delegar acesso a um GPO individual no arquivo morto
description: Delegar acesso a um GPO individual no arquivo morto
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797391"
---
# Delegar acesso a um GPO individual no arquivo morto


Como administrador do AGPM (controle total), você pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado no arquivo para que os grupos e editores selecionados possam editá-lo, os revisores podem revisá-lo e os aprovadores podem aprová-lo.

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para delegar o gerenciamento de um GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado:

    1.  Para adicionar acesso para um usuário ou grupo, clique no botão **Adicionar** , selecione o usuário ou grupo e clique em **OK**. Na caixa de diálogo **Adicionar grupo ou usuário** , selecione uma função e clique em **OK**.

    2.  Para remover o acesso de um usuário ou grupo, selecione o usuário ou grupo e clique no botão **remover** .

        **Observação**  Se um usuário ou grupo herda o acesso de todo o domínio, o botão **remover** não está disponível. Você pode modificar o acesso em todo o domínio na guia de **delegação de domínio** .

         

    3.  Para modificar as funções e permissões delegadas a um usuário ou grupo, clique no botão **avançado** . Na caixa de diálogo **permissões** , selecione o usuário ou grupo, marque a caixa de seleção de cada função a ser atribuída a esse usuário ou grupo e clique em **OK**.

        **Observação**  O editor e o aprovador incluem permissões do revisor.

         

### Considerações adicionais

-   Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.

-   Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** . Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM. Outras permissões devem ser explicitamente delegadas.

-   Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.

-   A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

### Referências adicionais

-   [Gerenciamento do arquivo morto](managing-the-archive.md)

 

 





