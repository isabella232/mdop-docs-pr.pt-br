---
title: Planejamento da implantação do DaRT 7.0
description: Planejamento da implantação do DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797901"
---
# Planejamento da implantação do DaRT 7.0


Há várias configurações e pré-requisitos de implantação diferentes que devem ser consideradas antes de criar seu plano de implantação. Esta seção inclui informações que podem ajudá-lo a obter as informações que você precisa ter para formular um plano de implantação que melhor atenda às suas necessidades de negócios.

Considere o seguinte ao planejar a instalação do Microsoft diagnóstico e do conjunto de ferramentas de recuperação (DaRT) 7:

-   Ao instalar o DaRT, você pode instalar toda a funcionalidade em um computador administrador de ti no qual executará todas as tarefas associadas à execução do DaRT. Ou você pode instalar apenas a funcionalidade DaRT que cria a imagem de recuperação no computador do administrador de ti. Em seguida, instale a funcionalidade usada para executar o DaRT, como o **Visualizador de conexão remota do DART** e o **Crash Analyzer**, no computador do agente da assistência técnica.

-   Para poder executar o DaRT remotamente, certifique-se de que o computador do agente de helpdesk e todos os computadores que você pode estar Solucionando remotamente estejam na mesma rede.

-   Antes de implantar o DaRT na produção, você pode primeiro construir um ambiente de laboratório para testes. Um laboratório de teste deve incluir no mínimo dois computadores, um para atuar como administrador de ti/agente de helpdesk e outro para atuar como um computador de usuário final. Ou você pode usar três computadores em seu laboratório se quiser separar as responsabilidades do administrador de ti daquelas do agente da assistência técnica.

## Examine as configurações com suporte


Você deve revisar as informações de configuração do Microsoft Diagnostics and Recovery Toolset (DaRT) 7 para confirmar que os computadores selecionados para a instalação de cliente ou de recurso atendem aos requisitos mínimos de hardware e sistema operacional.

[Configurações compatíveis do DaRT 7.0](dart-70-supported-configurations-dart-7.md)

## Plano para a criação da imagem de recuperação do DaRT


Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem. Quando você fizer essa decisão, lembre-se de que os usuários finais podem ter acesso às vezes a várias ferramentas DaRT. Quando você criar a imagem de recuperação, também será possível especificar se deseja incluir drivers ou arquivos adicionais. Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.

Você deve estar ciente dos pré-requisitos e outras recomendações de planejamento adicionais para criar a imagem de recuperação do DaRT.

[Planejamento para criar a imagem de recuperação do DaRT 7.0](planning-to-create-the-dart-70-recovery-image.md)

## Plano para salvar e implantar a imagem de recuperação do DaRT


Vários métodos podem ser usados para salvar e implantar a imagem de recuperação do DaRT. Ao determinar o método que você vai usar, considere as vantagens e desvantagens de cada um. Além disso, considere como você deseja usar o DaRT na sua empresa.

**Observação**  Talvez você queira usar mais de um método em sua organização. Por exemplo, você pode inicializar o DaRT a partir de uma partição remota para a maioria das situações e ter uma unidade flash USB disponível para o caso de o computador do usuário final não conseguir se conectar à rede.

 

[Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## Outros recursos para planejar a implantação do DaRT


[Planejamento para o DaRT 7.0](planning-for-dart-70-new-ia.md)

 

 





