---
title: Como gerenciar funções de administrador do MBAM
description: Como gerenciar funções de administrador do MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796132"
---
# Como gerenciar funções de administrador do MBAM


Após a conclusão da instalação do Microsoft BitLocker Administration and Monitoring (MBAM) para todos os recursos do servidor, os usuários administrativos devem ter acesso a esses recursos de servidor. Como prática recomendada, os administradores que gerenciam ou usam recursos do MBAM Server devem ser atribuídos aos grupos de segurança do Active Directory e esses grupos devem ser adicionados ao grupo local administrativo apropriado do MBAM.

**Para gerenciar associações de funções de administrador do MBAM**

1.  Atribua usuários administrativos a grupos de segurança nos serviços do ActiveDirectoryDomain.

2.  Adicione grupos de segurança de serviços do ActiveDirectoryDomain às funções para MBAM grupos locais administrativos no servidor de administração e monitoramento do Microsoft BitLocker para os respectivos recursos. As funções de usuário são as seguintes:

    -   **Os administradores de sistema do MBAM** têm acesso a todos os recursos de administração e monitoramento do Microsoft BitLocker no site de administração do MBAM.

    -   **Os usuários de hardware do MBAM** têm acesso aos recursos de compatibilidade de hardware no site de administração do MBAM.

    -   **Os usuários da assistência técnica do MBAM** têm acesso às opções gerenciar TPM e recuperação de unidade no site de administração do MBAM, mas devem preencher todos os campos quando usarem qualquer uma dessas opções.

    -   **Os usuários de relatório MBAM** têm acesso aos relatórios de conformidade e auditoria no site de administração do MBAM.

    -   O **MBAM Advanced helpdesk usa** tem acesso às opções gerenciar TPM e recuperação de unidade no site de administração do MBAM. Esses usuários não precisam preencher todos os campos quando usam qualquer uma dessas opções.

    Para obter mais informações sobre as funções de administração e monitoramento do Microsoft BitLocker, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

## Tópicos relacionados


[Administrando os Recursos do MBAM 1.0](administering-mbam-10-features.md)

 

 





