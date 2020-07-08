---
title: Como publicar um pacote usando o Console de Gerenciamento
description: Como publicar um pacote usando o Console de Gerenciamento
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796336"
---
# Como publicar um pacote usando o Console de Gerenciamento


Use o procedimento a seguir para publicar um pacote do App-V 5,0. Depois que você publica um pacote, os computadores que executam o cliente App-V 5,0 podem acessar e executar os aplicativos nesse pacote.

**Observação**  A capacidade de habilitar somente os administradores para publicar ou cancelar a publicação de pacotes (descritos abaixo) tem suporte a partir do App-V 5,0 SP3.

 

**Para publicar um pacote do App-V 5,0**

1.  No console de gerenciamento do App-V 5,0. Clique com o botão direito do mouse no nome do pacote a ser publicado e selecione **publicar**.

2.  Examine a coluna **status** para verificar se o pacote foi publicado e agora está disponível. Se o pacote estiver disponível, o status **publicado** será exibido.

    Se o pacote não for publicado com êxito, o status não **publicado** será exibido, juntamente com o texto de erro que explica por que o pacote não está disponível.

**Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes**

1.  Navegue até o seguinte nó de objeto de política de Grupo:

    **Configuração &gt; do computador Política &gt; modelos administrativos &gt; do &gt; App-V &gt; Publishing**.

2.  Habilite a configuração de política **exigir publicação como administrador** .

    Para usar opcionalmente o PowerShell para definir esse item, consulte [como gerenciar pacotes do App-V 5,0 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

[Como configurar o acesso a pacotes usando o Console de Gerenciamento](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





