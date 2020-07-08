---
title: Como gerenciar aplicativos virtuais manualmente
description: Como gerenciar aplicativos virtuais manualmente
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797060"
---
# Como gerenciar aplicativos virtuais manualmente


Você pode usar o console de gerenciamento de cliente do Application Virtualization (App-V) para gerenciar aplicativos virtuais no cliente da área de trabalho do App-V ou do App-V cliente para serviços de área de trabalho remota (anteriormente serviços de terminal). Os administradores do App-V podem usar executar as seguintes tarefas:

## Como carregar ou descarregar um aplicativo App-V


Você pode usar os procedimentos a seguir para carregar ou descarregar um aplicativo a partir do cache, diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization. Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de aplicativos.

**Observação**  Quando você carrega ou descarrega um pacote, todos os aplicativos no pacote são carregados em ou removidos do cache. Ao carregar um pacote, se você não tiver espaço suficiente em cache para carregar os aplicativos, aumente o tamanho do cache. Para obter mais informações sobre o tamanho do cache, consulte [como alterar o tamanho do cache e a designação da letra da unidade](how-to-change-the-cache-size-and-the-drive-letter-designation.md).

 

**Para carregar um aplicativo App-V**

1.  Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **carregar** no menu pop-up.

2.  O aplicativo é carregado automaticamente. O progresso é acompanhado na coluna rotulada **status do pacote**. Você deve atualizar o modo de exibição para ver se a carga está concluída ou para ver o progresso.

**Para descarregar um aplicativo App-V**

1.  Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **descarregar** no menu pop-up.

2.  O aplicativo é descarregado automaticamente, e a coluna **status do pacote** é atualizada para refletir a alteração.

## Como limpar um aplicativo App-V


Você pode limpar um aplicativo do console diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization. Quando você limpa um aplicativo, o sistema remove as configurações, atalhos e associações de tipo de arquivo que correspondem ao aplicativo e também remove o aplicativo da lista de aplicativos do usuário.

**Observação**  Ao limpar um aplicativo do console, você não pode mais usar esse aplicativo. No entanto, o aplicativo permanece em cache e ainda está disponível para outros usuários no mesmo sistema. Após uma atualização de publicação, os aplicativos limpos ficarão novamente disponíveis para você. Se houver vários aplicativos em um pacote, as configurações do usuário não serão removidas até que todos os aplicativos sejam limpos.

 

**Para limpar um aplicativo do console**

1.  Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **limpar** no menu pop-up.

2.  Na solicitação de confirmação, clique em **Sim** para remover o aplicativo ou clique em **não** para cancelar a operação.

## Como reparar um aplicativo App-V


Para reparar um aplicativo selecionado, você pode executar o seguinte procedimento diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization. Ao reparar um aplicativo, você remove qualquer configuração de usuário personalizada e restaura as configurações padrão. Essa ação não altera ou exclui atalhos ou associações de tipo de arquivo, e não remove o aplicativo do cache.

**Para reparar um aplicativo App-V**

1.  Mover o cursor para o painel de **resultados** .

2.  Clique com o botão direito do mouse no aplicativo desejado e selecione **reparar** no menu pop-up.

3.  Na solicitação de confirmação, clique em **Sim** para reparar o aplicativo ou em **não** para cancelar.

## Como importar um aplicativo App-V


Você pode usar o procedimento a seguir para importar um aplicativo para o cache diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.

**Para importar um aplicativo App-V**

1.  Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **importar** no menu pop-up.

2.  Na janela **procurar** , navegue até o local do arquivo de pacote do aplicativo desejado e clique em **OK**.

    **Observação**  Se você já configurou um caminho de pesquisa de importação ou se o arquivo SFT está no mesmo caminho da última importação bem-sucedida, a etapa 2 não é necessária.

     

## Como bloquear ou desbloquear um aplicativo App-V


Você pode usar os procedimentos a seguir para bloquear ou desbloquear qualquer aplicativo no cache do cliente da área de trabalho do Application Virtualization ou no cache do cliente dos serviços de área de trabalho remota (anteriormente Terminal Services). Um aplicativo bloqueado não pode ser removido do cache para criar espaço para novos aplicativos. Para remover um aplicativo bloqueado do cache de cliente de desktop virtualização de aplicativos ou do cliente para o cache de serviços de área de trabalho remota, você deve primeiro desbloqueá-lo.

