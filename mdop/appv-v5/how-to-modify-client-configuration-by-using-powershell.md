---
title: Como modificar a configuração do cliente usando o PowerShell
description: Como modificar a configuração do cliente usando o PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796347"
---
# Como modificar a configuração do cliente usando o PowerShell


Use o procedimento a seguir para configurar a configuração do cliente do App-V 5,0.

**Para modificar a configuração do cliente do App-V 5,0 usando o PowerShell**

1.  Para definir as configurações do cliente usando o PowerShell, use o cmdlet **set-AppvClientConfiguration** .

2.  Para modificar a configuração do cliente, abra um prompt de comando do PowerShell e execute o cmdlet **set-AppvClientConfiguration** a seguir com todos os parâmetros obrigatórios. Por exemplo:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





