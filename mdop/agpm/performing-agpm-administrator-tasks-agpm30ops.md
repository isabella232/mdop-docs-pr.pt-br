---
title: Executar tarefas de administração de AGPM
description: Executar tarefas de administração de AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799069"
---
# Executar tarefas de administração de AGPM


No gerenciamento avançado de política de grupo (AGPM), um administrador do AGPM (controle total) configura as opções de todo o domínio e delega permissões para Aprovadores, editores, revisores e outros administradores do AGPM. Por padrão, um administrador do AGPM é um indivíduo com controle total (todas as permissões do AGPM) e quem, portanto, pode executar tarefas associadas a qualquer função.

Em um ambiente no qual várias pessoas desenvolvem objetos de política de grupo (GPOs), você pode escolher se todos os usuários do AGPM executarão as mesmas tarefas e têm o mesmo nível de acesso ou se os administradores do AGPM delegam permissões para editores que fazem alterações em GPOs e para Aprovadores que implantam GPOs no ambiente de produção. Os administradores do AGPM podem configurar permissões para atender às necessidades da sua organização.

-   [Configurando o gerenciamento avançado de política de grupo](configuring-advanced-group-policy-management.md): Configure a conexão do servidor de AGPM e a notificação por email, acesse o acesso a GPOs no ambiente de produção e configure o registro em log e o rastreamento para solução de problemas.

-   [Gerenciar o arquivo](managing-the-archive.md): delegar o acesso a GPOs no arquivo morto e limitar o número de versões de cada GPO armazenado.

-   [Gerenciando o serviço do AGPM](managing-the-agpm-service-agpm30ops.md): Pare e inicie o serviço do AGPM ou altere o caminho do arquivo do AGPM, a conta de serviço do AGPM ou a porta que o serviço do AGPM escuta.

-   [Mova o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive.md): Mova o serviço do AGPM, o arquivo ou ambos para um servidor diferente.

Além disso, como a função de administrador do AGPM inclui as permissões para todas as outras funções, um administrador do AGPM pode executar as tarefas normalmente associadas a qualquer outra função.

-   [Executar tarefas do aprovador](performing-approver-tasks-agpm30ops.md), como criar, implantar ou excluir GPOs

-   [Executar tarefas do editor](performing-editor-tasks-agpm30ops.md), como editar, renomear, rotular ou importar GPOs, criar modelos ou definir um modelo padrão

-   [Executar tarefas do revisor](performing-reviewer-tasks-agpm30ops.md), como configurações de revisão e comparar GPOs

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

 

 





