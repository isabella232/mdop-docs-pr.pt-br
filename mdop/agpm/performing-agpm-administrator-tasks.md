---
title: Executar tarefas de administração de AGPM
description: Executar tarefas de administração de AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797733"
---
# Executar tarefas de administração de AGPM


Um administrador do AGPM (controle total) configura as permissões de todo o domínio e delega permissões para Aprovadores, editores, revisores e outros administradores do AGPM. Por padrão, um administrador do AGPM é um indivíduo com controle total (todas as permissões do gerenciamento avançado de política de grupo \ [AGPM \]) e, portanto, também pode executar tarefas associadas a qualquer função.

Em um ambiente no qual várias pessoas desenvolvem objetos de política de grupo (GPOs), você pode escolher se todos os usuários de gerenciamento de política de grupo (AGPM) avançados executarão as mesmas tarefas e têm o mesmo nível de acesso ou se os administradores do AGPM delegam permissões para editores que fazem alterações em GPOs e para Aprovadores que implantam GPOs no ambiente de produção. Os administradores do AGPM podem configurar permissões para atender às necessidades da sua organização.

-   [Configurar a conexão de servidor do AGPM](configure-the-agpm-server-connection.md)

-   [Configurar notificações por email](configure-e-mail-notification.md)

-   [Delegar acesso no nível do domínio](delegate-domain-level-access.md)

-   [Delegar acesso a um GPO individual](delegate-access-to-an-individual-gpo.md)

-   [Configurar log e rastreamento](configure-logging-and-tracing.md)

-   [Gerenciamento do serviço AGPM](managing-the-agpm-service.md)

    -   [Iniciar e parar o serviço AGPM](start-and-stop-the-agpm-service.md)

    -   [Modificar o caminho do arquivo morto](modify-the-archive-path.md)

    -   [Modificar a conta de serviço do AGPM](modify-the-agpm-service-account.md)

    -   [Modificar a porta na qual o serviço do AGPM escuta](modify-the-port-on-which-the-agpm-service-listens.md)

Além disso, como a função de administrador do AGPM inclui as permissões para todas as outras funções, um administrador do AGPM pode executar as tarefas normalmente associadas a qualquer outra função.

-   [Executar tarefas do aprovador](performing-approver-tasks.md), como criar, implantar ou excluir GPOs

-   [Executar tarefas do editor](performing-editor-tasks.md), como editar, renomear, rotular ou importar GPOs, criar modelos ou definir um modelo padrão

-   [Executar tarefas do revisor](performing-reviewer-tasks.md), como configurações de revisão e comparar GPOs

### Considerações adicionais

Por padrão, a função de administrador do AGPM tem controle total – todas as permissões do AGPM:

-   Conteúdo da lista

-   Ler configurações

-   Editar configurações

-   Criar GPO

-   Implantar GPO

-   Excluir GPO

-   Opções de modificação

-   Modificar a segurança

-   Criar modelo

As permissões de **modificação** e **modificação de segurança** são exclusivas da função de administrador do AGPM.

 

 





