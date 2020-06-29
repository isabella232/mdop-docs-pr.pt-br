---
title: Como sequenciar um novo aplicativo (App-V 4.6)
description: Como sequenciar um novo aplicativo (App-V 4.6)
author: dansimp
ms.assetid: f2c398c6-9200-4be3-b502-e00386fcd150
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a36021adf45f0f4c80ab08bcabbf9f18bf6e66b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796977"
---
# Como sequenciar um novo aplicativo (App-V 4.6)


Use o procedimento a seguir para criar um novo aplicativo virtual usando o sequenciador Application Virtualization (App-V). Você também pode usar o sequenciador do App-V para configurar quais arquivos e configurações são aplicáveis a todos os usuários e quais arquivos e configurações os usuários podem personalizar. Depois de você sequenciar o aplicativo com êxito, ele estará disponível no sequenciador App-V.

**Importante**  
Durante o sequenciamento, se o computador executando o sequenciador estiver executando o Windows Vista ou o Windows 7 e uma reinicialização for iniciada fora do ambiente virtual, por exemplo, ao clicar em **Iniciar**  /  **desligar**, você deverá clicar em **Cancelar** quando solicitado a fechar o programa que impede o desligamento do Windows. Se você clicar em **Forçar desligamento**, a criação do pacote irá falhar e o computador será reiniciado. Quando você clica em **Cancelar**, o sequenciador registra a reinicialização com êxito enquanto o aplicativo está sendo sequenciado.



**Para sequenciar um novo aplicativo**

1.  Para criar a unidade App-V, configure a unidade p como o local que pode ser usado para salvar arquivos enquanto você estiver sequenciando um aplicativo. Em seguida, você deve criar diretórios individuais para cada aplicativo que você planeja sequenciar na unidade Q. Você pode criar as pastas direcionadas do aplicativo virtual antes de sequenciar um aplicativo ou pode criá-los na etapa 5 deste procedimento.

    **Observação**  
    A unidade App-V que você especifica deve ser acessível nos computadores de destino. Se a unidade p não estiver acessível, você poderá escolher uma letra de unidade diferente.



2.  Para iniciar o console do App-v Sequencer, no computador que está executando o sequenciador do App-v, selecione **Iniciar**  /  **programas**  /  **Microsoft Application**Virtualization  /  **Sequencer**Virtualization. Para iniciar o assistente de sequenciamento, clique em **criar um pacote**.

3.  Na página **informações do pacote** , especifique o **nome do pacote** que será atribuído ao aplicativo virtual. O nome do pacote é necessário para gerar o arquivo do Windows Installer associado. Você também deve adicionar um comentário opcional que será atribuído ao pacote e que forneça informações detalhadas sobre o aplicativo virtual. Para exibir a página **Opções avançadas** , selecione **Mostrar opções de monitoramento avançado**e clique em **Avançar**; caso contrário, vá para a etapa 5.

4.  Na página **Opções avançadas** , para permitir que o Microsoft Update atualize o aplicativo conforme ele está sendo sequenciado, selecione **permitir que o Microsoft Update execute durante o monitoramento**. Se você selecionar essa opção, as atualizações da Microsoft poderão ser instaladas durante a fase de monitoramento, e você precisará aceitar as atualizações associadas para que elas sejam instaladas. Para remapear os arquivos. dll (biblioteca de vínculo dinâmico) compatíveis, para que eles usem um espaço contíguo de RAM, selecione as **DLLs de base**. Selecionar essa opção pode conservar a memória e ajudar a melhorar o desempenho. Muitos aplicativos não oferecem suporte a essa opção, mas é útil em ambientes com RAM limitada, como nos cenários do Terminal Server. Clique em **Avançar**.

5.  Na página **monitorar instalação** , quando você estiver pronto para instalar o aplicativo, clique em **Iniciar Monitoramento**e, na caixa de diálogo **Procurar pasta** , especifique o diretório na unidade p onde o aplicativo será instalado. Se você não configurou a unidade Q e usou uma letra de unidade diferente para o aplicativo de virtualização de aplicativo, selecione a letra da unidade especificada na etapa 1 deste procedimento. Para instalar o aplicativo em uma pasta que não foi criada na unidade de virtualização do aplicativo, clique em **criar nova pasta**. Depois de especificar a pasta, aguarde enquanto o sequenciador configura o computador para sequenciamento.

    **Importante**  
    Você deve instalar cada aplicativo que você sequenciar em um diretório separado na unidade do aplicativo virtual, e o nome da pasta associada não deve ter mais de oito caracteres.



~~~
After the computer has been configured for sequencing, install the application so that the App-V Sequencer can monitor the installation; when you are finished, click **Stop Monitoring**, and then click **Next**.
~~~

6. Na página **configurar aplicativos** , se necessário, configure os atalhos e associações de tipo de arquivo que serão associados ao aplicativo virtual. Para adicionar uma nova associação ou atalho de tipo de arquivo, clique em **Adicionar**e, na caixa de diálogo **Adicionar aplicativo** , especifique o novo elemento. Para remover um atalho existente ou uma associação de tipo de arquivo, clique em **remover**. Para editar um elemento existente, selecione o elemento que você deseja modificar e clique em **Editar**. Especifique as configurações na caixa de diálogo **Editar aplicativo** . Clique em **salvar**e, em seguida, clique em **Avançar**.

7. Na página **iniciar aplicativos** , para iniciar o aplicativo e garantir que o pacote tenha sido instalado corretamente e seja otimizado para streaming, selecione o pacote e clique em **Iniciar**. Esta etapa é útil para configurar como o aplicativo é executado inicialmente em computadores de destino e para aceitar qualquer contrato de licença associado antes que o pacote se torne disponível para clientes do App-V. Se vários aplicativos estiverem associados a este pacote, você poderá selecionar **Iniciar tudo** para abrir todos os aplicativos. Para sequenciar o pacote, clique em **Avançar**.

8. Depois de criar o pacote com êxito, no console do App-V Sequencer, selecione **arquivo**  /  **salvar** e especifique o nome e o local da unidade virtual em que o pacote será salvo.

   Opcionalmente, você pode criar um arquivo associado do Windows Installer (**. msi**) para instalar o pacote de aplicativo virtual em computadores de destino. Para criar um arquivo do Windows Installer, abra o pacote no sequenciador e selecione **ferramentas**  /  **criar MSI**. O arquivo do Windows Installer será criado e salvo no diretório onde o pacote do aplicativo virtual é salvo.

   **Importante**  
   Depois de criar um pacote de aplicativo virtual com êxito, não será possível executar o pacote de aplicativo virtual no computador que está executando o sequenciador.



## Tópicos relacionados


[Como atualizar um pacote de aplicativo virtual (App-V 4.6)](how-to-upgrade-a-virtual-application-package--app-v-46-.md)









