---
title: Como gerenciar isenções de criptografia BitLocker para computadores
description: Como gerenciar isenções de criptografia BitLocker para computadores
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799720"
---
# Como gerenciar isenções de criptografia BitLocker para computadores


A administração e o monitoramento do Microsoft BitLocker (MBAM) podem ser usados para isentar determinados computadores da proteção BitLocker. Por exemplo, uma organização pode decidir controlar a isenção de BitLocker individualmente em computador.

Para isenta um computador da criptografia do BitLocker, você deve adicionar o computador a um grupo de segurança no ActiveDirectoryDomainServices para ignorar qualquer regra de proteção do BitLocker baseada em computador.

**Observação**  Se o computador já estiver protegido pelo BitLocker, a política de isenção de computador não terá efeito.

 

**Para isenta um computador da criptografia do BitLocker**

1.  Adicione a conta de computador que você deseja que seja isenta a um grupo de segurança no ActiveDirectoryDomainServices. Isso permite ignorar qualquer regra de proteção do BitLocker baseada em computador.

2.  Crie um objeto de política de grupo usando o modelo de política de grupo do MBAM e associe o objeto de política de grupo ao grupo do Active Directory que você criou na etapa anterior. Para obter mais informações sobre como criar os objetos de política de grupo necessários, consulte [implantando objetos de política de grupo do MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

3.  Quando um computador isento é iniciado, o cliente do MBAM verifica a configuração da política de isenção do computador e suspende a proteção com base no fato de o computador fazer parte do grupo de segurança de isenção de BitLocker.

## Tópicos relacionados


[Administrando os Recursos do MBAM 1.0](administering-mbam-10-features.md)

 

 





