---
title: Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico
description: Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796323"
---
# Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico


Use o procedimento a seguir para reverter um pacote App-V 5,1 para o formato de arquivo App-V usando o arquivo de configuração do usuário.

**Para reverter um pacote**

1.  Certifique-se de que o pacote App-V 4,6 seja publicado para os usuários, mas que o FTAs e os atalhos tenham sido presumidos pelo pacote do App-v 5,1 usando o método de migração a seguir, [como migrar pontos de extensão de um pacote app-v 4,6 para o app-v 5,1 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

    Na seção **userconfiguration** do arquivo de configuração de implantação do pacote convertido, para definir a política, faça a seguinte atualização para a seção **Userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; do pacote**

2.  Em um prompt de comando elevado, digite:

    &gt;**$Pkg de publicação PS-AppVClientPackage-DynamicUserConfigurationPath** &lt; caminho para o arquivo de configuração do usuário&gt;

3.  Realize uma atualização de publicação ou aguarde a próxima atualização de publicação agendada para o App-V 4,6. Abra o aplicativo usando FTAs ou atalhos. Agora o aplicativo deve abrir usando o App-V 4,6.

    **Observação**  
    Se você não precisar mais do pacote App-V 5,1, poderá cancelar a publicação do pacote App-V 5,1 e os pontos de extensão serão revertidos automaticamente para o App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)









