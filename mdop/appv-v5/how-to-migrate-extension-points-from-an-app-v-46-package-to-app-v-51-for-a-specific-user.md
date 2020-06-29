---
title: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico
description: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796357"
---
# Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico


Use o procedimento a seguir para migrar os pacotes criados com o App-V usando o arquivo de configuração do usuário.

**Observação**  Este procedimento pressupõe que você esteja executando a versão mais recente do App-V 4,6.

**Para converter um pacote**

1. Localize o arquivo de configuração do usuário para o pacote que você deseja converter. Para definir a política, execute as seguintes atualizações na seção **userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGEname = &lt; ID &gt; do pacote**.

   Veja a seguir um exemplo de um arquivo de configuração do usuário:

   &lt;? XML Version = "1.0"?&gt;

   &lt;Userconfiguration PackageID = &lt; ID &gt; do pacote DisplayName = &lt; nome do pacote&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID do pacote&gt;

   &lt;/UserConfiguration&gt;

2. Para adicionar o pacote App-V 5,1, digite o seguinte em uma janela do prompt de comando do PowerShell com privilégios elevados:

   PS &gt; **$pkg = Add-AppvClientPackage –** caminho caminho &lt; para o local do pacote&gt;

   &gt;**Public Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; caminho para o arquivo de configuração do usuário&gt;

3. Abra o aplicativo usando FTAs ou atalhos agora. O aplicativo deve ser aberto usando o App-V 5,1.

   O pacote App-V 4,6 e o pacote App-V 5,1 convertido são publicados no usuário, mas o FTAs e os atalhos para os aplicativos foram considerados pelo pacote App-V 5,1.

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

[Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





