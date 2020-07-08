---
title: Importar um GPO de um arquivo
description: Importar um GPO de um arquivo
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797788"
---
# Importar um GPO de um arquivo


No gerenciamento avançado de política de grupo (AGPM), se você for um administrador do AGPM (controle total) e exportou um objeto de política de grupo (GPO) para um arquivo CAB, poderá importar as configurações de política desse GPO para um novo GPO ou um GPO existente em um domínio em outra floresta. Para obter informações sobre como exportar configurações de GPO para um arquivo CAB, consulte [exportar um GPO para um arquivo](export-a-gpo-to-a-file.md).

Uma conta de usuário com a função de administrador do AGPM ou as permissões necessárias no AGPM é necessária para importar as configurações de política para um novo GPO controlado. Uma conta de usuário com a função de administrador ou administrador do AGPM ou permissões necessárias no AGPM é necessária para importar configurações de política para um GPO existente. Examine os detalhes em "considerações adicionais" neste tópico.

## Importando configurações de política de um arquivo


Ao importar configurações de política de um arquivo, você pode importá-las para um novo GPO ou um GPO existente. No entanto, se você importar configurações de política para um GPO existente, todas as configurações de política dentro dela serão substituídas.

-   [Importar configurações de política para um novo GPO controlado](#bkmk-new)

-   [Importar configurações de política para um GPO existente](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**Para importar configurações de política para um novo GPO controlado**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** no domínio ao qual você deseja importar as configurações de política.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Crie um novo GPO controlado. Na caixa de diálogo **novo GPO controlado** , clique em **importar** e, em seguida, clique em **Iniciar assistente**. Para obter mais informações sobre como criar um GPO, consulte [criar um novo GPO controlado](create-a-new-controlled-gpo-agpm40.md).

4.  Siga as instruções no **Assistente de importação de configurações** para selecionar um backup de GPO, importar configurações de política dele para o novo GPO e inserir um comentário para a faixa de auditoria do novo GPO.

### <a href="" id="bkmk-existing"></a>

**Para importar configurações de política para um GPO existente**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** no domínio ao qual você deseja importar as configurações de política.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Verifique o GPO de destino para o qual você deseja importar as configurações de política.

4.  Clique com o botão direito do mouse no GPO de destino, aponte para **importar de**e clique em **arquivo**.

5.  Siga as instruções no **Assistente de importação de configurações** para selecionar um backup de GPO, importar suas configurações de política para substituir as do GPO de destino e inserir um comentário para a faixa de auditoria do GPO de destino. Por padrão, o GPO de destino é verificado quando o assistente é concluído.

### Considerações adicionais

-   Para importar configurações de política para um novo GPO controlado, você deve ter o **conteúdo da lista**, **importar GPO**e criar permissões de **GPO** para o domínio. Por padrão, você deve ser um administrador do AGPM para executar esse procedimento.

-   Para importar configurações de política para um GPO existente, você deve ter a **lista de conteúdo**, **Editar configurações**e importar permissões de **GPO** para o domínio, e o GPO deve ser verificado por você. Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.

### Referências adicionais

-   [Gerenciamento do arquivo morto](managing-the-archive-agpm40.md)

 

 





