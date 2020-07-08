---
title: Como sequenciar um novo Aplicativo middleware (App-V 4.6 SP1)
description: Como sequenciar um novo Aplicativo middleware (App-V 4.6 SP1)
author: dansimp
ms.assetid: 304045c2-5e5e-4c91-b59e-a91fdf2500fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b26559b8f5c451d01fefe899e96a83dd388b8140
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796972"
---
# Como sequenciar um novo Aplicativo middleware (App-V 4.6 SP1)


Use o procedimento a seguir para criar um novo pacote de aplicativo virtual middleware usando o sequenciador Application Virtualization (App-V). Um aplicativo de middleware é um software que conecta módulos de software ou aplicativos. Para obter mais informações sobre os tipos de aplicativos que você pode sequenciar, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

Use esse tipo de pacote usando a composição do pacote dinâmico em App-V. A composição do pacote dinâmico permite definir um pacote de aplicativo virtual como dependente de outro pacote de aplicativo virtual. A dependência permite que o aplicativo interaja com o middleware ou plug-in no ambiente virtual, onde geralmente essa interação é impedida. Isso é útil porque um pacote de aplicativo secundário pode ser usado com vários outros aplicativos principais, o que permite que cada aplicativo primário faça referência ao mesmo pacote secundário. Para obter mais informações sobre como usar a composição do pacote dinâmico, consulte [como usar a composição do pacote dinâmico](https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) na biblioteca técnica da Microsoft ( https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) .

**Importante**  
Durante o sequenciamento, se o computador que executa o sequenciador App-V estiver executando o Windows Vista ou o Windows 7 e uma reinicialização for iniciada fora do ambiente virtual, por exemplo, **Iniciar**o desligamento  /  **Shut Down**, você deverá clicar em **Cancelar** quando solicitado a fechar o programa que impede o desligamento do Windows. Se você clicar em **Forçar desligamento**, a criação do pacote falhará. Quando você clica em **Cancelar**, o sequenciador App-V registra a reinicialização com êxito enquanto o aplicativo está sendo sequenciado.



**Para sequenciar um novo aplicativo de middleware**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer Virtualization**.

2.  Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**. Para criar o pacote, selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.

3.  Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou para que o pacote contenha dados desnecessários. É altamente recomendável que você resolva todos os possíveis problemas antes de continuar. Depois de corrigir os conflitos, para atualizar as informações exibidas, clique em **Atualizar**. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

    **Importante**  
    Se for necessário desativar o software de verificação de vírus, você deve verificar o computador que executa o App-VSequencer para garantir que arquivos indesejados ou mal-intencionados possam ser adicionados ao pacote.



4.  Na página **tipo de aplicativo** , selecione **middlewaree**, em seguida, clique em **Avançar**.

    Para obter mais informações sobre os tipos de aplicativos que você pode sequenciar, consulte [como determinar qual tipo de aplicativo sequenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo. Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

6.  Na página **nome do pacote** , especifique um nome que será associado ao pacote. O nome ajuda a identificar a finalidade e a versão do aplicativo que serão adicionados ao pacote. O nome do pacote também é exibido no console de gerenciamento do App-V. O **local de instalação** exibe o caminho do aplicativo de virtualização onde o aplicativo será instalado. Para editar esse local, selecione **Editar (avançado)**.

    **Importante**  
    Editar o caminho de virtualização do aplicativo é uma tarefa de configuração avançada. Você deve entender completamente as implicações de alterar o caminho. Para a maioria dos aplicativos, recomendamos o caminho padrão.



~~~
Click **Next**.
~~~

7. Na página de **instalação** , quando o instalador do aplicativo de sequenciador e middleware estiver pronto, instale o aplicativo para que o sequenciador possa monitorar o processo de instalação. Execute a instalação usando o processo de instalação do aplicativo. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar**, para localizar e executar os arquivos de instalação adicionais. Quando terminar a instalação, marque a caixa de seleção **já terminei de instalar** e clique em **Avançar**.

8. Na página de **instalação** , aguarde enquanto o sequenciador configura o pacote de aplicativo virtual.

9. Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativo virtual que você acabou de sequenciar. Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento. Depois de revisar as informações, clique em **Avançar**.

10. Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote. Para habilitar todos os sistemas operacionais com suporte em seu ambiente para executar este pacote, marque a caixa de seleção **permitir que este pacote seja executado em qualquer sistema operacional** . Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, marque a caixa de seleção **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e selecione os sistemas operacionais que podem executar este pacote. Clique em **Avançar**.

11. Na página **criar pacote** , para modificar o pacote sem salvá-lo, marque a caixa de seleção **continuar a modificar o pacote sem salvar usando o editor de pacote** . Selecionar essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

   Para salvar o pacote imediatamente, selecione o padrão, a caixa de seleção **salvar o pacote agora** . Adicione comentários opcionais na caixa **comentários** que serão associados ao pacote. Os comentários são úteis para identificar a versão e outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar**e, em seguida, especifique o novo local. O tamanho do pacote descompactado será exibido. Se o tamanho do pacote exceder 4 GB (não compactado) e você planeja transmitir o pacote para computadores de destino, selecione **compactar pacote**. Clique em **Criar**.

12. Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativo virtual** , clique em **Fechar**. As informações exibidas no painel **relatório do pacote de aplicativo virtual** também estão disponíveis no diretório especificado na etapa 11 deste procedimento, em um arquivo denominado **Report.xml**.

   O pacote agora está disponível no sequenciador. Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**. Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

   **Importante**  
   Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.



## Tópicos relacionados


[Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









