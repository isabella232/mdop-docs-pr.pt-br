---
title: Nó Políticas de Provedor
description: Nó Políticas de Provedor
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796804"
---
# Nó Políticas de Provedor


O nó **políticas do provedor** é um nível abaixo do nó do sistema de virtualização do aplicativo no painel **escopo** no console de gerenciamento do servidor do Application Virtualization. Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de políticas de provedor. Clique com o botão direito do mouse no nó **políticas do provedor** para exibir um menu pop-up que contém os elementos a seguir.

<a href="" id="new-provider-policy"></a>**Nova política de provedor**  
Exibe o assistente de nova política de provedor. Este assistente consiste nas seguintes páginas:

1.  Digite um nome no campo **nome da política do provedor** . Marque a caixa de seleção **gerenciar área de trabalho cliente usando o console de gerenciamento** , se desejar essa funcionalidade. Marque uma ou ambas as caixas de seleção a seguir se quiser a funcionalidade associada:

    -   **Atualizar a configuração de publicação quando um usuário faz logon**

    -   **Atualizar a configuração a cada**. Depois de selecionar essa opção, insira um número e selecione a unidade no menu suspenso. As entradas válidas variam de um mínimo de **30 minutos** a um máximo de **999 dias**.

2.  Clique em **Adicionar** ou **remover** para adicionar ou remover uma atribuição de grupo. Use a caixa de diálogo de pesquisa padrão do **Windows** para localizar um grupo de usuários.

3.  Marque uma das seguintes caixas de seleção na caixa de diálogo **configuração de pipeline do provedor** para habilitar o recurso associado:

    -   **Autenticação**— selecione o tipo de autenticação na lista suspensa.

    -   **Impor as configurações de permissão de acesso**

    -   **Registrar informações de uso**

    -   **Licenciamento**— selecione um esquema de imposição na lista suspensa.

4.  Clique em **concluir** para adicionar a nova política de provedor.

<a href="" id="view"></a>**Exibir**  
Altera a aparência e o conteúdo do painel de **resultados** .

<a href="" id="new-window-from-here"></a>**Nova janela a partir daqui**  
Abre um novo console de gerenciamento com o nó selecionado como nó raiz.

<a href="" id="refresh"></a>**Atualizar**  
Atualiza o modo de exibição do servidor.

<a href="" id="export-list"></a>**Exportar lista**  
Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** . Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.

<a href="" id="help"></a>**Ajuda**  
Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.

## Tópicos relacionados


[Server Management Console: nó Políticas de Provedor](server-management-console-provider-policies-node.md)

 

 





