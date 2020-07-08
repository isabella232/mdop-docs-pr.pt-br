---
title: Como configurar o Servidor de Arquivos
description: Como configurar o Servidor de Arquivos
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797194"
---
# Como configurar o Servidor de Arquivos


Você pode usar o procedimento a seguir para configurar um computador local que é usado como um compartilhamento de arquivos e transmite aplicativos para o cliente da área de trabalho do Application Virtualization e para o cliente para serviços de área de trabalho remota (anteriormente serviços de terminal). Esse cenário é usado quando você não deseja adicionar uma infraestrutura de servidor adicional ao seu ambiente de hardware existente.

Se você estiver usando um servidor de gerenciamento do Application Virtualization como um ponto de distribuição para o compartilhamento de arquivos instalado em escritórios locais, você deve configurar esse servidor para que os aplicativos virtuais possam ser transmitidos para os computadores que são usados como compartilhamentos de arquivos. Ao configurar os servidores e os compartilhamentos de arquivos, você está configurando o diretório de conteúdo em que os arquivos SFT são carregados e armazenados. Os arquivos SFT contêm o aplicativo virtual (ou aplicativos).

**Importante**  Para que os aplicativos sejam transmitidos corretamente para o cliente da área de trabalho de virtualização do aplicativo e para os serviços de área de trabalho remota, o arquivo SFT flui do diretório de conteúdo no servidor em que você armazena o aplicativo virtual; o arquivo ICO (ícone) e o arquivo OSD (Open Software Descriptor) podem ser configurados para transmitir de um servidor diferente.

 

**Para configurar o servidor de arquivos do Application Virtualization**

1.  Conclua o procedimento de instalação a seguir para configurar o servidor que é usado como o ponto de distribuição:

    [Como instalar o Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Observação**  Durante o procedimento de instalação, especifique o local do diretório \\Content na tela **caminho do conteúdo** .

     

2.  Crie um diretório \\Content, que corresponde ao diretório especificado ao instalar o servidor, em cada computador que você está usando como um compartilhamento de arquivos.

    **Importante**  Configure os clientes da área de trabalho do Application Virtualization para transmitir aplicativos do computador que você está usando como um compartilhamento de arquivos, em vez de um servidor do Application Virtualization ou servidor IIS.

     

3.  Quando o diretório \\Content é criado, configure esse diretório como um compartilhamento de arquivo padrão.

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Como configurar os Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)

[Como configurar os Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)

[Como configurar o servidor para o IIS](how-to-configure-the-server-for-iis.md)

 

 





