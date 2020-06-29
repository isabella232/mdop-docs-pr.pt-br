---
title: Sobre a User Experience Virtualization 1.0
description: Sobre a User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799127"
---
# Sobre a User Experience Virtualization 1.0


O Microsoft User Experience Virtualization (UE-V Experience Virtualization) monitora as alterações feitas pelos usuários nas configurações do aplicativo e configurações do sistema operacional Windows. As configurações do usuário são capturadas e centralizadas em um local de armazenamento de configurações. Essas configurações podem ser aplicadas a diferentes computadores acessados pelo usuário, incluindo computadores de mesa, laptops e sessões de infraestrutura de área de trabalho virtual (VDI).

A virtualização da experiência do usuário usa modelos de local de configurações para especificar quais aplicativos e configurações do Windows nos computadores dos usuários são monitorados e centralizados. O modelo de local de configurações é um arquivo XML que especifica quais locais de arquivo e registro estão associados a cada aplicativo ou configuração do sistema operacional. O modelo não contém valores para as configurações; Ele contém somente os locais das configurações que devem ser monitoradas.

As configurações do aplicativo e as configurações do Windows são monitoradas pela UE-V quando os usuários trabalham em seus computadores. Os valores das configurações do aplicativo são armazenados no servidor de armazenamento de configurações quando o usuário fecha o aplicativo. Os valores das configurações do Windows são armazenados quando o usuário faz logoff, quando o computador está bloqueado ou quando eles são desconectados remotamente de um computador.

Um administrador pode criar um modelo de local de configurações do UE-V para especificar quais configurações do aplicativo empresarial serão transferidas para o roaming. O UE-V inclui um conjunto de modelos de local de configurações para algumas configurações do Windows e aplicativos da Microsoft. Para obter uma lista de aplicativos e configurações padrão no UE-V, consulte [planejar quais aplicativos sincronizar com o UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).

## Notas de versão do UEV 1,0


Para saber mais e saber mais sobre as últimas notícias que não o fizeram na documentação, confira [notas de versão do Microsoft User Experience Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).

## Tópicos relacionados


[Introdução à User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0](index.md)

[Arquitetura de alto nível para a UE-V 1.0](high-level-architecture-for-ue-v-10.md)

 

 





