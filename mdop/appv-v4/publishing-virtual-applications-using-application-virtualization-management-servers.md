---
title: Publicação de aplicativos virtuais usando os Application Virtualization Management Servers
description: Publicação de aplicativos virtuais usando os Application Virtualization Management Servers
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796791"
---
# Publicação de aplicativos virtuais usando os Application Virtualization Management Servers


Em uma implantação baseada em servidor do Application Virtualization, os pacotes de aplicativos virtuais que foram importados, testados e importados para implantação são copiados para o compartilhamento de conteúdo principal a ser usado pelo servidor de gerenciamento do Application Virtualization. Depois que os pacotes são importados no servidor de gerenciamento do Application Virtualization, eles podem ser publicados nos usuários finais.

**Observação**  O compartilhamento de conteúdo deve estar localizado no armazenamento de disco anexado do servidor. Usar um dispositivo de armazenamento de rede, como uma SAN ou um compartilhamento DFS, deve ser considerado cuidadosamente devido ao impacto na rede.

 

Os aplicativos são provisionados para grupos do Active Directory. Normalmente, o administrador do Application Virtualization criará grupos do Active Directory para cada aplicativo virtual a ser publicado e adicionará os usuários apropriados a esses grupos. Quando os usuários fazem logon em suas estações de trabalho, o cliente de virtualização de aplicativos, por padrão, executa uma atualização de publicação usando as credenciais do usuário conectado. Em seguida, o usuário pode iniciar aplicativos em qualquer lugar que os atalhos foram colocados. O administrador de virtualização de aplicativos determina onde e quantos atalhos estão localizados no sistema do cliente durante o sequenciamento do aplicativo.

**Observação**  Uma *atualização de publicação* é uma chamada para o servidor do Application Virtualization definido no cliente do Application Virtualization, para determinar quais atalhos de aplicativo virtual são enviados ao cliente para serem usados pelo usuário final.

 

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Visão geral dos Componentes do Application Virtualization System](overview-of-the-application-virtualization-system-components.md)

[Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





