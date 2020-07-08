---
title: Como configurar o servidor para o IIS
description: Como configurar o servidor para o IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797186"
---
# Como configurar o servidor para o IIS


Antes que os aplicativos virtuais possam ser transmitidos para o cliente da área de trabalho do Application Virtualization e para o cliente para serviços de área de trabalho remota (antes serviços de terminal), os servidores IIS devem ser configurados. Ao configurar os servidores, você está configurando o diretório de conteúdo em que os arquivos SFT são carregados e armazenados. Os arquivos SFT contêm o aplicativo virtual (ou aplicativos).

**Para configurar o diretório de conteúdo no servidor IIS**

1.  No servidor que está executando o IIS, localize o diretório que você deseja usar como o diretório de conteúdo ou crie o diretório, caso ele não exista. Configurar esse diretório como um compartilhamento de arquivo padrão.

2.  No servidor que está executando o IIS, abra o **Gerenciador do IIS**e, no site padrão, crie um diretório virtual que corresponda ao diretório de conteúdo que você criou no servidor. Verifique se a opção **leitura** está marcada.

3.  Dê ao diretório virtual recém-criado o **conteúdo**do alias.

4.  Aceite todas as outras configurações padrão para este diretório virtual.

5.  Configure as permissões do sistema de arquivos NTFS para o diretório de conteúdo e as pastas de pacote sob o diretório de conteúdo usando os grupos de segurança nos serviços de domínio do Active Directory que você definiu anteriormente.

**Observação**  Se você estiver usando o IIS para publicar os arquivos ICO e OSD, será preciso configurar um tipo MIME para OSD = TXT; caso contrário, o IIS não servirá os arquivos ICO e OSD para clientes. Se estiver usando o IIS para publicar pacotes (arquivos SFT), você deve configurar um tipo MIME para SFT = Binary; caso contrário, o IIS não servirá os arquivos SFT para clientes.

 

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Como configurar os Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)

[Como configurar os Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)

[Como configurar o Servidor de Arquivos](how-to-configure-the-file-server.md)

 

 





