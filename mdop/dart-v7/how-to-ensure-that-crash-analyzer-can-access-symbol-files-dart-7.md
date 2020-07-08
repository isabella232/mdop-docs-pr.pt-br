---
title: Como garantir que o Crash Analyzer possa acessar arquivos de símbolos
description: Como garantir que o Crash Analyzer possa acessar arquivos de símbolos
author: dansimp
ms.assetid: 150a2f88-68a5-40eb-8471-e5008488ab6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db56bb21ad885d1e3aa73bcbd922a7e8bde77080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799145"
---
# Como garantir que o Crash Analyzer possa acessar arquivos de símbolos


Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele travou.

Os arquivos de símbolo são baixados automaticamente quando você executa o analisador de falha do Microsoft (DaRT) 7 Microsoft Diagnostics and Recovery. Se o computador não tiver uma conexão com a Internet ou a rede exigir que o computador acesse um servidor proxy HTTP, os arquivos de símbolo não poderão ser baixados.

## Garantir o acesso aos arquivos de símbolo


Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele travou.

Os arquivos de símbolo são baixados automaticamente quando você executa o **Crash Analyzer**. Se o computador não tiver uma conexão com a Internet ou a rede exigir que o computador acesse um servidor proxy HTTP, os arquivos de símbolo não poderão ser baixados.

Veja a seguir uma lista de opções disponíveis para garantir o acesso a arquivos de símbolo:

-   **Copie o arquivo de despejo para outro computador.** Se não for possível baixar os símbolos devido à falta de uma conexão com a Internet, copie o arquivo de despejo de falha em um computador que tenha uma conexão com a Internet e execute o assistente autônomo do **Crash Analyzer** nesse computador.

-   **Acessar os arquivos de símbolo de outro computador.** Se não for possível baixar os símbolos devido à falta de uma conexão com a Internet, você poderá baixar os símbolos de um computador que tenha uma conexão com a Internet e, em seguida, copiá-los para o computador que não tenha uma conexão com a Internet, ou pode mapear uma unidade de rede para um local onde os símbolos estão disponíveis na rede local. Se você executar o **Crash Analyzer** em um ambiente de recuperação do Windows (WindowsRE), poderá incluir os arquivos de símbolo na imagem de recuperação do DART. Para obter mais informações sobre como criar uma imagem de recuperação, consulte [criando a imagem de recuperação do DaRT 7,0](creating-the-dart-70-recovery-image-dart-7.md).

-   **Acessar arquivos de símbolo por meio de um servidor proxy HTTP.** Se não for possível baixar os símbolos porque um servidor proxy HTTP deve ser acessado, use as etapas a seguir para acessar um servidor proxy HTTP. No DaRT7, o **Assistente do Crash Analyzer** tem uma configuração disponível na página de diálogo **especificar local dos arquivos de símbolos** , marcada com o **servidor proxy de rótulo (opcional, usando o formato "servidor: porta")**. Você pode usar essa caixa de texto para especificar um servidor proxy. Digite o endereço de proxy na forma ** &lt; nome do host &gt; : &lt; porta &gt; **, em que o nome do &lt; **host** &gt; é um nome DNS ou endereço IP, e a &lt; **porta** &gt; é um número de porta TCP, geralmente 80. Há dois modos em que o **analisador de falhas** pode ser executado. Veja como usar a configuração de proxy em cada um dos seguintes modos:

    -   **Modo online:** Nesse modo, se o campo servidor proxy for deixado em branco, o assistente usará as configurações de proxy das opções da Internet no painel de controle. Se você inserir um endereço proxy na caixa de texto que é fornecida, esse endereço será usado, e ele substituirá a configuração nas opções da Internet.

    -   **Ambiente de recuperação do Windows (WindowsRE):** Quando você executa o **Crash Analyzer** na janela **diagnóstico e recuperação do conjunto de ferramentas** , não há endereço proxy padrão. Se o computador estiver conectado diretamente à Internet, um endereço de proxy não será necessário. Portanto, você pode deixar este campo em branco na configuração do assistente. Se o computador não estiver diretamente conectado à Internet e estiver em um ambiente de rede com um servidor proxy, você deve definir o campo proxy no Assistente para acessar o repositório de símbolos. O endereço do proxy pode ser obtido com o administrador da rede. A configuração do servidor proxy é importante somente quando o armazenamento de símbolos públicos está conectado à Internet. Se os símbolos já estiverem na imagem de recuperação do DaRT ou se estiverem disponíveis localmente, a configuração do servidor proxy não será necessária.

## Tópicos relacionados


[Como diagnosticar falhas de sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





