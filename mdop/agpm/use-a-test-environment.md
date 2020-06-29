---
title: Usar um ambiente de teste
description: Usar um ambiente de teste
author: dansimp
ms.assetid: b8d7b3ee-030a-4b5b-8223-4a3276fd47a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2299fb6eaf7c75f6841056f67a05fe025ea19bb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797284"
---
# Usar um ambiente de teste


Se você usar uma UO (unidade organizacional de teste) para testar objetos de política de grupo (GPOs) antes da implantação para o ambiente de produção, você deve ter as permissões necessárias para acessar a OU de teste. O uso de uma OU de teste é opcional.

**Para usar uma OU de teste**

1.  Enquanto o GPO tiver sido verificado para edição, no console de **Gerenciamento de política de grupo**, clique em **objetos de política de grupo** na floresta e no domínio em que você está gerenciando GPOs.

2.  Clique na cópia checked-out do GPO a ser testado. O nome será precedido de **\ [AGPM \]**. (Se não estiver listado, clique em **ação**e em **Atualizar**. Classifique os nomes em ordem alfabética, e **\ [AGPM \]** os GPOs geralmente aparecem na parte superior da lista.)

3.  Arraste e solte o GPO na OU Test OU.

4.  Clique em **OK** na caixa de diálogo para perguntar se deseja criar um link para o GPO na OU Test ou.

### Considerações adicionais

-   Quando o teste estiver concluído, fazer check-in do GPO excluirá automaticamente o link para a cópia checked-out do GPO.

### Referências adicionais

-   [Editando um GPO](editing-a-gpo.md)

 

 





