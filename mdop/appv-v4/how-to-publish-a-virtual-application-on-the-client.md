---
title: Como publicar um aplicativo virtual no cliente
description: Como publicar um aplicativo virtual no cliente
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797012"
---
# Como publicar um aplicativo virtual no cliente


Ao implantar o Application Virtualization usando um sistema de distribuição de software eletrônico, você pode usar um dos procedimentos a seguir para publicar um pacote de aplicativo para seus usuários.

**Para publicar um pacote usando um arquivo autônomo do Windows Installer**

1.  O cliente deve ser instalado com o parâmetro *RequireAuthorizationIfCached* definido como 0 (zero). Para obter mais informações sobre como definir esse parâmetro, consulte [parâmetros da linha de comando do instalador do cliente do aplicativo virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md)

2.  Copie o arquivo do Windows Installer e o arquivo SFT para a mesma pasta no computador de destino.

3.  Execute o seguinte comando no computador:

    `Msiexec.exe /I "packagename.msi" /q`

**Para publicar um pacote usando o Windows Installer e o manifesto do pacote**

1.  Copie o arquivo do Windows Installer para o computador de destino e o arquivo SFT para o compartilhamento de conteúdo no servidor de streaming.

2.  Execute o seguinte comando no computador de cada usuário:

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **Importante**  Para OVERRIDEURL, todos os caracteres de barra invertida devem ter escape usando a barra invertida precedente ou o caminho OVERRIDEURL não será analisado corretamente. Além disso, propriedades e valores devem ser inseridos em letras maiúsculas, exceto quando o valor for um caminho para um arquivo.

     

**Para publicar um pacote usando SFTMIME**

-   Para obter um exemplo de como publicar um aplicativo para todos os usuários em um computador, execute o seguinte comando no computador do usuário:

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    Para obter mais detalhes sobre esses e outros comandos do SFTMIME, consulte [referência de comandos do SFTMIME](sftmime--command-reference.md).

## Tópicos relacionados


[Determinar o método de publicação](determine-your-publishing-method.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Referência de comando SFTMIME](sftmime--command-reference.md)

[Cenário de Entrega Autônoma Application Virtualization Clients](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





