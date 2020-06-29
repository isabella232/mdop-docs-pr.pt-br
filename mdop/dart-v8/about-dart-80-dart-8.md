---
title: Sobre o DaRT 8.0
description: Sobre o DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797894"
---
# Sobre o DaRT 8.0


O conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft 8,0 ajuda você a solucionar problemas e reparar computadores baseados no Windows. Isso inclui os computadores que não podem ser iniciados. O DaRT 8,0 é um poderoso conjunto de ferramentas que ampliam o ambiente de recuperação do Windows (WinRE). Ao usar o DaRT, você pode analisar um problema para determinar a causa, por exemplo, ao inspecionar o log de eventos do computador ou o registro do sistema. O DaRT é compatível com a recuperação de discos rígidos básicos que contêm partições, por exemplo, partições primárias e unidades lógicas, além de oferecer suporte à recuperação de volumes.

**Observação**  O DaRT não é compatível com a recuperação de discos dinâmicos.

 

O DaRT também fornece ferramentas para ajudá-lo a corrigir um problema assim que você determinar a causa. Por exemplo, você pode usar as ferramentas do DaRT para desabilitar um driver de dispositivo defeituoso, remover hotfixes, restaurar arquivos excluídos e verificar o computador em busca de malware, mesmo quando não for possível ou não deve iniciar o sistema operacional Windows instalado.

O DaRT pode ajudá-lo a recuperar rapidamente computadores que executam versões de 32 bits ou 64 bits do Windows 8, geralmente em menos tempo do que era necessário para fazer a nova imagem do computador.

A funcionalidade no DaRT permite criar uma imagem de recuperação. A imagem de recuperação inicia o ambiente de recuperação do Windows (Windows RE), a partir da qual você pode iniciar a janela **diagnóstico e do conjunto de ferramentas de recuperação** e acessar as ferramentas do DART.

Use o **Assistente de imagem de recuperação DART** para criar a imagem de recuperação do DART. Por padrão, o assistente cria um arquivo de imagem ISO (International Organization for Standardization) e um arquivo Windows Imaging Format (WIM) e permite que você grave a imagem em um CD, DVD ou USB. Você pode implantar a imagem localmente nos computadores dos usuários finais ou pode implantá-la a partir de uma partição de rede remota ou de uma partição de recuperação no disco rígido local.

## <a href="" id="what-s-new-in-dart-8-0"></a>O que há de novo no DaRT 8,0


O DaRT 8,0 pode ajudá-lo a recuperar rapidamente computadores que executam versões de 32 bits ou 64 bits do Windows 8, geralmente em menos tempo do que seria necessário para fazer a nova imagem do computador. O DaRT 8,0 tem os novos recursos a seguir.

### Criar imagens DaRT usando o Windows 8 ou o Windows Server 2012

O DaRT 8,0 permite que você crie imagens DaRT usando o Windows® 8 ou o Windows Server® 2012. Para versões do Windows anteriores ao Windows 8 e Windows Server 2012, os clientes devem continuar a usar versões anteriores do DaRT.

### Gerar imagens de 32 e de 64 bits a partir de um computador

O DaRT 8,0 permite que você gere imagens de 32 bits e de 64 bits a partir de um único computador que esteja executando o DaRT, independentemente de o computador ser um computador de 32 ou de 64 bits. No DaRT7, a imagem que foi criada precisa ser igual, bit a bit, como o computador que estava executando o DaRT.

### Crie uma imagem compatível com computadores que tenham uma interface BIOS ou UEFI

O suporte do DaRT 8.0 para a interface de firmware unificada (UEFI) e interfaces do BIOS permite que você crie apenas uma imagem que funcione com computadores que tenham uma interface.

### Usar uma GPT (tabela de partição GUID) para particionamento

Agora, as ferramentas do DaRT 8,0 dão suporte a discos GPT do Windows 8, que fornecem um mecanismo mais flexível para particionar discos do que o esquema de particionamento MBR (MBR) mais antigo. As ferramentas do DaRT 8,0 continuam a dar suporte ao particionamento MBR.

### Instalar o Windows 8 e o Windows Server 2012 no disco rígido local

As ferramentas do DaRT 8,0 podem ser usadas apenas quando o Windows 8 e o Windows Server 2012 são instalados no disco rígido local. No momento, não há suporte para o Windows to go.

### <a href="" id="-------------dart-8-0-release-notes"></a> Notas de versão do DaRT 8,0

Para saber mais e saber mais sobre as últimas notícias que não o fizeram na documentação, consulte as notas de [versão do DaRT 8,0](release-notes-for-dart-80--dart-8.md).

## Como obter o DaRT 8,0


Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Tópicos relacionados


[Introdução ao DaRT 8.0](getting-started-with-dart-80-dart-8.md)

[Notas de versão do DaRT 8.0](release-notes-for-dart-80--dart-8.md)

 

 





