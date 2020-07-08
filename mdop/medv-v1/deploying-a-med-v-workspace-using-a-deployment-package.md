---
title: Implantando um espaço de trabalho do MED-V usando um pacote de implantação
description: Implantando um espaço de trabalho do MED-V usando um pacote de implantação
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799311"
---
# Implantando um espaço de trabalho do MED-V usando um pacote de implantação


A instalação do pacote de implantação fornece um método de instalação do MED-V cliente juntamente com todos os pré-requisitos obrigatórios, bem como as configurações predefinidas pelo administrador.

Ao usar um pacote de implantação, o pacote é distribuído por meio de uma rede compartilhada ou mídia removível. A imagem pode ser incluída no pacote ou pode ser distribuída separadamente.

Antes de criar um pacote de implantação, certifique-se de que você criou uma imagem do MED-V Ready para implantação. Para obter mais informações sobre como criar uma imagem do MED-V, consulte [criando uma imagem do MED-v](creating-a-med-v-image.md).

Depois que a imagem do MED-V estiver preparada, considere o melhor método para distribuir a imagem no seu ambiente. A imagem pode ser distribuída de uma das seguintes maneiras:

-   Carregado na Web e distribuído via download da Web, opcionalmente, usando a tecnologia de transferência de corte.

-   Distribuído usando pré-preparação de imagem.

-   Incluído no pacote de implantação e distribuído em conjunto com todos os outros componentes do MED-V.

Se a imagem for incluída no pacote, nenhuma outra configuração será necessária para a imagem. Se a imagem não for incluída no pacote de implantação, siga um destes procedimentos:

-   Se você estiver implantando a imagem pela Web, carregue a imagem do MED-V para o servidor de distribuição da Web de imagem. Para obter informações sobre como configurar um servidor de distribuição da Web Image, consulte [como configurar o servidor de distribuição da Web de imagem](how-to-configure-the-image-web-distribution-server.md). Para obter informações sobre como carregar uma imagem no servidor, consulte [como carregar uma imagem do MED-V para o servidor](how-to-upload-a-med-v-image-to-the-server.md).

-   Se você estiver implantando a imagem via pré-teste de imagem, configure a pasta de pré-teste e empurre a imagem do MED-V para a pasta. Para obter mais informações sobre como configurar o pré-teste da imagem, consulte [como configurar o pré-teste da imagem](how-to-configure-image-pre-staging.md).

**Observação**  Se você estiver usando pré-preparação de imagem, é importante configurar a pasta de pré-estágio de imagem antes de criar o pacote de implantação. O caminho da pasta precisa ser incluído no pacote de implantação.

 

Por fim, crie o pacote de implantação. Para obter mais informações sobre como criar um pacote de implantação, consulte [como configurar um pacote de implantação](how-to-configure-a-deployment-package.md). Após a conclusão do pacote, distribua-o para implantação.

Depois que o pacote de implantação for distribuído, o cliente MED-V pode ser instalado e a imagem implantada. Para obter mais informações sobre como instalar o MED-V Client, consulte [como instalar o cliente do MED-v](how-to-install-med-v-clientdeployment-package.md). Para obter mais informações sobre a implantação da imagem, consulte [como implantar uma imagem de espaço de trabalho](how-to-deploy-a-workspace-imagedeployment-package.md).

 

 





