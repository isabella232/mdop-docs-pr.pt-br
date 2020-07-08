---
title: Analisar links do GPO
description: Analisar links do GPO
author: dansimp
ms.assetid: 5ae95afc-2b89-45cf-916c-efe2d43b2211
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6532a669c6841c2342514c0911f74bc0b1fbc86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797309"
---
# Analisar links do GPO


Você pode exibir um diagrama que mostra onde um objeto de política de grupo (GPO) ou GPOs selecionados estão vinculados a unidades organizacionais. Os diagramas de link de GPO são atualizados toda vez que o GPO é controlado, importado ou verificado.

Uma conta de usuário com a função revisor, editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

## Revisão de links de GPO


-   [Para um ou mais GPOs](#bkmk-gpos)

-   [Para uma ou mais versões de um GPO](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**Para exibir links de GPO para um ou mais GPOs**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado**, **pendente**ou **Lixeira** para exibir os GPOs.

3.  Selecione um ou mais GPOs para os quais exibir links, clique com o botão direito do mouse em um GPO selecionado, clique em **configurações**e, em seguida, clique em **vínculos de GPO** para exibir um diagrama de domínios e unidades organizacionais com links para o (s) GPO (s) selecionado (s).

### <a href="" id="bkmk-gpo-versions"></a>

**Para exibir links de GPO para uma ou mais versões de um GPO**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia de **Lixeira** ou **controlado** para exibir os GPOs.

3.  Clique duas vezes no GPO para exibir seu histórico.

4.  Clique com o botão direito do mouse na versão do GPO para a qual revisar as configurações, clique em **configurações**e, em seguida, clique em **relatório HTML** ou em **relatório XML** para exibir um resumo das configurações do GPO.

### Considerações adicionais

-   Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o GPO. Além disso, para exibir a lista de GPOs, você deve ter permissão de **lista de conteúdo** para o domínio.

### Referências adicionais

-   [Execução de tarefas do revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





