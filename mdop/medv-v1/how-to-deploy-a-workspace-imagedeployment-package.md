---
title: Como implantar uma imagem de espaço de trabalho
description: Como implantar uma imagem de espaço de trabalho
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799987"
---
# Como implantar uma imagem de espaço de trabalho


Ao usar um pacote de implantação, uma nova imagem pode ser implantada em computadores cliente de uma das seguintes maneiras:

-   [Download da Web](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pré-preparação de imagem](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [Implantando a imagem dentro do pacote de implantação](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Como implantar uma imagem de espaço de trabalho via Web


**Para implantar uma imagem de espaço de trabalho via Web**

1.  Carregue a imagem do MED-V para o servidor.

    Para obter informações sobre como carregar a imagem, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).

2.  Crie um pacote de implantação e inclua o caminho do servidor para o local da imagem.

    Para obter informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).

3.  Implante o pacote para os usuários finais.

    Para obter informações sobre a implantação do pacote, consulte [como instalar o cliente do MED-V](how-to-install-med-v-clientdeployment-package.md).

    O cliente MED-V está instalado e iniciado pela primeira vez. Na primeira inicialização, o cliente baixa a imagem do endereço do servidor especificado na instalação do cliente.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Como implantar uma imagem de espaço de trabalho usando a pré-preparação de imagem


**Para implantar uma imagem de espaço de trabalho usando a transferência prévia de imagem**

1.  Crie uma pasta pré-teste de imagem e empurre a imagem para a pasta.

    Para obter informações sobre como configurar o pré-teste de imagem, consulte [como configurar o pré-teste de imagem](how-to-configure-image-pre-staging.md).

2.  Crie um pacote de implantação e inclua o caminho para a pasta anterior ao pré-teste da imagem.

    Para obter informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).

3.  Implante o pacote para os usuários finais.

    Para obter informações sobre a implantação do pacote, consulte [como instalar o cliente do MED-V](how-to-install-med-v-clientdeployment-package.md).

    O cliente MED-V está instalado e iniciado pela primeira vez. Na primeira inicialização, o cliente busca a imagem da pasta de pré-teste especificada na instalação do cliente.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a>Como implantar uma imagem de espaço de trabalho usando um pacote de implantação


**Para implantar uma imagem de espaço de trabalho usando um pacote de implantação**

1.  Crie um pacote de implantação e inclua a imagem no pacote.

    Para obter informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md).

2.  Implante o pacote para os usuários finais.

    Para obter informações sobre a implantação do pacote, consulte [como instalar o cliente do MED-V](how-to-install-med-v-clientdeployment-package.md).

    A imagem é importada para o host como parte da instalação do pacote.

## Tópicos relacionados


[Como configurar o servidor de distribuição na Web de imagem](how-to-configure-the-image-web-distribution-server.md)

[Como configurar um pacote de implantação](how-to-configure-a-deployment-package.md)

 

 





