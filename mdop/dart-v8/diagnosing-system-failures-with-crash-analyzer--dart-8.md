---
title: Como diagnosticar falhas de sistema com o Crash Analyzer
description: Como diagnosticar falhas de sistema com o Crash Analyzer
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799493"
---
# Como diagnosticar falhas de sistema com o Crash Analyzer


O **Crash Analyzer** no Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 permite que você depure um arquivo de despejo de memória em um computador baseado no Windows e, em seguida, diagnostique qualquer erro de computador relacionado. O **analisador de falha** usa as ferramentas de depuração da Microsoft para Windows para examinar um arquivo de despejo de memória para o driver que causou a falha do computador. Você pode executar o Crash Analyzer em um computador de usuário final ou no modo autônomo em um computador que não seja um computador de usuário final.

## Executar o Crash Analyzer em um computador usuário final


Normalmente, você executa o **Crash Analyzer** na janela **diagnóstico e recuperação de conjunto de ferramentas** em um computador de usuário final que está apresentando o problema. O **analisador de falha** tenta localizar as ferramentas de depuração para Windows no computador problemático. Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft). Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.

Se você incluiu as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo ao criar a imagem de recuperação do DaRT 8,0, as ferramentas e os arquivos de símbolo devem estar disponíveis quando você executa o **Crash Analyzer** no computador com problema. Se você não os tiver incluído na imagem de recuperação do DaRT, ou se o tamanho do disco ou problemas de conectividade de rede estiverem impedindo que você os receba, é possível executar o Crash Analyzer no modo autônomo em um computador diferente do computador do usuário final, conforme descrito na seção a seguir.

[Como executar o Crash Analyzer em um computador de usuário final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a>Executar o Crash Analyzer no modo autônomo em um computador diferente do computador de um usuário final


Embora você normalmente execute o **Crash Analyzer** no computador do usuário final que está apresentando o problema, você também pode executar o Crash Analyzer no modo autônomo, em um computador que não seja um computador de usuário final. Você pode escolher essa opção se não incluíu as ferramentas de depuração do Windows na imagem de recuperação do DaRT ou se os problemas de conectividade de rede ou tamanho de disco impedem que você obtenha as ferramentas de depuração. Nesse caso, você pode copiar o arquivo de despejo do computador problemático e analisá-lo em um computador que tenha a versão autônoma do **Crash Analyzer** instalada, como em um computador do agente de suporte técnico.

[Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## Como garantir que o Crash Analyzer possa acessar arquivos de símbolo


Para depurar aplicativos que parou de responder, você precisa ter acesso ao arquivo de símbolo, que é separado do programa. Embora os arquivos de símbolo sejam baixados automaticamente quando você executa o Crash Analyzer, pode haver ocasiões em que o computador com problema não tenha acesso à Internet. Há várias maneiras de garantir o acesso garantido a arquivos de símbolo.

[Como garantir que o Crash Analyzer possa acessar arquivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## Outros recursos para diagnosticar falhas do sistema com o Crash Analyzer


[Operações do DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





