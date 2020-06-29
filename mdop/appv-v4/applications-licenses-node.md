---
title: Nó Licenças de Aplicativos
description: Nó Licenças de Aplicativos
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797540"
---
# Nó Licenças de Aplicativos


O nó de **licenças de aplicativos** é um nível abaixo do nó do sistema virtualização de aplicativos no painel **escopo** no console de gerenciamento do servidor do Application Virtualization. Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de licenças e grupos de licenças. Os seguintes tipos de licença estão disponíveis:

-   **Licença ilimitada**— fornece acesso a qualquer número de usuários simultâneos. Esse método de licenciamento é apropriado quando você deseja associar uma licença de toda a empresa a um aplicativo.

-   **Licença simultânea**— permite que você defina o número máximo de usuários simultâneos que têm permissão para usar o aplicativo.

-   **Licença nomeada**— permite atribuir uma licença a um usuário individual. Uma licença nomeada pode ser usada para garantir que um usuário em particular sempre será capaz de executar o aplicativo.

**Observação**  Você pode combinar licenças simultâneas e nomeadas para o mesmo aplicativo.

 

Clique com o botão direito do mouse no nó **licenças de aplicativos** para exibir um menu pop-up que contém os elementos a seguir.

<a href="" id="new-unlimited-license"></a>**Nova licença ilimitada**  
Exibe o assistente de nova licença ilimitada. Este assistente consiste nas seguintes páginas:

1.  Digite o nome do grupo de licenças no campo **nome do grupo de licenças do aplicativo** e insira um valor (em minutos) no campo de **aviso de expiração da licença** . (Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.

2.  Insira um breve texto descritivo no campo **Descrição da licença** e marque a caixa de seleção **habilitada** para habilitar a licença.

    Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença. Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.

3.  Clique em **concluir** para adicionar a nova licença.

<a href="" id="new-concurrent-license"></a>**Nova licença simultânea**  
Exibe o assistente de nova licença simultânea. Este assistente consiste nas três páginas a seguir e é quase idêntico ao assistente de nova licença ilimitada:

1.  Digite o nome do grupo de licenças no campo **nome do grupo de licenças do aplicativo** e insira um valor (em minutos) no campo de **aviso de expiração da licença** . (Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.

2.  Insira um breve texto descritivo no campo **Descrição da licença** e insira um valor no campo **quantidade da licença simultânea** .

    Você também pode usar as setas para cima e para baixo para especificar o número de licenças simultâneas. Marque a caixa de seleção **habilitado** para habilitar a licença.

    Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença. Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.

3.  Clique em **concluir** para adicionar as novas licenças.

<a href="" id="new-named-license"></a>**Nova licença nomeada**  
Exibe o novo assistente de licença nomeada. Este assistente consiste nas quatro páginas a seguir:

1.  Digite o nome do grupo de licenças no campo **nome do grupo de licenças do aplicativo** e insira um valor (em minutos) no campo de **aviso de expiração da licença** . (Você pode inserir qualquer valor de 0 a 100). Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.

2.  Insira um breve texto descritivo no campo **Descrição da licença** e marque a caixa de seleção **habilitada** para habilitar a licença.

    Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença. Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.

3.  Clique em **Adicionar**, **Editar**ou **remover** usuários nomeados.

4.  Clique em **concluir** para adicionar a nova licença.

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

Se você clicar em um grupo de licenças ou licença que aparece no nó **licenças do aplicativo** no painel **escopo** , os seguintes elementos estarão disponíveis.

<a href="" id="view"></a>**Exibir**  
Altera a aparência e o conteúdo do painel de **resultados** .

<a href="" id="new-window-from-here"></a>**Nova janela a partir daqui**  
Abre um novo console de gerenciamento com o nó selecionado como nó raiz.

<a href="" id="delete"></a>**Excluir**  
Exclui um pacote do painel **resultados** .

<a href="" id="rename"></a>**Renomear**  
Altera o nome de um pacote no painel de **resultados** .

<a href="" id="export-list"></a>**Exportar lista**  
Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** . Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.

<a href="" id="properties"></a>**Propriedades**  
Exibe a caixa de diálogo **Propriedades** do grupo de licenças selecionado. A guia **geral** da caixa de diálogo **Propriedades** exibe informações sobre o grupo de licenças e permite que você altere o valor de tempo no campo de **aviso de expiração da licença** . A guia **aplicativos** exibe a lista de aplicativos associados ao grupo de licenças.

<a href="" id="help"></a>**Ajuda**  
Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.

## Tópicos relacionados


[Sobre licenciamento de aplicativos](about-application-licensing.md)

[Como gerenciar licenças de aplicativos no Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Server Management Console: nó Licenças de Aplicativo](server-management-console-application-licenses-node.md)

 

 





