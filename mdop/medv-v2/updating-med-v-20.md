---
title: Atualização da MED-V 2.0
description: Atualização da MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799331"
---
# Atualização da MED-V 2.0


Ajude a proteger seu sistema aplicando as atualizações de segurança apropriadas para o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Atualização do MED-V


Você pode atualizar o MED-V interativamente, pelo usuário final ou silenciosamente, usando um sistema de distribuição de software eletrônico. A instalação do agente de host MED-V atualiza o host do MED-V Host Agent e, em seguida, atualiza o espaço de trabalho do MED-v, se necessário. O agente de host do MED-V e o agente convidado mantêm-se sincronizados. Se os aplicativos estiverem sendo executados do espaço de trabalho do MED-V enquanto o agente de host do MED-V estiver sendo atualizado, será necessário reiniciar o computador host para concluir a atualização. Se nenhum aplicativo estiver sendo executado, o MED-V será reiniciado automaticamente e a atualização será concluída sem a reinicialização do computador host.

Se estiver atualizando o MED-V usando um sistema de distribuição de software eletrônico, você pode controlar o comportamento de reinicialização. Para fazer isso, omita a reinicialização digitando **reboot = "ReallySuppress"** no prompt de comando ao instalar MED-V\_HostAgent\_Setup.exe. Em seguida, configure o sistema de distribuição de software eletrônico para capturar o código de retorno do 3010 (que sinaliza que uma reinicialização é necessária) e executar o comportamento definir reinicialização.

## Tópicos relacionados


[Referência técnica da MED-V](technical-reference-for-med-v.md)

 

 





