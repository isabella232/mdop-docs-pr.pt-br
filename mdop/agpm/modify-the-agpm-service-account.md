---
title: Modificar a conta de serviço do AGPM
description: Modificar a conta de serviço do AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797742"
---
# Modificar a conta de serviço do AGPM


O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção. Se esse serviço for interrompido ou desabilitado, os clientes do AGPM não poderão realizar operações por meio do servidor.

O caminho de arquivo morto e a conta do serviço do AGPM são configurados durante a instalação do servidor do AGPM e podem ser alterados posteriormente por meio de **Adicionar ou remover programas** no servidor do AGPM.

**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional. Isso pode impedir que o serviço do AGPM seja iniciado.

 

Uma conta de usuário que é membro do grupo Domain admins e tem acesso ao servidor do AGPM (o computador em que a Microsoft Advanced Group Policy Management-Server está instalado) é necessária para concluir este procedimento.

**Importante**  A conta de serviço do AGPM deve ter acesso total aos GPOs que ele gerenciará e receberá a concessão de **logon como permissão de serviço** . Se você estiver gerenciando GPOs em um único domínio, poderá tornar a conta do sistema local para o controlador de domínio primário a conta do serviço do AGPM.

Se você estiver gerenciando GPOs em vários domínios ou se um servidor membro for o servidor do AGPM, você deve configurar uma conta diferente como a conta de serviço do AGPM porque a conta do sistema local para um controlador de domínio não pode acessar GPOs em outros domínios.

 

**Para modificar a conta de serviço do AGPM**

1.  No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor está instalado, clique em **Iniciar**, **painel de controle**, clique em **Adicionar ou remover programas**.

2.  Clique em **gerenciamento avançado de política de grupo da Microsoft-servidor**e, em seguida, clique em **alterar**.

3.  Clique em **Avançar**e, em seguida, clique em **Modificar**.

4.  Siga as instruções na tela para definir as configurações do serviço do AGPM:

    1.  Para o caminho do arquivo morto, confirme ou altere a localização do arquivo relativo ao servidor do AGPM. O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas o local deve ter espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.

    2.  Insira novas credenciais para a conta de serviço do AGPM.

    3.  Para o proprietário do arquivo morto, insira as credenciais de um administrador do AGPM (controle total).

5.  Clique em **alterar**e, quando a instalação estiver concluída, clique em **concluir**.

### Referências adicionais

-   [Gerenciamento do serviço AGPM](managing-the-agpm-service.md)

 

 





