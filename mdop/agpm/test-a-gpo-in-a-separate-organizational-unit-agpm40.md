---
title: Testar um GPO em uma unidade organizacional separada
description: Testar um GPO em uma unidade organizacional separada
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797289"
---
# Testar um GPO em uma unidade organizacional separada


Se você usar uma unidade organizacional de teste (OU) para testar objetos de política de grupo (GPOs) no mesmo domínio antes da implantação para o ambiente de produção, você deve ter as permissões necessárias para acessar a OU de teste. Usar uma OU de teste é opcional.

**Para usar uma OU de teste**

1.  Embora você tenha feito o check-out do GPO para edição, no **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio em que você está gerenciando GPOs.

2.  Clique na cópia checked-out do GPO a ser testado. O nome será precedido por **\ [AGPM \]**. (Se não estiver listado, clique em **ação**e em **Atualizar**. Classifique os nomes em ordem alfabética, e **\ [AGPM \]** os GPOs geralmente aparecem na parte superior da lista.)

3.  Arraste o GPO para a OU Test.

4.  Clique em **OK** na caixa de diálogo que pergunta se deve criar um link para o GPO na OU Test ou.

### Considerações adicionais

-   Quando o teste estiver concluído, fazer check-in do GPO excluirá automaticamente o link para a cópia checked-out do GPO.

### Referências adicionais

-   [Como usar um ambiente de teste](using-a-test-environment.md)

 

 





