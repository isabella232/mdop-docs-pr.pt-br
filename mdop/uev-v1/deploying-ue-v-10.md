---
title: Implantação da UE-V 1.0
description: Implantação da UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800014"
---
# Implantação da UE-V 1.0


Há várias configurações de implantação diferentes que o Microsoft User Experience Virtualization (UE-V) suporta. Esta seção inclui informações gerais e procedimentos passo a passo para ajudar você a executar com êxito as tarefas que devem ser concluídas em diferentes estágios da implantação.

## Informações de implantação para UE-V


Uma implantação do UE-V exige um local de armazenamento de configurações em um compartilhamento de rede e um agente do UE-V instalado em cada computador que sincroniza as configurações. Os modelos de política de grupo UE-V podem ser usados para gerenciar as configurações de UE-V. Os tópicos a seguir descrevem como implantar esses recursos.

[Implantação da localização do armazenamento de configurações para a UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

Todas as implantações de UE-V exigem um local de armazenamento de configurações onde os pacotes de configurações que contêm os valores de configuração sincronizados estão localizados.

[Implantação do agente da UE-V](deploying-the-ue-v-agent.md)

Para sincronizar as configurações usando o UE-V, um computador deve ter o UE-V Agent instalado e em execução.

[Instalação dos modelos ADMX da Política de Grupo da UE-V](installing-the-ue-v-group-policy-admx-templates.md)

Você pode usar a política de grupo para pré-configurar as configurações de UE-V antes de implantar o UE-V Agent, bem como a configuração padrão de UE-V.

## Informações de implantação para a implantação de modelos personalizados


Se você planeja criar modelos de localização de configurações personalizadas para aplicativos que não sejam os aplicativos Microsoft incluídos na UE-V, como aplicativos de linha de negócios, poderá implantar um catálogo de modelos de configurações e instalar o UE-V Generator para criar esses modelos. Para obter mais informações, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

[Instalação do gerador da UE-V](installing-the-ue-v-generator.md)

Use o UE-V Generator para criar, editar e validar modelos de local de configurações personalizadas que ajudam a sincronizar as configurações de aplicativos diferentes dos aplicativos padrão.

[Implantação do catálogo de modelos de configurações para a UE-V 1.0](deploying-the-settings-template-catalog-for-ue-v-10.md)

Se você precisar implantar modelos de localização de configurações personalizadas para dar suporte a aplicativos diferentes dos aplicativos padrão no UE-V Agent, será preciso configurar um catálogo de modelos de configurações para armazená-los.

[Implantação dos modelos de localização das configurações da UE-V para a UE-V 1.0](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

Se você precisar sincronizar aplicativos diferentes dos aplicativos padrão no UE-V Agent, os modelos de local de configuração personalizada criados com o UE-V Generator podem ser distribuídos para o catálogo de modelos de configurações do UE-V.

**Observação**  A implantação de modelos personalizados exige um catálogo de modelos de configurações. Os modelos de aplicativos padrão da Microsoft são implantados com o UE-V Agent.

 

## Tópicos para este produto


[Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0](index.md)

[Introdução à User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

[Solução de problemas da UE-V 1.0](troubleshooting-ue-v-10.md)

 

 





