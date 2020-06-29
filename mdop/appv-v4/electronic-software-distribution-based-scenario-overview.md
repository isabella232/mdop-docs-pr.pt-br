---
title: Visão geral de cenário baseado em Distribuição Eletrônica de Software
description: Visão geral de cenário baseado em Distribuição Eletrônica de Software
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797957"
---
# Visão geral de cenário baseado em Distribuição Eletrônica de Software


Se você pretende usar uma solução ESD (Electronic Software Distribution) para implantar aplicativos virtuais, é importante entender os fatores que entram e são afetados por essa decisão. Este tópico descreve os benefícios de usar um cenário baseado em ESD e fornece informações sobre os métodos de publicação e streaming de pacote que você precisará considerar ao prosseguir com a implantação.

**Importante**  Seja qual for a solução ESD que você usa, você deve estar familiarizado com os requisitos de sua solução específica. Se você estiver usando o Gerenciador de configuração do Microsoft EndPoint, consulte a documentação do Configuration Manager em <https://go.microsoft.com/fwlink/?LinkId=66999> .

 

O uso de um sistema ESD existente oferece os seguintes benefícios:

-   Elimina duas infra-estruturas de gerenciamento

-   Reduz o custo de hardware adicional

-   Reduz o custo de licenças adicionais do sistema operacional e do banco de dados

## Métodos de publicação


Ao usar um cenário baseado em ESD, você tem as seguintes opções para publicar o aplicativo para os clientes:

-   **Windows Installer autônomo.** O arquivo do Windows Installer contém o manifesto e os arquivos OSD e ICO que os clientes usam para configurar um pacote. O arquivo do Windows Installer também copia o arquivo SFT para o cliente porque esse cenário não usa um servidor.

-   **Windows Installer com o manifesto do pacote.** O arquivo do Windows Installer contém o manifesto e os arquivos OSD e ICO que os clientes usam para configurar um pacote. O arquivo SFT está armazenado em um servidor. Um parâmetro de linha de comando direciona o cliente para o local do arquivo SFT.

-   **Comandos SFTMIME.** Os comandos SFTMIME são usados com os arquivos manifest, OSD, ICO e SFT para adicionar pacotes ao cliente. O arquivo de manifesto deve estar no computador cliente ou deve ser acessível por meio de um caminho UNC. Dependendo da configuração do cliente e das opções da linha de comando, os arquivos OSD, ICO e SFT podem estar no computador cliente ou em um servidor.

Para obter informações mais detalhadas sobre os métodos de publicação precedentes, consulte [determinar o método de publicação](determine-your-publishing-method.md).

## Métodos de streaming de pacote


Você precisará determinar o método que o sistema de virtualização de aplicativos usará para transmitir os pacotes de aplicativos virtuais ou arquivos SFT do servidor para os clientes. As opções de streaming a seguir estão disponíveis:

-   **Servidor de streaming do Application Virtualization.** Se você usar um servidor de streaming do Application Virtualization em sua configuração, os arquivos SFT serão transmitidos para os clientes desse servidor usando protocolos RTSP ou RTSP. Você deve instalar o software do servidor em um computador e deve configurá-lo por meio do registro, mas essa configuração não depende de serviços como SQL ou dos serviços de domínio do Active Directory. Os arquivos SFT são armazenados no servidor em um local acessível pelos clientes. As informações de publicação podem ser distribuídas para os clientes por meio de qualquer mecanismo de distribuição. No entanto, quando configurado, o cliente recebe atualizações automáticas de pacote e atualização ativa é compatível.

-   **Servidor de gerenciamento do Application Virtualization.** Se você usar um servidor de gerenciamento do Application Virtualization em sua configuração, os arquivos SFT serão transmitidos para os clientes desse servidor usando protocolos RTSP ou RTSP. Você gerencia esse servidor por meio do console de gerenciamento do Application Virtualization. Essa configuração usa um banco de dados SQL e os serviços do Active Directory. O servidor pode distribuir informações de publicação para os clientes, portanto, outros mecanismos de publicação não são necessários.

-   **Servidor de arquivos.** Se você usar um servidor de arquivos em sua configuração, os arquivos SFT serão transmitidos para os outros computadores cliente usando protocolos SMB. Os servidores de arquivos usados nessa configuração são gerenciados pela criação de listas de controle de acesso (ACLs) nos arquivos de compartilhamento e arquivos SFT. Deve-se ter cuidado para direcionar os clientes para os arquivos corretos no servidor de arquivos.

-   **Servidor IIS.** Se você usar um servidor IIS na configuração, os arquivos SFT serão transmitidos para os clientes desse servidor usando protocolos HTTP ou HTTPS. O servidor IIS é fácil de configurar e gerenciar. Deve-se tomar cuidado para direcionar os clientes para os arquivos corretos no servidor IIS.

Para obter informações mais detalhadas sobre os métodos de transmissão anteriores, consulte [determinar o método de transmissão](determine-your-streaming-method.md).

## Tópicos relacionados


[Parâmetros de linha de comando do instalador do Application Virtualization Client](application-virtualization-client-installer-command-line-parameters.md)

[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Determinar o método de publicação](determine-your-publishing-method.md)

[Determinar o método de streaming](determine-your-streaming-method.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





