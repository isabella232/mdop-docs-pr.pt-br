---
title: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
description: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
author: dansimp
ms.assetid: 0d2192c1-4058-49fb-b0b6-baf4699ac7f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: bc5f295d35dff1e4fc2a84c47188be40153b85c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796157"
---
# Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação


Após concluir a execução do assistente de imagem de recuperação do Microsoft Diagnostic and Recovery Toolset (DaRT) 10 e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 10. Uma partição é recomendada, porque qualquer problema de corrupção que impede o sistema operacional Windows de iniciar também impediria que a imagem de recuperação seja iniciada. Uma partição separada também elimina a necessidade de fornecer a chave de recuperação do BitLocker duas vezes. Considere ocultar a partição para impedir que os usuários armazenem arquivos nela.

**Para implantar o DaRT na partição de recuperação de uma imagem do Windows 10**

1.  Crie uma partição de destino na sua imagem do Windows 10 que seja igual ou maior do que o tamanho do arquivo de imagem ISO que você criou usando o **Assistente de imagem de recuperação do DART 10**.

    O tamanho mínimo necessário para uma partição DaRT é 500MB para acomodar a funcionalidade de conexão remota no DaRT.

2.  Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.

    1.  Usando o método preferido da sua empresa, monte o arquivo de imagem ISO que você criou na página **criar imagem de inicialização** .

    2.  Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.

        **Observação**  Se você gravou um CD, DVD ou USB da imagem de recuperação, poderá abrir os arquivos na mídia removível e copiar o arquivo boot. wim da pasta \\sources. Se você copiar um arquivo boot. wim, não será necessário montar a imagem.

         

3.  Use o arquivo boot. wim para criar uma partição de recuperação inicializável usando o método padrão de sua empresa para criar uma imagem personalizada do Windows RE.

    Para obter mais informações sobre como criar ou personalizar uma partição de recuperação, consulte [Personalizando a experiência do Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Substitua a partição de destino na sua imagem do Windows 10 pela partição de recuperação.

    Para obter mais informações sobre como implantar uma solução de recuperação para reinstalar a imagem de fábrica em caso de falha do sistema, consulte [implantar uma imagem de recuperação do sistema](https://go.microsoft.com/fwlink/?LinkId=214221).

## Tópicos relacionados


[Criação da imagem de recuperação do DaRT 10](creating-the-dart-10-recovery-image.md)

[Implantação da imagem de recuperação do DaRT](deploying-the-dart-recovery-image-dart-10.md)

[Planejamento para o DaRT 10](planning-for-dart-10.md)

 

 





