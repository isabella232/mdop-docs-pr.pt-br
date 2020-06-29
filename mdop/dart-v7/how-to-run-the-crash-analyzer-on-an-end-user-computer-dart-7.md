---
title: Como executar o Crash Analyzer em um computador de usuário final
description: Como executar o Crash Analyzer em um computador de usuário final
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799352"
---
# Como executar o Crash Analyzer em um computador de usuário final


Normalmente, você executa o Microsoft Diagnostics and Recovery Toolset (DaRT) 7 Crash Analyzer da janela Diagnostics and Recovery Toolset em um computador de usuário final com problemas. O analisador de falha tenta localizar as ferramentas de depuração para Windows no computador problemático. Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft). Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.

**Para abrir e executar o Crash Analyzer em um computador de usuário final**

1.  Na janela **diagnóstico e Recovery Toolset** em um computador usuário final, clique em **Crash Analyzer**.

2.  Forneça as informações necessárias para o seguinte:

    -   Ferramentas de depuração da Microsoft para Windows

    -   Arquivos de símbolo

        Para obter mais informações sobre arquivos de símbolos, consulte [como garantir que o Crash Analyzer possa acessar arquivos de símbolo](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Um arquivo de despejo de falha

        Siga estas etapas para determinar o local do arquivo de despejo de falha:

        1.  Abra a janela **Propriedades do sistema** .

            Clique em **Iniciar**, digite sysdm.cpl e, em seguida, pressione Enter.

        2.  Clique na guia **Avançado**.

        3.  Na área **inicialização e recuperação** , clique em **configurações**.

        **Observação**  Se você não tiver acesso à janela **Propriedades do sistema** , poderá pesquisar arquivos de despejo no computador do usuário final usando a ferramenta de **pesquisa** no DART.

         

3.  O **Crash Analyzer** verifica o arquivo de despejo de falha e relata uma provável causa da falha. Você pode ver mais informações sobre a falha, como a mensagem de erro e a descrição específicas, os drivers carregados no momento da falha e a saída completa da análise.

4.  Decidir sobre uma estratégia apropriada para solucionar o problema. Isso pode exigir a desativação ou atualização do driver de dispositivo que causou a falha com o uso do nó **serviços e drivers** da ferramenta de **Gerenciamento de computador** no DART.

## Tópicos relacionados


[Como diagnosticar falhas de sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





