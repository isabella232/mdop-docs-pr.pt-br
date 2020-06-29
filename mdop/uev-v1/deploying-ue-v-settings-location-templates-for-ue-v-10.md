---
title: Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0
description: Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800009"
---
# Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0


O Microsoft User Experience Virtualization (UE-V) usa modelos de local de configurações (arquivos XML) que definem as configurações que são capturadas e aplicadas pela virtualização da experiência do usuário. O UE-V inclui um conjunto de modelos padrão, bem como uma ferramenta, o UE-V Generator, que permite criar modelos de localização de configurações personalizadas. Depois de criar um modelo de local de configurações, você deve testá-lo para garantir que as configurações do aplicativo sejam referidas corretamente em um ambiente de teste. Em seguida, você pode implantar com segurança o modelo de local de configurações em computadores da empresa.

Os modelos de locais de configurações podem ser implantados usando ESD (Enterprise Software Distribution), preferências de política de grupo ou configurando um catálogo de modelos de configurações do UE-V. Os modelos implantados usando um ESD ou uma política de grupo devem ser registrados pelo UE-V WMI ou pelo PowerShell. Os modelos armazenados na localização do catálogo de modelos de configurações são automaticamente registrados pelo UE-V Agent.

## Implantar os modelos de local de configurações com um caminho de catálogo de modelos de configurações


O caminho do catálogo de modelos de local de configurações do UE-V pode ser definido usando os seguintes métodos: política de grupo, parâmetros de linha de comando de instalação de agente, WMI ou PowerShell. Após a definição do caminho do catálogo de modelos, o UE-V Agent recupera os modelos novos ou atualizados deste local. O UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos encontrados nessa pasta. Os modelos que foram adicionados ou atualizados nesta pasta desde a última verificação são registrados pelo UE-V Agent. O UE-V Agent também cancela o registro de modelos que foram removidos desta pasta. Os modelos são registrados e não registrados uma vez por dia pelo Agendador de tarefas.

**Para usar o caminho do catálogo de modelos de configurações para implantar os modelos de local das configurações do UE-V**

1.  Navegue até a pasta de compartilhamento de rede que é definida como o catálogo de modelos de configurações.

2.  Adicione, remova ou atualize os modelos de local de configurações no catálogo de modelos de configurações para refletir a configuração de modelo de agente do UE-V desejada para computadores UE-V.

3.  Os modelos em computadores são atualizados diariamente com base nas alterações do catálogo de modelos de configurações.

4.  Abra um prompt de comando elevado e navegue até **% Program Files%\\Microsoft de experiência do usuário \ \ agente \ \ &lt; x86 &gt; ou x64 **e, em seguida, execute **ApplySettingsTemplateCatalog.exe** para atualizar manualmente os modelos em um computador que executa o UE-V Agent.

## Tópicos relacionados


[Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0](index.md)

[Implantação da UE-V 1.0](deploying-ue-v-10.md)

[Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





