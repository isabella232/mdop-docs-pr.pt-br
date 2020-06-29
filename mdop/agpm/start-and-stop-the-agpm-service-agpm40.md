---
title: Iniciar e parar o serviço AGPM
description: Iniciar e parar o serviço AGPM
author: dansimp
ms.assetid: dcc9566c-c515-4fbe-b7f5-8ac030141307
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c254cc122c43262ff5ec4cb0bf5a5ab2c77fac3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797679"
---
# Iniciar e parar o serviço AGPM


O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção.

**Importante**  Parar ou desabilitar o serviço do AGPM impedirá que os clientes do AGPM realizem operações (como listagem ou edição de GPOs) pelo servidor.

 

Uma conta de usuário com acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) é necessária para concluir este procedimento.

**Para iniciar ou parar o serviço do AGPM**

1.  No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor (e, portanto, o serviço do AGPM) estiver instalado, clique em **Iniciar**, clique em **painel de controle**, clique em **Ferramentas administrativas**e clique em **Serviços**.

2.  Na lista de serviços, clique com o botão direito do mouse em **serviço do AGPM** e selecione **Iniciar**, **reiniciar**ou **parar**.

    **Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional. Isso pode impedir que o serviço do AGPM seja iniciado.

     

### Referências adicionais

-   [Gerenciamento do serviço AGPM](managing-the-agpm-service-agpm40.md)

 

 





