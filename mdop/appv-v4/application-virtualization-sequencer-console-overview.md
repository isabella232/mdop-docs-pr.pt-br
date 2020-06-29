---
title: Visão geral do console do Application Virtualization Sequencer
description: Visão geral do console do Application Virtualization Sequencer
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799023"
---
# Visão geral do console do Application Virtualization Sequencer


O sequenciador do Application Virtualization (App-V) cria aplicativos para que possam ser executados em um ambiente virtual, como aplicativos virtuais. Depois que um aplicativo é sequenciado, ele pode ser executado em um servidor App-V para computadores de destino que executam o cliente da área de trabalho do App-V ou o cliente App-V para serviços de área de trabalho remota (anteriormente serviços de terminal) usando um processo chamado streaming. O sequenciador App-V monitora o processo de instalação e configuração para aplicativos e registra todas as informações necessárias para que o aplicativo seja executado no ambiente virtual. Esse processo também determina quais arquivos e configurações são aplicáveis a todos os usuários e quais configurações os usuários podem personalizar. Os aplicativos virtuais são executados em computadores de destino e não afetam o sistema operacional em execução no computador de destino ou em todos os aplicativos instalados no computador de destino.

## Considerações de segurança do sequenciador do Application Virtualization


O sequenciador App-V executa todos os serviços detectados no tempo de sequenciamento usando a conta do sistema local e não aplica os descritores de segurança nas solicitações de controle de serviço. Se o serviço foi instalado usando uma conta de usuário diferente ou se os descritores de segurança destinam-se a conceder permissões de serviço específicas a grupos de usuários diferentes, considere cuidadosamente se o serviço deve ser virtualizado. Em alguns casos, você deve instalar o serviço localmente para garantir que a segurança do serviço pretendida seja preservada.

## Opções do menu do console do sequenciador do Application Virtualization


Os itens de menu a seguir estão disponíveis no console do App-V Sequencer:

-   **Arquivo**— contém vários comandos para ajudar a criar, abrir, modificar e salvar aplicativos sequenciados.

-   **Editar**— contém vários comandos para a edição de aplicativos virtuais existentes.

-   **Modo de exibição**— contém vários comandos para exibir as propriedades de um aplicativo virtual.

-   **Ferramentas**— contém várias ferramentas e diagnósticos para a configuração de aplicativos virtuais.

## Opções da barra de ferramentas do console do sequenciador do Application Virtualization


Os botões da barra de ferramentas a seguir estão disponíveis no console do App-V Sequencer:

-   **Novo pacote**— clique para criar um novo aplicativo sequenciado.

-   **Abrir**— clique para abrir um pacote de aplicativo sequenciado no console do App-V Sequencer.

-   **Abrir para atualização**— clique para abrir um aplicativo sequenciado para atualizar ou aplicar uma atualização.

-   **Salvar**— clique para salvar um aplicativo virtual sequenciado.

-   **Assistente de sequenciamento**— clique para abrir o assistente de sequenciamento. Você deve usar esse botão para iniciar o assistente de sequenciamento se fizer alterações na guia **geral** em **ferramentas**  /  **Opções**.

## Guias do aplicativo virtual


As guias a seguir são exibidas quando você vê um aplicativo virtual no console do sequenciador App-V:

-   **Propriedades**— exibe informações sobre o aplicativo virtual selecionado. Você pode atualizar o **nome** e os **comentários** do pacote associados ao aplicativo virtual.

-   **Implantação**– exibe informações sobre como o aplicativo virtual será acessado por computadores de destino. Você pode configurar o método de entrega do aplicativo virtual, e pode configurar quais sistemas operacionais devem estar em execução no computador de destino. Você também pode configurar as opções de saída associadas. Se você planeja ter clientes acessarem um aplicativo virtual de um arquivo, use o seguinte formato ao especificar o caminho: **file://Server/share/Path/.sft**. Selecione **aplicar descritores de segurança** para preservar a segurança associada ao pacote durante uma atualização, ou as permissões serão redefinidas durante a atualização.

-   **Histórico de alterações**— exibe informações sobre atualizações feitas no aplicativo virtual.

-   **Arquivos**— exibe os arquivos associados ao aplicativo virtual selecionado. Você pode fazer revisões secundárias nas propriedades de arquivo associadas usando os campos apropriados.

-   **Registro virtual**— exibe o registro virtual associado ao aplicativo virtual selecionado. Você pode adicionar ou excluir as chaves do registro clicando com o botão direito do mouse na entrada apropriada.

-   **Sistema de arquivos virtual**— exibe os sistemas de arquivos virtuais associados ao aplicativo virtual selecionado. Você pode adicionar, excluir ou editar entradas do sistema de arquivos nesta guia clicando com o botão direito do mouse na entrada apropriada e selecionando a opção.

-   **Serviços virtuais**— exibe os serviços associados ao aplicativo virtual selecionado.

-   **OSD**— exibe informações sobre o descritor de software aberto (OSD) associado ao aplicativo virtual. Você pode atualizar os arquivos associados ao arquivo OSD clicando com o botão direito do mouse na entrada apropriada e selecionando a ação desejada.

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





