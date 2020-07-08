---
title: Solicitar a criação de um novo GPO controlado
description: Solicitar a criação de um novo GPO controlado
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797701"
---
# Solicitar a criação de um novo GPO controlado


A menos que você seja um Aprovador ou administrador do AGPM (controle total), você deve solicitar a criação de um novo objeto de política de grupo (GPO).

Uma conta de usuário com a função de editor ou de revisor ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para criar um novo GPO com controle de alterações gerenciado por meio do AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Clique com o botão direito do mouse em **controle de alterações**e clique em **novo GPO controlado**.

3.  A menos que você tenha permissão especial para criar GPOs, você deve enviar uma solicitação de criação. Na caixa de diálogo **novo GPO controlado** :

    1.  Para receber uma cópia da solicitação, insira seu endereço de email no campo **CC** .

    2.  Digite um nome para o novo GPO.

    3.  Opcional: digite um comentário para o novo GPO.

    4.  Para implantar o novo GPO no ambiente de produção do domínio imediatamente após a aprovação, clique em **criar ao vivo**. Para criar o novo GPO offline sem implantá-lo imediatamente após a aprovação, clique em **criar offline**.

    5.  Selecione o modelo de GPO a ser usado como ponto de partida para o novo GPO.

    6.  Clique em **Enviar**.

4.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O novo GPO será exibido na lista de GPOs na guia **pendente** . Quando um Aprovador tiver aprovado sua solicitação, o GPO será movido para a guia **controlado** .

### Considerações adicionais

-   Por padrão, você deve ser um editor ou um revisor para executar esse procedimento. Especificamente, você deve ter permissão de **listar conteúdo** para o domínio.

-   Para refazer sua solicitação antes que ela seja aprovada, clique na guia **pendente** . Clique com o botão direito do mouse no GPO e clique em **retirar**. O GPO será destruído.

### Referências adicionais

-   [Criar ou controlar um GPO](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