**Para bloquear um aplicativo**

1.  Mover o cursor para o painel de **resultados** .

2.  Clique com o botão direito do mouse no aplicativo desejado e selecione **Bloquear** no menu pop-up. O aplicativo selecionado está bloqueado no cache.

**Para desbloquear um aplicativo**

1.  Mover o cursor para o painel de **resultados** .

2.  Clique com o botão direito do mouse no aplicativo desejado e selecione **desbloquear** no menu pop-up. O aplicativo selecionado está desbloqueado no cache e pode ser removido.

## Como excluir um aplicativo App-V


Quando você seleciona o nó do **aplicativo** no console de gerenciamento do cliente do Application Virtualization, o painel **resultados** exibe uma lista de aplicativos. Você pode usar o procedimento a seguir para excluir um aplicativo do painel **resultados** , que também remove o aplicativo do cache.

**Observação**  Quando você exclui um aplicativo, o aplicativo selecionado não estará mais disponível para os usuários do cliente. Os atalhos e associações de tipo de arquivo estão ocultos e o aplicativo é excluído do cache. No entanto, se outro aplicativo se refere a dados nos dados de cache do sistema de arquivos do aplicativo selecionado, esses itens não serão excluídos.

Após uma atualização de publicação, os aplicativos excluídos ficarão novamente disponíveis para você.

 

**Para excluir um aplicativo**

1.  Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **excluir** no menu pop-up.

2.  Na solicitação de confirmação, clique em **Sim** para remover o aplicativo ou clique em **não** para cancelar a operação.

## Como alterar um ícone do aplicativo App-V


Você pode usar o procedimento a seguir para alterar um ícone associado ao aplicativo selecionado diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento do aplicativo virtualização de cliente.

**Para alterar um ícone de aplicativo**

1.  Mova o cursor para o painel **resultados** e clique com o botão direito do mouse no aplicativo desejado.

2.  Selecione **Propriedades**.

3.  Na guia **geral** , clique em **Alterar ícone**.

4.  Selecione o ícone desejado ou navegue até outro local para selecionar o ícone. Depois de selecionar o ícone, clique em **OK**. O novo ícone aparecerá no painel de **resultados** .

## Como adicionar um aplicativo App-V


Você pode usar o procedimento a seguir para adicionar um aplicativo diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento do cliente do Application Virtualization.

**Para adicionar um aplicativo**

1.  No painel de **resultados** , clique com o botão direito do mouse e selecione **novo aplicativo** no menu pop-up.

2.  Na página do assistente, você pode executar as seguintes tarefas:

    1.  **Alterar ícone**— exibe um navegador padrão de ícones do Windows. Procure e selecione o ícone desejado.

    2.  **Caminho ou URL do arquivo OSD**— Insira um caminho absoluto local, um caminho UNC completo (arquivo compartilhado ou diretório em uma rede) ou uma URL http.

    3.  **(Botão procurar OSD)**— exibe a caixa de diálogo padrão **Abrir arquivo** do Windows. Navegue até localizar o arquivo desejado.

3.  Clique em **concluir** para adicionar o aplicativo ao painel de **resultados** .

## Como publicar um atalho do aplicativo App-V


Você pode usar o procedimento a seguir para publicar atalhos para um aplicativo diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.

**Para publicar atalhos de aplicativos**

1.  Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **novo atalho** no menu pop-up para exibir o assistente de novo atalho.

2.  Na primeira página do assistente de novo atalho, selecione um ícone e especifique um nome para o atalho.

    1.  **Alterar ícone**— exibe um navegador padrão de ícones do Windows. Procure e selecione o ícone desejado.

    2.  **Título do atalho**— Insira o nome que você deseja dar ao atalho. Este campo é definido como padrão para o nome e a versão existentes do aplicativo.

