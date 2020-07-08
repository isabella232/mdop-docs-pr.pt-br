---
title: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico
description: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796361"
---
# Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico

**Observação:** O App-V 4,6 tem saído do suporte básico.

Use o procedimento a seguir para migrar os pontos de extensão de um pacote App-V 4.6 para um pacote App-V 5,0 usando o arquivo de configuração de implantação.

**Observação**  O procedimento a seguir não requer um servidor de gerenciamento do App-V 5,0.

 

**Para migrar os pontos de extensão de um pacote de um pacote App-V 4.6 para um pacote App-V 5,0 convertido usando o arquivo de configuração de implantação**

1. Localize o diretório que contém o arquivo de configuração de implantação do pacote que você deseja migrar. Para definir a política, faça a seguinte atualização para a seção **userconfiguration** :

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID do pacote&gt;**

   Veja a seguir um exemplo de conteúdo de um arquivo de configuração de implantação:

   &lt;? XML Version = "1.0"?&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageID = &lt; ID do pacote &gt; DisplayName = &lt; Display Name&gt;

   &lt;MachineConfiguration/&gt;

   &lt;Userconfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID do pacote&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. Para adicionar o pacote App-V 5,0 em um prompt de comando do PowerShell com privilégios elevados, digite:

   PS &gt; **$pkg = Add-AppvClientPackage** **–** caminho caminho &lt; para o local &gt;  - do pacote**DynamicDeploymentConfiguration** &lt; caminho para o arquivo de configuração de implantação&gt;

   &gt;**$Pkg de publicação PS-AppVClientPackage**

3. Para testar a migração, abra o aplicativo virtual usando o FTAs ou atalhos associados. O aplicativo é aberto com o App-V 5,0. Ambos, o pacote App-V 4,6 e o pacote App-V 5,0 convertido são publicados no usuário, mas o FTAs e os atalhos para os aplicativos foram considerados pelo pacote App-V 5,0.

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





