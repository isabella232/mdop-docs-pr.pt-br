---
title: Como criar um acelerador de pacotes usando o PowerShell
description: Como criar um acelerador de pacotes usando o PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796460"
---
# Como criar um acelerador de pacotes usando o PowerShell


Os aceleradores de pacotes do App-V 5,1 seqüenciam automaticamente aplicativos grandes e complexos. Além disso, ao aplicar um acelerador de pacotes do App-V 5,1, você nem sempre é obrigado a instalar manualmente um aplicativo para criar o pacote virtualizado.

**Para criar um acelerador de pacote**

1.  Instale o sequenciador do App-V 5,1. Para obter mais informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Para abrir um console do PowerShell, clique em **Iniciar** e digite **PowerShell**. Clique com o botão direito do mouse em **Windows PowerShell** e selecione **Executar como Administrador**. Use o cmdlet **New-AppvPackageAccelerator** .

3.  Para criar um acelerador de pacote, certifique-se de que você tenha o pacote. AppV para criar um acelerador a partir da mídia de instalação ou arquivos de instalação e, opcionalmente, um arquivo Leia-me para que os consumidores do acelerador usem. Os parâmetros a seguir são necessários para usar o cmdlet do acelerador de pacote:

    -   **InstalledFilesPath** -especifica o caminho de instalação do aplicativo.

    -   **Instalador** – especifica o caminho para a mídia do instalador do aplicativo

    -   **InputPackagePath** – especifica o caminho para o pacote. AppV

    -   **Path** – especifica o diretório de saída do pacote.

    O exemplo a seguir mostra como você pode criar um acelerador de pacote com um pacote. AppV e a mídia de instalação:

    **Caminho New-AppvPackageAccelerator-InputPackagePath &lt; para o caminho do instalador de arquivo. AppV &gt; &lt; para o &gt; diretório do instalador executável-caminho &lt; do caminho de saída&gt;**

    Parâmetros opcionais adicionais que podem ser usados com o cmdlet **New-AppvPackageAccelerator** são exibidos na lista a seguir:

    -   **AcceleratorDescriptionFile** -especifica o caminho para instruções do acelerador do pacote criado pelo usuário. As instruções do pacote acelerador são arquivos de descrição **. txt** ou **. rtf** que serão empacotados com o pacote criado usando o acelerador de pacote.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Administração do App-V 5.1 usando o PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





