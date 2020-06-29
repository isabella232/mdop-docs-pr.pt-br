---
title: Painel Resultados de Associação de Arquivo
description: Painel Resultados de Associação de Arquivo
author: dansimp
ms.assetid: bc5ceb48-1b9f-45d9-a770-1bac90629c76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 73ea8e0e4145aeae309abff362a790287f19f6af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797950"
---
# Painel Resultados de Associação de Arquivo


O painel **resultados** da **Associação de arquivo** é um nível abaixo do painel do **sistema** no console de gerenciamento de cliente do Application Virtualization e exibe uma lista de associações de tipo de arquivo disponíveis. Os usuários podem ver uma lista de extensões de tipo de arquivo e os aplicativos aos quais elas correspondem.

Para exibir opções específicas para tipos de arquivo, clique com o botão direito do mouse em qualquer extensão de aplicativo para exibir um menu pop-up que contém os seguintes elementos.

<a href="" id="delete"></a>**Excluir**  
Exclui a extensão de nome de arquivo da lista e remove a associação para o tipo de arquivo.

<a href="" id="properties"></a>**Propriedades**  
Exibe a caixa de diálogo **Propriedades** para a extensão do aplicativo selecionada. Esta caixa de diálogo tem duas guias:

-   A guia **geral** exibe informações gerais sobre a associação de tipo de arquivo, incluindo o ícone e o nome do aplicativo:

    -   **— Exibe o ícone selecionado**para o tipo de arquivo associado.

    -   **Nome da Associação**— exibe o nome do tipo de arquivo.

    -   **Alterar ícone**— clique neste botão para alterar o ícone da Associação de tipo de arquivo.

    -   **Extensão**— exibe a extensão ou extensões associadas a um determinado tipo de arquivo.

    -   **Desvincular**— esse botão estará habilitado quando mais de uma extensão estiver associada a um aplicativo. Clique em **desvincular** para gerenciar a extensão do tipo de arquivo separadamente da extensão com a qual está vinculada no momento.

    -   **Aplicativo especificado**— selecione esse botão de opção e escolha um aplicativo na lista suspensa de aplicativos disponíveis. Você está alterando o aplicativo usado pela ação padrão. Você também pode procurar um aplicativo para localizar um aplicativo se ele não estiver disponível na lista suspensa.

    -   **Arquivo OSD**— selecione esse botão de opção e especifique um caminho para um arquivo OSD (Open Software Descriptor) aberto. Você também pode navegar até um arquivo OSD.

-   A guia **avançado** exibe informações detalhadas sobre a associação de tipo de arquivo:

    -   **Ação**— exibe uma lista das ações disponíveis para o tipo de arquivo associado.

    -   **Tipo de conteúdo**— exibe uma descrição do conteúdo do tipo de arquivo. Se este campo for deixado em branco, o cliente o preencherá.

    -   **Tipo percebido**— mostra o tipo de arquivo. Você pode selecionar uma das opções na lista suspensa ou adicionar sua própria.

    -   **Confirmar abertura após o download**— Marque esta caixa de seleção para exibir uma mensagem de confirmação após o carregamento de um arquivo. Se essa caixa estiver marcada, quando você tentar abrir um arquivo desse tipo fazendo o download para um navegador da Web, o navegador solicitará que você veja se deseja salvar o arquivo em vez de abri-lo diretamente no navegador sem confirmação.

    -   **Sempre mostrar extensão**— Marque essa caixa de seleção para especificar que as extensões devem ser mostradas mesmo quando o usuário solicitar que o sistema oculte as extensões para tipos de arquivo conhecidos.

    -   **Adicionar ao novo menu**— Marque essa caixa de seleção para especificar que a extensão ou as extensões devem ser listadas no menu de contexto **novo** Shell.

    -   **Aplicar a todos os usuários**— Marque esta caixa de seleção para especificar que as extensões devem estar disponíveis para todos os usuários.

<a href="" id="help"></a>**Ajuda**  
Exibe o sistema de ajuda do console de gerenciamento de cliente.

Para exibir opções gerais para o painel de **resultados** , clique com o botão direito do mouse em qualquer lugar do painel **resultados** para exibir um menu pop-up que contém os elementos a seguir.

<a href="" id="new-association"></a>**Nova associação**  
Este item de menu exibe o assistente de nova associação. Este assistente consiste em duas páginas:

1.  Insira uma extensão de nome de arquivo nova ou existente e associe a extensão a um tipo de arquivo:

    -   **Extensão**— Insira uma nova extensão de nome de arquivo. Este campo está em branco por padrão.

    -   **Crie um novo tipo de arquivo com esta descrição**: Selecione este botão de opção para inserir uma nova descrição de tipo de arquivo no campo ativo. Esse botão está selecionado por padrão, e o campo ativo está em branco.

    -   **Aplicar este tipo de arquivo a todos os usuários**— Marque essa caixa de seleção quando quiser que essa associação seja global para todos os usuários. Por padrão, essa caixa não está selecionada.

    -   **Vincular esta extensão a um tipo de arquivo existente**— Selecione este botão de opção para associar a extensão a um tipo de arquivo existente. Escolha um tipo de arquivo na lista suspensa. Quando você escolher essa opção, a **próxima** será alterada para **concluir**.

2.  Selecione o aplicativo que vai abrir arquivos com a extensão especificada:

    -   **Abrir arquivos com o aplicativo selecionado**— Selecione este botão de opção para abrir o arquivo com um aplicativo existente. Escolha um aplicativo na lista suspensa de aplicativos disponíveis.

    -   **Abrir arquivo com a associação descrita neste arquivo OSD**– Selecione este botão de opção para especificar um arquivo OSD que determina o aplicativo usado para abrir o arquivo. Use o botão procurar para selecionar um local existente ou digite um caminho ou uma URL formatada HTTP nesse campo.

<a href="" id="refresh"></a>**Atualizar**  
Este item atualiza o painel de **resultados** .

<a href="" id="export-list"></a>**Exportar lista**  
Com este item de menu, você pode criar um arquivo de texto delimitado por tabulação que contenha o conteúdo do painel de **resultados** . Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.

<a href="" id="view"></a>**Exibir**  
Esta lista pop-up de itens de menu permite alterar a aparência e o conteúdo do painel de **resultados** .

<a href="" id="arrange-line-up-icons"></a>**Ícones organizar/alinhar**  
Esses itens de menu podem ser usados para alterar como os ícones são exibidos no painel de **resultados** .

<a href="" id="help"></a>**Ajuda**  
Este item exibe o sistema de ajuda do console de gerenciamento.

## Tópicos relacionados


[Como alterar um ícone de aplicativo](how-to-change-an-application-icon.md)

[Nó Associações de Tipo de Arquivo](file-type-associations-node-client.md)

[Colunas do painel Resultados de Associação de Arquivo](file-type-association-results-pane-columns.md)

 

 





