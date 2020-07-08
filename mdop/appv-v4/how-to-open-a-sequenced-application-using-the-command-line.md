---
title: Como abrir um aplicativo sequenciado usando a linha de comando
description: Como abrir um aplicativo sequenciado usando a linha de comando
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797021"
---
# Como abrir um aplicativo sequenciado usando a linha de comando


Você pode abrir pacotes de aplicativos virtuais usando a linha de comando. Você deve executar o prompt **cmd** como administrador.

Use o procedimento a seguir para abrir pacotes de aplicativos sequenciados usando a linha de comando

**Para abrir um aplicativo sequenciado usando a linha de comando**

1.  Para abrir o prompt de comando, clique em **Iniciar**e selecione **executar**, digite **cmd**e clique em **OK**.

2.  Em um prompt de comando, digite **cd\\** e especifique o caminho para o diretório onde o sequenciador está instalado e pressione **Enter.**

3.  No prompt de comando, digite o seguinte comando, substituindo o texto em itálico pelos valores:

    SFTSequencer/OPEN:*"especifica o arquivo. sprj para abrir"*

    Pressione **Enter**.

4.  Você também pode especificar os seguintes parâmetros opcionais. No prompt de comando, digite os seguintes comandos, substituindo o texto em itálico pelos valores:

    /PACKAGENAME: "*especifica o nome do pacote"*

    /MSI-especifica a geração de um instalador do Microsoft Windows associado.

    /COMPRESS – especifica se o pacote será compactado. Por padrão, os pacotes não são compactados.

    Pressione **Enter**.

    **Observação**  Se o pacote de instalação ou o pacote do Windows Installer tiver uma interface gráfica do usuário, ela será exibida após a especificação dos parâmetros de linha de comando.

     

## Tópicos relacionados


[Como gerenciar aplicativos virtuais usando a linha de comando](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





