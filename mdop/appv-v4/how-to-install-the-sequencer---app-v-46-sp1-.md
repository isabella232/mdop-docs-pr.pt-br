---
title: Como instalar o sequenciador (App-V 4,6 SP1)
description: Como instalar o sequenciador (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797092"
---
# Como instalar o sequenciador (App-V 4,6 SP1)


O sequenciador do Microsoft Application Virtualization (App-V) monitora e registra o processo de instalação e configuração de aplicativos para que o aplicativo possa ser executado como um aplicativo virtual. Você deve instalar o sequenciador do App-V em um computador que tenha somente o sistema operacional instalado. Você também pode instalar o sequenciador em um computador executado em um ambiente virtual, por exemplo, um computador virtual. Esse método é útil porque é mais fácil manter um ambiente de sequenciamento de limpeza que você pode reutilizar com uma configuração adicional mínima.

Você deve ter credenciais administrativas no computador que você está usando para sequenciar o aplicativo, e o computador não deve estar executando qualquer versão do cliente App-V. A criação de um aplicativo virtual usando o sequenciador App-V requer várias operações, portanto, é importante que você instale o sequenciador em um computador que atenda ou exceda os [requisitos de hardware e software do sequenciador do Application Virtualization](application-virtualization-sequencer-hardware-and-software-requirements.md).

**Observação**  
Não há suporte para a execução do sequenciador App-V no modo de segurança.



**Para instalar o Microsoft Application Virtualization Sequencer**

1.  Copie os arquivos de instalação do Microsoft Application Virtualization Sequencer para o computador no qual você deseja instalá-lo.

2.  Para iniciar o assistente de instalação do Microsoft Application Virtualization Sequencer, clique duas vezes em **Setup.exe**. Se o **pacote redistribuível do Microsoft Visual C++ SP1 (x86)** não for detectado antes da instalação, clique em **instalar** para instalar o pré-requisito obrigatório.

3.  Para continuar a instalação, na página **Bem-vindo** , clique em **Avançar**.

4.  Na página **contrato de licença** , para aceitar os termos do contrato de licença, clique em **aceito os termos do contrato de licença**e, em seguida, clique em **Avançar**.

5.  Na página **pasta de destino** , para aceitar a pasta de instalação padrão, clique em **Avançar**. Para especificar uma pasta de destino diferente, clique em **alterar** e especifique a pasta de instalação que será usada para a instalação. Clique em **Avançar**.

6.  Na página **unidade virtual** , para configurar o **Q:\\** de unidade padrão do Application Virtualization (padrão) como a unidade em que todos os aplicativos sequenciados serão executados, clique em **Avançar**. Se você quiser especificar uma letra de unidade diferente, use a lista e selecione a letra de unidade que deseja usar, selecionando a letra de unidade apropriada e, em seguida, clique em **Avançar**.

    **Importante**  
    A letra da unidade de virtualização do aplicativo especificada com esta etapa é a letra da unidade na qual os aplicativos virtuais serão executados nos computadores de destino. A letra da unidade especificada deve estar disponível e não está sendo usada no momento nos computadores que executam o cliente App-V. Se a unidade especificada já estiver em uso, o aplicativo virtual falhará no computador de destino.



7.  Na página **pronto para instalar o programa** , clique em **instalar**para iniciar a instalação.

8.  Na página **Assistente InstallShield concluído** , para fechar o assistente de instalação e abrir o sequenciador do App-V, clique em **concluir**. Para fechar o assistente de instalação sem abrir o sequenciador, desmarque **iniciar o programa**e, em seguida, clique em **concluir**.

    **Observação**  
    Se você instalou o sequenciador do App-V em um computador que executa um ambiente virtual, por exemplo, um computador virtual, agora você deve fazer um instantâneo. Depois de sequenciar um aplicativo, você pode reverter para essa imagem, para que você possa sequenciar o próximo aplicativo.



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## Tópicos relacionados


[Configuração do Application Virtualization Sequencer (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









