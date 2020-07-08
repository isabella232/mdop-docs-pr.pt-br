---
title: Como atualizar um pacote de aplicativo virtual (App-V 4.6)
description: Como atualizar um pacote de aplicativo virtual (App-V 4.6)
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796929"
---
# Como atualizar um pacote de aplicativo virtual (App-V 4.6)


Use o procedimento a seguir para atualizar um aplicativo virtual existente usando o sequenciador Application Virtualization (App-V). Você também pode usar o console do sequenciador do App-V para fazer alterações em um aplicativo virtual existente sem realizar uma atualização, mas não é possível fazer modificações no sistema de arquivos do aplicativo virtual usando esse método, pois o sequenciador do App-V não realmente decodificará o arquivo. sft associado. Para obter mais informações sobre como editar um pacote existente, consulte [como modificar um pacote de aplicativo virtual (App-V 4,6)](how-to-modify-a-virtual-application-package--app-v-46-.md).

**Para atualizar um aplicativo virtual existente**

1.  Para iniciar o console do App-v Sequencer, no computador que executa o sequenciador app-v, selecione **Iniciar**  /  **programas**  /  **Microsoft Application**Virtualization  /  **Sequencer Virtualization**.

2.  Para abrir o pacote de aplicativo virtual existente e iniciar o **Assistente de sequenciamento**, selecione **atualizar um pacote**. Localize o pacote que você deseja atualizar e clique em **abrir**. Na caixa de diálogo **Procurar pasta** , especifique o local em que a versão atualizada do pacote será colocada. Este local especificado deve estar localizado na unidade especificada como a unidade de virtualização do aplicativo, que normalmente é a unidade Q:\\. Para criar uma nova pasta, selecione **criar nova pasta**.

    **Aviso**  Você deve especificar a pasta raiz do aplicativo virtual existente. Não crie uma subpasta manualmente ou a atualização não será bem-sucedida.

     

3.  Na página **informações do pacote** , especifique o **nome do pacote** que será atribuído ao pacote atualizado. O nome do pacote é necessário para gerar o arquivo do Windows Installer associado. Você também deve adicionar um comentário opcional que será atribuído ao pacote e que forneça informações detalhadas sobre o aplicativo virtual — por exemplo, um número de versão. Para exibir a página **Opções avançadas** , selecione **Mostrar opções de monitoramento avançado** e clique em **Avançar**; caso contrário, vá para a etapa 5.

4.  Na página **Opções avançadas** , para permitir que o Microsoft Update atualize o aplicativo conforme ele está sendo sequenciado, selecione **permitir que o Microsoft Update execute durante o monitoramento**. Se você selecionar essa opção, as atualizações da Microsoft poderão ser instaladas durante a fase de monitoramento, e você precisará aceitar as atualizações associadas para que elas sejam instaladas. Para remapear os arquivos de biblioteca de vínculo dinâmico (. dll) compatíveis, para que eles usem um espaço contíguo de RAM, selecione **alterar DLLs de base**. Selecionar essa opção pode conservar a memória e ajudar a melhorar o desempenho. Clique em **Avançar**.

5.  Na página **monitorar instalação** , quando você estiver pronto para atualizar o aplicativo, clique em **Iniciar Monitoramento**.

    Quando as atualizações do aplicativo forem aplicadas, clique em **parar monitoramento**. Clique em **Avançar**.

6.  Na página **configurar aplicativos** , se necessário, configure os atalhos e associações de tipo de arquivo que serão associados ao aplicativo virtual. Para adicionar uma nova associação ou atalho de tipo de arquivo, clique em **Adicionar**e, na caixa de diálogo **Adicionar aplicativo** , especifique o novo elemento. Para remover um atalho existente ou uma associação de tipo de arquivo, clique em **remover**. Para editar um elemento existente, selecione o elemento que você deseja modificar e clique em **Editar**. Especifique as configurações na caixa de diálogo **Editar aplicativo** . Clique em **Salvar**. Clique em **Avançar**.

7.  Na página **iniciar aplicativos** , para iniciar o aplicativo e garantir que o pacote tenha sido instalado corretamente e seja otimizado para streaming, selecione o pacote e clique em **Iniciar**. Esta etapa é útil para configurar como o aplicativo é executado inicialmente em computadores de destino e para aceitar qualquer contrato de licença associado antes de o pacote ser disponibilizado para clientes do App-V. Se vários aplicativos estiverem associados a este pacote, você poderá selecionar **Iniciar tudo** para abrir todos os aplicativos. Para sequenciar o pacote, clique em **Avançar**.

8.  Para fechar o assistente de sequenciamento, clique em **concluir**. Para salvar o pacote atualizado, no console do sequenciador, selecione **File**  /  **salvar**arquivo.

    Se você planeja implantar o pacote atualizado usando um arquivo do Windows Installer (. msi), deve criar um novo da seguinte maneira: no console do sequenciador, selecione **ferramentas**  /  **criar MSI**. O novo arquivo do Windows Installer será criado e salvo no diretório em que o pacote do aplicativo virtual atualizado é salvo.

## Tópicos relacionados


[Como sequenciar um novo aplicativo (App-V 4.6)](how-to-sequence-a-new-application--app-v-46-.md)

 

 





