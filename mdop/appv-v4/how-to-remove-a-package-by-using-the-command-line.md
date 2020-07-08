---
title: Como remover um pacote usando a linha de comando
description: Como remover um pacote usando a linha de comando
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797002"
---
# Como remover um pacote usando a linha de comando


Você pode usar os seguintes procedimentos de linha de comando para excluir um pacote de aplicativo virtual do cliente Application Virtualization (App-V) em um computador específico.

**Para excluir um pacote de aplicativo virtual para todos os usuários**

-   Se o pacote foi adicionado anteriormente para todos os usuários usando a opção/GLOBAL, use o comando a seguir para excluir o pacote e os tipos de arquivo e atalhos globais. É necessário ter direitos de administrador. A opção/GLOBAL não é necessária nesse caso porque o comando sempre executa uma exclusão global do pacote.

    `SFTMIME DELETE PACKAGE:”name”`

**Para excluir um pacote adicionado anteriormente para usuários individuais**

1.  Se o pacote foi adicionado anteriormente para usuários individuais, você tem várias opções.

    Execute o seguinte comando uma vez na conta de usuário de cada pessoa na qual o pacote foi publicado. Isso recusa o acesso do usuário aos aplicativos se eles se em outro computador. Ele exclui as configurações, atalhos e tipos de arquivo do usuário específico do perfil, e ele interrompe as cargas em segundo plano sob o contexto do usuário.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  Você também pode executar o seguinte comando sob a conta de usuário de cada pessoa na qual o pacote foi publicado.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    Em seguida, execute esse comando para o pacote.

    `SFTMIME DELETE PACKAGE:”name”`

    Isso remove completamente o pacote e exclui todas as configurações de usuário, atalhos e tipos de arquivo dos perfis. Se o pacote for adicionado novamente, os usuários precisarão especificar as configurações novamente. Somente a permissão "excluir aplicativos" (**DeleteApp**) é necessária para executar este comando.

3.  Como terceira alternativa, você pode simplesmente executar o comando **excluir pacote** sem usar o comando **Cancelar publicação do pacote** . Nesse caso, os tipos de arquivo e atalhos de cada usuário são ocultos, em vez de excluídos, e as configurações do usuário são mantidas. Isso significa que, se o pacote for adicionado novamente para o usuário, os tipos de arquivo e atalhos serão restaurados e as configurações do usuário serão reaplicadas.

## Tópicos relacionados


[Como adicionar um pacote usando a linha de comando](how-to-add-a-package-by-using-the-command-line.md)

[Como excluir todos os aplicativos virtuais usando a linha de comando](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





