---
title: Fazer backup do arquivo morto
description: Fazer backup do arquivo morto
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797479"
---
# Fazer backup do arquivo morto


Para ajudar na recuperação do arquivo para o gerenciamento avançado de política de grupo (AGPM) se houver um desastre, um administrador do AGPM (controle total) deve fazer o backup do arquivamento com frequência. Por padrão, o arquivo morto é criado no%ProgramData%\\Microsoft\\AGPM. No entanto, você pode especificar um caminho diferente durante a configuração do gerenciamento avançado de política de grupo da Microsoft-servidor.

Uma conta de usuário que tem acesso ao servidor do AGPM – o computador no qual o serviço do AGPM está instalado — e para a pasta que contém o arquivo morto é necessária para concluir este procedimento.

**Para fazer backup do arquivo morto**

1.  Interrompa o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Faça backup da pasta arquivo morto usando o Windows Explorer, xcopy, Windows Server® backup ou outra ferramenta de backup. Certifique-se de fazer backup dos arquivos ocultos, do sistema e somente leitura.

3.  Armazene o backup do arquivo morto em um local seguro.

4.  Reinicie o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

**Observação**  Se um administrador do AGPM faz o backup do arquivo raramente, os objetos de política de grupo (GPOs) no backup do arquivo morto não serão atuais. Para garantir que o backup do arquivo morto esteja atualizado, faça backup do arquivamento como parte da estratégia de backup diário da sua organização.

 

### Referências adicionais

-   [Restaurar o arquivo morto de um backup](restore-the-archive-from-a-backup.md)

-   [Mover o servidor e o arquivo morto do AGPM](move-the-agpm-server-and-the-archive.md)

-   [Gerenciamento do arquivo morto](managing-the-archive.md)

 

 





