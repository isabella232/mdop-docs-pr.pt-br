---
title: Como sequenciar um novo aplicativo com o App-V 5.0
description: Como sequenciar um novo aplicativo com o App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796320"
---
# Como sequenciar um novo aplicativo com o App-V 5.0


**Para revisar ou fazer antes de iniciar o sequenciamento**

1.  Determine o tipo de pacote de aplicativo virtualizado que você deseja criar:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de aplicativo</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Standard</p></td>
    <td align="left"><p>Cria um pacote que contém um aplicativo ou um pacote de aplicativos. Esta é a opção preferida para a maioria dos tipos de aplicativo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Complemento ou plug-in</p></td>
    <td align="left"><p>Cria um pacote que estende a funcionalidade de um aplicativo padrão, por exemplo, um plug-in para o Microsoft Excel. Além disso, você pode usar plug-ins para aplicativos instalados nativamente ou para outro pacote vinculado por meio de grupos de conexão.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Middleware</p></td>
    <td align="left"><p>Cria um pacote que é necessário para um aplicativo padrão, por exemplo, Java. Os pacotes middleware são usados para a vinculação a outros pacotes usando grupos de conexão.</p></td>
    </tr>
    </tbody>
    </table>



2.  Copie todos os arquivos de instalação necessários para o computador que está executando o sequenciador.

3.  Crie uma imagem de backup do seu ambiente virtual antes de sequenciar um aplicativo e, em seguida, reverta para essa imagem a cada vez após concluir o sequenciamento de um aplicativo.

4.  Revise os seguintes itens:

    -   Se um instalador do aplicativo alterar o acesso de segurança para um arquivo ou diretório novo ou existente, essas alterações não serão capturadas no pacote.

    -   Se demarcadores curtos forem desabilitados para o volume de destino do pacote virtualizado, você também deverá sequenciar o pacote para um volume que tenha sido criado e ainda ter caminhos curtos desativados. Ele não pode ser o volume do sistema.

    -   A partir do App-V 5,0 SP3, o diretório de aplicativos virtual primário (PVAD) está oculto, mas você pode ativá-lo novamente. Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).

**Para sequenciar um novo aplicativo padrão**

1.  No computador que executa o sequenciador, clique em **todos os programas**e, em seguida, clique em **Microsoft Application Virtualization**e, em seguida, clique em **Microsoft Application Virtualization Sequencer**.

2.  No sequenciador, clique em **criar um novo pacote de aplicativo virtual**. Selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.

3.  Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou fazer com que o pacote contenha dados desnecessários. Você deve resolver todos os possíveis problemas antes de continuar. Depois de fazer qualquer correção, clique em **Atualizar** para exibir as informações atualizadas. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

    **Importante**  
    Se for necessário desativar o software de verificação de vírus, você deve primeiro verificar o computador que executa o sequenciador para garantir que não seja possível adicionar arquivos indesejados ou mal-intencionados ao pacote.



4.  Na página **tipo de aplicativo** , clique na caixa de seleção **aplicativo padrão (padrão)** e, em seguida, clique em **Avançar**.

5.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo.

    **Observação**  
    Se o instalador do aplicativo especificado modificar o acesso de segurança a um arquivo ou diretório, existente ou novo, as alterações associadas não serão capturadas no pacote.



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. Na página **nome do pacote** , digite um nome que será associado ao pacote. Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote. O nome do pacote é exibido no console de gerenciamento do App-V 5,0.

   O **diretório de aplicativos virtual primário** exibe o caminho onde o aplicativo será instalado nos computadores de destino. Para especificar esse local, selecione **procurar**.

   **Observação**  
   A partir do App-V 5,0 SP3, o diretório de aplicativos virtual primário (PVAD) está oculto, mas você pode ativá-lo novamente. Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, você poderá continuar a instalar o aplicativo para que o sequenciador possa monitorar o processo de instalação.

   **Importante**  
   Você sempre deve instalar aplicativos em um local seguro e verificar se nenhum outro usuário está conectado ao computador executando o sequenciador durante o monitoramento.



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. Na página **instalação** , aguarde enquanto o sequenciador configura o pacote de aplicativo virtualizado.

