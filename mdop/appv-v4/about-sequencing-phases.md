---
title: Sobre Sequenciamento de Fases
description: Sobre Sequenciamento de Fases
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797638"
---
# Sobre Sequenciamento de Fases


O sequenciamento é o processo pelo qual você cria um pacote de aplicativo sequenciado usando o sequenciador do Microsoft Application Virtualization (App-V). Durante o sequenciamento, o sequenciador monitora e registra todos os processos de instalação e configuração de um aplicativo e cria os seguintes arquivos: ICO, OSD, SFT e SPRJ. Esses arquivos contêm todas as informações necessárias sobre um aplicativo e permitem que o aplicativo seja executado em um ambiente virtual.

As quatro fases para sequenciar um aplicativo e a criação de um pacote de aplicativo virtual são instalação, inicialização, personalização e salvamento. A lista a seguir fornece informações sobre cada uma das fases:

1.  **Fase de instalação**– durante a fase de instalação, você especifica o nome do pacote e um comentário associado opcional que será associado ao pacote. Você também pode configurar opções avançadas de monitoramento durante essa fase. As opções de monitoramento avançado incluem especificar o tamanho do bloco e se você vai instalar atualizações automáticas durante o monitoramento. O sequenciador registra todas as informações e configurações necessárias necessárias para criar um pacote de aplicativo virtual e as configurações de arquivo e registro associadas.

    **Importante**  Para exibir as opções avançadas, selecione **Mostrar opções de monitoramento avançado** na página **informações do pacote** .

     

2.  **Fase de lançamento**– durante a fase de lançamento, você pode especificar qualquer associação de arquivo e descritores de segurança necessários que devem ser configurados com o pacote. Você deve abrir o aplicativo quantas vezes forem necessárias para garantir a funcionalidade e estabilidade do aplicativo.

3.  **Fase de personalização**– durante a fase de personalização, você pode configurar seu pacote usando os arquivos. OSD associados. Você pode especificar se qualquer script associado deve ser executado dentro ou fora do ambiente virtual, especificar ações adicionais que devem ser realizadas, especificar como os scripts associados são executados (de forma síncrona ou assíncrona) e especificar quaisquer scripts adicionais que devem ser executados no contexto do usuário.

4.  **Fase de salvamento**– durante a fase de salvamento, todos os arquivos necessários para o pacote de aplicativo virtual são criados. Os arquivos criados são. sprj,. SFT,. OSD,. ico,. xml Manifest e o arquivo Windows Installer (. msi).

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





