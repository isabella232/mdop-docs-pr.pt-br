---
title: Exportar um GPO para um arquivo
description: Exportar um GPO para um arquivo
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797808"
---
# Exportar um GPO para um arquivo


Você pode exportar um GPO (objeto de política de grupo) controlado para um arquivo CAB para poder copiá-lo para um domínio em outra floresta e importar o GPO para o gerenciamento avançado de política de grupo (AGPM) nesse domínio. Para obter informações sobre como importar configurações de GPO para um GPO novo ou existente, consulte [importar um GPO de um arquivo](import-a-gpo-from-a-file-ed.md).

Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.Examine os detalhes em "considerações adicionais" neste tópico.

**Para exportar um GPO para um arquivo**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

3.  Clique com o botão direito do mouse no GPO e, em seguida, clique em **exportar para**.

4.  Insira um nome de arquivo para o arquivo para o qual você deseja exportar o GPO e, em seguida, clique em **Exportar**. Se o arquivo não existir, ele será criado. Se ele já existir, será substituído.

### Considerações adicionais

-   Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo da lista**, **ler configurações**e **Exportar** permissões de GPO para o GPO.

### Referências adicionais

-   [Como usar um ambiente de teste](using-a-test-environment.md)

 

 





