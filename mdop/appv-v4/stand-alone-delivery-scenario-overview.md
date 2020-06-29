---
title: Visão geral de cenário de entrega autônoma
description: Visão geral de cenário de entrega autônoma
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796699"
---
# Visão geral de cenário de entrega autônoma


O cenário de entrega autônomo é uma solução de virtualização de aplicativos ideal para ambientes em que a conectividade de largura de banda baixa ou nenhuma conectividade limita a capacidade do cliente de desktop do Application Virtualization para transmitir aplicativos de servidores centralizados. Nesses ambientes, os usuários geralmente trabalham remotamente e os proprietários de dispositivos instalam aplicativos usando arquivos do Windows Installer.

Você pode usar o sequenciador do Application Virtualization para criar aplicativos sequenciados que incluem arquivos do Windows Installer. Esses pacotes incluem os aplicativos virtualizados, as informações de publicação e as rotinas de instalação necessárias para instalar os pacotes nos sistemas do cliente. O instalador adiciona o pacote de aplicativo virtual ao cliente da área de trabalho do Microsoft Application Virtualization. As informações da publicação são configuradas para carregar aplicativos de um local local em vez de transmiti-los em uma WAN. Os usuários podem se conectar temporariamente a uma rede para recuperar os arquivos do Windows Installer ou executá-los a partir de um DVD.

O cenário de entrega autônomo oferece aos usuários os seguintes benefícios:

-   Operação de implantação simples.

-   Rede e servidores não necessários em tempo de execução.

-   Aplicativos previamente armazenados em cache e disponíveis para todos os usuários.

O cenário de entrega autônomo tem as seguintes limitações:

-   Relatórios internos e automatizados não estão disponíveis; relatórios devem ser gerados com ferramentas de relatórios externos.

-   Os aplicativos devem ser entregues ao cliente manualmente, como os arquivos originais do Windows Installer.

## Tópicos relacionados


[Como instalar manualmente o Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md)

 

 





