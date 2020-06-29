---
title: Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)
description: Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797914"
---
# Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)


Você pode usar aceleradores de pacotes do App-V para gerar automaticamente um novo pacote de aplicativo virtual. Para obter mais informações sobre aceleradores de pacote, consulte [sobre o app-v Package Accelerators (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

**Importante**  
Aviso de isenção de responsabilidade: o aplicativo de sequência de virtualização do aplicativo não lhe concede nenhum direito de licença para o aplicativo de software que você está usando para criar um acelerador de pacote. Você deve obedecer a todos os termos de licença de usuário final para tal aplicativo. É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o Application Virtualization Sequencer.



**Observação**  
Antes de iniciar este procedimento, copie o acelerador de pacote necessário localmente para o computador executando o sequenciador App-V. Você também deve copiar todos os arquivos de instalação necessários para o pacote para um diretório local no computador que executa o sequenciador. Este é o diretório que você precisa especificar na etapa 5 deste procedimento.



Use o procedimento a seguir para criar um pacote de aplicativo virtual usando um acelerador de pacote.

**Para criar um pacote de aplicativo virtual usando um acelerador de pacote App-V**

1. Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2. Para iniciar o **Assistente para criar novo pacote**, clique em **criar um novo pacote de aplicativo virtual**. Para criar o pacote, marque a caixa de seleção **criar um pacote usando um acelerador de pacote** e clique em **Avançar**.

3. Na página **selecionar acelerador de pacote** , para especificar o acelerador de pacote que será usado para criar o novo pacote de aplicativo virtual, clique em **procurar** para localizar o acelerador de pacote que você deseja usar. Clique em **Avançar**.

   **Importante**  
   Se o fornecedor do acelerador de pacote não puder ser validado e não contiver uma assinatura digital válida, na caixa de diálogo **aviso de segurança** , você precisará confirmar que confia na fonte do acelerador de pacote antes de clicar em **executar**.



4. Na página **orientação** , examine as informações de orientação de publicação exibidas no painel de informações. As informações exibidas foram adicionadas quando o acelerador do pacote foi criado e contém informações sobre a criação e a publicação do pacote. Para exportar as informações de orientação para um arquivo de texto (. txt), clique em **Exportar** e especifique o local onde o arquivo deve ser salvo e clique em **Avançar**.

5. Na página **selecionar arquivos de instalação** , para criar uma pasta local que contenha todos os arquivos de instalação necessários para o pacote, clique em **criar nova pasta** e especifique onde a pasta deve ser salva. Você também deve especificar um nome a ser atribuído à pasta. Em seguida, você deve copiar todos os arquivos de instalação necessários para o local que você especificou. Se a pasta que contém os arquivos de instalação já existir no computador que executa o sequenciador, clique em **procurar** para selecionar a pasta.

   Ou, se você já tiver copiado os arquivos de instalação para um diretório neste computador, clique em **criar nova pasta**, navegue até a pasta que contém os arquivos de instalação e clique em **Avançar**.

   **Observação**  
   Você pode especificar os seguintes tipos de arquivos de instalação com suporte:

   -   Arquivos do Windows Installer (**. msi**

   -   arquivos. cab

   -   Arquivos compactados com uma extensão de nome de arquivo. zip

   -   Os arquivos de aplicativo reais

   Não há suporte para os seguintes tipos de arquivo: arquivos **. msp** e <strong> . exe </strong> . Se você especificar um arquivo **. exe** , deverá extrair os arquivos de instalação manualmente.



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. Na página **nome do pacote** , especifique um nome que será associado ao pacote. O nome especificado identifica o pacote no console de gerenciamento do App-V. Clique em **Avançar**.

7. Na página **criar pacote** , forneça comentários que serão associados ao pacote. Os comentários devem conter informações de identificação sobre o pacote que você está criando. Para confirmar o local em que o pacote foi criado, examine as informações exibidas em **local para salvar**. Para compactar o pacote, selecione **compactar pacote**. Marque a caixa de seleção **compactar pacote** se o pacote for transmitido na rede ou quando o tamanho do pacote exceder 4 GB.

   Para criar o pacote, clique em **criar**. Após a criação do pacote, clique em **Avançar**.

8. Na página **configurar software** , para habilitar o sequenciador para configurar os aplicativos contidos no pacote, selecione **configurar software**. Esta etapa é útil para configurar quaisquer tarefas associadas que devem ser concluídas para executar o aplicativo em computadores de destino, como a configuração de qualquer contrato de licença associado.

   Se você selecionar **configurar software**, os seguintes itens serão configurados pelo sequenciador como parte desta etapa:

   -   **Carregar pacote**. O sequenciador carrega os arquivos associados ao pacote. Pode demorar vários segundos até uma hora para decodificar o pacote.

   -   **Executar cada programa**. Opcionalmente, execute os programas contidos no pacote. Esta etapa é útil para concluir todas as tarefas de configuração ou licença associadas que são necessárias para executar o aplicativo antes de implantar e executar o pacote nos computadores de destino. Para executar todos os programas de uma vez, selecione pelo menos um programa e clique em **executar tudo**. Para executar programas específicos, selecione o programa ou programas que você deseja executar e clique em **executar selecionado**. Conclua as tarefas de configuração necessárias e, em seguida, feche os aplicativos. Pode demorar vários minutos para que todos os programas sejam executados. Clique em **Avançar**.

   -   **Salve o pacote**. O sequenciador salva o pacote.

   -   **Bloco de recursos primário**. O sequenciador otimiza o pacote para streaming recriando o bloco de recursos principal.

   Se você não quiser configurar os aplicativos, clique em **ignorar esta etapa**e vá para a etapa 9 deste procedimento e clique em **Avançar**.

9. Na página de **conclusão** , depois de revisar as informações exibidas no painel **relatório de pacote de aplicativo virtual** , clique em **Fechar**.

   O pacote agora está disponível no sequenciador. Para editar as propriedades do pacote, clique em **Editar \ [nome do pacote \]**. Para obter mais informações sobre como modificar um pacote, consulte [como modificar um pacote de aplicativo virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

## Tópicos relacionados


[Configuração do Application Virtualization Sequencer (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









