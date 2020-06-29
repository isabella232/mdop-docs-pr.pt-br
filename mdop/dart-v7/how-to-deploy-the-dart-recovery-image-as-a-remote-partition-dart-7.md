---
title: Como implantar a imagem de recuperação do DaRT como uma partição remota
description: Como implantar a imagem de recuperação do DaRT como uma partição remota
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799298"
---
# Como implantar a imagem de recuperação do DaRT como uma partição remota


Depois de terminar de executar o assistente de imagem de recuperação DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição remota na rede.

**Para implantar o DaRT como uma partição remota**

1.  Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.

    1.  Monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** usando o método preferido da sua empresa para montar uma imagem.

    2.  Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.

        **Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o arquivo boot. wim da pasta \\sources. Isso permite que você ignore a necessidade de montar a imagem.

         

2.  Implante o arquivo boot. wim em um servidor WDS que possa ser acessado dos computadores de usuários finais na sua empresa.

3.  Configure o servidor WDS para usar o arquivo boot. wim para DaRT seguindo seus procedimentos de implantação padrão do WDS.

Para obter mais informações sobre como implantar o DaRT como uma partição remota, consulte o seguinte:

-   [Passo a passo: implantar uma imagem usando o PXE](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [Guia de introdução aos serviços de implantação do Windows](https://go.microsoft.com/fwlink/?LinkId=212106)

## Tópicos relacionados


[Implantação da imagem de recuperação do DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





