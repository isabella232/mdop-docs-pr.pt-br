---
title: Implantação da imagem de recuperação do DaRT
description: Implantação da imagem de recuperação do DaRT
author: dansimp
ms.assetid: 2b859da6-e31a-4240-8868-93a754328cf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de3ed9c01a1808364158124c4f2dcab835823a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796169"
---
# Implantação da imagem de recuperação do DaRT


Depois de criar o arquivo ISO (organização internacional de normalização) que contém a imagem de recuperação do Microsoft (Microsoft Diagnostics and Recovery Toolset) 10, você pode implantar a imagem de recuperação do DaRT 10 em toda a sua empresa, para que ela fique disponível para usuários finais e trabalhadores de suporte técnico. Há quatro métodos compatíveis que você pode usar para implantar a imagem de recuperação do DaRT. Para revisar as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).

Gravar o arquivo de imagem ISO em um CD ou DVD usando o assistente de imagem de recuperação do DaRT

Salvar o conteúdo do arquivo de imagem ISO em uma unidade flash USB (UFD) usando o assistente de imagem de recuperação do DaRT

Extrair o arquivo boot. wim da imagem ISO e implantá-lo como uma partição remota disponível para os computadores dos usuários finais

Extrair o arquivo boot. wim da imagem ISO e implantá-lo na partição de recuperação de uma nova instalação do Windows 10

**Importante**  O **Assistente de imagem de recuperação do DART** fornece a opção de gravar a imagem em um CD, DVD ou UFD, mas os outros métodos de salvar e implantar a imagem de recuperação exigem etapas adicionais que envolvem ferramentas que não estão incluídas no DART. Algumas diretrizes e links para esses outros métodos são fornecidos nesta seção.

 

## Implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação


Depois de terminar de executar o assistente de recuperação de imagem do DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 10.

[Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-10.md)

## Implantar a imagem de recuperação do DaRT como uma partição remota


Você pode hospedar a imagem de recuperação em um servidor de inicialização de rede central, como os serviços de implantação do Windows, e permitir que os usuários ou a equipe de suporte transmitam a imagem para os computadores sob demanda.

[Como implantar a imagem de recuperação do DaRT como uma partição remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-10.md)

## Outros recursos para a implantação da imagem de recuperação do DaRT


[Implantação do DaRT 10](deploying-dart-10.md)

 

 





