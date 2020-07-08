---
title: Como sequenciar um novo complemento ou plug-in de aplicativo (App-V 4.6 SP1)
description: Como sequenciar um novo complemento ou plug-in de aplicativo (App-V 4.6 SP1)
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796979"
---
# Como sequenciar um novo complemento ou plug-in de aplicativo (App-V 4.6 SP1)


Use o procedimento a seguir para criar um novo pacote de aplicativo virtual de plug-in ou de suplemento usando o sequenciador do Application Virtualization (App-V). Um aplicativo de complemento ou de plug-in é um aplicativo que estende a funcionalidade de um aplicativo, por exemplo, um plug-in para o Microsoft Excel. Para obter mais informações sobre os tipos de aplicativos que você pode sequenciar, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

**Importante**  
Antes de executar o procedimento a seguir, instale o aplicativo pai localmente no computador que está executando o sequenciador. Por exemplo, se você estiver sequenciando um plug-in do Microsoft Excel, instale o Microsoft Excel localmente no computador que está executando o sequenciador. Além disso, instale o aplicativo pai no mesmo diretório em que o aplicativo está instalado nos computadores de destino. Se o plug-in ou complemento for usado com um pacote de aplicativo virtual existente, instale o aplicativo na mesma unidade de aplicativo virtual que foi usada quando você criou o pacote de aplicativo virtual pai.



Você também pode usar um pacote de aplicativo virtual existente como o aplicativo pai. Para usar um pacote de aplicativo virtual existente, use o procedimento a seguir antes de sequenciar o novo complemento ou plug-in.

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Para expandir um pacote existente para o computador que executa o sequenciador, clique em **ferramentas**  /  **expanda pacote para o sistema local**.

3.  Procure e selecione o pacote (arquivo **. sprj** ) que você deseja expandir e, em seguida, clique em **abrir**. Continue com o procedimento a seguir.

**Para sequenciar um novo aplicativo de complemento ou de plug-in**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**. Para criar o pacote, selecione **criar pacote (padrão)** e clique em **Avançar**.

3.  Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou para que o pacote contenha dados desnecessários. É altamente recomendável que você resolva todos os possíveis problemas antes de continuar. Depois de corrigir os conflitos, para atualizar as informações exibidas, clique em **Atualizar**. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

    **Importante**  
    Se for necessário desativar o software de verificação de vírus, verifique se o computador está executando o sequenciador para garantir que não seja possível adicionar arquivos indesejados ou mal-intencionados ao pacote.



4.  Na página **tipo de aplicativo** , selecione **complemento ou plug-in**e clique em **Avançar**.

    Para obter mais informações sobre os tipos de aplicativos que você pode sequenciar, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação para o complemento ou plug-in. Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

6.  Na página **selecionar principal** , clique em **procurar** e especifique o aplicativo pai.

    **Importante**  
    Se o aplicativo pai ao qual o complemento ou plug-in que você está instalando não tiver sido instalado localmente, pare aqui e instale o aplicativo no computador que executa o sequenciador. Por exemplo, o arquivo de programa **Excel.exe** deve ser instalado localmente para um plug-in do Microsoft Excel.



~~~
Click **Next**.
~~~

7. Na página **nome do pacote** , especifique um nome que será associado ao pacote. Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote. O nome do pacote também será exibido no console de gerenciamento do App-V. O **local de instalação** exibe o caminho do aplicativo de virtualização onde o aplicativo será instalado. Para editar esse local, selecione **Editar (avançado)**.

   **Importante**  
   Editar o caminho de virtualização do aplicativo é uma tarefa de configuração avançada. Você deve entender completamente as implicações de alterar o caminho. Para a maioria dos aplicativos, recomendamos o caminho padrão.



~~~
Click **Next**.
~~~

8. Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, instale o plug-in ou o aplicativo de suplemento para que o sequenciador possa monitorar o processo de instalação. Execute a instalação usando o processo de instalação do aplicativo. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar** e localize e execute os arquivos de instalação adicionais. Quando tiver terminado a instalação, selecione concluído a **instalação**e, em seguida, clique em **Avançar**.

9. Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativo virtual que você acabou de sequenciar. Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento. Depois de revisar as informações, clique em **Avançar**.

10. Na página **Personalizar** , se você tiver concluído a instalação e a configuração do aplicativo virtual, selecione **parar agora** e pule para a etapa 14 deste procedimento. Se você quiser personalizar qualquer um dos itens na lista a seguir, selecione **Personalizar**.

    -   Edite as associações de tipo de arquivo associadas a um aplicativo.

    -   Prepare o pacote virtual para streaming. A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino.

    -   Especifique os sistemas operacionais que podem executar este pacote.

    Clique em **Avançar**.

11. Na página **editar atalhos** , você pode, opcionalmente, configurar associações de tipo de arquivo (FTA) que serão associadas a vários aplicativos no pacote. Para criar um novo FTA, no painel esquerdo, selecione e expanda o aplicativo que você deseja personalizar e clique em **Adicionar**. Na caixa de diálogo **Adicionar Associação de tipo de arquivo** , forneça as informações necessárias para o novo FTA. No aplicativo, selecione **atalhos** para examinar as informações de atalho associadas a um aplicativo. No painel **local** , você pode revisar as informações do arquivo de ícone. Para editar um FTA existente, clique em **Editar**. Para remover um FTA, selecione FTA e, em seguida, clique em **remover**. Clique em **Avançar**.

12. Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

   **Observação**  
   Se você quiser interromper o carregamento de um aplicativo durante esta etapa, na caixa de diálogo **Iniciar aplicativo** , clique em **parar** e marque uma das caixas de seleção, **parar todos os aplicativos** ou **interromper o aplicativo somente**.



13. Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote. Para habilitar todos os sistemas operacionais com suporte em seu ambiente para executar este pacote, marque a caixa de seleção **permitir que este pacote seja executado em qualquer sistema operacional** . Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, marque a caixa de seleção **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e, em seguida, selecione os sistemas operacionais que podem executar este pacote. Clique em **Avançar**.

14. Na página **criar pacote** , para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvar usando a caixa de seleção do editor de pacote** . Selecionar essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

   Para salvar o pacote imediatamente, selecione o padrão **salvar o pacote agora**. Opcionalmente, selecione **comentários** para adicionar comentários que serão associados ao pacote. Os comentários são úteis para identificar a versão e outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar** e especifique o novo local. O tamanho do pacote descompactado será exibido. Se o tamanho do pacote exceder 4 GB (não compactado) e você planeja transmitir o pacote para computadores de destino, selecione **compactar pacote**. Clique em **Criar**.

15. Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativos virtual bem-sucedido** , clique em **Fechar**. As informações exibidas no painel **relatório de pacote de aplicativo virtual bem-sucedido** também estão disponíveis no diretório especificado na etapa 14 deste procedimento, em um arquivo denominado **Reports.xml**.

   O pacote agora está disponível no sequenciador. Clique em **Editar \ [nome do pacote \]** para editar as propriedades do pacote. Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

   **Importante**  
   Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.



## Tópicos relacionados


[Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









