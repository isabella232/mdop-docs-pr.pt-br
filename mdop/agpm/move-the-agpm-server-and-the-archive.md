---
title: Mover o servidor e o arquivo morto do AGPM
description: Mover o servidor e o arquivo morto do AGPM
author: dansimp
ms.assetid: 13cb83c4-bb42-4e81-8660-5b7540f473d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6ae5ba9c2346caf81f5aff9f57f6b9dc97127ad1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799088"
---
# Mover o servidor e o arquivo morto do AGPM


Se você estiver substituindo o servidor do AGPM e o servidor no qual o arquivo está hospedado, será necessário mover o serviço do AGPM e o arquivo morto. Se preferir, você pode mover o serviço do AGPM e o arquivamento separadamente.

**Observação**  
-   O servidor do AGPM é o computador que hospeda o serviço do AGPM e o computador no qual o gerenciamento avançado de política de grupo da Microsoft – servidor está instalado.

-   Por padrão, o arquivo morto é hospedado no servidor do AGPM, mas você pode especificar um caminho de arquivo morto para hospedá-lo em outro servidor em vez disso.

 

Uma conta de usuário que é membro do grupo Domain admins e tem acesso aos servidores AGPM anteriores e novos necessários para concluir este procedimento. Além disso, você deve fornecer credenciais para que a conta de serviço do AGPM seja usada pelo novo servidor do AGPM para concluir este procedimento.

**Para mover o serviço do AGPM e o arquivo para um servidor ou servidores diferentes**

1.  Faça backup do arquivo morto. Para obter mais informações, consulte [fazer backup do arquivo morto](back-up-the-archive.md).

2.  Mover o serviço do AGPM:

    1.  Interrompa o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

    2.  Instale o gerenciamento avançado de política de grupo da Microsoft-servidor no novo servidor que hospedará o serviço do AGPM. Durante esse processo, você especifica o novo caminho de arquivo morto, o local para o arquivo morto em relação ao servidor do AGPM. Para obter mais informações, consulte o guia passo a passo para o guia de planejamento e gerenciamento avançado de política de grupo 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> ) da Microsoft para o gerenciamento avançado de política de grupo da Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=141871> ).

    3.  Um administrador do AGPM (controle total) deve configurar a conexão do servidor do AGPM para todos os administradores de política de grupo que usarão o novo servidor do AGPM e removerão a conexão do servidor do AGPM antigo, ou o administrador da política de grupo deve configurar manualmente a nova conexão do servidor do AGPM e remover a conexão do servidor do AGPM antigo para o snap-in do AGPM no computador. Para obter mais informações, consulte [Configurar conexões do servidor de AGPM](configure-agpm-server-connections-agpm30ops.md).

        **Observação**  Como prática recomendada, você deve desinstalar o gerenciamento avançado de política de grupo da Microsoft – servidor do servidor do AGPM anterior. Isso garantirá que o serviço do AGPM não pode ser reiniciado acidentalmente nesse servidor e poderá causar confusão se qualquer conexão do servidor do AGPM for mantida.

         

3.  Copie o arquivo do backup para o novo servidor que irá hospedar o arquivo morto. Para obter mais informações, consulte [restaurar o arquivo de um backup](restore-the-archive-from-a-backup.md).

    **Importante**  Se você moveu o arquivo sem mover o serviço do AGPM ao mesmo tempo:

    1.  Você deve alterar o caminho do arquivo morto para apontar para o novo local para o arquivo morto em relação ao servidor do AGPM. Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm30ops.md).

    2.  Você deve digitar novamente e confirmar a senha na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification-agpm30ops.md).

     

### Referências adicionais

-   [Fazer backup do arquivo morto](back-up-the-archive.md)

-   [Restaurar o arquivo morto de um backup](restore-the-archive-from-a-backup.md)

-   [Configurar conexões de servidor do AGPM](configure-agpm-server-connections-agpm30ops.md)

-   [Modificar o serviço AGPM](modify-the-agpm-service-agpm30ops.md)

-   Guia passo a passo para o gerenciamento avançado de política de grupo 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> ) da Microsoft

-   Guia de planejamento para o gerenciamento avançado de política de grupo da Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=141871> )

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





