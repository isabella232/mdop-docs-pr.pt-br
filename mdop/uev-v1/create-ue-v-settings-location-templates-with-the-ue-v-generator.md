---
title: Criar modelos de localização de configurações da UE-V com o gerador da UE-V
description: Criar modelos de localização de configurações da UE-V com o gerador da UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799913"
---
# Criar modelos de localização de configurações da UE-V com o gerador da UE-V


O Microsoft User Experience Virtualization (UE-V Experience Virtualization) usa *modelos de local de configurações* para direcionar as configurações de aplicativo entre computadores dos usuários. Alguns modelos de local de configurações padrão estão incluídos na virtualização da experiência do usuário. Você também pode criar, editar ou validar modelos de local de configurações personalizadas com o UE-V Generator.

O UE-V Generator monitora um aplicativo para descobrir e capturar os locais onde o aplicativo armazena suas configurações. O aplicativo que está sendo monitorado deve ser um aplicativo tradicional. O UE-V Generator não pode criar um modelo de local de configurações dos seguintes tipos de aplicativos:

-   Aplicativos virtualizados

-   Aplicativo oferecido por meio dos serviços de terminal

-   Aplicativos Java

-   Aplicativos do Windows 8

**Observação**  Não é possível criar modelos UE-V em aplicativos virtualizados ou aplicativos de serviços de terminal. No entanto, as configurações sincronizadas usando os modelos podem ser aplicadas a esses aplicativos. Para criar modelos compatíveis com o VDI (Virtual Desktop Infrastructure) e aplicativos de serviços de terminal, abra um arquivo do Windows Installer (. msi) do aplicativo com o UE-V Generator.

 

**Locais excluídos**

O processo de descoberta exclui locais que normalmente armazenam arquivos de software do aplicativo que não são bem transferidos entre computadores ou ambientes do usuário. Os itens a seguir estão excluídos:

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows

-   Todas as chaves do registro localizadas na seção HKEY \ _LOCAL \ _MACHINE

-   Arquivos localizados em diretórios de arquivos de programas

-   Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow

-   Arquivos do sistema operacional Windows localizado em% SystemRoot%

Se as chaves do registro e os arquivos armazenados nestes locais excluídos forem necessários para fazer roaming das configurações do aplicativo, os administradores poderão adicionar manualmente os locais ao modelo de local de configurações durante o processo de criação de modelos.

## Criar modelos UE-V


Use o UE-V Generator para criar modelos de local de configurações para aplicativos de linha de negócios ou outros aplicativos. Após a criação do modelo de um aplicativo, você pode implantar o modelo nos computadores para que os usuários possam fazer roaming das configurações desse aplicativo.

**Para criar um modelo de local de configurações de UE-V com o UE-V Generator**

1.  Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.

2.  Clique em **criar um modelo de local de configurações**.

3.  Especifique o aplicativo. Navegue até o caminho do arquivo do aplicativo (. exe) ou o atalho do aplicativo (. lnk) para o qual você deseja criar um modelo de local de configurações. Especifique os argumentos de linha de comando, se houver e em diretório de trabalho, se houver. Clique em **Avançar** para continuar.

    **Observação**  Antes de o aplicativo ser iniciado, o sistema exibe uma solicitação de **controle de conta de usuário**. É necessário ter permissão para monitorar o registro e os locais de arquivo que o aplicativo usa para armazenar as configurações.

     

4.  Depois que o aplicativo for iniciado, feche o aplicativo. O gerador do UE-V registra os locais onde o aplicativo armazena suas configurações.

5.  Depois que o processo for concluído, clique em **Avançar** para continuar.

6.  Revise e marque as caixas de seleção ao lado dos locais de arquivos de configurações e locais de configurações do registro para fazer roaming deste aplicativo. A lista inclui as duas categorias a seguir para locais de configurações:

    -   **Padrão**: configurações de aplicativo que são armazenadas no registro nas chaves hKey \ _CURRENT \ _USER ou nas pastas de arquivo em \ \ **Users** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **roaming**. O gerador do UE-V inclui essas configurações por padrão.

    -   Não **padrão**: configurações do aplicativo armazenadas fora dos locais especificados nas práticas recomendadas para armazenamento de dados de configurações (opcional). Isso inclui arquivos e pastas em **usuários** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **local**. Revise esses locais para determinar se devem ser incluídos no modelo de local de configurações. Marque as caixas de seleção de locais para incluí-las.

    Clique em **Avançar** para continuar.

7.  Revise e edite quaisquer **Propriedades**, locais **do registro** e locais de **arquivos** para o modelo de local de configurações.

    -   Edite as seguintes propriedades na guia **Propriedades** :

        -   **Nome do aplicativo**: o nome do aplicativo escrito na descrição das propriedades dos arquivos de programa.

        -   **Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa. Esse nome geralmente tem a extensão. exe.

        -   **Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo. Essa propriedade, em conjunto com a versão do arquivo, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do produto.

        -   **Versão do arquivo**: o número da versão do arquivo the.exe arquivo do aplicativo. Essa propriedade, em conjunto com a versão do produto, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do programa.

        -   **Nome do autor do modelo** (opcional): o nome do autor do modelo de local de configurações.

        -   **Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.

    -   A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações. Edite os locais do registro usando o menu suspenso **tarefas** . As tarefas incluem adicionar novas chaves, editar o nome ou o escopo de chaves existentes, excluir chaves e navegar no registro em que as chaves estão localizadas. Use o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada. Use **todas as configurações e subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.

    -   A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais do arquivo incluídos no modelo de local de configurações. Edite os locais de arquivos usando o menu suspenso **tarefas** . As tarefas para locais de arquivos incluem adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer. Deixe a máscara de arquivo vazia para incluir todos os arquivos na pasta especificada.

8.  Clique em **criar** e salvar o modelo de local de configurações no computador.

9.  Clique em **fechar** para fechar o assistente de modelo de configurações. Saia do aplicativo do gerador do UE-V.

    Depois de criar o modelo de local de configurações para um aplicativo, você deve testar o modelo. Implante o modelo em um ambiente de laboratório antes de colocá-lo em produção na empresa.

## Tópicos relacionados


[Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





