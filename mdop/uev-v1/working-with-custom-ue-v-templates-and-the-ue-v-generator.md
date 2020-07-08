---
title: Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V
description: Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799380"
---
# Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V


Para fazer roaming de aplicativos entre computadores de usuário, o Microsoft User Experience Virtualization (UE-V it Virtualization) usa *modelos de local de configurações*. Alguns modelos de local de configurações estão incluídos na virtualização da experiência do usuário. Você também pode criar, editar ou validar modelos de local de configurações personalizadas com o UE-V Generator.

O UE-V Generator monitora um aplicativo para descobrir e capturar os locais onde o aplicativo armazena suas configurações. O aplicativo que está sendo monitorado deve ser um aplicativo tradicional. O UE-V Generator não pode criar um modelo de local de configurações para os seguintes tipos de aplicativos:

-   Aplicativos virtualizados

-   Aplicativo oferecido por meio dos serviços de terminal

-   Aplicativos Java

-   Aplicativos do Windows 8

## Criar modelos de localização de configurações da UE-V com o gerador da UE-V


Como usar o UE-V Generator para criar modelos de local de configurações.

[Criar modelos de localização de configurações da UE-V com o gerador da UE-V](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Editar modelos de localização de configurações da UE-V com o gerador da UE-V


Como usar o UE-V Generator para editar modelos de local de configurações.

[Editar modelos de localização de configurações da UE-V com o gerador da UE-V](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Validar modelos de localização de configurações da UE-V com o gerador da UE-V


Como usar o UE-V Generator para validar modelos de local de configurações modificados fora do gerador do UE-V.

[Validar modelos de localização de configurações da UE-V com o gerador da UE-V](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a>Locais de configurações padrão e não padrão


O UE-V Generator ajuda você a identificar onde os aplicativos procuram arquivos de configurações e configurações do registro que os aplicativos usam para armazenar as informações das configurações. Você pode usar o UE-V Generator para abrir o aplicativo como parte do processo de descoberta para capturar as configurações em locais padrão. Os locais padrão incluem o seguinte:

-   **Configurações do registro** – locais do registro em **HKEY \ _CURRENT \ _USER**

-   **Arquivos de configurações do aplicativo** – arquivos armazenados em \ \ **usuários** \ \ [nome de usuário \] \ \ **AppData**em  \\  **roaming**

O gerador do UE-V exclui locais que normalmente armazenam arquivos de software do aplicativo, não se movimente bem entre computadores ou ambientes do usuário. O gerador do UE-V exclui estes locais. Locais excluídos são os seguintes:

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows

-   Todas as chaves do registro localizadas no hive \ _LOCAL \ _MACHINE Hive (requer direitos de administrador e exija que o contrato de UAC seja definido)

-   Arquivos localizados em diretórios de arquivos de programas (exige direitos de administrador e podem exigir um contrato de UAC para definir)

-   Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow

-   Arquivos do sistema operacional do Windows localizados em% SystemRoot% (exige direitos de administrador e podem exigir um contrato de UAC para definir)

Se as chaves do registro e os arquivos armazenados nesses locais forem necessários para fazer roaming das configurações do aplicativo, você pode adicionar manualmente os locais excluídos ao modelo de local de configurações durante o processo de criação de modelos.

## Outros recursos para este produto


[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

[Administração da UE-V 1.0](administering-ue-v-10.md)

 

 





