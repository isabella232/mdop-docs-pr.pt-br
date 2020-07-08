---
title: Como executar o Crash Analyzer em um computador de usuário final
description: Como executar o Crash Analyzer em um computador de usuário final
author: dansimp
ms.assetid: d36213e5-7719-44d7-be65-971c3ef7df2c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 028f1dd0a1651809ec54ae19094302586d864f99
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799458"
---
# Como executar o Crash Analyzer em um computador de usuário final


Para executar o **Crash Analyzer** na janela **diagnóstico e recuperação do conjunto de ferramentas** em um computador de usuário final com problemas, você deve ter as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo instalados. Para baixar as ferramentas de depuração do Windows, consulte [ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).

**Para executar o Crash Analyzer em um computador de usuário final**

1.  Na janela **diagnóstico e Recovery Toolset** em um computador usuário final, clique em **Crash Analyzer**.

2.  Forneça as informações necessárias para as ferramentas de depuração da Microsoft para Windows.

3.  Forneça as informações necessárias para os arquivos de símbolo. Para obter mais informações sobre arquivos de símbolos, consulte [como garantir que o Crash Analyzer possa acessar arquivos de símbolo](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).

4.  Forneça as informações necessárias para um arquivo de despejo de memória. Para determinar a localização do arquivo de despejo de memória:

    1.  Abra a janela **Propriedades do sistema** .

    2.  Clique em **Iniciar**, digite **sysdm.cpl**e, em seguida, pressione **Enter**.

    3.  Clique na guia **Avançado**.

    4.  Na área **inicialização e recuperação** , clique em **configurações**.

        Se você não tiver acesso à janela **Propriedades do sistema** , poderá pesquisar arquivos de despejo no computador do usuário final usando a ferramenta **Pesquisar** no Microsoft Diagnostics e o conjunto de ferramentas de recuperação (DART) 8,0.

    O **Crash Analyzer** verifica o arquivo de despejo de memória e relata uma provável causa do problema. Você pode ver mais informações sobre a falha, como a mensagem de despejo de memória específica e a descrição, os drivers carregados no momento da falha e a saída completa da análise.

5.  Identifique a estratégia apropriada para solucionar o problema. A estratégia pode exigir a desativação ou atualização do driver de dispositivo que causou a falha usando o nó **serviços e drivers** da ferramenta de **Gerenciamento do computador** no DART 8,0.

## Tópicos relacionados


[Como diagnosticar falhas de sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[Operações do DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





