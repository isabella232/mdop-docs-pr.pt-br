---
title: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1
description: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796471"
---
# Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1


Você pode usar uma configuração dinâmica para personalizar um pacote App-V 5,1 para um usuário específico. No entanto, você deve primeiro criar o arquivo de configuração dinâmica do usuário (. xml) ou o arquivo de configuração de implantação dinâmica antes de poder usar os arquivos. A criação do arquivo é uma operação manual avançada. Para obter informações gerais sobre arquivos de configuração de usuários dinâmicos, consulte [sobre a configuração dinâmica do App-V 5,1](about-app-v-51-dynamic-configuration.md).

Use o procedimento a seguir para criar um arquivo de configuração de usuário dinâmico usando o console de gerenciamento do App-V 5,1.

**Para criar um arquivo de configuração de usuário dinâmico**

1.  Clique com o botão direito do mouse no nome do pacote que você deseja exibir e selecione **Editar acesso ao Active Directory** para exibir a configuração atribuída a um determinado grupo de usuários. Ou, se preferir, selecione o pacote e clique em **Editar**.

2.  Usando a lista de **entidades do anúncio com o Access**, selecione o grupo do anúncio que você deseja personalizar. Selecione **personalizado** na lista suspensa, se ainda não estiver selecionado. Um link chamado **Editar** será exibido.

3.  Clique em **Editar**. A configuração do usuário dinâmico atribuído ao grupo do anúncio será exibida.

4.  Clique em **avançado**e, em seguida, clique em **Exportar configuração**. Digite um nome de arquivo e clique em **salvar**. Agora, você pode editar o arquivo para configurar um pacote para um usuário.

    **Observação**  
    Para exportar uma configuração durante a execução no Windows Server, você deve desabilitar "configuração de segurança avançada do IE". Se ele estiver habilitado e definido para bloquear downloads, não será possível baixar nada do servidor do App-V.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)









