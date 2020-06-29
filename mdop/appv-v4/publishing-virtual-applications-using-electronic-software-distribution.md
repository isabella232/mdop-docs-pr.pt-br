---
title: Publicação de aplicativos virtuais usando a Distribuição Eletrônica de Software
description: Publicação de aplicativos virtuais usando a Distribuição Eletrônica de Software
author: dansimp
ms.assetid: 295fbc1d-ed1c-43b4-aeee-0df384d4e630
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0354fc1226aa78d947dd764a0ab6157b563a321
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796786"
---
# Publicação de aplicativos virtuais usando a Distribuição Eletrônica de Software


Um sistema ESD (Electronic Software Distribution) foi projetado para mover eficientemente o software para vários computadores diferentes em conexões de rede lentas ou rápidas. Com o Application Virtualization, usando um sistema ESD, você pode usar um dos seguintes métodos para distribuir seus pacotes de aplicativo virtual:

-   Configure o seu sistema ESD para distribuir os pacotes diretamente para cada computador cliente usando a versão do Windows Installer do pacote gerado pelo Application Virtualization Sequencer. O arquivo do Windows Installer contém os ícones, as informações de definição do pacote e o conteúdo e, quando você usa o Windows Installer, ele publica os ícones na área de trabalho do Windows e no menu iniciar e carrega o conteúdo do pacote no cache do cliente do Application Virtualization. O usuário pode começar imediatamente a usar os aplicativos sem mais requisitos de configuração. A atualização de um pacote para uma versão mais recente é realizada usando o Windows Installer para desinstalar o arquivo package.msi e, em seguida, instalar a nova versão.

-   Coloque o conteúdo do pacote em um ponto de distribuição de software ou em um servidor de streaming do Application Virtualization que seja facilmente acessível para os computadores cliente em uma conexão de rede com uma boa largura de banda, como uma LAN. Por exemplo, você pode usar os computadores de ponto de distribuição de sistema ESD existentes em cada filial. Usando parâmetros de linha de comando para definir a origem de streaming a partir da qual os clientes transmitirão o pacote de aplicativo virtual, o sistema ESD implantaria a versão do Windows Installer do pacote em cada cliente. O sistema ESD também pode ser usado para copiar o arquivo SFT que contém o conteúdo do pacote para o compartilhamento de arquivos em todos os servidores de streaming. A atualização de um pacote para uma versão mais recente é realizada usando o Windows Installer para desinstalar o arquivo de package.msi e, em seguida, instalar a nova versão.

-   Como uma alternativa para usar o arquivo autocontido do Windows Installer em qualquer um dos modos anteriores para implantar os pacotes, você pode controlar a implantação de forma muito mais detalhada usando o idioma da linha de comando do Application Virtualization SFTMIME. Isso fornece muitos comandos para controlar todos os aspectos de gerenciamento dos pacotes. Embora o SFTMIME seja potente, ele também é complexo, portanto, os administradores devem planejar criar todos os comandos como scripts e testá-los exaustivamente em um ambiente de teste antes do uso da produção. Para obter mais informações sobre os comandos SFTMIME disponíveis, consulte [referência de comandos do SFTMIME](sftmime--command-reference.md).

## Tópicos relacionados


[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

[Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)

[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





