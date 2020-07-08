---
title: Como adicionar um pacote usando a linha de comando
description: Como adicionar um pacote usando a linha de comando
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797919"
---
# Como adicionar um pacote usando a linha de comando


Os procedimentos a seguir listam as etapas necessárias para adicionar um pacote de aplicativo virtual ao cliente do Application Virtualization (App-V) em um computador específico.

**Para adicionar um pacote de aplicativo virtual para um usuário específico**

-   Execute o seguinte comando na conta de usuário da pessoa que está para obter o pacote. O comando adiciona e publica o pacote para esse usuário.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**Para adicionar um pacote de aplicativo virtual para todos os usuários**

-   Execute o seguinte comando em uma conta com direitos de administrador. O pacote é adicionado e publicado para todos os usuários do computador.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**Para adicionar um pacote usando um sistema de distribuição de software eletrônico**

1.  Se você estiver usando um sistema de distribuição de software eletrônico que executa os comandos na conta do **sistema** do computador, o pacote será publicado somente para essa conta, a menos que você use a opção/global Execute o seguinte comando para adicionar e publicar o pacote para todos os usuários do computador:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    Se você quiser adicionar o pacote somente para usuários específicos, execute o comando **Adicionar pacote** e, em seguida, publique explicitamente o pacote para cada usuário executando o seguinte comando de **pacote de publicação** na conta de usuário de cada pessoa:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    Publicar o pacote sem o parâmetro GLOBAL concede ao usuário acesso aos aplicativos no pacote e publica os tipos de arquivo e atalhos listados no manifesto para o perfil do usuário. As permissões necessárias são "gerenciar associações de tipo de arquivo" (**ManageTypes**) e "publicar atalhos" (**PublishShortcut**).

## Tópicos relacionados


[Como excluir todos os aplicativos virtuais usando a linha de comando](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[Como remover um pacote usando a linha de comando](how-to-remove-a-package-by-using-the-command-line.md)

 

 





