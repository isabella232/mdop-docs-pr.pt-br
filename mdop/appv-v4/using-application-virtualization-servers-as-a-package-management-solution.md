---
title: Uso do Application Virtualization Servers como uma Solução de Gerenciamento de Pacotes
description: Uso do Application Virtualization Servers como uma Solução de Gerenciamento de Pacotes
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796662"
---
# Uso do Application Virtualization Servers como uma Solução de Gerenciamento de Pacotes


Se você não tiver um sistema ESD existente para implantar sua solução de virtualização de aplicativo ou não quiser usar uma, será necessário instalar um ou mais servidores de gerenciamento do Application Virtualization como núcleo da arquitetura do seu sistema. O servidor de gerenciamento do Application Virtualization requer um computador servidor dedicado e precisa de um banco de dados do Microsoft SQL Server. O banco de dados pode estar no mesmo servidor ou pode ser configurado em um servidor de banco de dados corporativo que seja acessível ao servidor de gerenciamento do Application Virtualization em uma conexão LAN de alta velocidade. Além disso, você precisará instalar o console de gerenciamento do Microsoft Application Virtualization, no servidor de gerenciamento do Application Virtualization ou em uma estação de trabalho de gerenciamento designado, e será necessário instalar o serviço Web de gerenciamento do Microsoft Application Virtualization, que também pode ser instalado no servidor de gerenciamento do Application Virtualization ou em um servidor IIS separado. O console de gerenciamento do Application Virtualization é usado para se conectar ao serviço Web de gerenciamento do Application Virtualization, permitindo que o administrador do sistema interaja com o servidor de gerenciamento do Application Virtualization.

**Observação**  O acesso aos aplicativos é controlado por meio de grupos de segurança nos serviços de domínio Active Directory, portanto, você precisará planejar um processo para configurar um grupo de segurança para cada aplicativo virtualizado e para gerenciar quais usuários serão adicionados a cada grupo. O administrador do servidor de gerenciamento do Application Virtualization configura o servidor para usar esses grupos do Active Directory, e o servidor controla automaticamente o acesso aos pacotes com base em associações de grupo do Active Directory.

 

## Nesta seção


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Visão geral dos Componentes do Application Virtualization System](overview-of-the-application-virtualization-system-components.md)  
Lista e descreve os componentes principais do sistema de gerenciamento do Microsoft Application Virtualization.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Publicação de aplicativos virtuais usando os Application Virtualization Management Servers](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
Fornece uma breve visão geral de como os aplicativos virtuais são publicados em um cenário de implantação baseado em servidor do Application Virtualization.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
Descreve as opções disponíveis para usar os servidores de streaming do Application Virtualization em conjunto com a implementação baseada em servidor de gerenciamento de virtualização de aplicativos.

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