9. Na página **configurar software** , execute a opção executar os programas contidos no pacote. Esta etapa permite concluir todas as tarefas necessárias de licença ou configuração antes de você implantar e executar o pacote em computadores de destino. Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**. Para executar programas específicos, selecione o programa ou programas e, em seguida, clique em **executar selecionado**. Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos. Talvez seja necessário aguardar alguns minutos para que todos os programas sejam executados.

   **Observação**  
   Para executar as tarefas de primeira utilização para qualquer aplicativo que não esteja disponível na lista, abra o aplicativo. As informações associadas serão capturadas durante esta etapa.



~~~
Click **Next**.
~~~

10. Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativos virtualizados que você acabou de sequenciar. Em **informações adicionais**, clique duas vezes em um evento para obter informações mais detalhadas. Para continuar, clique em **Avançar**.

11. A página **Personalizar** será exibida. Se você tiver terminado de instalar e configurar o aplicativo virtual, selecione **parar agora** e pule para a etapa 14 deste procedimento. Para executar qualquer uma das seguintes personalizações, selecione **Personalizar**.

    -   Prepare o pacote virtual para streaming. A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino.

    -   Especifique os sistemas operacionais que podem executar este pacote.

    Clique em **Avançar**.

12. Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

   **Observação**  
   Se você não abrir nenhum aplicativo durante esta etapa, o método de streaming padrão será a entrega de streaming sob demanda. Isso significa que os aplicativos serão baixados por bit até que possam ser abertos e, em seguida, dependendo de como o carregamento em segundo plano está configurado, carregará o restante do aplicativo.



13. Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote. Para permitir que todos os sistemas operacionais com suporte em seu ambiente executem este pacote, selecione **permitir que este pacote seja executado em qualquer sistema operacional**. Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, selecione **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e selecione os sistemas operacionais que podem executar este pacote. Clique em **Avançar**.

   **Importante**  
   Verifique se os sistemas operacionais especificados aqui são suportados pelo aplicativo que você está sequenciando.



14. A página **criar pacote** será exibida. Para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvá-lo usando o editor de pacote**. Essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

   Para salvar o pacote imediatamente, selecione **salvar o pacote agora** (padrão). Adicione **comentários** opcionais a serem associados ao pacote. Os comentários são úteis para identificar a versão do programa e outras informações sobre o pacote.

   **Importante**  
   O sistema não oferece suporte a caracteres que não podem ser impressos em **comentários** e **descrições**.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. A página de **conclusão** será exibida. Examine as informações no painel **relatório do pacote do aplicativo virtual** conforme necessário e clique em **fechar**. Essas informações também estão disponíveis no arquivo **Report.xml** localizado no diretório em que o pacote foi criado.

   O pacote agora está disponível no sequenciador.

   **Importante**  
   Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.



**Para sequenciar um complemento ou aplicativo de plug-in**

1.  

    **Observação**  
    Antes de executar o procedimento a seguir, instale o aplicativo pai localmente no computador que está executando o sequenciador. Ou, se você tiver o aplicativo pai virtualizado, poderá seguir as etapas no complemento ou no fluxo de trabalho de plug-in para descompactar o aplicativo pai no computador.

    Por exemplo, se você estiver sequenciando um plug-in do Microsoft Excel, instale o Microsoft Excel localmente no computador que está executando o sequenciador. Além disso, instale o aplicativo pai no mesmo diretório em que o aplicativo está instalado nos computadores de destino. Se o plug-in ou complemento for usado com um pacote de aplicativo virtual existente, instale o aplicativo na mesma unidade de aplicativo virtual que foi usada quando você criou o pacote de aplicativo virtual pai.



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. *<strong><em>No sequenciador, clique em * </em> criar um novo pacote de aplicativo virtual </strong> . Selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.

3. Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou fazer com que o pacote contenha dados desnecessários. Você deve resolver todos os possíveis problemas antes de continuar. Depois de fazer qualquer correção, clique em **Atualizar** para exibir as informações atualizadas. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

   **Importante**  
   Se for necessário desativar o software de verificação de vírus, você deve primeiro verificar o computador que executa o sequenciador para garantir que não seja possível adicionar arquivos indesejados ou mal-intencionados ao pacote.



4. Na página **tipo de aplicativo** , selecione **complemento ou plug-in**e clique em **Avançar**.

5. Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação para o complemento ou plug-in. Se o complemento ou o plug-in não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

6. Na página **instalar primário** , verifique se o aplicativo principal está instalado no computador que executa o sequenciador. Você também pode expandir um pacote existente que tenha sido salvo localmente no computador que executa o sequenciador. Para fazer isso, clique em **expandir pacote**e, em seguida, selecione o pacote. Depois de expandir ou instalar o programa pai, selecione **eu instalei o programa pai primário**.

   Clique em **Avançar**.

7. Na página **nome do pacote** , digite um nome que será associado ao pacote. Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote. O nome do pacote será exibido no console de gerenciamento do App-V 5,0. O **diretório de aplicativos virtual primário** exibe o caminho onde o aplicativo será instalado. Para especificar esse local, digite o caminho ou clique em **procurar**.

   **Observação**  
   A partir do App-V 5,0 SP3, o diretório de aplicativos virtual primário (PVAD) está oculto, mas você pode ativá-lo novamente. Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).



~~~
Click **Next**.
~~~

8. Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estão prontos, você pode prosseguir para instalar o plug-in ou o aplicativo de suplemento para que o sequenciador possa monitorar o processo de instalação. Use o processo de instalação do aplicativo para executar a instalação. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar** e localize e execute os arquivos de instalação adicionais. Quando tiver terminado a instalação, selecione concluído a **instalação**e, em seguida, clique em **Avançar**.

9. Na página **relatório de instalação** , você pode examinar informações sobre o pacote de aplicativo virtual que você acabou de sequenciar. Para obter uma explicação mais detalhada sobre as informações exibidas em **informações adicionais**, clique duas vezes no evento. Depois de revisar as informações, clique em **Avançar**.

10. A página **Personalizar** será exibida. Se você tiver terminado de instalar e configurar o aplicativo virtual, selecione **parar agora** e pule para a etapa 12 deste procedimento. Para executar qualquer uma das seguintes personalizações, selecione **Personalizar**.

    -   Otimize como o pacote será executado em uma rede lenta ou não confiável.

    -   Especifique os sistemas operacionais que podem executar este pacote.

    Clique em **Avançar**.

11. Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino em redes de alta latência. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos. Você também pode configurar o pacote para ser totalmente baixado antes de abrir marcando a caixa de seleção **forçar aplicativos a serem baixados** . Clique em **Avançar**.

   **Observação**  
   Se necessário, você pode interromper o carregamento de um aplicativo durante esta etapa. Na caixa de diálogo **Iniciar aplicativo** , clique em **parar** e marque uma das caixas de seleção: **interromper todos os aplicativos** ou **interromper somente este aplicativo**.



12. Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote. Para permitir que todos os sistemas operacionais com suporte em seu ambiente executem este pacote, marque a caixa de seleção **permitir que este pacote seja executado em qualquer sistema operacional** . Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, marque a caixa de seleção **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e, em seguida, selecione os sistemas operacionais que podem executar este pacote. Clique em **Avançar**.

13. A página **criar pacote** será exibida. Para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvar usando a caixa de seleção do editor de pacote** . Essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

   Para salvar o pacote imediatamente, selecione **salvar o pacote agora**. Opcionalmente, adicione uma **Descrição** que será associada ao pacote. Descrições são úteis para identificar a versão e outras informações sobre o pacote.

   **Importante**  
   O sistema não oferece suporte a caracteres que não podem ser impressos em comentários e descrições.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**Para sequenciar um aplicativo de middleware**

