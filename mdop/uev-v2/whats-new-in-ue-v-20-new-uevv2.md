---
title: Novidades da UE-V 2.0
description: Novidades da UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799577"
---
# Novidades da UE-V 2.0


O Microsoft User Experience Virtualization (UE-V) 2,0 oferece esses novos recursos e funcionalidades em comparação com o UE-V 1,0. As [notas de versão do Microsoft User Experience Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) fornecem mais informações sobre o lançamento do UE-v 2,0.

## O CSC (cache do lado do cliente) não é mais necessário


Esta versão do UE-V apresenta o **provedor de sincronização**, que substitui a necessidade do recurso de arquivos offline do Windows para dar suporte a um cache de configurações do lado do cliente.

Enquanto o UE-V é usado para sincronizar as configurações somente quando um aplicativo é aberto, fechado ou quando o Windows foi bloqueado ou desbloqueado, ou no logon ou logoff, o provedor de sincronização também...

-   Sincroniza o aplicativo local e as configurações do Windows fora da faixa usando "**disparar eventos**"

-   Usa uma **tarefa agendada** para sincronizar o pacote de armazenamento de configurações em qualquer intervalo que você escolher para seus requisitos de empresa (a cada 30 minutos por padrão)

Determinadas condições fornecem sincronização mais frequente.

-   As configurações são sincronizadas quando o usuário clica no botão **sincronizar agora** no novo aplicativo da central de configurações de empresa.

-   O provedor de sincronização também pode iniciar para um único aplicativo sem aguardar a tarefa de sincronização programada. Por exemplo, quando um aplicativo é fechado, todas as alterações de configurações são gravadas no cache local, e o processo do provedor de sincronização é executado de forma assíncrona para mover as alterações de novas configurações para o local de armazenamento de configurações.

## Sincronização do aplicativo Windows


O desenvolvedor de um aplicativo do Windows pode definir quais configurações, se houver, serão sincronizadas, e essas configurações agora podem ser capturadas e sincronizadas com UE-V.

Por padrão, o UE-V sincroniza as configurações de muitos aplicativos do Windows incluídos no Windows 8 e no Windows 8,1. Você pode modificar a lista de aplicativos sincronizados com o Windows PowerShell, a instrumentação de gerenciamento do Windows (WMI) ou a política de grupo.

**Observação**  O UE-V não sincroniza as configurações de aplicativo do Windows se os usuários do domínio vinculem suas credenciais de entrada à conta da Microsoft. Essa vinculação sincronizará as configurações com o Microsoft OneDrive para que o UE-V sincronize somente os aplicativos da área de trabalho.

 

## Vinculação de conta da Microsoft


A sincronização de configurações pelo OneDrive é nova para o Windows 8 quando você está conectado com uma conta da Microsoft ou se você vincula sua conta da Microsoft à sua conta de domínio. Se um usuário de domínio usa UE-V e se conectou a uma conta da Microsoft, então...

-   O UE-V sincroniza apenas as configurações para aplicativos da área de trabalho

-   Conta da Microsoft manipula configurações do aplicativo Windows e as configurações da área de trabalho do Windows

## Centro de configurações da empresa


Você pode fornecer a seus usuários algum controle sobre quais configurações são sincronizadas por meio de um aplicativo no UE-V 2 chamado centro de configurações da empresa. O centro de configurações da empresa é instalado juntamente com o UE-V Agent e os usuários podem acessá-lo no painel de controle, no menu **Iniciar** ou na tela **inicial** e no ícone da área de notificação do UE-V.

O centro de configurações de empresa mostra quais configurações são sincronizadas e permite que os usuários vejam o status de sincronização da UE-V. Se você permitir, os usuários poderão usar o centro de configurações da empresa para selecionar quais configurações sincronizar. Eles também podem clicar no botão **sincronizar agora** para sincronizar todas as configurações imediatamente.






## Tópicos relacionados


[Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





