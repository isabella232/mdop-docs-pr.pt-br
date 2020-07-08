---
title: Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico
description: Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796322"
---
# Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico

*Observação:** App-V 4,6 saiu do suporte básico. O seguinte pressupõe que o cliente App-V 4,6 SP3 já está instalado.

Use o procedimento a seguir para reverter os pontos de extensão de um pacote App-V 5,0 para o formato de arquivo App-V 4,6 usando o arquivo de configuração de implantação.

**Para reverter um pacote**

1.  Certifique-se de que o pacote App-V 4,6 seja publicado para os usuários, mas que o FTAs e os atalhos tenham sido presumidos pelo pacote do App-v 5,0 usando o método de migração a seguir, [como migrar pontos de extensão de um pacote do App-v 4,6 para um pacote app-v 5,0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).

    Na seção **userconfiguration** do arquivo de configuração de implantação do pacote convertido, para definir a política, faça a seguinte atualização para a seção **Userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; do pacote**

2.  Em um prompt de comando elevado, digite:

    PS &gt; **set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; caminho para o arquivo de configuração de implantação&gt;

    &gt;**$Pkg de publicação do PS-AppVClientPackage-DynamicUserConfigurationType useDeploymentConfiguration**

3.  Realize uma atualização de publicação ou aguarde a próxima atualização de publicação agendada do pacote App-V 4,6 SP2.

    Abra o aplicativo usando FTAs ou atalhos. Agora o aplicativo deve abrir usando o App-V 4,6.

    **Observação**  
    Se você não precisar mais do pacote App-V 5,0, poderá cancelar a publicação do pacote App-V 5,0 e os pontos de extensão serão revertidos automaticamente para o App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)









