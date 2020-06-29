---
title: Como garantir que o Crash Analyzer possa acessar arquivos de símbolos
description: Como garantir que o Crash Analyzer possa acessar arquivos de símbolos
author: dansimp
ms.assetid: 39e307bd-5d21-4e44-bed6-bf532f580775
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8e0ba2fa777039e1c6ffb91dd997438d8ea50616
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799106"
---
# Como garantir que o Crash Analyzer possa acessar arquivos de símbolos


Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do programa. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder.

Os arquivos de símbolo são baixados automaticamente quando você executa o **Crash Analyzer**. Se o computador não tiver uma conexão com a Internet ou a rede exigir que o computador acesse um servidor proxy HTTP, os arquivos de símbolo não poderão ser baixados.

**Para garantir que o Crash Analyzer possa acessar arquivos de símbolo**

1.  **Copie o arquivo de despejo para outro computador.** Se não for possível baixar os símbolos devido à falta de uma conexão com a Internet, copie o arquivo de despejo de memória para um computador que tenha uma conexão com a Internet e execute o assistente autônomo do **Crash Analyzer** nesse computador.

2.  **Acessar os arquivos de símbolo de outro computador.** Se não for possível baixar os símbolos devido à falta de uma conexão com a Internet, você poderá baixar os símbolos de um computador que tenha uma conexão com a Internet e, em seguida, copiá-los para o computador que não tenha uma conexão com a Internet, ou pode mapear uma unidade de rede para um local onde os símbolos estão disponíveis na rede local. Se você executar o **Crash Analyzer** em um ambiente de recuperação do Windows (WindowsRE), você pode incluir os arquivos de símbolo na imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DART) 10.

3.  **Acessar arquivos de símbolo por meio de um servidor proxy HTTP.** Se não for possível baixar os símbolos porque um servidor proxy HTTP deve ser acessado, use as etapas a seguir para acessar um servidor proxy HTTP. No DaRT 10, o **Assistente do Crash Analyzer** tem uma configuração disponível na página de diálogo **especificar local dos arquivos de símbolos** , marcada com o **servidor proxy de rótulo (opcional, usando o formato "servidor: porta")**. Você pode usar essa caixa de texto para especificar um servidor proxy. Digite o endereço de proxy na forma ** &lt; nome do host &gt; : &lt; &gt; porta**, em que o nome do &lt; **host** &gt; é um nome DNS ou endereço IP, e a &lt; **porta** &gt; é um número de porta TCP. Há dois modos em que o **analisador de falhas** pode ser executado. Veja como usar a configuração de proxy em cada um dos seguintes modos:

    -   **Modo online:** Nesse modo, se o campo servidor proxy for deixado em branco, o assistente usará as configurações de proxy das opções da Internet no painel de controle. Se você inserir um endereço proxy na caixa de texto que é fornecida, esse endereço será usado, e ele substituirá a configuração nas opções da Internet.

    -   Ambiente de recuperação do Windows (WindowsRE): quando você executa o **Crash Analyzer** na janela **diagnóstico e recuperação de conjunto de ferramentas de recuperação** , não há um endereço proxy padrão. Se o computador estiver conectado diretamente à Internet, um endereço de proxy não será necessário. Portanto, você pode deixar este campo em branco na configuração do assistente. Se o computador não estiver diretamente conectado à Internet e estiver em um ambiente de rede com um servidor proxy, você deve definir o campo proxy no Assistente para acessar o repositório de símbolos. O endereço do proxy pode ser obtido com o administrador da rede. A configuração do servidor proxy é importante somente quando o armazenamento de símbolos públicos está conectado à Internet. Se os símbolos já estiverem na imagem de recuperação do DaRT ou se estiverem disponíveis localmente, a configuração do servidor proxy não será necessária.

## Tópicos relacionados


[Como diagnosticar falhas de sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[Operações do DaRT 10](operations-for-dart-10.md)

 

 





