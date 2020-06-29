---
title: Como sequenciar um novo aplicativo
description: Como sequenciar um novo aplicativo
author: dansimp
ms.assetid: e01e98cd-2378-478f-9739-f72c465bf79a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aab769256116e2635edbc4bcf55d212e3a2152f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796971"
---
# Como sequenciar um novo aplicativo


O sequenciador do Application Virtualization (App-V) cria aplicativos que podem ser executados em um ambiente virtual. O sequenciador App-V monitora o processo de instalação e configuração para um aplicativo, e ele registra as informações necessárias para que o aplicativo seja executado em um ambiente virtual. Você também pode usar o sequenciador do App-V para configurar quais arquivos e configurações são aplicáveis a todos os usuários e quais arquivos e configurações os usuários podem personalizar. Ao sequenciar um aplicativo, você deve salvá-lo em uma unidade local para o computador no qual você está sequenciando.

Um aplicativo sequenciado não interage com o sistema operacional porque cada aplicativo é executado em um ambiente virtual e é isolado de outros aplicativos que podem estar instalados ou em execução no computador de destino. Esse isolamento reduz drasticamente os conflitos de aplicativos e reduz a quantidade necessária de testes de pré-implantação de aplicativos.

Depois de você sequenciar o aplicativo com êxito, ele estará disponível no console do App-V Sequencer. Não há suporte para a execução do sequenciador App-V no modo de segurança.

**Para sequenciar um novo aplicativo**

1.  Você deve criar a unidade de virtualização do aplicativo para sequenciar um novo aplicativo virtual. Para criar a unidade de virtualização do aplicativo, mapeie a unidade Q:\\ para um local que possa ser usado para salvar arquivos enquanto você estiver sequenciando um aplicativo. Em seguida, você deve criar diretórios individuais para cada aplicativo que você planeja sequenciar na unidade Q:\\. Você pode criar as pastas de destino do aplicativo virtual antes de sequenciar um aplicativo ou pode criá-lo na etapa 5 deste procedimento.

2.  Para iniciar o console do App-v Sequencer, no computador que está executando o sequenciador do App-v, selecione **Iniciar**  /  **programas**  /  **Microsoft Application**Virtualization  /  **Sequencer**Virtualization. Para iniciar o **Assistente de sequenciamento**, selecione **arquivo**  /  **novo pacote**.

3.  Na página **informações do pacote** , especifique o **nome do pacote** que será atribuído ao aplicativo virtual. O nome do pacote é necessário para gerar o arquivo do Windows Installer associado. Você também deve adicionar um comentário opcional que será atribuído ao pacote e que forneça informações detalhadas sobre o aplicativo virtual. Para exibir a página **Opções avançadas** , selecione **Mostrar opções avançadas de monitoramento**. Clique em **Avançar**.

    **Observação**  
    Para exibir a página **Opções avançadas** , você deve selecionar **Mostrar opções avançadas de monitoramento**. Se você não precisar da página **Opções avançadas** , pule para a etapa 4.



4.  Na página **Opções avançadas** , para especificar o **tamanho do bloco** do aplicativo virtual, selecione o tamanho desejado. O tamanho do bloco determina como o arquivo **. sft** será dividido para transmitir o pacote pela rede para computadores de destino. Para permitir que o Microsoft Update atualize o aplicativo à medida que ele está sendo sequenciado; Selecione **permitir que o Microsoft Update seja executado durante o monitoramento**. Se você selecionar essa opção, as atualizações da Microsoft poderão ser instaladas durante a fase de monitoramento, e você precisará aceitar as atualizações associadas para que elas sejam instaladas. Para remapear os arquivos. dll (biblioteca de vínculo dinâmico) compatíveis, para que eles usem um espaço contíguo de RAM, selecione as **DLLs de base**. Selecionar essa opção pode conservar a memória e ajudar a melhorar o desempenho. Muitos aplicativos não oferecem suporte a essa opção, mas é útil em ambientes com RAM limitada, como nos cenários do Terminal Server. Clique em **Avançar**.

5.  Na página **monitorar instalação** , para monitorar a instalação de um aplicativo, clique em **Iniciar Monitoramento**. Depois de clicar em **Iniciar Monitoramento**, especifique o diretório na unidade Q:\\ na qual o aplicativo será instalado. Para instalar o aplicativo em uma pasta que não foi criada, clique em **criar nova pasta**. Você deve instalar cada aplicativo que você sequenciar em um diretório separado.

    **Importante**  
    O nome da pasta especificado não deve ter mais de 8 caracteres.



~~~
Wait for the virtual environment to load, and then install the application so that the App-V Sequencer can monitor the process. When you have completed the installation, click **Stop Monitoring** and then click **Next**.
~~~

6. Nos **arquivos adicionais a serem mapeados para a página do sistema de arquivos virtual (VFS)** , para especificar arquivos adicionais a serem adicionados ao VFS (sistema de arquivos virtual), clique em **Adicionar**. Navegue até o arquivo que você deseja adicionar e clique em **abrir**. Para limpar os arquivos existentes que foram adicionados, clique em **Redefinir** e, em seguida, clique em **Avançar**.

7. Na página **configurar aplicativos** , configure os atalhos e associações de tipo de arquivo que serão associados ao aplicativo virtual. Selecione o elemento que você deseja atualizar e, em seguida, clique em **Editar locais**. Especifique as configurações na caixa de diálogo **locais do atalho** . Clique em **OK** e, em seguida, clique em **Avançar**.

8. Na página **iniciar aplicativos** , para iniciar o aplicativo e garantir que o pacote seja otimizado para streaming, selecione o pacote e clique em **Iniciar**. Esta etapa é útil para configurar como o aplicativo é executado inicialmente em computadores de destino e para aceitar qualquer contrato de licença associado antes de o pacote ser disponibilizado para os clientes. Se houver vários aplicativos associados a este pacote, você poderá selecionar **Iniciar tudo** para abrir todos os aplicativos. Para sequenciar o pacote, clique em **Avançar**.

9. Na página **pacote de sequência** , para fechar o assistente, clique em **concluir**.

10. Depois de criar o pacote com êxito, para salvar o pacote, no console do App-V Sequencer, selecione **arquivo**  /  **salvar** e especifique o nome e o local onde o pacote será salvo.

## Tópicos relacionados


[Tarefas para o Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









