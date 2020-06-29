---
title: Planejar a implantação de modelo personalizado para a UE-V 1.0
description: Planejar a implantação de modelo personalizado para a UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797876"
---
# Planejar a implantação de modelo personalizado para a UE-V 1.0


O Microsoft User Experience Virtualization (UE-V) usa modelos de local de configurações (arquivos XML) que definem as configurações que são capturadas e aplicadas pela UE-V. Você pode usar o UE-V Generator para criar modelos de local de configurações personalizadas que permitem aos usuários fazer roaming das configurações de aplicativos diferentes daqueles incluídos nos modelos UE-V padrão. Depois de testar o modelo personalizado para garantir que as configurações do aplicativo sejam referidas corretamente em um ambiente de teste, você pode implantar esses modelos de local de configurações em computadores na empresa.

Você pode implantar seus modelos de local de configurações personalizadas com uma infraestrutura de implantação existente, como o ESD (Enterprise Software Distribution), com preferências de política de grupo ou configurando um catálogo de modelos de configurações do UE-V. Os modelos implantados usando ESD ou a política de grupo devem ser registrados com o UE-V WMI ou o PowerShell.

## Catálogo de modelos de configurações


O catálogo de modelos de configurações de experiência de usuário da experiência do usuário é um caminho de pasta em computadores UE-V ou um compartilhamento de rede de servidor de mensagens (SMB) que armazena todos os modelos de local de configurações personalizadas. O UE-V Agent recupera modelos novos ou atualizados deste local. O UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos desta pasta. Os modelos que foram adicionados ou atualizados nesta pasta desde a última vez que a pasta foi verificada são registrados pelo UE-V Agent. O UE-V Agent cancela o registro de modelos que são removidos desta pasta. Por padrão, os modelos são registrados e não registrados uma vez por dia em 3:30 A.M. Hora local pelo Agendador de tarefas. Para obter mais informações sobre as tarefas do UE-V, consulte [alterando a frequência de tarefas agendadas de UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).

Você pode configurar o caminho do catálogo de modelos de configurações usando as opções de linha de comando de instalação, a política de grupo, o WMI ou o PowerShell. Os modelos armazenados no caminho do catálogo de modelos de configurações são automaticamente registrados e não são registrados por uma tarefa agendada. Você pode personalizar essa tarefa agendada conforme necessário.

## Substituir os modelos padrão da Microsoft


O UE-V Agent instala um grupo padrão de modelos de local de configurações para aplicativos comuns da Microsoft e configurações do Windows. Se a sua empresa precisa de versões personalizadas desses modelos, o UE-V Agent pode ser configurado para usar um catálogo de modelos de configurações e, em seguida, substituir os modelos padrão da Microsoft.

Durante a instalação do UE-V Agent, o parâmetro de linha de comando, `RegisterMSTemplates` pode ser usado para desabilitar o registro dos modelos padrão da Microsoft. Para obter mais informações sobre como definir os parâmetros do UE-V, consulte [planejando métodos de configuração do UE-v](planning-for-ue-v-configuration-methods.md).

Ao usar a política de grupo para definir o caminho do catálogo de modelos de configurações, você pode optar por substituir os modelos padrão da Microsoft. Se você definir as configurações de política para substituir os modelos padrão da Microsoft, todos os modelos padrão da Microsoft instalados pelo UE-V Agent serão excluídos do computador e somente os modelos localizados no catálogo de modelos de configurações serão usados. A configuração do UE-V Agent `RegisterMSTemplates` deve ser definida como true para substituir o modelo padrão da Microsoft.

**Observação**  Se você desabilitar essa configuração de política depois que ela for habilitada, o UE-V Agent não restaurará os modelos padrão da Microsoft.

 

Se houver modelos personalizados no catálogo de modelos de configurações que usam a mesma ID que os modelos padrão da Microsoft, e o UE-V Agent não estiver configurado para substituir os modelos padrão da Microsoft, os modelos da Microsoft no catálogo serão ignorados.

Você também pode substituir os modelos padrão usando os recursos do PowerShell do UE-V. Para substituir o modelo padrão da Microsoft pelo PowerShell, cancele o registro de todos os modelos padrão da Microsoft e registre os modelos personalizados.

**Observação**  Os pacotes de configurações antigas permanecem no local de armazenamento configurações, mesmo que novos modelos de configurações sejam implantados para um aplicativo. Esses pacotes não são lidos pelo agente, mas nenhum deles é excluído automaticamente.

 

## Tópicos relacionados


[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

[Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planejamento para os métodos de configuração da UE-V](planning-for-ue-v-configuration-methods.md)

Planejando a implantação de modelos personalizados
 

 





