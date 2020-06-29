---
title: Como instalar o sequenciador
description: Como instalar o sequenciador
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797091"
---
# Como instalar o sequenciador


O sequenciador do Microsoft Application Virtualization (App-V) monitora e registra o processo de instalação e configuração de aplicativos para que o aplicativo possa ser executado como um aplicativo virtual. Você deve instalar o sequenciador em um computador que tenha somente o sistema operacional instalado. Você também pode instalar o sequenciador em um computador que executa um ambiente virtual, por exemplo, Microsoft Virtual PC. Esse método é útil porque é mais fácil manter um ambiente de sequenciamento de limpeza que pode ser reutilizado com configuração adicional mínima.

Você deve ter direitos administrativos no computador que você está usando para sequenciar o aplicativo e o computador deve estar conectado à rede. O computador não deve estar executando nenhuma versão do cliente do Application Virtualization (App-V). A criação de um aplicativo virtual usando o sequenciador exige muitos recursos, portanto, é importante que você instale o sequenciador em um computador que atenda ou exceda os requisitos recomendados. Para obter mais informações sobre os requisitos do sistema, consulte [requisitos de hardware e software do sequenciador](sequencer-hardware-and-software-requirements.md).

**Para instalar o Microsoft Application Virtualization Sequencer**

1.  Copie os arquivos de instalação do Microsoft Application Virtualization Sequencer para o computador em que você deseja instalá-lo.

2.  Para iniciar o assistente de instalação do Microsoft Application Virtualization Sequencer, selecione **setup.exe**. Se o **Microsoft Visual C++ SP1 Redistributable Package (x86)** não for detectado antes da instalação, o **setup.exe** será instalado.

3.  Na página de **boas-vindas** , clique em **Avançar**.

4.  Na página **contrato de licença** , para aceitar os termos do contrato de licença, selecione **aceito os termos do contrato de licença**. Clique em **Avançar**.

5.  Na página **pasta de destino** , para aceitar a pasta de instalação padrão, clique em **Avançar**. Para especificar uma pasta de destino diferente, clique em **alterar** e especifique a pasta de instalação que será usada para a instalação. Clique em **Avançar**.

6.  Na página **pronto para instalar o programa** , clique em **instalar**para iniciar a instalação.

7.  Na página **Assistente InstallShield concluído** , para fechar o assistente de instalação e abrir o sequenciador, clique em **concluir**. Para fechar o assistente de instalação sem abrir o sequenciador, desmarque **iniciar o programa** e clique em **concluir**.

## Tópicos relacionados


[Configurando o Application Virtualization Sequencer](configuring-the-application-virtualization-sequencer.md)

 

 





