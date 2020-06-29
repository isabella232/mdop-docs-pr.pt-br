---
title: Como configurar os Application Virtualization Management Servers
description: Como configurar os Application Virtualization Management Servers
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797206"
---
# Como configurar os Application Virtualization Management Servers


Antes que aplicativos virtualizados possam ser transmitidos para o cliente da área de trabalho do Application Virtualization ou o cliente para serviços de área de trabalho remota (antes serviços de terminal), o servidor de gerenciamento do Application Virtualization deve ser configurado. Ao configurar o servidor, você está configurando o *diretório de conteúdo* em que os arquivos SFT são carregados e armazenados. Os arquivos SFT contêm o aplicativo virtualizado (ou aplicativos).

**Importante**  Os servidores de virtualização de aplicativos transmitem arquivos SFT para o cliente da área de trabalho e o cliente para serviços de área de trabalho remota usando somente protocolos RTSP ou RTSP. O arquivo ICO (ícone) e o arquivo OSD (Open Software Descriptor) podem ser configurados para transmitir de um arquivo ou servidor HTTP diferente.

 

**Para configurar o servidor de gerenciamento do Application Virtualization**

1.  Conclua o seguinte procedimento:

    [Como instalar o Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Observação**  Durante o procedimento de instalação, especifique o local do diretório \\Content na tela **caminho do conteúdo** .

     

2.  Navegue até o local que você especificou para o diretório \\Content e, se necessário, crie o diretório.

3.  Quando o diretório de conteúdo é criado, configure esse diretório como um compartilhamento de arquivo padrão.

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Requisitos de Sistema do Application Virtualization](application-virtualization-system-requirements.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Como configurar os servidores para a implantação baseada em servidor](how-to-configure-servers-for-server-based-deployment.md)

 

 





