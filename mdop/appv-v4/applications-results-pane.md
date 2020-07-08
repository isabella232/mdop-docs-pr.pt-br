---
title: Painel Resultados de Aplicativos
description: Painel Resultados de Aplicativos
author: dansimp
ms.assetid: 977a4d35-5344-41fa-af66-14957b38ed47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdabaeee0b9aaa1c96b6ae732ae4bb5b6d63ef3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797536"
---
# Painel Resultados de Aplicativos


O painel **resultados de aplicativos** no console de gerenciamento de cliente do Application Virtualization exibe uma lista dos aplicativos disponíveis. Os usuários podem ver uma lista de aplicativos para os quais receberam privilégios de acesso.

Para obter mais informações sobre os procedimentos que você pode executar neste painel, consulte [como gerenciar aplicativos no console de gerenciamento de cliente](how-to-manage-applications-in-the-client-management-console.md).

Clique com o botão direito do mouse em qualquer aplicativo para exibir um menu pop-up que contém os elementos a seguir.

<a href="" id="new-shortcut"></a>**Novo atalho**  
Este item de menu exibe o assistente de novo atalho. Este assistente consiste em três páginas:

1.  Selecione um ícone e especifique um nome para o atalho:

    1.  **Alterar ícone**— exibe um navegador padrão de ícones do Windows. Procure e selecione o ícone desejado.

    2.  **Título do atalho**— Insira o nome que você deseja dar ao atalho. Este campo é definido como padrão para o nome e a versão existentes do aplicativo.

2.  Determinar a localização do atalho publicado.

    1.  **Local do atalho**— selecione um local marcando uma das caixas de seleção. Os locais disponíveis são **área de trabalho**, **barra de ferramentas de início rápido**, **menu Enviar para**, **menu iniciar**e **outro local**.

    2.  **Programas no menu iniciar**– quando você marca a caixa de seleção **menu iniciar** , este campo torna-se ativo. Deixe este campo em branco para publicar o atalho diretamente na raiz da pasta programas, ou insira um nome de pasta ou hierarquia — por exemplo, "meu \ _Computer aplicativos do \\Office." Os atalhos criados dessa maneira estão disponíveis somente para o usuário atual.

    3.  **Outro local** e botão procurar — quando você marca a caixa de seleção **outro local** , esse campo torna-se ativo. Insira qualquer local válido no computador ou qualquer caminho de convenção universal de nomenclatura (UNC) disponível (arquivo compartilhado ou diretório em uma rede). O botão procurar exibe uma caixa de diálogo padrão **Abrir arquivo** do Windows.

3.  Insira os parâmetros de linha de comando desejados e clique em **concluir** para sair do assistente.

<a href="" id="new-association"></a>**Nova associação**  
Este item de menu exibe o assistente de nova associação. Este assistente consiste em duas páginas:

1.  Insira uma extensão de nome de arquivo e associe a extensão a um tipo de arquivo.

    1.  **Extensão**— Insira uma extensão de nome de arquivo. Este campo está em branco por padrão.

    2.  **Crie um novo tipo de arquivo com esta descrição**: Selecione este botão de opção para inserir uma nova descrição de tipo de arquivo no campo ativo. Esse botão está selecionado por padrão, e o campo ativo está em branco.

    3.  **Aplicar este tipo de arquivo a todos os usuários**— Marque essa caixa de seleção quando quiser que essa associação seja global para todos os usuários. Por padrão, essa caixa não está selecionada.

    4.  **Vincular esta extensão a um tipo de arquivo existente**— Selecione este botão de opção para associar a extensão a um tipo de arquivo existente. Escolha um tipo de arquivo na lista suspensa. Quando você escolher essa opção, a **próxima** será alterada para **concluir**.

2.  Selecione o aplicativo que vai abrir arquivos com a extensão especificada:

    1.  **Abrir arquivos com o aplicativo selecionado**— Selecione este botão de opção para abrir o arquivo com um aplicativo existente. Escolha um aplicativo na lista suspensa de aplicativos disponíveis.

    2.  **Abrir arquivo com a associação descrita neste arquivo OSD**– Selecione este botão de opção para especificar um arquivo do descritor de software (OSD) aberto que determina o aplicativo usado para abrir o arquivo. Use o botão procurar para selecionar um local existente ou digite um caminho ou uma URL formatada HTTP nesse campo.

