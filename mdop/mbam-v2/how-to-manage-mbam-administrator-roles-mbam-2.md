---
title: Como gerenciar funções de administrador do MBAM
description: Como gerenciar funções de administrador do MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799608"
---
# Como gerenciar funções de administrador do MBAM


Após a conclusão da instalação do Microsoft BitLocker Administration and Monitoring (MBAM) para todos os recursos do servidor, os usuários administrativos terão que conceder acesso a eles. Como prática recomendada, os administradores que gerenciam ou usam os recursos de servidor de administração e monitoramento do Microsoft BitLocker devem ser atribuídos a grupos de segurança de serviços de domínio e esses grupos devem ser adicionados ao grupo local administrativo MBAM apropriado.

**Para gerenciar associações de funções de administrador do MBAM**

1.  Atribua usuários administrativos a grupos de segurança nos serviços de domínio do ActiveDirectory.

2.  Adicione grupos de segurança do ActiveDirectory às funções dos grupos locais administrativos do MBAM no servidor MBAM para os respectivos recursos.

    -   **Os administradores do sistema do MBAM** têm acesso a todos os recursos do MBAM no site de administração e monitoramento do MBAM.

    -   **Usuários da assistência técnica do MBAM** têm acesso às opções gerenciar TPM e recuperação de unidade no site de administração e monitoramento do MBAM, mas devem preencher todos os campos quando usarem qualquer uma dessas opções.

    -   **MBAM relatório os usuários** têm acesso aos relatórios de conformidade e auditoria no site de administração e monitoramento do MBAM.

    -   **Os usuários de helpdesk avançados do MBAM** têm acesso às opções gerenciar TPM e recuperação de unidade no site de administração e monitoramento do MBAM, mas não são necessários para preencher todos os campos quando eles usam qualquer uma dessas opções.

    Para obter mais informações sobre as funções de administração e monitoramento do Microsoft BitLocker, consulte [planejando funções de administrador do MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

## Tópicos relacionados


[Administrando os Recursos do MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





