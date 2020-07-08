---
title: Como diagnosticar falhas de sistema com o Crash Analyzer
description: Como diagnosticar falhas de sistema com o Crash Analyzer
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799278"
---
# Como diagnosticar falhas de sistema com o Crash Analyzer


O Crash Analyzer no Microsoft Diagnostics and Recovery Toolset (DaRT) 7 permite que você depure um arquivo de despejo de falha em um computador baseado no Windows e, em seguida, diagnostique qualquer erro de computador relacionado. O analisador de falha usa as ferramentas de depuração da Microsoft para Windows para examinar um arquivo de despejo de falha para o driver que causou a falha do computador.

## Executar o Crash Analyzer em um computador de usuário final


Normalmente, você executa o Crash Analyzer na janela diagnóstico e recuperação de conjunto de ferramentas em um computador de usuário final com problemas. O analisador de falha tenta localizar as ferramentas de depuração para Windows no computador problemático. Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft). Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.

Se você incluiu as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo ao criar a imagem de recuperação do DaRT, elas deverão estar disponíveis quando você executar o Crash Analyzer no computador com problema.

[Como executar o Crash Analyzer em um computador de usuário final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## Executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final


O analisador de falha tenta localizar as ferramentas de depuração para Windows no computador problemático. Se a caixa de diálogo caminho do diretório estiver vazia, você deverá digitar o local ou navegar até o local das ferramentas de depuração para Windows (você pode baixar os arquivos da Microsoft). Você também deve fornecer um caminho para o local onde os arquivos de símbolo estão localizados.

Se você não incluiu as ferramentas de depuração da Microsoft para Windows e os arquivos de símbolo ao criar a imagem de recuperação do DaRT, ou se os problemas de conectividade de rede ou tamanho de disco impedirem você de obtê-los, poderá copiar o arquivo de despejo do computador com problema e analisá-lo em um computador que tenha a versão autônoma do Crash Analyzer instalada , como um computador administrador da assistência técnica.

[Como executar o Crash Analyzer no modo autônomo em um computador que não seja um computador de usuário final](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## Verifique se o Crash Analyzer pode acessar arquivos de símbolo


Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele travou.

Os arquivos de símbolo são baixados automaticamente quando você executa o Crash Analyzer. Se o computador não tiver uma conexão com a Internet ou a rede exigir que o computador acesse um servidor proxy HTTP, os arquivos de símbolo não poderão ser baixados.

[Como garantir que o Crash Analyzer possa acessar arquivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## Outros recursos para diagnosticar falhas do sistema com o Crash Analyzer


[Operações do DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





