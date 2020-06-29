---
title: Como converter um pacote criado em uma versão anterior do App-V
description: Como converter um pacote criado em uma versão anterior do App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796480"
---
# Como converter um pacote criado em uma versão anterior do App-V


Você pode usar o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais que foram criados com versões anteriores do App-V.

**Observação**  
Se estiver executando um computador com uma arquitetura de 64 bits, você deve usar a versão x86 do PowerShell.



O conversor de pacote só pode converter diretamente pacotes que foram criados usando o sequenciador do App-V 4,5 ou uma versão subsequente. Os pacotes que foram criados usando uma versão anterior ao App-V 4,5 devem ser atualizados para o formato App-V 4,5 ou App-V 4,6 antes da conversão.

As informações a seguir fornecem a direção para converter pacotes de aplicativos virtuais existentes.

**Importante**  
Você deve configurar o conversor de pacote para sempre salvar o arquivo ingredientes do pacote em um local seguro e diretório. Um local seguro pode ser acessado apenas por um administrador. Além disso, ao implantar o pacote, salve-o em um local seguro ou certifique-se de que nenhum outro usuário tenha permissão para ser conectado durante o processo de conversão.



**Introdução**

1.  Instale o sequenciador do App-V em um computador no seu ambiente. Para obter informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-beta-gb18030.md).

2. Importar o módulo do PowerShell necessário

```powershell
Import-Module AppVPkgConverter
```

3. Os seguintes cmdlets estão disponíveis:

   -   Test-AppvLegacyPackage – este cmdlet foi projetado para verificar pacotes. Ele retornará informações sobre qualquer falha com o pacote, como arquivos **. sft** ausentes, uma fonte inválida, erros de arquivo **. OSD** ou uma versão de pacote inválida. Esse cmdlet não analisará o arquivo **. sft** nem fará nenhuma validação em profundidade. Para obter informações sobre opções e funcionalidade básica para esse cmdlet, usando o PowerShell cmdline, digite `Test-AppvLegacyPackage -?` .

   -   ConvertFrom-AppvLegacyPackage – para converter um pacote existente, digite-o `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` . Nesse comando, `c:\contentStore` representa a localização do pacote existente e `c:\convertedPackages` é o diretório de saída no qual o arquivo do pacote de aplicativo virtual do App-5,0 V resultante será salvo. Por padrão, se você não especificar um novo nome, o nome do pacote antigo será usado para o nome do arquivo App-V 5,0.

       Além disso, o conversor de pacote otimiza o desempenho de pacotes no App-V 5,0 definindo o pacote para transmitir a falha do pacote App-V.  Isso é mais performativo do que o bloco de recursos principal e baixando completamente o pacote. O sinalizador **DownloadFullPackageOnFirstLaunch** permite que você converta o pacote e defina o pacote para ser totalmente baixado por padrão.

       **Observação**  
       Antes de especificar o diretório de saída, você deve criar o diretório de saída.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)









