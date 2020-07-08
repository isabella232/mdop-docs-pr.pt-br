---
title: Como modificar a configuração do cliente usando o PowerShell
description: Como modificar a configuração do cliente usando o PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796343"
---
# Como modificar a configuração do cliente usando o PowerShell


Use o procedimento a seguir para configurar a configuração do cliente do App-V 5,1.

**Para modificar a configuração do cliente do App-V 5,1 usando o PowerShell**

1.  Para definir as configurações do cliente usando o PowerShell, use o cmdlet **set-AppvClientConfiguration** . Para obter mais informações sobre como instalar o PowerShell e uma lista de cmdlets, consulte [como carregar os cmdlets do PowerShell e obter ajuda do cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).

2.  Para modificar a configuração do cliente, abra um prompt de comando do PowerShell e execute o cmdlet **set-AppvClientConfiguration** a seguir com todos os parâmetros obrigatórios. Por exemplo:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





