---
title: Recuperar computadores usando o DaRT 7.0
description: Recuperar computadores usando o DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799138"
---
# Recuperar computadores usando o DaRT 7.0


Há dois métodos disponíveis para recuperar computadores usando o Microsoft Diagnostics e o conjunto de ferramentas de recuperação (DaRT) 7. Você pode executar a imagem de recuperação do DaRT7 localmente ou usar o recurso conexão remota disponível no DaRT7 para recuperar um computador remoto. Os dois métodos são descritos com mais detalhes nesta seção.

## Recuperar computadores locais usando a imagem de recuperação do DaRT


Para recuperar um computador local usando o DaRT7, você deve estar fisicamente presente no computador do usuário final que está apresentando problemas que exijam o DaRT.

Você tem vários métodos diferentes para escolher para inicializar o DaRT, dependendo de como você implanta a imagem de recuperação do DaRT.

-   Insira um CD, DVD ou unidade flash USB para a imagem de recuperação do DaRT no computador com problema e use-o para inicializar no computador.

-   Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.

-   Inicialize no DaRT a partir de uma partição remota na rede.

Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.

**Observação**  A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.

 

[Como recuperar computadores locais usando a imagem de recuperação do DaRT](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## Recuperar computadores remotos usando a imagem de recuperação do DaRT


O recurso conexão remota no DaRT permite que um administrador de ti execute as ferramentas do DaRT remotamente em um computador de usuário final. Depois que determinadas informações forem fornecidas pelo usuário final (ou por um profissional de assistência técnica em funcionamento no computador do usuário final), o administrador de ti ou o agente de helpdesk poderá assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.

**Importante**  Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.

 

A janela **diagnóstico e recuperação do conjunto de ferramentas de recuperação** inclui a opção para executar o DART em um computador de usuário final remotamente a partir de um computador administrador. O usuário final abre as ferramentas DaRT no computador problemático e inicia a sessão remota clicando em **conexão remota**.

O recurso conexão remota no computador do usuário final cria as seguintes informações de conexão: um número de tíquete, uma porta e uma lista de todos os endereços IP disponíveis. O número do bilhete e a porta são gerados aleatoriamente.

O administrador de ti ou o agente de assistência técnica insere essas informações no **Visualizador de conexão remota do DART** para estabelecer a conexão de serviços de terminal com o computador do usuário final. A conexão de serviços de terminal que é estabelecida permite que um administrador de ti interaja remotamente com as ferramentas do DaRT no computador do usuário final. Em seguida, o computador do usuário final processa as informações de conexão, compartilha sua tela e responde às instruções do computador do administrador de ti.

[Como recuperar computadores remotos usando a imagem de recuperação do DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## Outros recursos para recuperar computadores usando o DaRT7


[Operações do DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





