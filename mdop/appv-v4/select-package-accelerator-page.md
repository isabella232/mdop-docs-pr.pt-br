---
title: Selecione a página Acelerador de pacote
description: Selecione a página Acelerador de pacote
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796756"
---
# Selecione a página Acelerador de pacote


Use a página **selecionar acelerador de pacote** para selecionar o acelerador de pacote que será usado para criar o novo pacote de aplicativo virtual. Você deve copiar o acelerador de pacote para uma pasta no computador que executa o sequenciador App-V. Para obter mais informações, consulte sobre o app [-v Package Accelerators (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

Só execute aceleradores de pacote de editores nos quais você confia. Os aceleradores de pacote geralmente incluem uma assinatura digital. Uma assinatura digital é uma marca de segurança eletrônica que pode ajudar a indicar o fornecedor do software e se o pacote foi adulterado após a transformação ter sido assinada originalmente. Se você usar uma transformação que foi assinada digitalmente por um fornecedor e o fornecedor tiver verificado sua identidade com uma autoridade de certificação, você poderá ter mais certeza de que a transformação vem desse fornecedor específico e não tenha sido alterada.

O sequenciador App-V informa se qualquer uma das seguintes condições é verdadeira:

-   A transformação selecionada não foi assinada digitalmente.

-   A transformação selecionada é assinada por um fornecedor que não verificou sua identidade com uma autoridade de certificação.

-   A transformação selecionada foi alterada após ter sido assinada e liberada digitalmente.

Se qualquer uma dessas mensagens for exibida ao usar aceleradores de pacote, acesse o site do Publisher aceleradores de pacote para obter uma versão assinada digitalmente da transformação.

Esta página contém os seguintes elementos:

<a href="" id="browse"></a>**Procurar**  
Clique em **procurar** para especificar o acelerador de pacote que será usado para criar o pacote de aplicativo virtual. Salve o acelerador de pacote especificado localmente no computador que está executando o sequenciador.

## Tópicos relacionados


[Assistente do Sequencer - Acelerador de Pacote (App-V 4.6 SP1)](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





