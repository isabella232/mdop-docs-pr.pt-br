---
title: Erros de linha de comando
description: Erros de linha de comando
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797519"
---
# Erros de linha de comando


Use a seguinte lista de erros para identificar os motivos pelos quais o sequenciamento de linha de comando não está funcionando corretamente. Você também pode ver esses erros exibindo o arquivo de log do sequenciador.

**Observação**  Mais de um erro pode ser exibido durante o sequenciamento. Além disso, o código de erro exibido pode ser a soma de dois códigos de erro. Por exemplo, se os parâmetros */InstallPath* e */OutputFile* estiverem ausentes, o Microsoft System Center Application Virtualization Sequencer retornará 96 — a soma dos dois códigos de erro.

 

<a href="" id="01"></a>Dezembro  
Há um erro não especificado.

<a href="" id="02"></a>02  
O diretório de instalação especificado (/INSTALLPACKAGE) especificado não é válido.

<a href="" id="04"></a>04  
O diretório raiz do pacote especificado (/INSTALLPATH) não é válido.

<a href="" id="08"></a>08  
O parâmetro */OutputFile* especificado não é válido.

<a href="" id="16"></a>16  
O diretório de instalação (/INSTALLPACKAGE) não foi especificado.

<a href="" id="32"></a>32  
O diretório raiz do pacote (/INSTALLPATH) não foi especificado.

<a href="" id="64"></a>64  
O parâmetro */OutputFile* não foi especificado.

<a href="" id="128"></a>128  
A unidade de virtualização do aplicativo especificada não é válida.

<a href="" id="256"></a>256  
Falha no instalador.

<a href="" id="512"></a>512  
Falha no sequenciamento do aplicativo.

<a href="" id="1024"></a>1024  
Falha na avaliação dos atalhos instalados.

<a href="" id="2048"></a>2048  
O pacote do aplicativo sequenciado não pode ser salvo.

<a href="" id="4096"></a>4096  
O nome do pacote especificado (/PACKAGENAME) não é válido.

<a href="" id="8192"></a>8192  
O tamanho de bloco especificado (/BLOCKSIZE <em> ) </em> não é válido.

<a href="" id="16384"></a>16384  
O tipo de compactação especificado (/COMPRESSION) não é válido.

<a href="" id="32768"></a>32768  
O caminho do projeto especificado não é válido.

<a href="" id="65536"></a>65536  
O parâmetro de atualização especificado não é válido.

<a href="" id="131072"></a>131072  
O parâmetro projeto de atualização especificado não é válido.

<a href="" id="262144"></a>262144  
O parâmetro de caminho de decodificação especificado não é válido.

<a href="" id="525288"></a>525288  
O nome do pacote não foi especificado.

## Tópicos relacionados


[Sobre como usar a linha de comando do Sequencer](about-using-the-sequencer-command-line.md)

[Parâmetros de linha de comando](command-line-parameters.md)

 

 





