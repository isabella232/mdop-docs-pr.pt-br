---
title: Delegar o gerenciamento de um GPO controlado
description: Delegar o gerenciamento de um GPO controlado
author: dansimp
ms.assetid: 96b4bfb3-5657-4267-8326-85d7a0db87ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0833e6b002d15c64e3b60fa0570640f8ea7fb2ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797838"
---
# Delegar o gerenciamento de um GPO controlado


Um Aprovador pode delegar o gerenciamento de um objeto de política de grupo (GPO) controlado criado pelo aprovador. Como um administrador do AGPM (controle total), o aprovador pode delegar o acesso a tal GPO para que os editores selecionados possam editá-lo, os revisores podem revisá-lo e outros Aprovadores possam aprová-lo. Por padrão, um aprovador não pode delegar o acesso a GPOs criados por outro administrador de política de grupo.

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO ou uma conta de usuário com as permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para delegar o gerenciamento de um GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados e, em seguida, clique no GPO a ser delegado:

    1.  Para adicionar acesso para um usuário ou grupo, clique no botão **Adicionar** , selecione o usuário ou grupo e clique em **OK**. Na caixa de diálogo **Adicionar grupo ou usuário** , selecione uma função e clique em **OK**.

    2.  Para remover o acesso de um usuário ou grupo, selecione o usuário ou grupo e clique no botão **remover** .

        **Observação**  Se um usuário ou grupo herda o acesso de todo o domínio, o botão **remover** não está disponível. Você pode modificar o acesso em todo o domínio na guia de **delegação de domínio** .

         

    3.  Para modificar as funções e permissões delegadas a um usuário ou grupo, clique no botão **avançado** . Na caixa de diálogo **permissões** , selecione o usuário ou grupo, marque a caixa de seleção de cada função a ser atribuída a esse usuário ou grupo e, em seguida, clique em **OK**.

        **Observação**  O editor e o aprovador incluem permissões do revisor.

         

### Considerações adicionais

-   Por padrão, você deve ser o aprovador que criou ou controlado o GPO ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **listar conteúdo** para o domínio e modificar a permissão de **segurança** para o GPO.

-   Para delegar o acesso de leitura a administradores de política de grupo que usam o AGPM, você deve conceder a eles o **conteúdo da lista** e ler permissões de **configurações** . Isso permite que eles exibam os GPOs na guia **conteúdo** do AGPM. Outras permissões devem ser explicitamente delegadas.

-   Os editores devem ter permissão de **leitura** para a cópia implantada de um GPO para fazer uso total da instalação do software de política de grupo.

### Referências adicionais

-   [Criar ou controlar um GPO](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





