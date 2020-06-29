---
title: Como aplicar o arquivo de configuração da implantação usando o PowerShell
description: Como aplicar o arquivo de configuração da implantação usando o PowerShell
author: dansimp
ms.assetid: 5df5d5bc-6c72-4087-8b93-d6d4b502a1f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6764f07dfe8cff1fb30c354937a405202468428
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796501"
---
# Como aplicar o arquivo de configuração da implantação usando o PowerShell


O arquivo de configuração de implantação dinâmica é aplicado quando um pacote é adicionado ou definido como um computador executando o cliente App-V 5,0 antes do pacote ser publicado. O arquivo define as configurações padrão do pacote para todos os usuários do computador que executam o cliente App-V 5,0. Esta seção descreve as etapas usadas para usar um arquivo de configuração de implantação. O procedimento se baseia no exemplo a seguir e pressupõe que os seguintes arquivos de pacote e configuração existam em um computador:

**c:\\Packages\\Contoso\\MyApp.appv**

**c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

**Para aplicar o arquivo de configuração de implantação usando o PowerShell**

-   Para especificar um novo conjunto padrão de configurações para todos os usuários que executarão o pacote em um computador específico, usando um console do PowerShell, digite o seguinte:

    **Add-AppVClientPackage – caminho c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

    **Observação**  
    Esse comando captura o objeto resultante em $pkg. Se o pacote já estiver presente no computador, o cmdlet **set-AppVclientPackage** pode ser usado para aplicar o documento de configuração de implantação:

    **Set-AppVClientPackage – Name MyApp-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)









