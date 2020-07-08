---
title: Como modificar um pacote de aplicativo virtual existente
description: Como modificar um pacote de aplicativo virtual existente
author: dansimp
ms.assetid: 6cdeec00-e4fe-4210-b4c7-6ca1ac643ddd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 95963610c8b725412f6d516ee22b1c2f4e186df6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796356"
---
# Como modificar um pacote de aplicativo virtual existente


Este tópico explica como:

-   [Atualizar um aplicativo em um pacote de aplicativo virtual existente](#bkmk-update-app-in-pkg)

-   [Modificar as propriedades associadas a um pacote de aplicativo virtual existente](#bkmk-chg-props-in-pkg)

-   [Adicionar um novo aplicativo a um pacote de aplicativo virtual existente](#bkmk-add-app-to-pkg)

**Antes de atualizar um pacote:**

-   Verifique se você instalou o sequenciador do Microsoft Application Virtualization (App-V), que é necessário para modificar um pacote de aplicativo virtual. Para instalar o sequenciador do App-V, consulte [como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md).

-   Salve o arquivo. AppV em um local seguro e sempre confie na fonte antes de tentar abrir o pacote para edição.

-   A seção autoridade de gerenciamento é removida erroneamente do arquivo de configuração de implantação quando você atualiza um pacote. Antes de iniciar a atualização, copie a seção Gerenciamento de autoridade do arquivo de configuração de implantação existente e cole a seção copiada no novo arquivo de configuração após a conclusão da conversão.

-   Se você clicar em **modificar um pacote de aplicativo virtual existente** no sequenciador para editar um pacote, mas não fizer alterações e fechar o pacote, o comportamento de streaming do pacote será alterado. O bloco de recursos principal é removido do arquivo StreamMap.xml, e todos os arquivos que foram listados no bloco de recursos de publicação são removidos. Os usuários que recebem a experiência de pacote editado que acompanham o pacote como se estivessem com defeito, independentemente de como o pacote original foi configurado.

<a href="" id="bkmk-update-app-in-pkg"></a>**Atualizar um aplicativo em um pacote de aplicativo virtual existente**

1.  No computador que executa o sequenciador, clique em **todos os programas**, aponte para **Microsoft Application Virtualization**e clique em **Microsoft Application Virtualization Sequencer**.

2.  No sequenciador App-V, clique em **modificar um pacote de aplicativo virtual existente** &gt; **em seguida**.

3.  Na página **selecionar tarefa** , clique em **Atualizar aplicativo em pacote existente** em &gt; **seguida**.

4.  Na página **selecionar pacote** , clique em **procurar** para localizar o pacote do aplicativo virtual que contém o aplicativo a ser atualizado e clique em **Avançar**.

5.  Na página **preparar computador** , revise os problemas que podem causar falha na atualização do aplicativo ou fazer com que o aplicativo atualizado contenha dados desnecessários. Resolva todos os possíveis problemas antes de continuar. Após realizar qualquer correção e resolver todos os possíveis problemas, clique em **Atualizar** &gt; **próximo**.

    **Importante**  Se for necessário desativar o software de verificação de vírus, primeiro verifique o computador que executa o sequenciador para garantir que nenhum arquivo indesejado ou mal-intencionado seja adicionado ao pacote.

6.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação de atualização para o aplicativo. Se a atualização não tiver um arquivo de instalação associado e se você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

7.  Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, você poderá continuar a instalar a atualização do aplicativo para que o sequenciador possa monitorar o processo de instalação. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar**e localize e execute os arquivos de instalação adicionais. Quando terminar a instalação, selecione **concluído a instalação**. Clique em **Avançar**.

    **Observação**  O sequenciador monitora todas as alterações e instalações que ocorrem no computador que executa o sequenciador. Isso inclui qualquer alteração e instalação realizada fora do assistente de sequenciamento.

8.  Na página **relatório de instalação** , você pode examinar informações sobre o aplicativo virtual atualizado. Em **informações adicionais**, clique duas vezes no evento para obter informações mais detalhadas. Para continuar, clique em **Avançar**.

9.  Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

    **Observação**  Você pode interromper o carregamento de um aplicativo durante esta etapa. Na caixa de diálogo **Iniciar aplicativo** , clique em **parar**e, em seguida, selecione **interromper todos os aplicativos** ou **interromper somente este aplicativo**.   

10. Na página **criar pacote** , para modificar o pacote sem salvá-lo, marque a caixa de seleção **continuar a modificar o pacote sem salvar usando o editor de pacotes**. Quando você seleciona essa opção, o pacote abre no console do App-V Sequencer, no qual você pode modificar o pacote antes de salvá-lo. Clique em **Avançar**.

    Para salvar o pacote imediatamente, selecione o padrão **salvar o pacote agora**. Adicione **comentários** opcionais para associar ao pacote. Os comentários são úteis para identificar a versão do aplicativo e fornecer outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar** e especifique o novo local. Clique em **Criar**.

11. Na página **conclusão** , clique em **fechar** para fechar o assistente. O pacote agora está disponível no sequenciador.

<a href="" id="bkmk-chg-props-in-pkg"></a>**Modificar as propriedades associadas a um pacote de aplicativo virtual existente**

1.  No computador que executa o sequenciador, clique em **todos os programas**, aponte para **Microsoft Application Virtualization**e clique em **Microsoft Application Virtualization Sequencer**.

2.  No sequenciador App-V, clique em **modificar um pacote de aplicativo virtual existente** &gt; **em seguida**.

3.  Na página **selecionar tarefa** , clique em **Editar pacote** &gt; **próximo**.

4.  Na página **selecionar pacote** , clique em **procurar** para localizar o pacote do aplicativo virtual que contém as propriedades do aplicativo a serem modificadas e, em seguida, clique em **Editar**.

5.  No console do App-V Sequencer, execute qualquer uma das seguintes tarefas conforme necessário:

    -   Importar e exportar o arquivo de manifesto.

    -   Habilitar ou desabilitar objetos auxiliares do navegador.

    -   Importar ou exportar um arquivo VFS.

    -   Importar um diretório para o sistema de arquivos virtual.

    -   Importar e exportar chaves do registro virtual.

    -   Exiba as propriedades do pacote.

    -   Exibir arquivos de pacote associados.

    -   Editar configurações do registro.

    -   Revisar configurações de pacote adicionais (exceto propriedades de arquivos do sistema operacional).

    -   Definir o estado virtualizado da chave do registro (substituir ou mesclar).

    -   Definir o estado da pasta virtualizada.

    -   Adicionar ou editar atalhos e associações de tipo de arquivo.

        **Observação**  Para editar os atalhos ou associações de tipo de arquivo, primeiro você deve abrir o pacote para atualização para adicionar um novo aplicativo e, em seguida, ir para a página de edição final.

6.  Quando terminar de alterar as propriedades do pacote, **File** clique em &gt; **salvar** arquivo para salvar o pacote.

<a href="" id="bkmk-add-app-to-pkg"></a>**Adicionar um novo aplicativo a um pacote de aplicativo virtual existente**

1.  No computador que executa o sequenciador, clique em **todos os programas**, aponte para **Microsoft Application Virtualization**e clique em **Microsoft Application Virtualization Sequencer**.

2.  No sequenciador App-V, clique em **modificar um pacote de aplicativo virtual existente** &gt; **em seguida**.

3.  Na página **selecionar tarefa** , clique em **Adicionar novo aplicativo** em &gt; **seguida**.

4.  Na página **selecionar pacote** , clique em **procurar** para localizar o pacote do aplicativo virtual ao qual você irá adicionar o aplicativo e clique em **Avançar**.

5.  Na página **preparar computador** , revise os problemas que podem causar falha na criação do pacote ou fazer com que o pacote revisado contenha dados desnecessários. Resolva todos os possíveis problemas antes de continuar. Após realizar qualquer correção e resolver todos os possíveis problemas, clique em **Atualizar** &gt; **próximo**.

    **Importante**  Se for necessário desativar o software de verificação de vírus, primeiro verifique o computador que executa o sequenciador para garantir que arquivos indesejados ou mal-intencionados possam ser adicionados ao pacote.

6.  Na página **selecionar instalador** , clique em **procurar** e especifique o arquivo de instalação do aplicativo. Se o aplicativo não tiver um arquivo de instalação associado e você planeja executar todas as etapas de instalação manualmente, marque a caixa de seleção **selecionar esta opção para executar uma instalação personalizada** e clique em **Avançar**.

7.  Na página de **instalação** , quando o sequenciador e o instalador do aplicativo estiverem prontos, instale o aplicativo para que o sequenciador possa monitorar o processo de instalação. Se arquivos de instalação adicionais precisarem ser executados como parte da instalação, clique em **executar**, localize e execute os arquivos de instalação adicionais. Quando concluir a instalação, selecione **concluído a instalação** &gt; **Next**. Na caixa de diálogo **Procurar pasta** , especifique o diretório primário onde o aplicativo será instalado. Certifique-se de que esse é um novo local para que você não substitua a versão existente do pacote de aplicativo virtual.

    **Observação**  O sequenciador monitora todas as alterações e instalações que ocorrem no computador que executa o sequenciador. Isso inclui qualquer alteração e instalação realizada fora do assistente de sequenciamento.

8.  Na página **configurar software** , execute a opção executar os programas contidos no pacote. Esta etapa completa todas as tarefas associadas ou tarefas de configuração necessárias para executar o aplicativo antes de você implantar e executar o pacote nos computadores de destino. Para executar todos os programas ao mesmo tempo, selecione pelo menos um programa e clique em **executar tudo**. Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**. Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos. Pode demorar vários minutos para que todos os programas sejam executados. Clique em **Avançar**.

9.  Na página **relatório de instalação** , você pode examinar informações sobre o aplicativo virtual atualizado. Em **informações adicionais**, clique duas vezes no evento para obter informações mais detalhadas e, em seguida, clique em **Avançar** para abrir a página **Personalizar** .

10. Se você tiver terminado de instalar e configurar o aplicativo virtual, selecione **parar agora** e pule para a etapa 13 deste procedimento. Se você quiser executar a seguinte personalização descrita, clique em **Personalizar**.

    Se você estiver personalizando, prepare o pacote virtual para streaming e clique em **Avançar**. A transmissão aprimora a experiência quando o pacote do aplicativo virtual é executado em computadores de destino.

11. Na página de **streaming** , execute cada programa para que ele possa ser otimizado e executado com mais eficiência nos computadores de destino. Pode levar alguns minutos para que todos os aplicativos sejam executados. Depois que todos os aplicativos tiverem sido executados, feche cada um dos aplicativos e clique em **Avançar**.

    **Observação**  Você pode interromper o carregamento de um aplicativo durante esta etapa. Na caixa de diálogo **Iniciar aplicativo** , clique em **parar** e, em seguida, selecione **interromper todos os aplicativos** ou **interromper somente este aplicativo**.

12. Na página **criar pacote** , para modificar o pacote sem salvá-lo, marque a caixa de seleção **continuar a modificar o pacote sem salvar usando o editor de pacote** . Selecionar essa opção abre o pacote no console do App-V Sequencer, no qual você pode modificar o pacote antes de salvá-lo. Clique em **Avançar**.

    Para salvar o pacote imediatamente, selecione o padrão **salvar o pacote agora**. Adicione **comentários** opcionais para associar ao pacote. Os comentários são úteis para fornecer versões do aplicativo e outras informações sobre o pacote. O **local de salvamento** padrão também é exibido. Para alterar o local padrão, clique em **procurar** e especifique o novo local. O tamanho do pacote descompactado será exibido. Clique em **Criar**.

13. Na página **Conclusão**, clique em **Fechar**. O pacote agora está disponível no sequenciador.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados

[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





