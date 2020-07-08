---
title: Como implantar o DaRT 10
description: Como implantar o DaRT 10
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796158"
---
# Como implantar o DaRT 10


As instruções a seguir explicam como implantar o diagnóstico e o conjunto de ferramentas de recuperação (DaRT) 10 da Microsoft no seu ambiente. Para obter o software DaRT, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049). Presume-se que você esteja instalando toda a funcionalidade em um computador administrador. Se você precisar implantar ou desinstalar o DaRT 10 em vários computadores, usando um sistema de distribuição de software eletrônico, por exemplo, talvez seja mais fácil usar as opções de instalação de linha de comando. Descrições e exemplos das opções de linha de comando disponíveis são fornecidas nesta seção.

**Importante**  Antes de instalar o DaRT, consulte [configurações compatíveis com o DART 10](dart-10-supported-configurations.md) para garantir que você tenha instalado todo o software de pré-requisito e que o computador atenda aos requisitos mínimos do sistema. O computador no qual você instala o DaRT deve estar executando o Windows 10.

 

Você pode instalar o DaRT usando uma das duas configurações diferentes:

-   Instale o DaRT e todas as ferramentas do DaRT no computador administrador.

-   Instalar no computador do administrador somente as ferramentas de que você precisa para criar a imagem de recuperação do DaRT e, em seguida, instalar o **Visualizador de conexão remota** e, opcionalmente, o **Crash Analyzer** em um computador de suporte técnico.

O arquivo de instalação do DaRT está disponível nas versões de 32 bits e 64 bits. Instale a versão que corresponde à arquitetura do computador no qual você está executando o assistente de imagem de recuperação DaRT, não a arquitetura de computador da imagem de recuperação que você está criando.

Você pode usar qualquer versão do arquivo de instalação do DaRT para criar uma imagem de recuperação para computadores de 32 bits ou 64 bits, mas não pode criar uma imagem de recuperação para computadores de 32 e 64 bits.

**Para instalar o DaRT e todas as ferramentas DaRT em um computador administrador**

1.  Baixe a versão de 32 bits ou 64 bits do arquivo de instalação do DaRT 10. Escolha a arquitetura que corresponde ao computador no qual você está instalando o DaRT e executando o assistente de recuperação de imagem de DaRT.

2.  Na pasta para a qual você baixou o DaRT 10, execute o arquivo de instalação **MSDaRT.msi** que corresponde aos requisitos do sistema.

3.  Na página **Bem-vindo ao assistente de configuração do Microsoft DART 10** , clique em **Avançar**.

4.  Aceite os termos de licença para software Microsoft e clique em **Avançar**.

5.  Na página **Microsoft Update** , selecione **usar o Microsoft Update quando eu verificar se há atualizações**e clique em **Avançar**.

6.  Na página **Selecionar pasta de instalação** , selecione uma pasta ou clique em **Avançar** para instalar o DART no local de instalação padrão.

7.  Na página **Opções de instalação** , selecione os recursos DART que você deseja instalar ou clique em **Avançar** para instalar o DART com todos os recursos.

8.  Para iniciar a instalação, clique em **instalar**.

9.  Depois que a instalação for concluída com êxito, clique em **concluir** para sair do assistente.

## Para instalar o DaRT e todas as ferramentas DaRT em um computador administrador usando um prompt de comando


Ao instalar ou desinstalar o DaRT, você tem a opção de executar os arquivos de instalação no prompt de comando. Esta seção descreve alguns exemplos de opções diferentes que você pode especificar ao instalar ou desinstalar o DaRT no prompt de comando.

O exemplo a seguir mostra como instalar toda a funcionalidade do DaRT.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

O exemplo a seguir mostra como instalar apenas o assistente de imagem de recuperação do DaRT.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

O exemplo a seguir mostra como instalar somente o Crash Analyzer e o Visualizador de conexão remota do DaRT.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

O exemplo a seguir cria um log de configuração para o Windows Installer. Isso é importante para a depuração.

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

**Observação**  Você pode adicionar/qn ou/QB para executar uma instalação silenciosa.

 

**Para validar a instalação do DaRT**

1.  Clique em **Iniciar**e selecione **conjunto de ferramentas de diagnóstico e recuperação**.

    A janela **diagnóstico e Recovery Toolset** é aberta.

2.  Verifique se todas as ferramentas do DaRT selecionadas para instalação foram instaladas com sucesso.

## Tópicos relacionados


[Implantar o DaRT 10 em computadores de administrador](deploying-dart-10-to-administrator-computers.md)

 

 





