---
title: Práticas recomendadas para o Application Virtualization Sequencer
description: Práticas recomendadas para o Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798984"
---
# Práticas recomendadas para o Application Virtualization Sequencer


Este tópico fornece as práticas recomendadas para executar o sequenciador do Microsoft Application Virtualization (App-V). Revise e considere as seguintes recomendações ao planejar e usar o sequenciador no seu ambiente.

## Sequenciando as práticas recomendadas de configuração do computador


As seguintes práticas recomendadas devem ser consideradas ao configurar o computador que executa o sequenciador App-V:

-   **Sequência em um computador que tem uma configuração semelhante e que está executando uma versão anterior do sistema operacional do que os computadores de destino.**

    Verifique se o computador que está executando o sequenciador está executando uma versão anterior do sistema operacional do que os computadores de destino. Isso inclui o Service Pack e as versões de atualização. Por exemplo, se os computadores de destino estiverem executando o WindowsVista e o WindowsXP, você deve sequenciar aplicativos em um computador que esteja executando o WindowsXP. A capacidade de sequenciar em um sistema operacional e executar o aplicativo virtualizado em um sistema operacional diferente não é garantida e depende do aplicativo específico e do sistema operacional. Se você encontrar problemas, talvez seja necessário sequenciar o mesmo ambiente do sistema operacional que o do aplicativo do aplicativo do App-V está em execução.

-   **Configurar o computador que executa o sequenciador com várias partições.**

    Você deve configurar o computador que executa o sequenciador com pelo menos duas partições primárias. A primeira partição (**C:**) deve conter o sistema operacional e deve ser formatada usando o sistema de arquivos NTFS. A segunda partição (**Q:**) é usada como o caminho de destino para a instalação do aplicativo virtual e também deve ser formatada usando o sistema de arquivos NTFS.

-   **Configure o diretório Temp com espaço livre suficiente em disco.**

    O sequenciador usa o diretório **% tmp%** ou **% Temp%** e o diretório de **rascunho** para armazenar arquivos temporários durante o sequenciamento. Você deve configurar esses diretórios no computador que executa o sequenciador com espaço livre em disco equivalente aos requisitos estimados de instalação do aplicativo. Você pode verificar o local do diretório de **rascunho** abrindo o console do sequenciador e selecionando **ferramentas**, **Opções**e, em seguida, selecionando a guia **caminhos** . a configuração de diretórios temporários e o diretório de **rascunho** em partições de disco rígido diferentes podem melhorar o desempenho durante o sequenciamento.

-   **Sequenciar aplicativos usando o Microsoft VirtualPC.**

    Você vai sequenciar a maioria dos aplicativos mais de uma vez. Para ajudar a facilitar isso, você deve considerar o sequenciamento em um computador executado em um ambiente virtual. Dessa forma, você poderá sequenciar um aplicativo e reverter a um estado limpo, com a reconfiguração mínima, no computador que está executando o sequenciador.

    Se você estiver executando o Microsoft Hyper-V em seu ambiente, o sequenciador do App-V será executado quando o computador virtual Hyper-V em que estiver sendo executado for:

    -   pausado e retomado.

    -   tem seu estado salvo e restaurado.

    -   salvo como instantâneo e é restaurado.

    -   migrado para hardware diferente como parte de uma migração ao vivo.

-   **Antes de sequenciar um novo aplicativo, desligue outros programas em execução.**

    Os processos e as tarefas agendadas que normalmente são executados no computador de sequenciamento podem retardar o processo de sequenciamento e fazer com que dados irrelevantes sejam coletados durante o sequenciamento. Todos os aplicativos e programas desnecessários devem ser desligados antes de você começar a sequenciamento.

-   **Sequência em um computador que esteja executando serviços de terminal**

    Você não deve configurar o modo de instalação em um computador que esteja executando serviços de terminal antes de instalar o sequenciador.

## Práticas recomendadas de sequenciamento


As seguintes práticas recomendadas devem ser consideradas ao sequenciar um novo aplicativo:

-   

    **Observação**  Se estiver executando o App-V 4,6 SP1, você não precisará sequenciar para um diretório que siga a Convenção de nomenclatura do 8,3.

     

-   **Sequência para um diretório exclusivo que acompanha a Convenção de nomenclatura do 8,3.**

    Você deve sequenciar todos os aplicativos para um diretório que siga a Convenção de nomenclatura do 8,3. O nome do diretório especificado não pode conter mais de oito caracteres, seguidos por uma extensão de nome de arquivo de três caracteres — por exemplo, **Q:\\MYAPP. ABC**.

-   **Sequência para uma pasta de destino na raiz da unidade, não a um subdiretório.**

    Se o pacote de aplicativos tiver várias partes, instale cada aplicativo em um subdiretório do diretório principal. Por exemplo, se um pacote contiver um aplicativo juntamente com um cliente, use **Q:\\AppSuite** como o diretório principal e sequenciando o aplicativo principal para **Q:\\AppSuite\\Main**e sequenciando o cliente para o **Q:\\AppSuite\\Client**.

-   **Configure e teste o aplicativo durante a fase de instalação.**

    Concluir a instalação de um aplicativo geralmente requer a execução de várias etapas manuais que não fazem parte do processo de instalação do aplicativo. Essas etapas podem envolver a configuração de uma conexão com um banco de dados ou a cópia de arquivos atualizados. Você deve executar essas configurações durante a fase de instalação e, em seguida, executar o aplicativo para garantir que ele funcione.

-   **Execute o aplicativo, várias vezes, se necessário, até que o programa seja estável.**

    Você deve executar o aplicativo várias vezes durante a instalação para garantir que todas as configurações de registro e de caixa de diálogo associadas sejam concluídas. Abrir o aplicativo várias vezes durante a instalação garantirá que somente os recursos relevantes do aplicativo sejam carregados no **bloco de recursos principal**.

-   **Desabilitar todos os recursos de atualização automática associados ao aplicativo.**

    Alguns aplicativos têm a capacidade de verificar as atualizações mais recentes automaticamente durante a instalação. Para auxiliar no controle de versão dos pacotes de aplicativos virtuais, você deve desabilitar esse recurso durante o sequenciamento. Se houver atualizações necessárias, você deve sequenciar um novo pacote de aplicativo virtual com as atualizações associadas instaladas.

## Tópicos relacionados


[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





