---
title: Executar tarefas de administração de AGPM
description: Executar tarefas de administração de AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799068"
---
# Executar tarefas de administração de AGPM


O gerenciamento avançado de política de grupo (AGPM) permite que um administrador do AGPM (controle total) Configure opções em todo o domínio e delegue permissões para Aprovadores, editores, revisores e administradores do AGPM. Por padrão, um administrador do AGPM é alguém que tem controle total – todas as permissões do AGPM e, portanto, podem executar tarefas associadas a qualquer função.

Em um ambiente no qual várias pessoas desenvolvem objetos de política de grupo (GPOs), você pode optar por permitir que todos os administradores de política de grupo realizem as mesmas tarefas e tenham o mesmo nível de acesso. Ou você pode optar por permitir que os administradores do AGPM deleguem permissões para editores que podem alterar GPOs e para Aprovadores que implantam GPOs no ambiente de produção. Os administradores do AGPM podem configurar permissões para atender às necessidades da sua organização.

-   [Configurando o gerenciamento avançado de política de grupo](configuring-advanced-group-policy-management-agpm40.md): Configure a conexão do servidor de AGPM e a notificação por email, acesse o acesso a GPOs no ambiente de produção e configure o registro em log e o rastreamento para solução de problemas.

-   [Gerenciar o arquivo](managing-the-archive-agpm40.md): delegar o acesso a GPOs no arquivo morto, limitar o número de versões de cada GPO armazenado, importar um GPO de outro domínio e fazer backup e restaurar o arquivo morto.

-   [Gerenciando o serviço do AGPM](managing-the-agpm-service-agpm40.md): Pare e inicie o serviço do AGPM ou altere o caminho do arquivo do AGPM, a conta de serviço do AGPM ou a porta que o serviço do AGPM escuta.

-   [Mova o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive-agpm40.md): Mova o serviço do AGPM, o arquivo ou ambos para um servidor diferente.

**Observação**  Como a função de administrador do AGPM inclui as permissões para todas as outras funções, um administrador do AGPM pode executar as tarefas geralmente associadas a qualquer outra função.

[Executar tarefas do aprovador](performing-approver-tasks-agpm40.md), como criar, implantar ou excluir GPOs

[Executar tarefas do editor](performing-editor-tasks-agpm40.md), como editar, renomear, rotular ou importar GPOs, criar modelos ou definir um modelo padrão

[Executar tarefas do revisor](performing-reviewer-tasks-agpm40.md), como configurações de revisão e comparar GPOs

 

### Considerações adicionais

Por padrão, a função de administrador do AGPM tem controle total – todas as permissões do AGPM:

-   Conteúdo da lista

-   Ler configurações

-   Editar configurações

-   Criar GPO

-   Implantar GPO

-   Excluir GPO

-   GPO de exportação

-   Importar GPO

-   Criar modelo

-   Opções de modificação

-   Modificar a segurança

As permissões de **modificação** e **modificação de segurança** são exclusivas da função de administrador do AGPM.

 

 





