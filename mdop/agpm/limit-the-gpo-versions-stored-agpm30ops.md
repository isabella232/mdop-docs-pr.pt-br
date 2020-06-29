---
title: Limitar as versões de GPO armazenadas
description: Limitar as versões de GPO armazenadas
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797762"
---
# Limitar as versões de GPO armazenadas


Por padrão, todas as versões de cada objeto de política de grupo controlado (GPO) são mantidas no arquivo morto no servidor do AGPM. No entanto, você pode limitar o número de versões retidas para cada GPO e excluir versões mais antigas quando esse limite for excedido. Quando as versões do GPO são excluídas, um registro da versão permanece no histórico do GPO, mas a própria versão do GPO é excluída do arquivamento.

Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para limitar o número de versões de GPO armazenadas**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  No painel detalhes, clique na guia **servidor do AGPM** .

3.  Marque a caixa de seleção **Excluir versões antigas de cada GPO da lista de arquivos** e digite o número máximo de versões de GPO a serem armazenadas para cada GPO, não incluindo a versão atual. Para reter apenas a versão atual, digite 0. O máximo não deve ser maior do que 999.

    **Importante**  Somente as versões de GPO exibidas na guia **versões exclusivas** da janela do **histórico** contam para o limite.

     

4.  Clique no botão **aplicar** .

### Considerações adicionais

-   Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e **Opções de modificação** para o domínio.

-   Você pode impedir que uma versão do GPO seja excluída marcando-a no histórico como não qualificado para exclusão. Para fazer isso, clique com o botão direito do mouse na versão no histórico do GPO e clique em não **excluir**.

### Referências adicionais

-   [Gerenciamento do arquivo morto](managing-the-archive.md)

 

 





