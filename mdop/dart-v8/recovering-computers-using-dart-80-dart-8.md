---
title: Recuperar computadores usando o DaRT 8.0
description: Recuperar computadores usando o DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799558"
---
# Recuperar computadores usando o DaRT 8.0


Após implantar a imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, você pode usar o DaRT 8,0 para recuperar computadores. As informações nesta seção descrevem as tarefas de recuperação que você pode executar.

Você tem vários métodos diferentes para escolher para inicializar o DaRT, dependendo de como você implanta a imagem de recuperação do DaRT.

-   Insira um CD, DVD ou unidade flash USB para a imagem de recuperação do DaRT no computador com problema e use-o para inicializar no computador.

-   Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.

-   Inicialize no DaRT a partir de uma partição remota na rede.

Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.

**Observação**  A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.

 

## Recuperar um computador local usando a imagem de recuperação do DaRT


Para recuperar um computador local usando o DaRT, você deve estar fisicamente presente no computador do usuário final que está tendo problemas que exijam o DaRT.

[Como recuperar computadores locais usando a imagem de recuperação do DaRT](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## Recuperar um computador remoto usando a imagem de recuperação do DaRT


O recurso conexão remota no DaRT permite que um administrador de ti execute as ferramentas do DaRT remotamente em um computador de usuário final. Depois que determinadas informações são fornecidas pelo usuário final (ou por um profissional de suporte técnico trabalhando no computador do usuário final), o administrador de ti ou o trabalhador de suporte técnico pode assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.

**Importante**  Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.

 

A janela **diagnóstico e recuperação do conjunto de ferramentas de recuperação** inclui a opção para executar o DART em um computador de usuário final remotamente a partir de um computador administrador. O usuário final abre as ferramentas DaRT no computador problemático e inicia a sessão remota clicando em **conexão remota**.

O recurso conexão remota no computador do usuário final cria as seguintes informações de conexão: um número de tíquete, uma porta e uma lista de todos os endereços IP disponíveis. O número do bilhete e a porta são gerados aleatoriamente.

O administrador de ti ou o trabalho de suporte técnico insere essas informações no **Visualizador de conexão remota do DART** para estabelecer a conexão de serviços de terminal com o computador do usuário final. A conexão de serviços de terminal que é estabelecida permite que um administrador de ti interaja remotamente com as ferramentas do DaRT no computador do usuário final. Em seguida, o computador do usuário final processa as informações de conexão, compartilha sua tela e responde às instruções do computador do administrador de ti.

[Como recuperar computadores remotos usando a imagem de recuperação do DaRT](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## Outros recursos para recuperar computadores usando o DaRT 8,0


[Operações do DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





