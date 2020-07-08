---
title: Administração da UE-V 1.0
description: Administração da UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799124"
---
# Administração da UE-V 1.0


Depois de implantar o Microsoft User Experience Virtualization (UE-V), você deve ser capaz de executar várias tarefas administrativas em andamento. Estas tarefas pós-instalação estão descritas nas seções a seguir.

## Gerenciando recursos do UE-V


No curso do ciclo de vida de UE-V, você precisará gerenciar a configuração do UE-V Agent e também gerenciar locais de armazenamento para recursos como pacotes de configurações. Talvez seja necessário executar outras tarefas, como restaurar as configurações de um usuário ao estado original antes de o UE-V ter sido instalado para recuperar as configurações perdidas. Os tópicos a seguir fornecem orientação para o gerenciamento de recursos do UE-V.

### Alterando a frequência das tarefas agendadas do UE-V

Você pode configurar as tarefas agendadas que gerenciam quando o UE-V Verifica se há modelos de localização de configurações personalizadas novas, atualizadas ou removidas no catálogo de modelos de configurações.

[Alterando a frequência das tarefas agendadas do UE-V](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a>Compartilhamento de modelos de localização de configurações com a galeria de modelos da UE-V

A Galeria de modelos UE-V facilita o compartilhamento de modelos de local de configurações do UE-V. A Galeria permite carregar modelos de local de configurações para compartilhar com outras pessoas e baixar modelos que outras pessoas criaram.

[Compartilhamento de modelos de localização de configurações com a galeria de modelos da UE-V](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### Restaurando configurações do aplicativo e do Windows sincronizadas com o UE-V 1,0

Os recursos do WMI e do PowerShell da UE-V fornecem a capacidade de restaurar pacotes de configurações. Os comandos do WMI e do PowerShell permitem restaurar configurações do aplicativo e configurações do Windows para os valores de configurações que estavam no computador na primeira vez em que o aplicativo foi iniciado após o início do agente do UE-V.

[Restauração de configurações de aplicativos e do Windows com a UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### Configuração da UE-V com objetos de Política de Grupo

Você pode usar a política de grupo para modificar as configurações que definem como o UE-V sincroniza as configurações em computadores.

[Configurando o UE-V com objetos de Política de Grupo](configuring-ue-v-with-group-policy-objects.md)

### Administração da UE-V com o PowerShell e o WMI

Você pode usar o PowerShell e o WMI para modificar as configurações que definem como o UE-V sincroniza as configurações em computadores.

[Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### Migrando pacotes de configurações do UE-V

Você pode realocar os pacotes de configurações de usuário ao migrar para um novo servidor ou para fins de backup.

[Migrando pacotes de configurações do UE-V](migrating-ue-v-settings-packages.md)

## Outros recursos para este produto


[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





