---
title: Como sequenciar um pacote usando o PowerShell
description: Como sequenciar um pacote usando o PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796315"
---
# Como sequenciar um pacote usando o PowerShell


Use o procedimento a seguir para criar um novo pacote App-V 5,0 usando o PowerShell.

**Observação**  Antes de usar este procedimento, você deve copiar os arquivos de instalação associados para o computador que executa o sequenciador e ler e entender a seção Sequencer de [planejamento para o App-V 5,0 Sequencer e para a implantação do cliente](planning-for-the-app-v-50-sequencer-and-client-deployment.md).

 

**Para criar um novo aplicativo virtual usando o PowerShell**

1.  Instale o sequenciador do App-V 5,0. Para obter mais informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-beta-gb18030.md).

2.  Para abrir um console do PowerShell, clique em **Iniciar** e digite **PowerShell**. Clique com o botão direito do mouse em **Windows PowerShell** e selecione **Executar como Administrador**.

3.  Usando o console do PowerShell, digite o seguinte: **Import-Module appvsequencer**.

4.  Para criar um pacote, use o cmdlet **New-AppvSequencerPackage** . Os parâmetros a seguir são necessários para criar um pacote:

    -   **Name** -especifica o nome do pacote.

    -   **PrimaryVirtualApplicationDirectory** -especifica o caminho para o diretório que será usado para instalar o aplicativo. Esse caminho deve existir.

    -   **Installer** – especifica o caminho para o instalador do aplicativo associado.

    -   **Path** -especifica o diretório de saída do pacote.

    Por exemplo:

    **New-AppvSequencerPackage – nome &lt; do caminho do pacote &gt; -PrimaryVirtualApplicationDirectory &lt; para o caminho do instalador raiz do pacote &gt; &lt; para o &gt; diretório executável do instalador-OutputPath &lt; do caminho de saída&gt;**

    Aguarde até que o sequenciador crie o pacote. A criação de um pacote usando o PowerShell pode levar tempo. Se o pacote não foi criado com êxito, um erro será retornado.

    A lista a seguir exibe parâmetros opcionais adicionais que podem ser usados com o cmdlet **New-AppvSequencerPackage** :

    -   AcceleratorFilePath – especifica o caminho para o arquivo Accelerator. cab para gerar um pacote.

    -   InstalledFilesPath-especifica o caminho para o local onde os arquivos locais instalados do aplicativo são salvos.

    -   InstallMediaPath-especifica o caminho para o local onde a mídia de instalação está

    -   TemplateFilePath-especifica o caminho para um arquivo de modelo se você quiser personalizar o processo de sequenciamento.

    -   FullLoad-especifica que o pacote deve ser totalmente baixado para o computador que está executando o App-V 5,0 antes de poder ser aberto.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Administração do App-V usando o PowerShell](administering-app-v-by-using-powershell.md)

 

 





