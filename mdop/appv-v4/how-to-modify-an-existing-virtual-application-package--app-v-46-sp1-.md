---
title: Como modificar um pacote de aplicativos virtuais existente (App-V 4.6 SP1)
description: Como modificar um pacote de aplicativos virtuais existente (App-V 4.6 SP1)
author: dansimp
ms.assetid: f43a9927-4325-4b2d-829f-3068e4e84349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e9d45a32afa240ce7f6fb2ee5dfbc51889c1fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797045"
---
# Como modificar um pacote de aplicativos virtuais existente (App-V 4.6 SP1)


Use os procedimentos a seguir para modificar um pacote de aplicativo virtual existente. Você pode usar esses procedimentos para:

-   Atualizar um aplicativo que faz parte de um pacote de aplicativo virtual existente. Para executar essa tarefa, use o procedimento **"para atualizar um aplicativo em um pacote de aplicativo existente"** neste documento.

-   Modifique as propriedades associadas a um pacote de aplicativo virtual existente. Para executar essa tarefa, use o procedimento **"para modificar as propriedades associadas a um pacote de aplicativo virtual existente"** neste documento.

-   Adicionar um novo aplicativo a um pacote de aplicativo virtual existente. Para executar essa tarefa, use o procedimento **"para adicionar um novo aplicativo a um pacote de aplicativo virtual existente"** neste documento.

