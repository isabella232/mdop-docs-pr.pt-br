---
title: Como gerenciar o cache do cliente do App-V usando contadores de desempenho
description: Como gerenciar o cache do cliente do App-V usando contadores de desempenho
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797064"
---
# Como gerenciar o cache do cliente do App-V usando contadores de desempenho


Você pode usar o procedimento a seguir para determinar a quantidade de espaço livre disponível no cache do cliente do Application Virtualization (App-V) usando o monitor de desempenho para exibir as informações graficamente. Essas informações são capturadas no computador cliente por um contador de desempenho chamado "cache do cliente do aplicativo virt" e inclui os seguintes contadores: "tamanho do cache (MB)," "espaço livre em cache (MB)" e "% espaço livre".

**Para determinar o uso do espaço em cache do cliente**

1.  Abra um prompt de comando como administrador ou clique em **Iniciar**, **executar**, digite **perfmon.exe**e clique em **OK**.

2.  Dependendo do sistema operacional Windows sendo usado, clique na ferramenta Monitor de desempenho ou monitor do sistema após a abertura da janela do MMC.

3.  Para adicionar contadores, clique com o botão direito do mouse na área do gráfico e selecione **Adicionar contadores**.

4.  Clique na lista suspensa para exibir a lista de contadores disponíveis, role para localizar o **App Virt o cache do cliente**e, em seguida, adicione os três contadores.

    **Importante**  Os contadores de desempenho do App-V são implementados em uma DLL de 32 bits, portanto, para vê-los, você deve usar o seguinte comando para iniciar a versão de 32 bits do monitor de desempenho: **MMC/32 perfmon. msc**. Esse comando deve ser executado diretamente no computador que está sendo monitorado e não pode ser usado para monitorar um computador remoto que executa um sistema operacional de 64 bits.

     

## Tópicos relacionados


[Como gerenciar aplicativos virtuais usando a linha de comando](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





