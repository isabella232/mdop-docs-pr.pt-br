---
title: Como configurar ou desabilitar o tamanho de banco de dados
description: Como configurar ou desabilitar o tamanho de banco de dados
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796950"
---
# Como configurar ou desabilitar o tamanho de banco de dados


Você pode usar os procedimentos a seguir no console de gerenciamento do servidor do Application Virtualization para especificar o tamanho (em MB) do uso do sistema do Application Virtualization que você deseja armazenar no banco de dados.

Quando o tamanho dos dados armazenados alcança 95% (a marca-d ' água alta) do limite especificado, o sistema excluirá 10% dos dados de uso, deixando 85% dos dados. Os dados de uso do pacote e do aplicativo serão excluídos. Quando o banco de dados cresce grande o suficiente e se aproxima da marca d' água alta, uma mensagem de aviso é enviada ao log do SQL Server para informar que esse limite foi atingido. Esse aviso é necessário porque a ação de limpeza pode afetar a saída dos relatórios. Ele também ajudará você a decidir se precisa aumentar o tamanho máximo do banco de dados, reduzir o número de meses de dados de uso a serem mantidos ou desativar o nível de log.

**Observação**  As opções **sem limite de tamanho** e **manter todas as** opções de uso são fornecidas para que você possa desabilitar o relatório de uso e a limpeza do banco de dados. Selecionar esses itens limpará também o log de transação do banco de dados. (Todas as transações confirmadas do Microsoft SQL Server serão removidas do log de banco de dados.)

 

**Para configurar o tamanho do banco de dados**

1.  Clique com o botão direito do mouse no nó do sistema de virtualização do aplicativo no painel esquerdo e selecione **Opções do sistema**.

2.  Selecione a guia **banco de dados** .

3.  Selecione o botão de opção **tamanho máximo do banco de dados (MB)** ou **limite de tamanho** .

4.  Se você optar por especificar um tamanho de banco de dados, as práticas recomendadas recomendam que você insira um número entre 512 e 4096 MB. O tamanho padrão é de 1024 MB e, se você precisar aumentar o tamanho do banco de dados, o valor máximo que você pode inserir é 2.147.483.647. Se você selecionar **sem limite de tamanho**, o banco de dados será aumentado até atingir o limite de tamanho do disco.

5.  Clique em **aplicar** ou em **OK**.

**Para desabilitar os limites de tamanho do banco de dados**

1.  Clique com o botão direito do mouse no nó do sistema do Application Virtualization no painel **escopo** e selecione **Opções do sistema**.

2.  Selecione a guia **banco de dados** .

3.  Selecione os botões de opção **sem limite de tamanho** e **manter todos os usos** .

4.  Clique em **aplicar** ou em **OK**.

## Tópicos relacionados


[Como personalizar um Application Virtualization System no Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Como configurar ou desabilitar os relatórios de uso](how-to-set-up-or-disable-usage-reporting.md)

 

 





