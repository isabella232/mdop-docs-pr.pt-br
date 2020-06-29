---
title: Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial
description: Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799310"
---
# Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial


O cliente MED-V pode ser distribuído usando um sistema de distribuição de software corporativo, como o Microsoft System Center Configuration Manager.

**Observação**  Se o MED-V estiver instalado usando o Microsoft System Center Configuration Manager, ao criar um pacote para MED-V, defina o modo de execução como direitos administrativos.

 

Antes de implantar o MED-V usando um sistema de distribuição de software corporativo, certifique-se de ter criado uma imagem do MED-V pronto para implantação. Para obter mais informações sobre como criar uma imagem do MED-V, consulte [criando uma imagem do MED-v](creating-a-med-v-image.md).

Depois que a imagem do MED-V estiver preparada, considere o melhor método para distribuir a imagem no seu ambiente. A imagem pode ser distribuída de uma das seguintes maneiras:

-   Carregado na Web e distribuído via download da Web, opcionalmente, utilizando a tecnologia de transferência de corte.

-   Distribuído usando pré-preparação de imagem.

## Implantando a imagem pela Web


Se você estiver implantando a imagem pela Web, carregue a imagem do MED-V em um servidor de distribuição da Web de imagem. Para obter informações sobre como configurar um servidor de distribuição da Web Image, consulte [como configurar o servidor de distribuição da Web de imagem](how-to-configure-the-image-web-distribution-server.md). Para obter informações sobre como carregar uma imagem no servidor, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).

## Implantando a imagem via pré-preparação


Se você estiver implantando a imagem via pré-teste de imagem, configure a pasta de pré-teste e empurre a imagem do MED-V para a pasta. Para obter mais informações sobre como configurar o pré-teste de imagem, consulte [como configurar o pré-teste de imagem](how-to-configure-image-pre-staging.md).

**Observação**  Se você estiver usando pré-preparação de imagem, é importante configurar a pasta de pré-estágio de imagem antes de colocar o pacote. msi do cliente. O caminho da pasta precisa ser incluído no pacote Client. msi.

 

Por fim, empurre o pacote Client. msi usando o centro de distribuição de software corporativo. Em seguida, o MED-V pode ser instalado e a imagem implantada. Para obter mais informações sobre como instalar o MED-V Client, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientesds.md). Para obter mais informações sobre a implantação da imagem, consulte [como implantar uma imagem de espaço de trabalho](how-to-deploy-a-workspace-imageesds.md).

 

 





