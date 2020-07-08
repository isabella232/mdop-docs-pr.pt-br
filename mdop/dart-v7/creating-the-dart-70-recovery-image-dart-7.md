---
title: Criação da imagem de recuperação do DaRT 7.0
description: Criação da imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799241"
---
# Criação da imagem de recuperação do DaRT 7.0


O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 inclui o **Assistente de imagem de recuperação do DART** que é usado no Windows para criar uma imagem ISO (organização internacional) inicializável (ISO). Uma imagem ISO é um arquivo que representa o conteúdo bruto de um CD.

## Usar o assistente de imagem de recuperação do DaRT para criar a imagem de recuperação


O ISO criado pelo assistente de imagem de recuperação DaRT contém a imagem de recuperação do DaRT que permite que você inicialize em um computador com problema, mesmo que ele não seja iniciado. Após inicializar o computador no DaRT, você pode executar as diferentes ferramentas do DaRT para tentar diagnosticar e reparar o computador.

Você pode escrever o ISO em um CD ou DVD gravável, salvá-lo em uma unidade flash USB ou salvá-lo em um formato que você pode usar para inicializar o DaRT a partir de uma partição remota ou de uma partição de recuperação. Para obter mais informações, consulte [implantando a imagem de recuperação do DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

**Observação**  Se o seu computador inclui uma unidade de CD-RW, o assistente oferece para gravar a imagem ISO em um CD ou DVD em branco. Se o seu computador não incluir uma unidade compatível com o assistente, você poderá gravar a imagem ISO em um CD ou DVD usando a maioria dos programas que podem gravar um CD ou DVD.

 

Para criar um CD ou DVD inicializável a partir da imagem ISO, você deve ter:

-   Uma unidade de CD-RW.

-   Um CD ou DVD gravável (em um formato compatível com a unidade gravável).

-   Software que dá suporte à unidade gravável e suporta a gravação de uma imagem ISO diretamente em um CD ou DVD.

    **Importante**  Teste o CD ou DVD que você cria em todos os diferentes tipos de computadores que você pretende dar suporte, porque alguns computadores não podem iniciar de todos os tipos de mídias graváveis.

     

Para salvar a imagem ISO em uma unidade flash USB (UFD), você deve ter:

-   Uma unidade UFD formatada corretamente.

-   Um programa que você pode usar para montar a imagem ISO.

[Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## Criar uma imagem de recuperação limitada por tempo


Você pode criar uma imagem de recuperação do DaRT que só pode ser usada por um determinado número de dias após a geração. Para fazer isso, você deve executar o **Assistente de imagem de recuperação do DART** em um prompt de comando e especificar o número de dias.

[Como criar uma imagem de recuperação por tempo limitado](how-to-create-a-time-limited-recovery-image-dart-7.md)

## Outros recursos para criar a imagem de recuperação do DaRT7


-   [Implantação do DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





