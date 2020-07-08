---
title: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
description: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799296"
---
# Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação


Depois de terminar de executar o assistente de recuperação de imagem do DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 7.

**Para implantar o DaRT na partição de recuperação de uma imagem do Windows 7**

1.  Crie uma partição de destino na sua imagem do Windows 7 que seja igual ou maior do que o tamanho do arquivo de imagem ISO que você criou usando o **Assistente de imagem de recuperação DART**.

    O tamanho mínimo necessário para uma partição DaRT é de aproximadamente 300MB. No entanto, recomendamos que o 450MB acomode a funcionalidade de conexão remota no DaRT.

2.  Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.

    1.  Monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** usando o método preferido da sua empresa para montar uma imagem.

    2.  Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.

        **Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o arquivo boot. wim da pasta \\sources. Isso permite que você ignore a necessidade de montar a imagem.

         

3.  Use o arquivo boot. wim para criar uma partição de recuperação inicializável usando o método padrão de sua empresa para criar uma imagem personalizada do Windows RE.

    Para obter mais informações sobre como criar ou personalizar uma partição de recuperação, consulte [Personalizando a experiência do Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Substitua a partição de destino na sua imagem do Windows 7 pela partição de recuperação.

Depois que a imagem do Windows 7 estiver pronta, distribua a imagem para os computadores da sua empresa usando o processo padrão de implantação de imagens da sua empresa. Para obter mais informações sobre como criar uma imagem do Windows 7, consulte [criando uma imagem padrão do Windows 7: guia](https://go.microsoft.com/fwlink/?LinkId=212103)passo a passo.

Para obter mais informações sobre como implantar uma solução de recuperação para reinstalar a imagem de fábrica em caso de falha do sistema, consulte [implantar uma imagem de recuperação do sistema](https://go.microsoft.com/fwlink/?LinkId=214221).

## Tópicos relacionados


[Implantação da imagem de recuperação do DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





