---
title: Editar modelos de localização de configurações da UE-V com o gerador da UE-V
description: Editar modelos de localização de configurações da UE-V com o gerador da UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800007"
---
# Editar modelos de localização de configurações da UE-V com o gerador da UE-V


Use o gerador do Microsoft User Experience Virtualization (UE-V) para editar modelos de local de configurações. Quando as configurações revisadas são adicionadas aos modelos usando o UE-V Generator, as informações de versão no modelo são atualizadas automaticamente para garantir que os modelos existentes implantados na empresa sejam atualizados corretamente.

**Como editar um modelo de local de configurações do UE-V com o UE-V Generator**

1.  Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.

2.  Clique em **Editar um modelo de local de configurações**.

3.  Na lista de modelos usados recentemente, selecione o modelo a ser editado. Ou, se preferir, **navegue** até o arquivo de modelo de configurações. Clique em **Avançar** para continuar.

4.  Examine as **Propriedades**, locais **do registro** e locais de **arquivos** do modelo de configurações. Edite conforme necessário.

    -   A guia **Propriedades** permite que você exiba e edite as seguintes propriedades:

        -   **Nome do aplicativo**: o nome do aplicativo escrito na descrição das propriedades do arquivo de programa.

        -   **Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa. Esse nome geralmente tem a extensão. exe.

        -   **Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo. Essa propriedade, juntamente com a **versão do arquivo**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do produto.

        -   **Versão do arquivo**: o número da versão do arquivo the.exe arquivo do aplicativo. Essa propriedade, juntamente com a **versão do produto**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do programa.

        -   **Nome do autor do modelo** (opcional): o nome do autor do modelo de configurações.

        -   **Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.

    -   A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações. Você pode editar os locais do registro usando o menu suspenso **tarefas** . As tarefas incluem adicionar novas chaves, editar o nome ou o escopo de chaves existentes, excluir chaves e navegar pelo registro no qual as chaves estão localizadas. Ao definir o escopo do registro, você pode usar o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada. Use **todas as configurações** e **subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.

    -   A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais do arquivo incluídos no modelo de local de configurações. Você pode editar os locais de arquivos usando o menu suspenso **tarefas** . As tarefas para locais de arquivos incluem adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer. Para incluir todos os arquivos na pasta especificada, deixe a máscara de arquivo vazia.

5.  Clique em **salvar** para salvar as alterações no modelo de local de configurações.

6.  Clique em **fechar** para fechar o assistente de modelo de configurações. Saia do aplicativo do gerador do UE-V.

    Depois de editar o modelo de local de configurações para um aplicativo, você deve testar o modelo. Implante o modelo de local de configurações revisado em um ambiente de laboratório antes de colocá-lo em produção na empresa.

**Como editar manualmente um modelo de local de configurações**

1.  Criar uma cópia local do modelo de local de configurações (arquivo. xml). Os modelos de local das configurações do UE-V são arquivos. xml identificando os locais onde os valores das configurações de repositório do aplicativo.

2.  Abra o arquivo de modelo de local de configurações com um editor de XML.

3.  Edite o arquivo de modelo de local de configurações. Todas as alterações devem estar de acordo com o arquivo de esquema do UE-V definido em SettingsLocationTempate. xsd. Uma cópia do arquivo. xsd está localizada `\ProgramData\Microsoft\UEV\Templates` por padrão.

4.  Salve o arquivo de modelo de local de configurações e feche o editor de XML.

5.  Valide o arquivo de modelo de local de configurações modificadas com o UE-V Generator. Para obter mais informações sobre como validar com o UE-V Generator, consulte [validar modelos de local de configurações do UE-v com o UE-v Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).

## Tópicos relacionados


[Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





