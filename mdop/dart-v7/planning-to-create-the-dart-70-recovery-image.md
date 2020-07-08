---
title: Planejamento para criar a imagem de recuperação do DaRT 7.0
description: Planejamento para criar a imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797904"
---
# Planejamento para criar a imagem de recuperação do DaRT 7.0


Use as informações desta seção quando planejar a criação da imagem de recuperação do Microsoft diagnóstico e do conjunto de ferramentas de recuperação (DaRT) 7.

## Planejando criar a imagem de recuperação do DaRT 7


Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem. Quando você fizer essa decisão, lembre-se de que os usuários finais podem ter acesso às vezes a várias ferramentas DaRT. Para obter mais informações sobre as ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 7,0](overview-of-the-tools-in-dart-70-new-ia.md). Para obter mais informações sobre como criar uma imagem de recuperação segura, consulte [considerações de segurança para o DaRT 7,0](security-considerations-for-dart-70-dart-7.md).

Ao criar a imagem de recuperação do DaRT, você também especifica se deseja incluir drivers ou arquivos adicionais. Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.

## Pré-requisitos


Os seguintes itens são necessários ou recomendados para criar a imagem de recuperação do DaRT:

-   Arquivos de origem do Windows 7

    Você deve fornecer o caminho de um DVD do Windows 7 ou dos arquivos de origem do Windows 7. Os arquivos de origem do Windows 7 são necessários para criar a imagem de recuperação do DaRT.

-   Ferramentas de depuração do Windows para a sua plataforma

    As ferramentas de depuração do Windows são necessárias ao executar o **Crash Analyzer** para determinar a causa da falha do computador. Recomendamos que você especifique o caminho das ferramentas de depuração do Windows no momento em que cria a imagem de recuperação do DaRT. Se for necessário, você pode baixar as ferramentas de depuração do Windows aqui: [baixar e instalar as ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

-   Opcional: definições de **limpeza de sistema autônomo**

    As definições mais recentes para o **standalone System Sweeper** são necessárias ao executar essa ferramenta. Embora você possa baixar as definições ao executar o **standalone System Sweeper**, recomendamos que baixe as definições mais recentes no momento em que cria a imagem de recuperação do DART. Dessa forma, você ainda pode executar a ferramenta com as definições mais recentes mesmo que o computador com problema não tenha conectividade de rede.

-   Opcional: Arquivos de símbolos do Windows para uso com o **Crash Analyzer**

    Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele travou. Para obter mais informações, consulte [diagnosticar falhas do sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

## Tópicos relacionados


[Planejamento da implantação do DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





