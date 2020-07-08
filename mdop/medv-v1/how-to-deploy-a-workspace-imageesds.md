---
title: Como implantar uma imagem de espaço de trabalho
description: Como implantar uma imagem de espaço de trabalho
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799985"
---
# Como implantar uma imagem de espaço de trabalho


Ao usar um sistema de distribuição de software corporativo, uma nova imagem pode ser implantada em computadores cliente de uma das seguintes maneiras:

-   [Download da Web](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pré-preparação de imagem](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Como implantar uma imagem de espaço de trabalho via Web


**Para implantar uma imagem de espaço de trabalho via Web**

1.  Carregue a imagem do MED-V para o servidor.

    Para obter informações sobre como carregar a imagem, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).

2.  Usando o sistema de distribuição de software corporativo, instale o pacote. msi do cliente MED-V nos computadores dos usuários.

    Para obter informações sobre como instalar o pacote do cliente. msi do MED-V, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientesds.md).

    O cliente MED-V está instalado e iniciado pela primeira vez. Na primeira inicialização, o cliente baixa a imagem do endereço do servidor especificado na instalação do cliente.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Como implantar uma imagem de espaço de trabalho usando a pré-preparação de imagem


**Para implantar uma imagem de espaço de trabalho usando a transferência prévia de imagem**

1.  Crie uma pasta pré-teste de imagem e empurre a imagem para a pasta.

    Para obter informações sobre como configurar o pré-teste de imagem, consulte [como configurar o pré-teste de imagem](how-to-configure-image-pre-staging.md).

2.  Usando o sistema de distribuição de software corporativo, instale o pacote. msi do cliente MED-V nos computadores dos usuários.

    Para obter informações sobre como instalar o pacote do cliente. msi do MED-V, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientesds.md).

    O cliente MED-V está instalado e iniciado pela primeira vez. Na primeira inicialização, o cliente busca a imagem da pasta de pré-teste especificada na instalação do cliente.

## Tópicos relacionados


[Como configurar o servidor de distribuição na Web de imagem](how-to-configure-the-image-web-distribution-server.md)

 

 





