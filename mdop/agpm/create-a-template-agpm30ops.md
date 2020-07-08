---
title: Criar um modelo
description: Criar um modelo
author: dansimp
ms.assetid: 8208f14a-5c18-43a7-8564-118230398cca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f6713cd0fadb651e1de028bbcf2ae3ec1dd067c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797854"
---
# Criar um modelo


A criação de um modelo permite que você salve todas as configurações de uma versão específica de um objeto de política de grupo (GPO) para usar como ponto de partida para a criação de novos GPOs.

**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.

 

Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para criar um modelo com base em um GPO existente**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** ou não **controlado** para exibir os GPOs disponíveis.

3.  Clique com o botão direito do mouse no GPO do qual você deseja criar um modelo e, em seguida, clique em **salvar como modelo**.

4.  Digite um nome para o modelo e um comentário e, em seguida, clique em **OK**.

5.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. O novo modelo aparece na guia **modelos** .

### Considerações adicionais

-   Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter **conteúdo de lista** e criar permissões de **modelo** para o domínio.

-   Renomear ou excluir um modelo não afeta os GPOs criados a partir desse modelo.

-   Como não pode ser alterado, um modelo não tem um histórico.

### Referências adicionais

-   [Criação de um modelo e ajuste de um modelo padrão](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [Solicitar a criação de um novo GPO controlado](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)

 

 