3.  Na segunda página do assistente, determine o local do atalho publicado.

    1.  **A área de trabalho**— Marque esta caixa de seleção para publicar o atalho na área de trabalho.

    2.  **A barra de ferramentas início rápido**— Marque esta caixa de seleção para publicar o atalho na barra de ferramentas início rápido.

    3.  **O menu Enviar para**-Marque esta caixa de seleção para publicar o atalho no menu **Enviar para** .

    4.  **Programas no menu iniciar**– quando você marca a caixa de seleção **menu iniciar** , este campo torna-se ativo. Deixe este campo em branco para publicar o atalho diretamente na raiz da pasta programas, ou insira um nome de pasta ou hierarquia — por exemplo, "meu \ _Computer aplicativos do \\Office." Os atalhos criados dessa maneira estão disponíveis somente para o usuário atual.

    5.  **Outro local** e botão **procurar** — quando você marca a caixa de seleção **outro local** , esse campo torna-se ativo. Insira qualquer local válido no computador ou qualquer caminho UNC disponível (arquivo compartilhado ou diretório em uma rede). O botão **procurar** exibe uma caixa de diálogo padrão **Abrir arquivo** do Windows.

4.  Na terceira página do assistente, insira os parâmetros de linha de comando desejados.

5.  Clique em **concluir** para publicar os atalhos e sair para o painel de **resultados** .

## Como adicionar uma associação de tipo de arquivo para um aplicativo App-V


Você pode usar o procedimento a seguir para adicionar uma associação de tipo de arquivo, usando o nó **associações de tipo de arquivo** no console de gerenciamento de cliente do Application Virtualization.

**Para adicionar uma associação de tipo de arquivo**

1.  Clique com o botão direito do mouse no nó **associações de tipo de arquivo** e selecione **nova associação** no menu pop-up.

2.  Complete a primeira etapa da caixa de diálogo completando as informações a seguir e, em seguida, clique em **Avançar**:

    1.  **Extensão**— Insira uma nova extensão de nome de arquivo. Este campo está em branco por padrão.

    2.  **Crie um novo tipo de arquivo com esta descrição**: Selecione este botão de opção para inserir uma nova descrição de tipo de arquivo no campo ativo. Esse botão está selecionado por padrão, e o campo ativo está em branco.

    3.  **Aplicar este tipo de arquivo a todos os usuários**— Marque essa caixa de seleção quando quiser que essa associação seja global para todos os usuários. Por padrão, essa caixa está desmarcada.

    4.  **Vincular esta extensão a um tipo de arquivo existente**— Selecione este botão de opção para associar a extensão a um tipo de arquivo existente. Escolha um tipo de arquivo na lista suspensa. Quando você escolher essa opção, a **próxima** será alterada para **concluir**.

3.  Complete a segunda etapa da caixa de diálogo completando as informações a seguir e, em seguida, clique em **concluir** para retornar ao console de gerenciamento de cliente:

    1.  **Alterar ícone**— clique neste botão para alterar o ícone do aplicativo. Selecione um dos ícones disponíveis ou navegue até um novo local e selecione um ícone.

    2.  **Abrir arquivos com o aplicativo selecionado**— Selecione este botão de opção para abrir o arquivo com um aplicativo existente. Escolha um aplicativo na lista suspensa de aplicativos disponíveis.

    3.  **Abrir arquivo com a associação descrita neste arquivo OSD**– Selecione este botão de opção para especificar um arquivo do descritor de software (OSD) aberto que determina o aplicativo usado para abrir o arquivo. Use o botão procurar para selecionar um local existente ou digite um caminho ou uma URL formatada HTTP nesse campo.

## Como excluir uma associação de tipo de arquivo para um aplicativo App-V


Você pode usar o procedimento a seguir para excluir uma associação de tipo de arquivo. O nó **associações de tipo de arquivo** é um nível abaixo do nó **virtualização do aplicativo** no painel **escopo** . Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de associações de tipo de arquivo.

**Para remover uma associação de tipo de arquivo**

1.  No painel de **resultados** , clique com o botão direito do mouse na extensão da Associação de tipo de arquivo que você deseja excluir.

2.  Selecione **excluir** no menu pop-up.

3.  Clique em **Sim** para excluir a associação ou em **não** para retornar ao painel de **resultados** .

## Tópicos relacionados


[Cliente do Application Virtualization](application-virtualization-client.md)

 

 





