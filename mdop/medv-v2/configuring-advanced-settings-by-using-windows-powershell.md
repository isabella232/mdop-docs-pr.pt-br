---
title: Definição das configurações avançadas usando o Windows PowerShell
description: Definição das configurações avançadas usando o Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800063"
---
# Definição das configurações avançadas usando o Windows PowerShell


O pacote do espaço de trabalho do MED-V que você cria inclui um arquivo de script do Windows PowerShell (. ps1) que você pode editar antes de testar e implantar o pacote do espaço de trabalho do MED-V. Esta seção fornece informações e orientação para ajudá-lo a gerenciar as configurações de configuração do MED-V usando o Windows PowerShell antes de implantar os espaços de trabalho do MED-V.

## Usando cmdlets do Windows PowerShell no MED-V


Os seguintes cmdlets do Windows PowerShell estão disponíveis na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0:

**New-MedvConfiguration**

**Export-MedvConfiguration**

**New-MedvWorkspace**

**Export-MedvWorkspace**

Para acessar cmdlets do Windows PowerShell para MED-V, abra o Windows PowerShell e digite o seguinte comando para importar os módulos MED-V.

``` syntax
Import-Module microsoft.medv
```

Depois que os módulos forem importados, você poderá acessar a ajuda embutida para os cmdlets usando os comandos de ajuda padrão do Windows PowerShell, **Man** ou **Get-Help**. Por exemplo, para acessar uma descrição do cmdlet **New-MedvConfiguration** incluindo uma lista completa de parâmetros disponíveis, digite o comando a seguir.

``` syntax
get-help New-MedvConfiguration
```

Você também pode exibir a ajuda para parâmetros específicos. Por exemplo, para exibir a ajuda para o parâmetro VmMemory, digite o seguinte:

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

Para exibir uma lista de todas as configurações do MED-V e seus padrões, digite o comando a seguir.

``` syntax
New-MedvConfiguration -ForceDefaults
```

Para exibir uma lista de todas as definições de configuração do MED-V e seus valores atuais, digite o comando a seguir.

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## Criando um espaço de trabalho do MED-V com configurações personalizadas


Depois de criar com êxito um pacote do espaço de trabalho do MED-V usando o pacote do espaço de trabalho do MED-V, um script do Windows PowerShell é gerado na pasta que você especificou para salvar os arquivos do pacote. O conteúdo desse script mostra algumas das configurações de configuração do MED-V disponíveis que você pode editar.

Seguindo estas etapas, você pode personalizar o script e executá-lo no Windows PowerShell para criar um espaço de trabalho do MED-V com as novas configurações.

**Importante**  Execute o Windows PowerShell com credenciais administrativas e certifique-se de que a política de execução do Windows PowerShell permita a execução de scripts.

1.  Edite o script do Windows PowerShell gerado pelo pacote do espaço de trabalho do MED-V ou crie um novo script com as definições de configuração desejadas.

2.  Execute o Windows PowerShell com credenciais administrativas e, no prompt de comando, digite o comando a seguir.

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    Esse comando executa o script do Windows PowerShell e executa o cmdlet **New-MedvWorkspace** para gerar um novo pacote de espaço de trabalho do MED-V. Os novos arquivos do packager são salvos na pasta que você especificou originalmente para armazenar os arquivos do pacote do espaço de trabalho do MED-V. Para obter ajuda adicional sobre esse cmdlet, consulte a ajuda do Windows PowerShell.

 

## Exportar uma configuração do MED-V para um arquivo do registro


Você pode atualizar as configurações de configuração do MED-V após a instalação do espaço de trabalho do MED-V. Use o cmdlet **New-MedvConfiguration** para especificar os parâmetros que você deseja alterar. Por exemplo, para criar um arquivo de registro que altere a configuração de memória da máquina virtual, digite os comandos a seguir.

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

Você pode importar o arquivo resultante do registro do computador host para um espaço de trabalho do MED-V para aplicar as novas configurações.

## Tópicos relacionados


[Gerenciamento de configurações do espaço de trabalho da MED-V](managing-med-v-workspace-configuration-settings.md)

[Testar e implantar o pacote de espaço de trabalho da MED-V](test-and-deploy-the-med-v-workspace-package.md)

 

 





