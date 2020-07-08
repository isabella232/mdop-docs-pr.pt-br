---
title: Configurar uma conexão de servidor do AGPM
description: Configurar uma conexão de servidor do AGPM
author: dansimp
ms.assetid: ae78dc74-111d-4509-b0a6-e8b8b451c22a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 50968d8b1b1eb5d464c6dbdb251354a9dc691d62
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797439"
---
# Configurar uma conexão de servidor do AGPM


Para garantir que você esteja conectado ao arquivo central correto, examine a configuração da conexão do servidor do AGPM. Se um administrador do AGPM (controle total) não configurou uma conexão do servidor do AGPM para você, você deve configurá-lo manualmente.

**Para selecionar um servidor do AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  No painel detalhes, clique na guia **servidor do AGPM** :

    -   Se as opções na guia **servidor do AGPM** não estiverem disponíveis, elas foram configuradas centralmente por um administrador do AGPM.

    -   Se as opções na guia **servidor do AGPM** estiverem disponíveis, digite o nome do computador totalmente qualificado para o servidor do AGPM (por exemplo, Server.contoso.com) e a porta na qual o serviço do AGPM escuta (por padrão, a porta 4600). Clique em **aplicar**e, em seguida, clique em **Sim** para confirmar.

### Considerações adicionais

-   Os servidores de AGPM selecionados determinam quais GPOs são exibidos na guia **conteúdo** e em que local as configurações da guia de **delegação de domínio** são aplicadas. Se não for gerenciado centralmente por meio do modelo administrativo, cada administrador da política de grupo deve definir essa configuração para apontar para o servidor do AGPM do domínio.

### Referências adicionais

-   [Como executar tarefas de editor](performing-editor-tasks-agpm30ops.md)

-   [Execução de tarefas do aprovador](performing-approver-tasks-agpm30ops.md)

-   [Execução de tarefas do revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





