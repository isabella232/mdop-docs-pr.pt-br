---
title: Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V
description: Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V
author: dansimp
ms.assetid: 715e7526-e100-419c-8fc1-75cbfe433835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 547cb93f334e025243937a97a1f904410fe2d504
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796457"
---
# Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V


**Importante**  
O sequenciador do App-V 5,0 não concede direitos de licença para o aplicativo de software que você usa para criar o acelerador de pacote. Você deve obedecer a todos os termos de licença de usuário final para o aplicativo que você usa. É sua responsabilidade ter certeza de que os termos de licença do aplicativo de software permitem que você crie um acelerador de pacote com o sequenciador do App-V 5,0.



Use o procedimento a seguir para criar um pacote de aplicativo virtual com o acelerador de pacote do App-V 5,0.

**Observação**  
Antes de iniciar este procedimento, copie o acelerador de pacote necessário localmente para o computador que executa o sequenciador do App-V 5,0. Você também deve copiar todos os arquivos de instalação necessários para o pacote para um diretório local no computador que executa o sequenciador. Este é o diretório que você precisa especificar na etapa 5 deste procedimento.



**Para criar um pacote de aplicativo virtual com um acelerador de pacote do App-V 5,0**

1.  Para iniciar o sequenciador do App-v, no computador que executa o sequenciador do App-v 5,0, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**. Para criar o pacote, marque a caixa de seleção **criar um pacote usando um acelerador de pacote** e clique em **Avançar**.

3.  Para especificar o acelerador de pacote que será usado para criar o novo pacote de aplicativo virtual, clique em **procurar** na página **selecionar acelerador de pacote** . Clique em **Avançar**.

    **Importante**  
    Se o fornecedor do acelerador de pacote não puder ser validado e não contiver uma assinatura digital válida, antes de clicar em **executar**, você precisará confirmar que confia na fonte do acelerador de pacote. Confirme sua escolha na caixa de diálogo **aviso de segurança** .



4.  Na página **orientação** , examine as informações de orientação de publicação exibidas no painel de informações. Essas informações foram adicionadas quando o acelerador de pacote foi criado e contém orientação sobre como criar e publicar o pacote. Para exportar as informações de orientação para um arquivo de texto (. txt), clique em **Exportar** e especifique o local onde o arquivo deve ser salvo e clique em **Avançar**.

5.  Na página **selecionar arquivos de instalação** , clique em **criar nova pasta** para criar uma pasta local que contenha todos os arquivos de instalação necessários para o pacote e especifique onde a pasta deve ser salva. Você também deve especificar um nome a ser atribuído à pasta. Em seguida, você deve copiar todos os arquivos de instalação necessários para o local que você especificou. Se a pasta que contém os arquivos de instalação já existir no computador que executa o sequenciador, clique em **procurar** para selecionar a pasta.

    Ou, se você já tiver copiado os arquivos de instalação para um diretório neste computador, clique em **criar nova pasta**, navegue até a pasta que contém os arquivos de instalação e clique em **Avançar**.

    **Observação**  
    Você pode especificar os seguintes tipos de arquivos de instalação com suporte:

    -   Arquivos do Windows Installer (**. msi**)

    -   Arquivos cabinet (. cab)

    -   Arquivos compactados com uma extensão de nome de arquivo. zip

    -   Os arquivos de aplicativo reais

    Não há suporte para os seguintes tipos de arquivo: arquivos **. msp** e **. exe** . Se você especificar um arquivo **. exe** , deverá extrair os arquivos de instalação manualmente.



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. Na página **nome do pacote** , especifique um nome que será associado ao pacote. O nome que você especificar identifica o pacote no console de gerenciamento do App-V. Clique em **Avançar**.

7. Na página **criar pacote** , forneça comentários que serão associados ao pacote. Os comentários devem conter informações de identificação sobre o pacote que você está criando. Para confirmar o local em que o pacote foi criado, revise as informações exibidas no **local de salvamento**. Para compactar o pacote, selecione **compactar pacote**. Marque a caixa de seleção **compactar pacote** se o pacote for transmitido na rede ou quando o tamanho do pacote exceder 4 GB.

   Para criar o pacote, clique em **criar**. Após a criação do pacote, clique em **Avançar**.

8. Na página **configurar software** , para habilitar o sequenciador para configurar os aplicativos contidos no pacote, selecione **configurar software**. Nesta etapa, você pode configurar todas as tarefas associadas que devem ser concluídas para executar o aplicativo nos computadores de destino. Por exemplo, você pode configurar qualquer contrato de licença associado.

   Se você selecionar **configurar software**, os seguintes itens podem ser configurados usando o sequenciador como parte desta etapa:

   -   **Carregar pacote**. O sequenciador carrega os arquivos associados ao pacote. Pode levar vários segundos a uma hora para decodificar o pacote.

   -   **Executar cada programa**. Opcionalmente, execute os programas contidos no pacote. Esta etapa é útil para concluir todas as tarefas ou tarefas de configuração associadas que são necessárias para executar o aplicativo antes de implantar e executar o pacote nos computadores de destino. Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**. Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**. Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos. Pode demorar vários minutos para que todos os programas sejam executados. Clique em **Avançar**.

   -   **Salve o pacote**. O sequenciador salva o pacote.

   -   **Bloco de recursos primário**. O sequenciador otimiza o pacote para streaming recriando o bloco de recursos principal.

   Se você não quiser configurar os aplicativos, clique em **ignorar esta etapa**e vá para a etapa 9 deste procedimento e clique em **Avançar**.

9. Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativo virtual** , clique em **Fechar**.

   O pacote agora está disponível no sequenciador. Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**. Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente](how-to-modify-an-existing-virtual-application-package-beta.md).

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)









