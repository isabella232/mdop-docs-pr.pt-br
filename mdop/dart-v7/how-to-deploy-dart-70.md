---
title: Como implantar o DaRT 7.0
description: Como implantar o DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796152"
---
# Como implantar o DaRT 7.0


Este tópico fornece instruções para implantar o Microsoft Diagnostic and Recovery Toolset (DaRT) 7 em seu ambiente. O primeiro procedimento deste tópico pressupõe que você está instalando toda a funcionalidade em um computador administrador. Quando você precisa implantar ou desinstalar o DaRT em vários computadores, usando um sistema de distribuição de software eletrônico por exemplo, pode ser mais fácil usar as opções de instalação de linha de comando. Essas opções são definidas no segundo procedimento deste tópico, que fornece um exemplo de uso para as opções de linha de comando disponíveis.

**Importante**  Antes de instalar o DaRT, verifique se o computador atende aos requisitos mínimos de sistema listados nas [configurações compatíveis com o DaRT 7,0](dart-70-supported-configurations-dart-7.md).

 

**Para instalar o DaRT em um computador administrador**

1.  Localize os arquivos de instalação do DaRT que você recebeu como parte do download do software.

2.  Clique duas vezes no arquivo de instalação do DaRT que corresponde aos requisitos do sistema, seja 32 bits ou 64 bits. O arquivo de instalação do DaRT é chamado de **MSDaRT70.msi**.

3.  Aceite os termos de licença para software Microsoft e clique em **Avançar**.

4.  Selecione a pasta de destino para instalar o DaRT, selecione se o DaRT deve ser instalado para todos os usuários ou apenas para o usuário atual e clique em **Avançar**.

5.  Selecione se a instalação deve ser **típica**, **personalizada**ou **completa**e clique em **Avançar**.

    -   **Típica** instala as ferramentas que são usadas com mais frequência. Esse método é recomendado para a maioria dos usuários.

    -   **Personalizado** permite que você selecione as ferramentas que estão instaladas e onde elas serão instaladas. Isso é recomendado para usuários avançados, especialmente se você estiver instalando diferentes ferramentas DaRT em diferentes computadores de helpdesk.

    -   **Concluído** instala todas as ferramentas DART e requer mais espaço em disco.

    Depois de selecionar o método de instalação, clique em **Avançar**.

6.  Para iniciar a instalação, clique em **instalar**.

7.  Depois que a instalação for concluída com êxito, clique em **concluir** para sair do assistente.

**Para instalar o DaRT no prompt de comando**

1.  O exemplo a seguir mostra como instalar toda a funcionalidade do DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  O exemplo a seguir mostra como instalar apenas o **Assistente de imagem de recuperação do DART**.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  O exemplo a seguir mostra como instalar somente o Crash Analyzer e o Visualizador de conexão remota do DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  O exemplo a seguir cria um log de configuração para o Windows Installer. Isso é importante para a depuração.

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

**Observação**  Você pode adicionar/qn ou/QB a qualquer uma das opções de prompt de comando de instalação do DaRT para executar uma instalação silenciosa.

 

## Tópicos relacionados


[Implantar o DaRT 7.0 em computadores de administrador](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





