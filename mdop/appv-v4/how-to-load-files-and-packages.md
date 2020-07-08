---
title: Como Carregar Arquivos e Pacotes
description: Como Carregar Arquivos e Pacotes
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797085"
---
# Como Carregar Arquivos e Pacotes


Você pode usar o procedimento a seguir para carregar arquivos e pacotes em servidores de virtualização de aplicativos.

**Observação**  Durante o processo de instalação, você especificou o local do diretório \\Content na página **caminho do conteúdo** . Esse diretório deve ser criado e configurado como um compartilhamento de arquivo padrão antes de você apontar para sua localização.

 

**Para carregar arquivos e pacotes**

1.  No computador do qual você irá transmitir aplicativos, navegue até o local que você especificou para o diretório \\Content. Se necessário, crie o diretório e configure-o como um compartilhamento de arquivo padrão.

2.  Mova os arquivos SFT dos aplicativos e pacotes virtuais para o diretório \\Content. Para manter os arquivos SFT organizados e evitar confusão, coloque aplicativos e pacotes em subpastas dedicadas.

3.  Carregue os aplicativos e pacotes de acordo com os requisitos do seu cenário e configuração, considerando as seguintes condições:

    -   Se seus aplicativos e pacotes estiverem armazenados em um servidor de gerenciamento do Application Virtualization (App-V), carregue-os pelo console de gerenciamento. Para obter mais informações, consulte [como carregar ou descarregar um aplicativo](how-to-load-or-unload-an-application.md) ou [como carregar aplicativos virtuais na área de notificação da área de trabalho](how-to-load-virtual-applications-from-the-desktop-notification-area.md).

    -   Se seus aplicativos estiverem armazenados em um servidor de streaming App-V, um servidor Web ou um computador configurado como um servidor de arquivos, os aplicativos poderão ser carregados automaticamente.

        **Observação**  O servidor de streaming App-V sonda automaticamente o diretório \\Content para aplicativos e pacotes e coloca essas informações na RAM para atender às solicitações do aplicativo.

        Os clientes do App-V devem ser configurados corretamente para recuperar aplicativos e pacotes de servidores Web e servidores de arquivos. Para obter mais informações, consulte [como configurar o cliente para a recuperação de pacotes de aplicativos](how-to-configure-the-client-for-application-package-retrieval.md).

         

## Tópicos relacionados


[Application Virtualization Server](application-virtualization-server.md)

 

 





