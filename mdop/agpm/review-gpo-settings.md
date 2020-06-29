---
title: Analisar configurações do GPO
description: Analisar configurações do GPO
author: dansimp
ms.assetid: e82570b2-d8ce-4bf0-8ad7-8910409f3041
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 681492f423266ce3722bb1a657ee93527c6bdd7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797304"
---
# Analisar configurações do GPO


Você pode gerar relatórios baseados em HTML e baseados em XML para revisar as configurações dentro de qualquer versão de um objeto de política de grupo (GPO).

Uma conta de usuário com a função revisor, editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para revisar as configurações em qualquer versão de um GPO**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs.

3.  Clique duas vezes no GPO para exibir seu histórico.

4.  Clique com o botão direito do mouse na versão do GPO para a qual revisar as configurações, clique em **configurações**e, em seguida, clique em **relatório HTML** ou em **relatório XML** para exibir um resumo das configurações do GPO.

### Considerações adicionais

-   Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o GPO. Além disso, para exibir a lista de GPOs, você deve ter permissão de **lista de conteúdo** para o domínio.

### Referências adicionais

-   [Execução de tarefas do revisor](performing-reviewer-tasks.md)

 

 





