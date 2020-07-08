---
title: Como configurar os Application Virtualization Streaming Servers
description: Como configurar os Application Virtualization Streaming Servers
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797202"
---
# Como configurar os Application Virtualization Streaming Servers


Antes que os aplicativos virtuais possam ser transmitidos para o cliente da área de trabalho do Application Virtualization ou o cliente para serviços de área de trabalho remota (antes serviços de terminal), os servidores de streaming do Application Virtualization devem ser configurados. Ao configurar os servidores, você está configurando o *diretório de conteúdo* em que os arquivos SFT são carregados e armazenados. Os arquivos SFT contêm o aplicativo virtual (ou aplicativos).

**Importante**  Os servidores de virtualização de aplicativos transmitem arquivos SFT para o cliente da área de trabalho e o cliente para serviços de área de trabalho remota usando somente protocolos RTSP ou RTSP. O arquivo ICO (ícone) e o arquivo OSD (Open Software Descriptor) podem ser configurados para transmitir de um arquivo ou servidor HTTP diferente.

 

**Para configurar os servidores de streaming do Application Virtualization**

1.  Conclua o procedimento de instalação do servidor de streaming do Application Virtualization. Durante o procedimento de instalação, especifique o local do diretório \\Content na tela **caminho do conteúdo** .

2.  Navegue até o local que você especificou para o diretório \\Content e, se necessário, crie o diretório.

3.  Quando o diretório de conteúdo é criado, configure esse diretório como um compartilhamento de arquivo padrão.

4.  Configure as permissões do sistema de arquivos NTFS para o diretório de conteúdo e as pastas do pacote no diretório de conteúdo. Você deve usar grupos de segurança nos serviços de domínio Active Directory que definem quais usuários podem acessar cada aplicativo.

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Como configurar os Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)

[Como configurar o Servidor de Arquivos](how-to-configure-the-file-server.md)

[Como configurar o servidor para o IIS](how-to-configure-the-server-for-iis.md)

 

 





