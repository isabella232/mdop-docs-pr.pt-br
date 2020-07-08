---
title: Como criar um acelerador de pacote
description: Como criar um acelerador de pacote
author: dansimp
ms.assetid: b61f3581-7933-443e-b872-a96bed9ff8d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6893f2e9bb9db473d285026015c3399fb0074015
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796456"
---
# Como criar um acelerador de pacote


Aceleradores de pacotes do App-V 5,1 geram automaticamente novos pacotes de aplicativos virtuais.

**Observação**  
Você pode usar o PowerShell para criar um acelerador de pacote. Para obter mais informações [, consulte como criar um acelerador de pacote usando o PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).



Use o procedimento a seguir para criar um acelerador de pacote.

**Importante**  
Os aceleradores de pacote podem conter informações específicas de senha e usuário. Portanto, você deve salvar aceleradores de pacote e a mídia de instalação associada em um local seguro, e deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o fornecedor possa ser verificado quando o acelerador de pacotes do App-V 5,1 for aplicado.



**Importante**  
Antes de começar o procedimento a seguir, você deve executar o seguinte:

-   Copie o pacote de aplicativo virtual que você usará para criar o acelerador de pacote localmente para o computador que está executando o sequenciador.

-   Copie todos os arquivos de instalação necessários associados ao pacote de aplicativo virtual para o computador que executa o sequenciador.



**Para criar um acelerador de pacote**

1.  **Importante**  
    O sequenciador do App-V 5,1 não concede direitos de licença para o aplicativo de software que você está usando para criar o acelerador de pacote. Você deve obedecer a todos os termos de licença de usuário final para o aplicativo que você está usando. É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o sequenciador do App-V 5,1.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Para iniciar o assistente do Gerenciador de **aceleração de criação** do App-v 5,1, no console app-v 5,1 Sequencer, clique em **ferramentas**  /  **criar acelerador**.

3. Na página **selecionar pacote** , para especificar um pacote de aplicativo virtual existente a ser usado para criar o acelerador de pacote, clique em **procurar**e localize o pacote de aplicativo virtual existente (arquivo. AppV).

   **Dica**  
   Copie os arquivos associados ao pacote de aplicativo virtual que você planeja usar localmente para o computador que está executando o sequenciador.



~~~
Click **Next**.
~~~

4. Na página **arquivos de instalação** , para especificar a pasta que contém os arquivos de instalação que você usou para criar o pacote de aplicativo virtual original, clique em **procurar**e selecione o diretório que contém os arquivos de instalação.

   **Dica**  
   Copie a pasta que contém os arquivos de instalação necessários para o computador que está executando o sequenciador.



5. Se o aplicativo já estiver instalado no computador que executa o sequenciador, para especificar o arquivo de instalação, selecione os **arquivos instalados no sistema local**. Para usar essa opção, o aplicativo já deve estar instalado no local de instalação padrão.

6. Na página **coletando informações** , examine os arquivos que não foram encontrados no local especificado na página **arquivos de instalação** deste assistente. Se os arquivos exibidos não forem necessários, selecione **remover estes arquivos**e, em seguida, clique em **Avançar**. Se os arquivos forem necessários, clique em **anterior** e copie os arquivos necessários para o diretório especificado na página **arquivos de instalação** .

   **Observação**  
   Você deve remover os arquivos desnecessários ou clicar em **anterior** e localizar os arquivos necessários para avançar para a próxima página deste assistente.



7. Na página **selecionar arquivos** , examine atentamente os arquivos detectados e desmarque todos os arquivos que devem ser removidos do acelerador de pacote. Selecione apenas os arquivos necessários para que o aplicativo seja executado com êxito e clique em **Avançar**.

8. Na página **verificar aplicativos** , confirme se todos os arquivos de instalação necessários para compilar o pacote são exibidos. Quando o acelerador de pacote é usado para criar um novo pacote, todos os arquivos de instalação exibidos no painel **aplicativos** são necessários para criar o pacote.

   Se necessário, para adicionar outros arquivos do instalador, clique em **Adicionar**. Para remover arquivos de instalação desnecessários, selecione o arquivo de instalação e, em seguida, clique em **excluir**. Para editar as propriedades associadas a um instalador, clique em **Editar**. Os arquivos de instalação especificados nesta etapa serão obrigatórios quando o acelerador de pacote for usado para criar um novo pacote de aplicativo virtual. Depois de confirmar as informações exibidas, clique em **Avançar**.

9. Na página **selecionar orientação** , para especificar um arquivo que contenha informações sobre como o acelerador de pacote, clique em **procurar**. Por exemplo, esse arquivo pode conter informações sobre como o computador que executa o sequenciador deve ser configurado, informações de pré-requisito do aplicativo para computadores de destino e anotações gerais. Você deve fornecer todas as informações necessárias para que o acelerador de pacote seja aplicado com êxito. O arquivo que você selecionar deve estar no formato Rich Text (. rtf) ou arquivo de texto (. txt). Clique em **Avançar**.

10. Na página **Create Package Accelerator** , para especificar onde salvar o acelerador de pacote, clique em **procurar** e selecione o diretório.

11. Na página **conclusão** , para fechar o assistente **criar acelerador de pacote** , clique em **Fechar**.

   **Importante**  
   Para ajudar a garantir que o acelerador do pacote seja o mais seguro possível e para que o fornecedor possa ser verificado quando o acelerador de pacote é aplicado, você sempre deve assinar digitalmente o acelerador de pacote.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

[Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)









