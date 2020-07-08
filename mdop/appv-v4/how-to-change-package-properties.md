---
title: Como alterar as propriedades do pacote
description: Como alterar as propriedades do pacote
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797246"
---
# Como alterar as propriedades do pacote


Você pode usar os procedimentos a seguir para modificar o nome de um pacote de virtualização de aplicativo e seus comentários associados.

Se essa for a primeira vez que o pacote foi criado, você também pode alterar o tamanho do bloco de parâmetro de sequenciamento, que determina como um pacote de aplicativo sequenciado é transmitido de um servidor de virtualização de aplicativos para um cliente de desktop do Application Virtualization.

**Observação**  Ao selecionar um tamanho de bloco, considere o tamanho do arquivo SFT e a largura de banda da rede. Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda. Arquivos com tamanhos de blocos maiores podem ser usados com mais rapidez, mas usam mais largura de banda de rede. Por meio da experimentação, você pode descobrir o tamanho de bloco ideal para aplicativos de streaming na sua rede.

 

O restante das propriedades do pacote na guia **Propriedades** é gerado automaticamente e não pode ser modificado nessa guia.

**Para alterar o nome ou os comentários do pacote**

1.  Clique na guia **Propriedades** .

2.  Na caixa de texto **nome do pacote** , digite ou edite o nome único usado para o pacote, que pode conter vários aplicativos.

3.  Na caixa de texto **comentários** , opcionalmente, digite ou edite os comentários. A prática recomendada sugerida é fornecer informações detalhadas sobre o pacote e o sequenciamento.

4.  No menu **arquivo** , selecione **salvar**.

**Para alterar o tamanho do bloco**

1.  Clique na guia **Propriedades** .

2.  Na lista suspensa **tamanho do bloco** , selecione **4 KB**, **16 kb**, **32 KB**ou **64 KB**.

3.  No menu **arquivo** , selecione **salvar**.

## Tópicos relacionados


[Sobre a guia Propriedades](about-the-properties-tab.md)

[Console do Sequencer](sequencer-console.md)

 

 





