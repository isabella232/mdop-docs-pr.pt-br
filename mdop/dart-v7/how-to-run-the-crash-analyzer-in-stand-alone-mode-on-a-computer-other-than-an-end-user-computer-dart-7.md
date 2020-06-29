---
title: Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final
description: Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799142"
---
# Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final


Se não for possível acessar as ferramentas de depuração da Microsoft para Windows ou os arquivos de símbolo no computador do usuário final, você poderá copiar o arquivo de despejo do computador com problema e analisá-lo em um computador que tenha a versão autônoma do Crash Analyzer instalada, como um computador do administrador da assistência técnica.

**Para executar o Crash Analyzer no modo autônomo**

1.  Em um computador com o DaRT7 instalado, clique em **Iniciar**  /  **todos os programas**  /  **Microsoft DART 7**.

2.  Forneça as informações necessárias para o seguinte:

    -   Ferramentas de depuração da Microsoft para Windows

    -   Arquivos de símbolo

        Para obter mais informações sobre arquivos de símbolos, consulte [como garantir que o Crash Analyzer possa acessar arquivos de símbolo](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Um arquivo de despejo de falha

        **Observação**  Use a ferramenta de pesquisa no DaRT7 para localizar o arquivo de despejo de falha copiado.

         

3.  O **Crash Analyzer** verifica o arquivo de despejo de falha e relata uma provável causa da falha. Você pode ver mais informações sobre a falha, como a mensagem de erro e a descrição específicas, os drivers carregados no momento da falha e a saída completa da análise.

4.  Decidir sobre uma estratégia apropriada para solucionar o problema. Isso pode exigir a desativação ou atualização do driver de dispositivo que causou a falha com o uso do nó **serviços e drivers** da ferramenta de **Gerenciamento de computador** no DART.

## Tópicos relacionados


[Como diagnosticar falhas de sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