<a href="" id="repair"></a>**Reparar**  
Redefine as configurações padrão do aplicativo e elimina todas as configurações definidas pelo usuário para o aplicativo selecionado.

<a href="" id="load-or-unload"></a>**Carregar** ou **descarregar**  
Carrega ou descarrega o aplicativo selecionado no cache. Esse comando não estará disponível se 100% do aplicativo estiver no cache.

<a href="" id="clear"></a>**Apagar**  
Remove as configurações do usuário, atalhos e associações de tipo de arquivo para o aplicativo selecionado. Este item não estará disponível se um usuário estiver executando qualquer aplicativo de um pacote de aplicativos. Exibe um prompt de confirmação.

<a href="" id="lock-or-unlock"></a>**Bloquear** ou **desbloquear**  
Bloqueia ou desbloqueia um aplicativo no cache. Quando um aplicativo está bloqueado, ele não pode ser excluído ou substituído.

<a href="" id="import"></a>**Importar**  
Importa um aplicativo para o cache diretamente deste comando no nó **aplicativos** .

<a href="" id="delete"></a>**Excluir**  
Exclui um aplicativo do painel **resultados** e do computador e limpa o aplicativo do cache.

<a href="" id="refresh"></a>**Atualizar**  
Atualiza o conteúdo do painel de **resultados** .

<a href="" id="properties"></a>**Propriedades**  
Exibe a caixa de diálogo **Propriedades** para o aplicativo selecionado. Esta caixa de diálogo tem duas guias:

1.  A guia **geral** exibe o nome e o ícone do aplicativo, o local de onde o aplicativo foi transmitido e o caminho para o arquivo OSD local. Nessa guia, você pode alterar o ícone do aplicativo ou pode limpar as configurações (que remove os atalhos e as associações de tipo de arquivo).

2.  A **guia pacote** exibe informações sobre o pacote do aplicativo, e você pode **Bloquear**, **desbloquear**, **carregar**, **descarregar**e **importar** aplicativos.

<a href="" id="help"></a>**Ajuda**  
Exibe o sistema de ajuda do console de gerenciamento de cliente.

## Exibir opções gerais para o painel de resultados


Clique com o botão direito do mouse em qualquer lugar do painel **resultados** para exibir um menu pop-up que contém os elementos a seguir.

<a href="" id="new-application"></a>**Novo aplicativo**  
Este item de menu exibe o assistente de novo aplicativo. Este assistente consiste em uma página onde você pode selecionar um ícone para o aplicativo e navegar ou inserir uma URL ou um caminho para o arquivo OSD:

1.  **Alterar ícone**— exibe um navegador padrão de ícones do Windows. Procure e selecione o ícone desejado.

2.  **Caminho ou URL do arquivo OSD**— Insira um caminho absoluto local, um caminho UNC completo ou uma URL http.

3.  **... (Botão procurar OSD)** — Exibe a caixa de diálogo padrão **Abrir arquivo** do Windows. Navegue até localizar o arquivo desejado.

<a href="" id="refresh"></a>**Atualizar**  
Atualiza o painel de **resultados** .

<a href="" id="export-list"></a>**Exportar lista**  
Você pode usar esse item de menu para criar um arquivo de texto delimitado por tabulação que contenha o conteúdo do painel de **resultados** . Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.

<a href="" id="view"></a>**Exibir**  
Esta lista pop-up de itens de menu permite alterar a aparência e o conteúdo do painel de **resultados** .

<a href="" id="arrange-line-up-icons"></a>**Ícones organizar/alinhar**  
Esses itens de menu podem ser usados para alterar como os ícones são exibidos no painel de **resultados** .

<a href="" id="help"></a>**Ajuda**  
Exibe o sistema de ajuda para o console de gerenciamento.

## Tópicos relacionados


[Nó Aplicativos](applications-node.md)

[Colunas do painel Resultados de Aplicativos](applications-results-pane-columns.md)

[Referência do Application Virtualization Client Management Console](application-virtualization-client-management-console-reference.md)

[Como gerenciar aplicativos no Client Management Console](how-to-manage-applications-in-the-client-management-console.md)

 

 





