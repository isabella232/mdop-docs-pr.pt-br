---
title: Como criar o diretório raiz do pacote do Sequencer
description: Como criar o diretório raiz do pacote do Sequencer
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797161"
---
# Como criar o diretório raiz do pacote do Sequencer


O diretório raiz do pacote é o diretório no computador que executa o sequenciador App-V em que os arquivos do aplicativo sequenciado são instalados. Esse diretório também existe virtualmente no computador para o qual um aplicativo sequenciado será transmitido. Você deve criar o diretório raiz do pacote antes de monitorar a instalação de um novo aplicativo.

Depois de criar o diretório raiz do pacote, você pode começar a sequenciar aplicativos. Para obter mais informações sobre como sequenciar um novo aplicativo, consulte [como sequenciar um aplicativo](how-to-sequence-an-application.md).

**Para criar o diretório raiz do pacote**

1.  Para criar o diretório raiz do pacote, no computador que executa o sequenciador App-V, mapeie a unidade Q:\\ para o local de rede especificado. O local especificado deve ter espaço suficiente para salvar o aplicativo que você está sequenciando.

2.  Para criar um diretório que você pode usar para um novo aplicativo virtual, crie uma pasta na unidade Q:\\ e atribua um nome a ela.

    **Importante**  O nome que você atribui a arquivos de aplicativo virtual que serão salvos no diretório raiz do pacote deve usar o formato de nomenclatura do 8,3. Os nomes dos arquivos não devem ter mais de 8 caracteres com uma extensão de nome de arquivo de três caracteres.

     

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Para modificar a localização do diretório de log](how-to-modify-the-log-directory-location.md)

[Como modificar a localização do diretório temporário](how-to-modify-the-scratch-directory-location.md)

 

 





