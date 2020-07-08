---
title: Usar um ambiente de teste
description: Usar um ambiente de teste
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797285"
---
# Usar um ambiente de teste


Se você usar uma UO (unidade organizacional de teste) para testar objetos de política de grupo (GPOs) antes da implantação para o ambiente de produção, você deve ter as permissões necessárias para acessar a OU de teste. O uso de uma OU de teste é opcional.

**Para usar uma OU de teste**

1.  Enquanto o GPO tiver sido verificado para edição, no console de **Gerenciamento de política de grupo**, clique em **objetos de política de grupo** na floresta e no domínio em que você está gerenciando GPOs.

2.  Clique na cópia checked-out do GPO a ser testado. O nome será precedido por **\ [check out \]**. (Se não estiver listado, clique em **ação**e em **Atualizar**. Classifique os nomes em ordem alfabética e **\ [check out \]** os GPOs normalmente aparecem na parte superior da lista.)

3.  Arraste e solte o GPO na OU Test OU.

4.  Clique em **OK** na caixa de diálogo para perguntar se deseja criar um link para o GPO na OU Test ou.

### Considerações adicionais

-   Quando o teste estiver concluído, fazer check-in do GPO excluirá automaticamente o link para a cópia checked-out do GPO.

### Referências adicionais

-   [Editando um GPO](editing-a-gpo-agpm30ops.md)

 

 





