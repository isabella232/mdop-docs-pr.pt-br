---
title: Como configurar ou desabilitar os relatórios de uso
description: Como configurar ou desabilitar os relatórios de uso
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796947"
---
# Como configurar ou desabilitar os relatórios de uso


Você pode usar os procedimentos a seguir no console de gerenciamento do servidor do Application Virtualization para especificar a duração (em meses) das informações de uso do sistema do Application Virtualization que você deseja armazenar no banco de dados.

**Observação**  Para armazenar informações de uso, você deve marcar a caixa de seleção **registrar informações de uso** na guia **pipeline do provedor** . Para exibir essa guia, clique com o botão direito do mouse na política do provedor no painel **resultados das políticas do provedor** e selecione **Propriedades**.

 

**Para configurar o relatório de uso**

1.  Clique com o botão direito do mouse no nó do sistema de virtualização do aplicativo no painel esquerdo e selecione **Opções do sistema**.

2.  Selecione a guia **banco de dados** .

3.  Marque a caixa de seleção **manter uso de (meses)** ou **manter todos os usos** .

4.  Se você optar por especificar a duração do uso em meses, insira um número entre 1 e 120 (o valor padrão é de 6 meses). Se você selecionar **manter todo o uso**, o banco de dados será ampliado até atingir o limite de tamanho especificado.

5.  Clique em **aplicar** ou em **OK**.

**Para desabilitar o relatório de uso**

1.  Clique no nó **políticas de provedor** .

2.  Clique com o botão direito do mouse em **política do provedor** e selecione **Propriedades**.

3.  Selecione a guia **pipeline do provedor** .

4.  Desmarque a caixa de seleção **registrar informações de uso** .

5.  Clique em **aplicar** ou em **OK**.

## Tópicos relacionados


[Como personalizar um Application Virtualization System no Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Como configurar ou desabilitar o tamanho de banco de dados](how-to-set-up-or-disable-database-size.md)

 

 





