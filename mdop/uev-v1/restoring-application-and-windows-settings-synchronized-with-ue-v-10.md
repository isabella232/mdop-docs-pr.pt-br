---
title: Restauração de configurações de aplicativos e do Windows com a UE-V 1.0
description: Restauração de configurações de aplicativos e do Windows com a UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795984"
---
# Restauração de configurações de aplicativos e do Windows com a UE-V 1.0


Os recursos do WMI e do PowerShell da Microsoft User Experience Virtualization (UE-V) oferecem a capacidade de restaurar pacotes de configurações. Os comandos do WMI e do PowerShell permitem restaurar as configurações do aplicativo e do Windows para os valores de configurações que estavam no computador na primeira vez que o aplicativo foi iniciado após a instalação do agente do UE-V. Essa ação de restauração é realizada em uma base de configurações por aplicativo ou Windows. As configurações serão restauradas na próxima vez que o aplicativo for executado ou quando o usuário fizer logon no sistema operacional.

**Para restaurar as configurações do aplicativo e as configurações do Windows com o PowerShell**

1.  Abra a janela do Windows PowerShell. Para importar o módulo Microsoft UE-V PowerShell, digite o seguinte comando:

    ``` syntax
    Import-module UEV
    ```

2.  Digite o seguinte cmdlet do PowerShell para restaurar as configurações do aplicativo e as configurações do Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet do PowerShell</strong></th>
    <th align="left"><strong>Descrição</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Restore-UevUserSetting</p></td>
    <td align="left"><p>Restaura as configurações do usuário para um aplicativo ou restaura um grupo de configurações do Windows</p></td>
    </tr>
    </tbody>
    </table>

     

**Para restaurar as configurações do aplicativo e as configurações do Windows com WMI**

1.  Abra uma janela do PowerShell.

2.  Digite o seguinte comando WMI para restaurar as configurações do aplicativo e as configurações do Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando WMI</strong></th>
    <th align="left"><strong>Descrição</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Setting UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</p></td>
    <td align="left"><p>Restaura as configurações do usuário para um aplicativo ou restaura um grupo de configurações do Windows</p></td>
    </tr>
    </tbody>
    </table>

     

## Tópicos relacionados


[Administração da UE-V 1.0](administering-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





