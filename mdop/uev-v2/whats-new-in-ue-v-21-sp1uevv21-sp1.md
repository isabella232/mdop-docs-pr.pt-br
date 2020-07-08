---
title: Novidades da UE-V 2.1 SP1
description: Novidades da UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800070"
---
# Novidades da UE-V 2.1 SP1


O User Experience Virtualization 2,1 SP1 oferece esses novos recursos e funcionalidades em comparação com o UE-V 2,1. As [notas de versão do Microsoft User Experience Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) fornecem mais informações sobre a versão do UE-v 2,1 SP1.

## Suporte para Windows 10


O UE-V 2,1 SP1 adiciona suporte para o Windows 10, além do mesmo software que é compatível com versões anteriores do UE-V.

### Compatibilidade com o Microsoft Azure

O Windows 10 permite que os usuários corporativos sincronizem as configurações do aplicativo do Windows e do sistema operacional do Windows com o Azure em vez do OneDrive. Você pode usar a funcionalidade de sincronização do Windows 10 Enterprise em conjunto com o UE-V para computadores somente associados a um domínio local. Para habilitar a coexistência entre o Windows 10 e o UE-V, você deve desabilitar os seguintes modelos de UE-V usando o PowerShell em cada cliente ou política de grupo.

Na política de grupo, no nó Microsoft User Experience Virtualization, defina estas configurações de política:

-   Habilitar "não sincronizar aplicativos do Windows"

-   Desabilitar "sincronizar configurações do Windows"

### O comportamento de sincronização de configurações mudou para suporte do Windows 10

As configurações de barra de tarefas de roaming do UE-V 2,1 SP1 entre dispositivos Windows 10. No entanto, o UE-V não sincroniza as configurações da barra de tarefas entre dispositivos Windows 10 e dispositivos que executam sistemas operacionais anteriores.

Além disso, o UE-V 2,1 SP1 não sincroniza as configurações entre a calculadora da Microsoft no Windows 10 e a calculadora da Microsoft em sistemas operacionais anteriores.

## Suporte adicionado para impressoras de rede de roaming


O UE-V 2,1 SP1 permite que impressoras de rede sejam movidas entre dispositivos para que um usuário tenha acesso às suas impressoras de rede quando estiver conectado a qualquer dispositivo na rede. Isso inclui o roaming da impressora definida como padrão.

O roaming da impressora no UE-V exige um dos seguintes cenários:

-   O servidor de impressão pode baixar o driver necessário quando ele está em roaming para um novo dispositivo.

-   O driver para a impressora de rede de roaming está pré-instalado em qualquer dispositivo que precise acessar a impressora de rede.

-   O driver da impressora pode ser obtido no Windows Update.

**Observação**  O recurso de roaming da impressora UE-V **não transfere** preferências ou configurações de impressora, como impressão em frente e verso.

 

## Modelo de local de configurações do Office 2013


O UE-V 2,1 e o 2,1 SP1 incluem o modelo de local de configurações do Microsoft Office 2013 com suporte à assinatura do Outlook aprimorado. Adicionamos a sincronização das configurações de assinatura padrão para emails novos, de resposta e encaminhados. Os clientes não precisam mais escolher as configurações de assinatura padrão.

**Observação**  Um perfil do Outlook deve ser criado para qualquer dispositivo no qual o usuário deseja sincronizar a assinatura do Outlook. Se o perfil ainda não tiver sido criado, o usuário poderá criar um e, em seguida, reiniciar o Outlook nesse dispositivo para habilitar a sincronização de assinatura.

 

Anteriormente, o UE-V incluía modelos de local de configurações do Microsoft Office 2010 que foram automaticamente distribuídos e registrados com o UE-V Agent. O UE-V 2,1 funciona com o Office 365 para determinar se as configurações do Office 2013 estão em roaming pelo Office 365. Se as configurações estiverem em roaming pelo Office 365, elas não serão em roaming pela UE-V. [Visão geral sobre as configurações de usuário e roaming do Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fornecem mais informações.

Para habilitar a sincronização de configurações usando o UE-V 2,1, siga um destes procedimentos:

-   Usar a política de grupo para desabilitar a sincronização do Office 365

-   Não habilite a experiência de sincronização do Office 365 durante a instalação do Office 2013

O UE-V 2,1 envia os [modelos do office 2013 e do office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Esta versão remove os modelos do Office 2007. Os usuários ainda podem usar os modelos do Office 2007 do UE-V 2,0 ou versões anteriores e ainda podem obter os modelos da Galeria de modelos do UE-V localizada [aqui](https://go.microsoft.com/fwlink/p/?LinkID=246589).






## Tópicos relacionados


[Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





