---
title: Como sequenciar um novo aplicativo padrão (App-V 4.6 SP1)
description: Como sequenciar um novo aplicativo padrão (App-V 4.6 SP1)
author: dansimp
ms.assetid: c4a2eb33-def8-4535-b93a-3d2de21ce29f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47c93b4880d0095c87a98292fda743acc1659e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796970"
---
# Como sequenciar um novo aplicativo padrão (App-V 4.6 SP1)


Use o procedimento a seguir para criar um novo pacote de aplicativo virtual padrão usando o sequenciador Application Virtualization (App-V). Esse procedimento se aplica à maioria dos aplicativos que você sequênciau. Para obter mais informações sobre os tipos de aplicativos que você pode sequenciar, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md). Você deve executar o sequenciador (**SFTSequencer.exe**) usando uma conta com privilégios de administrador, devido às alterações que o sequenciador faz ao sistema local. Essas alterações podem incluir a gravação de arquivos no diretório de **arquivos de c:\\Arquivos** , o que torna o registro alterado, o início e a interrupção de serviços, a atualização dos descritores de segurança para arquivos e a alteração de permissões.

**Importante**  
Durante o sequenciamento, se o computador executando o sequenciador estiver executando o Windows Vista ou o Windows 7 e uma reinicialização for iniciada fora do ambiente virtual, por exemplo, **Iniciar**o desligamento  /  **Shut Down**, você deverá clicar em **Cancelar** quando solicitado a fechar o programa que impede que o Windows Vista ou Windows seja desligado. Se você clicar em **Forçar desligamento**, a criação do pacote falhará. Quando você clica em **Cancelar**, o sequenciador registra a reinicialização com êxito enquanto o aplicativo está sendo sequenciado.



**Observação**  
Não há suporte para a execução do sequenciador App-V no modo de segurança.



**Para sequenciar um novo aplicativo padrão**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**. Para criar o pacote, selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.

3.  Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou para que o pacote contenha dados desnecessários. É altamente recomendável que você resolva todos os possíveis problemas antes de continuar. Depois de corrigir os conflitos, para atualizar as informações exibidas, clique em **Atualizar**. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

    **Importante**  
    Se for necessário desativar o software de verificação de vírus, verifique se o computador está executando o sequenciador para garantir que não seja possível adicionar arquivos indesejados ou mal-intencionados ao pacote.



4.  Na página **tipo de aplicativo** , clique em **aplicativo padrão (padrão)** e, em seguida, clique em **Avançar**.

    Para obter mais informações sobre os tipos de aplicativos que você pode sequenciar, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo. Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **executar uma instalação personalizada** e clique em **Avançar**.

6.  Na página **nome do pacote** , especifique um nome que será associado ao pacote. O nome ajuda a identificar a finalidade e a versão do aplicativo que são adicionados ao pacote. O nome do pacote também é exibido no console de gerenciamento do App-V. O **diretório de aplicativos virtual primário** exibe o caminho do aplicativo de virtualização onde o aplicativo será instalado nos computadores de destino. Para editar esse local, selecione **Editar (avançado)**.

    **Importante**  
    Editar o caminho de virtualização do aplicativo é uma tarefa de configuração avançada. Você deve entender completamente as implicações de alterar o caminho. Para a maioria dos aplicativos, é recomendável o caminho padrão.



~~~
Click **Next**.
~~~

7. Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, instale o aplicativo para que o sequenciador possa monitorar o processo de instalação. Execute a instalação usando o processo de instalação do aplicativo. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar** para localizar e executar os arquivos de instalação adicionais. Quando terminar a instalação, selecione **concluído a instalação**. Clique em **Avançar**.

8. Na página de **instalação** , aguarde enquanto o sequenciador configura o pacote de aplicativo virtual.

9. Na página **configurar software** , execute a opção executar os programas contidos no pacote. Esta etapa ajuda a concluir todas as tarefas associadas ou tarefas de configuração que são necessárias para executar o aplicativo antes de você implantar e executar o pacote nos computadores de destino. Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**. Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**. Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos. Pode demorar vários minutos para que todos os programas sejam executados. Clique em **Avançar**.

10. Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativo virtual que você acabou de sequenciar. Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento. Depois de revisar as informações, clique em **Avançar**.

11. Na página **Personalizar** , se você tiver concluído a instalação e a configuração do aplicativo virtual, selecione **parar agora** e pule para a etapa 15 deste procedimento. Se você quiser personalizar qualquer um dos itens na lista a seguir, selecione **Personalizar**.

    -   Edite as associações de tipo de arquivo e os ícones associados a um aplicativo.

    -   Prepare o pacote virtual para streaming. A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino.

    -   Especifique os sistemas operacionais que podem executar este pacote.

    Clique em **Avançar**.

12. Na página **editar atalhos** , você pode, opcionalmente, configurar associações de tipo de arquivo (FTA) e locais de atalho que serão associados a vários aplicativos no pacote. Para criar um novo FTA, no painel esquerdo, selecione e expanda o aplicativo que você deseja personalizar e clique em **Adicionar**. Na caixa de diálogo **Adicionar Associação de tipo de arquivo** , forneça as informações necessárias para o novo FTA. Para revisar as informações de atalho associadas a um aplicativo, no aplicativo, selecione **atalhos**e, no painel **local** , você pode editar as informações do arquivo de ícone. Para editar um FTA existente, clique em **Editar**. Para remover um FTA, selecione FTA e, em seguida, clique em **remover**. Clique em **Avançar**.

13. Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

   **Observação**  
   Se você quiser interromper o carregamento de um aplicativo durante esta etapa, na caixa de diálogo **Iniciar aplicativo** , clique em **parar**e marque uma das caixas de seleção, **parar todos os aplicativos** ou **interromper o aplicativo somente**dependendo do que você deseja.



14. Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote. Para habilitar todos os sistemas operacionais com suporte em seu ambiente para executar este pacote, selecione **permitir que este pacote seja executado em qualquer sistema operacional**. Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, selecione **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e especifique os sistemas operacionais que podem executar este pacote. Clique em **Avançar**.

   **Importante**  
   Os sistemas operacionais especificados durante esta etapa refletem os sistemas operacionais em computadores de destino que estão habilitados para executar o pacote. Você deve garantir que os sistemas operacionais especificados são suportados pelo aplicativo que você está sequenciando.



15. Na página **criar pacote** , para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvá-lo usando o editor de pacote**. Selecionar essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

   Para salvar o pacote imediatamente, selecione o padrão **salvar o pacote agora**. Adicione **comentários** opcionais que serão associados ao pacote. Os comentários são úteis para identificar a versão e outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar** e especifique o novo local. O tamanho do pacote descompactado será exibido. Se o tamanho do pacote exceder 4 GB (não compactado) e você planeja transmitir o pacote para computadores de destino, selecione **compactar pacote**. Clique em **Criar**.

16. Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativo virtual** , clique em **Fechar**. As informações exibidas no painel **relatório do pacote de aplicativo virtual** também estão disponíveis no diretório especificado na etapa 15 deste procedimento, em um arquivo denominado **Report.xml**.

    O pacote agora está disponível no sequenciador. Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**. Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

    **Importante**  
    Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.



## Tópicos relacionados


[Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