Você deve ter o sequenciador App-V instalado para modificar um pacote de aplicativo virtual. Para obter mais informações sobre como instalar o App-V Sequencer, consulte [como instalar o sequenciador (App-v 4,6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md).

**Para atualizar um aplicativo em um pacote de aplicativo virtual existente**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Na sequência App-V, clique em **modificar um pacote de aplicativo virtual existente**e, em seguida, clique em **Avançar**.

3.  Na página **selecionar tarefa** , clique em **Atualizar aplicativo em pacote existente**e, em seguida, clique em **Avançar**.

4.  Na página **selecionar pacote** , clique em **procurar** para localizar o pacote do aplicativo virtual que contém o aplicativo que você deseja atualizar e clique em **Avançar**.

5.  Na página **preparar computador** , examine os problemas que podem causar falha na atualização do aplicativo ou para que a atualização do aplicativo contenha dados desnecessários. É altamente recomendável que você resolva todos os possíveis problemas antes de continuar. Depois de corrigir os conflitos, para atualizar as informações exibidas, clique em **Atualizar**. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

    **Importante**  Se for necessário desativar o software de verificação de vírus, verifique se o computador está executando o sequenciador para garantir que nenhum arquivo indesejado ou mal-intencionado seja adicionado ao pacote.

     

6.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação de atualização para o aplicativo. Se a atualização não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

7.  Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, instale a atualização do aplicativo para que o sequenciador possa monitorar o processo de instalação. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar** e localize e execute os arquivos de instalação adicionais. Quando terminar a instalação, selecione **concluído a instalação**. Clique em **Avançar**.

    **Observação**  O sequenciador monitora todas as alterações e instalações no computador executando o sequenciador, incluindo as alterações e as instalações executadas fora do assistente de sequenciamento.

     

8.  Na página **relatório de instalação** , você pode revisar as informações sobre o aplicativo virtual que você acabou de atualizar. Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento. Depois de revisar as informações, clique em **Avançar**.

9.  Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

    **Observação**  Se você quiser interromper o carregamento de um aplicativo durante esta etapa, na caixa de diálogo **Iniciar aplicativo** , clique em **parar**e, em seguida, clique em uma das opções a seguir, **parar todos os aplicativos** ou **interromper o aplicativo somente**dependendo do que você deseja.

     

10. Na página **criar pacote** , para modificar o pacote sem salvá-lo, marque a caixa de seleção **continuar a modificar o pacote sem salvar usando o editor de pacote** . Quando você seleciona essa opção, o pacote no console do sequenciador é aberto para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

    Para salvar o pacote imediatamente, selecione o padrão **salvar o pacote agora**. Adicione **comentários** opcionais que serão associados ao pacote. Os comentários são úteis para identificar a versão e outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar** e especifique o novo local. O tamanho do pacote descompactado será exibido. Se o tamanho do pacote exceder 4 GB (não compactado) e você planeja transmitir o pacote para os computadores de destino, você deve selecionar **compactar pacote**e, em seguida, clicar em **criar**.

11. Na página **conclusão** , clique em **fechar** para fechar o assistente. O pacote agora está disponível no sequenciador.

**Para modificar as propriedades associadas a um pacote de aplicativo virtual existente**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Na sequência App-V, clique em **modificar um pacote de aplicativo virtual existente**e, em seguida, clique em **Avançar**.

3.  Na página **selecionar tarefa** , clique em **Editar pacote**e, em seguida, clique em **Avançar**.

4.  Na página **selecionar pacote** , clique em **procurar** para localizar o pacote do aplicativo virtual que contém as propriedades do aplicativo que você deseja modificar e, em seguida, clique em **Editar**.

5.  No console do sequenciador, você pode executar qualquer uma das seguintes tarefas:

    -   Exiba as propriedades do pacote.

    -   Exiba o histórico de alterações do pacote.

    -   Exibir arquivos de pacote associados.

    -   Editar configurações do registro.

    -   Revisar configurações de pacote adicionais (exceto propriedades de arquivos do sistema operacional).

    -   Crie um MSI (Windows Installer) associado.

    -   Modifique o arquivo OSD.

    -   Compactar e descompactar pacote.

    -   Adicionar associações de tipo de arquivo.

    -   Definir o estado virtualizado da chave do registro (substituir ou mesclar).

    -   Definir o estado da pasta virtualizada.

    -   Editar mapeamentos do sistema de arquivos virtual.

6.  Quando terminar de modificar as propriedades do pacote, clique **File**em  /  **salvar** arquivo para salvar o pacote.

**Para adicionar um novo aplicativo a um pacote de aplicativo virtual existente**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Na sequência App-V, clique em **modificar um pacote de aplicativo virtual existente**e, em seguida, clique em **Avançar**.

3.  Na página **selecionar tarefa** , clique em **Adicionar novo aplicativo**e, em seguida, clique em **Avançar**.

4.  Na página **selecionar pacote** , clique em **procurar** para localizar o pacote de aplicativo virtual ao qual você deseja adicionar o aplicativo e, em seguida, clique em **Avançar**.

5.  Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou para que a atualização contenha dados desnecessários. É altamente recomendável que você resolva todos os possíveis problemas antes de continuar. Depois de corrigir os conflitos, para atualizar as informações exibidas, clique em **Atualizar**. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

    **Importante**  Se for necessário desativar o software de verificação de vírus, verifique se o computador está executando o sequenciador para garantir que arquivos indesejados ou mal-intencionados possam ser adicionados ao pacote.

     

6.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo. Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

7.  Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, instale o aplicativo para que o sequenciador possa monitorar o processo de instalação. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar**, localize e execute os arquivos de instalação adicionais. Quando terminar a instalação, selecione **concluído a instalação**. Clique em **Avançar**. Na caixa de diálogo **Procurar pasta** , especifique o diretório primário onde o aplicativo será instalado. Isso deve ser um novo local para que você não substitua a versão existente do pacote de aplicativo virtual.

    **Observação**  Todas as alterações e instalações do computador que executam o sequenciador são monitoradas pelo sequenciador, incluindo as alterações e as instalações executadas fora do assistente de sequenciamento.

     

8.  Na página **configurar software** , execute a opção executar os programas contidos no pacote. Esta etapa ajuda a concluir todas as tarefas associadas ou tarefas de configuração que são necessárias para executar o aplicativo antes de você implantar e executar o pacote nos computadores de destino. Para executar todos os programas ao mesmo tempo, selecione pelo menos um programa e clique em **executar tudo**. Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**. Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos. Pode demorar vários minutos para que todos os programas sejam executados. Clique em **Avançar**.

9.  Na página **relatório de instalação** , você pode revisar as informações sobre o aplicativo virtual que você acabou de atualizar. Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento. Depois de revisar as informações, clique em **Avançar**.

10. Na página **Personalizar** , se você tiver concluído a instalação e a configuração do aplicativo virtual, selecione **parar agora** e pule para a etapa 14 deste procedimento. Se você quiser personalizar qualquer um dos itens na lista a seguir, clique em **Personalizar**.

    -   Edite as associações de tipo de arquivo associadas a um aplicativo.

    -   Prepare o pacote virtual para streaming. A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino.

    Clique em **Avançar**.

11. Na página **editar atalhos** , você pode, opcionalmente, configurar associações de tipo de arquivo (FTA) que serão associadas a vários aplicativos no pacote. Para criar um novo FTA, selecione e expanda o aplicativo que você deseja personalizar no painel esquerdo e clique em **Adicionar**. Na caixa de diálogo **Adicionar Associação de tipo de arquivo** , forneça as informações necessárias para o novo FTA. Para revisar as informações de atalho associadas a um aplicativo, sob o aplicativo, marque a caixa de seleção **atalhos** e, no painel **local** , você pode revisar as informações do arquivo de ícone. Para editar um FTA existente, clique em **Editar**. Para remover um FTA, selecione FTA e, em seguida, clique em **remover**. Clique em **Avançar**.

12. Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

    **Observação**  Se você quiser interromper o carregamento de um aplicativo durante esta etapa, na caixa de diálogo **Iniciar aplicativo** , clique em **parar** e marque a caixa de seleção **parar todos os aplicativos** ou **parar este aplicativo apenas** , dependendo do que você deseja.

     

13. Na página **criar pacote** , marque a caixa de seleção **continuar a modificar pacote sem salvar usando o editor de pacote** para modificar o pacote sem salvá-lo. Quando você seleciona essa opção, o pacote no console do sequenciador é aberto para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

    Selecione o padrão **salvar o pacote agora**para salvar o pacote imediatamente. Adicione **comentários** opcionais que serão associados ao pacote. Os comentários são úteis para identificar a versão e outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar** e especifique o novo local. O tamanho do pacote descompactado será exibido. Se o tamanho do pacote exceder 4 GB (não compactado) e você planeja transmitir o pacote para computadores de destino, selecione **compactar pacote**. Clique em **Criar**.

14. Na página **Conclusão**, clique em **Fechar**. O pacote agora está disponível no sequenciador.

## Tópicos relacionados


[Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





