---
title: Rotular a versão atual de um GPO
description: Rotular a versão atual de um GPO
author: dansimp
ms.assetid: 3845211a-0bc9-4875-9906-cb758c443825
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f9e656258591a56397c5a8053b2e98772f57949a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797771"
---
# Rotular a versão atual de um GPO


Você pode rotular a versão atual de um objeto de política de grupo (GPO) para facilitar a identificação em seu histórico. Você pode usar um rótulo para identificar uma versão válida conhecida para a qual você pode reverter se ocorrer um problema. Além disso, ao rotular vários GPOs com o mesmo rótulo ao mesmo tempo, você pode marcar os GPOs relacionados que devem ser revertidos para o mesmo ponto se a reversão posteriormente for necessária.

Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para rotular a versão atual dos GPOs em seus históricos**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique em um GPO para o qual você deseja rotular a versão atual. Para selecionar vários GPOs, pressione SHIFT e clique no último GPO em um grupo contíguo de GPOs ou pressione CTRL e clique em GPOs individuais. Clique com o botão direito do mouse em um GPO selecionado e, em seguida, clique em **rótulo**.

4.  Digite um rótulo e um comentário a ser exibido no histórico de cada GPO selecionado e, em seguida, clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.

### Considerações adicionais

-   Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter o **conteúdo da lista** e **Editar as** permissões do **GPO** para o GPO.

### Referências adicionais

-   [Editando um GPO](editing-a-gpo-agpm30ops.md)

 

 





