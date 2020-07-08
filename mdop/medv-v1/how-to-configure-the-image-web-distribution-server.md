---
title: Como configurar o servidor de distribuição na Web de imagem
description: Como configurar o servidor de distribuição na Web de imagem
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799616"
---
# Como configurar o servidor de distribuição na Web de imagem


Um repositório de imagens é um servidor opcional que é usado para distribuição de imagens (em que os administradores carregam novas imagens e os computadores cliente verificam o servidor a cada 15 minutos e atualizam sua imagem se um novo estiver disponível).

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


Um servidor de distribuição de imagens requer o seguinte:

-   Serviços de informações da Internet (IIS) — para obter informações, consulte [serviços de informações da Internet](https://go.microsoft.com/fwlink/?LinkId=142995).

    Durante a instalação do IIS, ao adicionar serviços de função, selecione os seguintes métodos de autenticação compatíveis:

    -   **Autenticação básica**

    -   **Autenticação do Windows**

    -   **Autenticação de mapeamento de certificado do cliente**

    Ao configurar o IIS, inclua o seguinte:

    -   Adicione um diretório virtual, com o alias chamado **MEDVImages**. O caminho físico deve apontar para o local das imagens.

    -   Habilite o BITS.

    -   Adicione os seguintes tipos de MIME:

        -   **. CKM (application/octet-stream)**

        -   **. Index (application/octet-stream**)

    -   No site do MED-V, adicione permissões de leitura para **todos**.

    -   Reinicie o IIS.

-   Extensões de servidor BITS para IIS — para obter informações, consulte [instalar extensões de servidor bits](https://go.microsoft.com/fwlink/?LinkId=142996).

## Tópicos relacionados


[Configurações com suporte](supported-configurationsmedv-orientation.md)

[Projetar os repositórios de imagens do MED-V](design-the-med-v-image-repositories.md)

 

 





