---
title: Importar um GPO de um arquivo
description: Importar um GPO de um arquivo
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797782"
---
# Importar um GPO de um arquivo


No gerenciamento avançado de política de grupo (AGPM), se você exportou um objeto de política de grupo (GPO) para um arquivo CAB, poderá importar as configurações de política desse GPO para um GPO existente em um domínio de outra floresta. Importar configurações de política para um GPO existente substitui todas as configurações de política dentro desse GPO. Para obter informações sobre como exportar configurações de GPO para um arquivo CAB, consulte [exportar um GPO para um arquivo](export-a-gpo-to-a-file.md).

Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.Examine os detalhes em "considerações adicionais" neste tópico.

## <a href="" id="bkmk-existing"></a>


**Para importar configurações de política para um GPO existente**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** no domínio ao qual você deseja importar as configurações de política.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Verifique o GPO de destino para o qual você deseja importar as configurações de política.

4.  Clique com o botão direito do mouse no GPO de destino, aponte para **importar de**e clique em **arquivo**.

5.  Siga as instruções no **Assistente de importação de configurações** para selecionar um backup de GPO, importar suas configurações de política para substituir as do GPO de destino e inserir um comentário para a faixa de auditoria do GPO de destino. Por padrão, o GPO de destino é verificado quando o assistente é concluído.

### Considerações adicionais

-   Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo da lista**, **Editar configurações**e **importar** permissões de GPO para o domínio, e o GPO deve ser submetido a check-out por você.

-   Embora um editor não possa importar configurações de política para um novo GPO durante sua criação, um editor pode solicitar a criação de um novo GPO e, em seguida, importar as configurações de política para ele após a criação.

### Referências adicionais

-   [Como usar um ambiente de teste](using-a-test-environment.md)

 

 





