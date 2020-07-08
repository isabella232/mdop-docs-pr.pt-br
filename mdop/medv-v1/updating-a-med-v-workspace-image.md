---
title: Atualizando uma imagem de espaço de trabalho do MED-V
description: Atualizando uma imagem de espaço de trabalho do MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799755"
---
# Atualizando uma imagem de espaço de trabalho do MED-V


Uma imagem pode ser atualizada de uma das seguintes maneiras:

-   A atualização pode ser enviada para o sistema operacional convidado usando o sistema de distribuição de software corporativo.

-   A atualização pode ser carregada para o servidor de distribuição de imagens da Web e, em seguida, baixada pelo cliente e aplicada à imagem do MED-V.

-   A imagem base do MED-V pode ser atualizada e reimplantada.

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a>Como atualizar uma imagem do MED-V usando um sistema de distribuição de software corporativo


**Para atualizar uma imagem do MED-V usando um sistema de distribuição de software corporativo**

-   Consulte a documentação do sistema que você está usando.

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a>Como atualizar uma imagem do MED-V usando o download da Web


**Para atualizar uma imagem do MED-V usando o download da Web**

1.  No gerenciamento do MED-V, na guia **máquina virtual** , verifique se as configurações a seguir são aplicadas às políticas do espaço de trabalho do MED-v associadas à imagem do MED-v que está sendo atualizada:

    -   A caixa de seleção **sugerir atualização quando uma nova versão estiver disponível** estará marcada.

    -   Opcionalmente, a caixa de seleção **clientes devem usar a transferência de corte ao baixar imagens para este espaço de trabalho** está marcada.

    Para obter mais informações, consulte [como aplicar as configurações da máquina virtual a um espaço de trabalho do MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).

2.  Carregue a atualização de imagem para o servidor Web de distribuição de imagens.

    Todos os clientes com imagens que precisam ser atualizadas baixam automaticamente a atualização e a aplicam à imagem.

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a>Como atualizar uma imagem base do MED-V


**Para atualizar uma imagem base do MED-V**

1.  Abra a imagem existente no PC2007 virtual.

2.  Faça as alterações necessárias na imagem, atualizando a imagem (como instalar o novo software).

3.  Feche o PC2007 virtual.

4.  Testar a imagem.

5.  Depois que a imagem for testada, compacte-a no repositório local, usando o mesmo nome da imagem existente.

    **Observação**  Se você nomear a imagem como um nome diferente da versão existente, uma nova imagem será criada em vez de uma nova versão da imagem existente.

     

6.  Carregue a nova versão para o servidor, empurre-a para a pasta pre-Stage de imagem ou distribua-a por meio de um pacote de implantação.

## Tópicos relacionados


[Criando uma imagem do MED-V](creating-a-med-v-image.md)

[Como atualizar uma imagem do MED-V](how-to-update-a-med-v-image.md)

[Configurando políticas de espaço de trabalho do MED-V](configuring-med-v-workspace-policies.md)

[Como configurar o servidor de distribuição na Web de imagem](how-to-configure-the-image-web-distribution-server.md)

 

 





