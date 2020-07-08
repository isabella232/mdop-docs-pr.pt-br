---
title: Configurando o firewall para os App-V Servers
description: Configurando o firewall para os App-V Servers
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798001"
---
# Configurando o firewall para os App-V Servers


Depois de instalar o servidor de gerenciamento do Microsoft Application Virtualization (App-V) ou o servidor de streaming e configurá-lo para usar o protocolo RTSP ou RTSPs, você deve criar exceções de firewall para os programas App-V.

## Configurando exceções de firewall para o servidor de gerenciamento do Application Virtualization


Crie uma exceção de firewall para **sghwdsptr.exe** e **sghwsvr.exe**. Esses programas são encontrados na pasta C:\\Arquivos de Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin em um sistema operacional de 32 bits. Se você estiver usando uma versão do sistema operacional de 64 bits, a pasta estará localizada em C:\\Arquivos de programas (x86) \\Microsoft System Center App Center Virt Management Server\\App virt gerenciamento Server\\bin.

## Configurando exceções de firewall para o servidor de streaming do Application Virtualization


Crie uma exceção de firewall para **sglwdsptr.exe** e **sglwsvr.exe**. Esses programas são encontrados na pasta C:\\Arquivos de Files\\Microsoft System Center virt streaming Server\\App virt streaming Server\\bin em um sistema operacional de 32 bits. Se você estiver usando uma versão do sistema operacional de 64 bits, a pasta estará localizada em C:\\Arquivos de programas (x86) \\Microsoft System Center App Virt streaming Server\\App virt streaming Server\\bin.

## Tópicos relacionados


[Como configurar os servidores para a implantação baseada em servidor](how-to-configure-servers-for-server-based-deployment.md)

[Como instalar e configurar o aplicativo padrão](how-to-install-and-configure-the-default-application.md)

 

 