1. No computador que executa o sequenciador, clique em **todos os programas**e, em seguida, clique em **Microsoft Application Virtualization**e, em seguida, clique em **Microsoft Application Virtualization Sequencer**.

2. *<strong><em>No sequenciador, clique em * </em> criar um novo pacote de aplicativo virtual </strong> . Selecione **criar pacote (padrão)** e, em seguida, clique em **Avançar**.

3. Na página **preparar computador** , examine os problemas que podem causar falha na criação do pacote ou fazer com que o pacote contenha dados desnecessários. Você deve resolver todos os possíveis problemas antes de continuar. Depois de fazer qualquer correção, clique em **Atualizar** para exibir as informações atualizadas. Depois de ter resolvido todos os possíveis problemas, clique em **Avançar**.

   **Importante**  
   Se for necessário desativar o software de verificação de vírus, você deve primeiro examinar o computador que executa o sequenciador do App-V 5,0 para garantir que arquivos indesejados ou mal-intencionados possam ser adicionados ao pacote.



4. Na página **tipo de aplicativo** , selecione **middlewaree**, em seguida, clique em **Avançar**.

5. Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo. Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

6. Na página **nome do pacote** , digite um nome que será associado ao pacote. Use um nome que ajude a identificar a finalidade e a versão do aplicativo que será adicionada ao pacote. O nome do pacote é exibido no console de gerenciamento do App-V 5,0. O **diretório de aplicativos virtual primário** exibe o caminho onde o aplicativo será instalado. Para especificar esse local, digite o caminho ou clique em **procurar**.

   Clique em **Avançar**.

7. Na página de **instalação** , quando o instalador do aplicativo de sequenciador e middleware estiver pronto, você pode continuar a instalar o aplicativo para que o sequenciador possa monitorar o processo de instalação. Use o processo de instalação do aplicativo para executar a instalação. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar**, para localizar e executar os arquivos de instalação adicionais. Quando terminar a instalação, marque a caixa de seleção **já terminei de instalar** e clique em **Avançar**.

8. Na página de **instalação** , aguarde enquanto o sequenciador configura o pacote de aplicativo virtual.

9. Na página **relatório de instalação** , você pode revisar as informações sobre o pacote de aplicativo virtual que você acabou de sequenciar. Em **informações adicionais**, clique duas vezes em um evento para obter informações mais detalhadas. Para continuar, clique em **Avançar**.

10. Na página **sistema** operacional de destino, especifique os sistemas operacionais que podem executar este pacote. Para habilitar todos os sistemas operacionais com suporte em seu ambiente para executar este pacote, marque a caixa de seleção **permitir que este pacote seja executado em qualquer sistema operacional** . Para configurar esse pacote para ser executado somente em sistemas operacionais específicos, marque a caixa de seleção **permitir que este pacote seja executado somente nos seguintes sistemas operacionais** e selecione os sistemas operacionais que podem executar este pacote. Clique em **Avançar**.

11. Na página **criar pacote** é exibida. Para modificar o pacote sem salvá-lo, selecione **continuar para modificar o pacote sem salvá-lo usando o editor de pacote**. Essa opção abre o pacote no console do sequenciador para que você possa modificar o pacote antes de salvá-lo. Clique em **Avançar**.

    Para salvar o pacote imediatamente, selecione **salvar o pacote agora**. Opcionalmente, adicione uma **Descrição** para estar associado ao pacote. Descrições são úteis para identificar a versão do programa e outras informações sobre o pacote.

    **Importante**  
    O sistema não oferece suporte a caracteres que não podem ser impressos em comentários e descrições.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. A página de **conclusão** será exibida. Examine as informações no painel **relatório do pacote do aplicativo virtual** conforme necessário e clique em **fechar**. Essas informações também estão disponíveis no arquivo **Report.xml** localizado no diretório especificado na etapa 11 deste procedimento.

   O pacote agora está disponível no sequenciador. Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**.

   **Importante**  
   Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)









