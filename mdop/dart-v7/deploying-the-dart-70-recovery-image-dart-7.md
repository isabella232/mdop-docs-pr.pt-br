---
title: Implantação da imagem de recuperação do DaRT 7.0
description: Implantação da imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796054"
---
# Implantação da imagem de recuperação do DaRT 7.0


Depois de criar o arquivo ISO (organização internacional de normalização) que contém a imagem de recuperação do Microsoft diagnóstico e recuperação do conjunto de ferramentas de recuperação (DaRT) 7, você pode implantar a imagem de recuperação do DaRT em toda a sua empresa para que ela fique disponível para os usuários finais e agentes da assistência técnica. Há quatro métodos compatíveis que você pode usar para implantar a imagem de recuperação do DaRT.

-   Gravar o arquivo de imagem ISO em um CD ou DVD

-   Salvar o conteúdo do arquivo de imagem ISO em uma unidade flash USB (UFD)

-   Extrair o arquivo boot. wim da imagem ISO e implantá-lo como uma partição remota disponível para os computadores dos usuários finais

-   Extrair o arquivo boot. wim da imagem ISO e implantá-lo na partição de recuperação de uma nova instalação do Windows 7

**Importante**  O **Assistente de imagem de recuperação DART** oferece apenas a opção de gravar um CD ou DVD. Todos os outros métodos de salvar e implantar a imagem de recuperação exigem etapas adicionais que envolvem ferramentas que não estão incluídas no DaRT. Algumas diretrizes e links para esses outros métodos são fornecidos nesta seção.

 

## Implantar a imagem de recuperação do DaRT usando uma unidade flash USB


Após concluir a execução do assistente de imagem de recuperação DaRT, você pode usar a ferramenta em <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar o arquivo de imagem ISO para uma unidade flash USB (UFD).

[Como implantar a imagem de recuperação do DaRT usando um pen drive](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## Implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação


Depois de terminar de executar o assistente de recuperação de imagem do DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 7.

[Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## Implantar a imagem de recuperação do DaRT como uma partição remota


Depois de terminar de executar o assistente de imagem de recuperação DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição remota na rede.

[Como implantar a imagem de recuperação do DaRT como uma partição remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## Outros recursos para manter a implantação da imagem de recuperação do DaRT


-   [Implantação do DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





