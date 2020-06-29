---
title: Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)
description: Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797165"
---
# Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)


Você pode usar aceleradores de pacotes do App-V para gerar automaticamente um novo pacote de aplicativo virtual. Depois de criar um acelerador de pacote com êxito, você poderá reutilizar e compartilhar o acelerador de pacote. Para obter mais informações sobre aceleradores de pacote, consulte [sobre o app-v Package Accelerators (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md). A criação de aceleradores de pacotes do App-V é uma tarefa avançada. Os aceleradores de pacote podem conter informações específicas de senha e usuário. Portanto, você deve salvar aceleradores de pacotes e a mídia de instalação associada em um local seguro e deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o fornecedor possa ser verificado quando o acelerador de pacotes do App-V for aplicado.

Em algumas situações, para criar o acelerador de pacote, talvez seja necessário instalar o aplicativo localmente no computador que está executando o sequenciador. Primeiro, tente criar o acelerador de pacote usando a mídia de instalação e, se houver vários arquivos ausentes necessários, instale o aplicativo localmente no computador que executa o sequenciador e crie o acelerador de pacote.

**Importante**  
Antes de começar o procedimento a seguir, você deve fazer o seguinte:

-   Copie o pacote de aplicativo virtual que você deve usar para criar o acelerador de pacote localmente para o computador que está executando o sequenciador.

-   Copie todos os arquivos de instalação necessários associados ao pacote de aplicativo virtual para o computador que executa o sequenciador.



**Importante**  
Aviso de isenção de responsabilidade: o Microsoft Application Virtualization Sequencer não lhe concede nenhum direito de licença para o aplicativo de software que você está usando para criar um acelerador de pacote. Você deve obedecer a todos os termos de licença de usuário final para tal aplicativo. É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o Application Virtualization Sequencer.



**Para criar um acelerador de pacote App-V**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Para iniciar o assistente app-v **Create Package Accelerator** na App-v Sequencer, clique em **ferramentas**  /  **Create Package Accelerator**.

3.  Na página **selecionar pacote** , para especificar um pacote de aplicativo virtual existente a ser usado para criar o acelerador de pacote, clique em **procurar**e localize o pacote de aplicativo virtual existente (arquivo. sprj).

    **Dica**  
    Copie os arquivos associados ao pacote de aplicativo virtual que você planeja usar localmente para o computador que está executando o sequenciador.



~~~
Click **Next**.
~~~

4. Na página **arquivos de instalação** , para especificar a pasta que contém os arquivos de instalação que você usou para criar o pacote de aplicativo virtual original, clique em **procurar**e selecione o diretório que contém os arquivos de instalação.

   **Dica**  
   Copie a pasta que contém os arquivos de instalação necessários para o computador que está executando o sequenciador.



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. Na página **coletando informações** , examine os arquivos que não foram encontrados no local especificado na página **arquivos de instalação** deste assistente. Se os arquivos exibidos não forem necessários, selecione **remover estes arquivos**e, em seguida, clique em **Avançar**. Se os arquivos forem necessários, clique em **anterior** e copie os arquivos necessários para o diretório especificado na página **arquivos de instalação** .

   **Observação**  
   Você deve remover os arquivos desnecessários ou clicar em **anterior** e localizar os arquivos necessários para avançar para a próxima página deste assistente.



6. Na página **selecionar arquivos** , examine atentamente os arquivos detectados e desmarque todos os arquivos que devem ser removidos do acelerador de pacote. Selecione apenas os arquivos necessários para que o aplicativo seja executado com êxito e clique em **Avançar**.

7. Na página **verificar aplicativos** , confirme se todos os arquivos de instalação necessários para compilar o pacote são exibidos. Quando o acelerador de pacote é usado para criar um novo pacote, todos os arquivos de instalação exibidos no painel **aplicativos** são necessários para criar o pacote.

   Se necessário, para adicionar outros arquivos do instalador, clique em **Adicionar**. Para remover arquivos de instalação desnecessários, selecione o arquivo de instalação e, em seguida, clique em **excluir**. Para editar as propriedades associadas a um instalador, clique em **Editar**. Os arquivos de instalação especificados nesta etapa serão obrigatórios quando o acelerador de pacote for usado para criar um novo pacote de aplicativo virtual. Depois de confirmar as informações exibidas, clique em **Avançar**.

8. Na página **selecionar orientação** , para especificar um arquivo que contenha informações sobre como o acelerador de pacote, clique em **procurar**. Por exemplo, esse arquivo pode conter informações sobre como o computador que executa o sequenciador deve ser configurado, informações de pré-requisito do aplicativo para computadores de destino e anotações gerais. Você deve fornecer todas as informações necessárias para que o acelerador de pacote seja aplicado com êxito. O arquivo que você selecionar deve estar no formato Rich Text (. rtf) ou arquivo de texto (. txt). Clique em **Avançar**.

9. Na página **Create Package Accelerator** , para especificar onde salvar o acelerador de pacote, clique em **procurar** e selecione o diretório.

10. Na página **conclusão** , para fechar o assistente **criar acelerador de pacote** , clique em **Fechar**.

   **Importante**  
   Para ajudar a garantir que o acelerador do pacote seja o mais seguro possível e para que o fornecedor possa ser verificado quando o acelerador de pacote é aplicado, você sempre deve assinar digitalmente o acelerador de pacote.



## Tópicos relacionados


Configurando o Application Virtualization Sequencer (App-V 4,6 SP1) [como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)









