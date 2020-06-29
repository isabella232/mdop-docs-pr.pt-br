---
title: Sobre o DaRT 7.0
description: Sobre o DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799239"
---
# Sobre o DaRT 7.0


O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 ajuda você a solucionar problemas e reparar desktops baseados no Windows. Isso inclui as áreas de trabalho que não podem ser iniciadas. O DaRT é um poderoso conjunto de ferramentas que ampliam o ambiente de recuperação do Windows (WinRE). Ao usar o DaRT, você pode analisar um problema para determinar a causa, por exemplo, ao inspecionar o log de eventos do computador ou o registro do sistema.

O DaRT também fornece ferramentas para ajudá-lo a corrigir um problema assim que você determinar a causa. Por exemplo, você pode usar as ferramentas do DaRT para desabilitar um driver de dispositivo defeituoso, remover hotfixes, restaurar arquivos excluídos e verificar o computador em busca de malware, mesmo quando não for possível ou não deve iniciar o sistema operacional Windows instalado.

O DaRT pode ajudá-lo a recuperar rapidamente computadores que executam versões de 32 bits ou 64 bits do Windows 7, geralmente em menos tempo do que era necessário para fazer a nova imagem do computador.

## Sobre a imagem de recuperação do DaRT 7


A funcionalidade no DaRT permite criar uma imagem de recuperação baseada no WinRE combinado com um conjunto de ferramentas fornecidas pelo DaRT. A imagem de recuperação do DaRT aproveita o WinRE, a partir da qual você pode acessar a janela **diagnóstico e conjunto de ferramentas de recuperação** .

Use o **Assistente de imagem de recuperação DART** para criar a imagem de recuperação do DART. Por padrão, o assistente cria um arquivo de imagem International Organization for Standardization (ISO) na sua área de trabalho chamado DaRT70. ISO, embora você possa especificar um local e um nome de arquivo diferentes. O assistente também permite que você grave a imagem em um CD ou DVD. Depois de concluir o assistente, você pode salvar a imagem de recuperação em uma unidade flash USB ou salvá-la em um formato que possa ser usado para criar uma partição remota ou uma partição de recuperação.

Quando você precisa usar o DaRT para inicializar um computador de usuário final que não inicia, você pode seguir as instruções sobre [como recuperar computadores locais usando a imagem de recuperação do DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).

Para obter informações detalhadas sobre as ferramentas no DaRT, consulte [visão geral das ferramentas do dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

## <a href="" id="what-s-new-in-dart-7"></a>O que há de novo no DaRT 7


O DaRT7 continua a dar suporte a todos os cenários incluídos nas versões anteriores e ele adiciona um novo recurso de conexão remota, além de três novas opções de implantação.

### Criação de imagens do DaRT 7

O assistente que você usa para criar imagens ISO do DaRT agora é chamado de **imagem de recuperação DART** e agora oferece suporte a uma opção para habilitar ou desabilitar o novo recurso de conexão remota. A conexão remota permite que um agente de helpdesk execute as ferramentas DaRT a partir de um local remoto. Em versões anteriores, o agente de helpdesk precisa estar fisicamente presente no computador do usuário final para executar as ferramentas do DaRT.

O assistente também permite que você personalize a mensagem de boas-vindas do recurso conexão remota (a mensagem é exibida quando os usuários finais executam a ferramenta conexão remota). Os administradores de ti também podem configurar qual número de porta deve ser usado pela conexão remota.

Para obter mais informações sobre o **Assistente de imagem de recuperação do DART** ou conexão remota, consulte [criando a imagem de recuperação do DART 7,0](creating-the-dart-70-recovery-image-dart-7.md).

### Implantação ISO do DaRT 7

Além de gravar em um CD ou DVD, o DaRT7 adiciona três novas opções ao implantar o ISO que contém a imagem de recuperação do DaRT:

-   Implantação de unidade flash USB

-   Implantação de partição remota

-   Implantação de partição de recuperação

A opção de implantação de unidade flash USB permite que uma empresa use o DaRT em computadores que não tenham unidades de CD ou DVD disponíveis. As opções de recuperação e partição remota permitem que os usuários finais tenham acesso fácil à imagem do DaRT e habilitar a funcionalidade de conexão remota.

Para obter mais informações sobre como implantar imagens de recuperação do DaRT, consulte [implantando a imagem de recuperação do dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

## Tópicos relacionados


[Introdução ao DaRT 7.0](getting-started-with-dart-70-new-ia.md)

[Notas de versão do DaRT 7.0](release-notes-for-dart-70-new-ia.md)

 

 





