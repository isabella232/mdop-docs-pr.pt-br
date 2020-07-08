---
title: Modificar o caminho do arquivo morto
description: Modificar o caminho do arquivo morto
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797736"
---
# Modificar o caminho do arquivo morto


O caminho do arquivo morto é o local do arquivo morto relativo ao servidor do AGPM. O caminho de arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro servidor na mesma floresta.

O caminho de arquivo morto e a conta do serviço do AGPM são configurados durante a instalação do servidor do AGPM e podem ser alterados posteriormente por meio de **Adicionar ou remover programas** no servidor do AGPM.

Uma conta de usuário que é membro do grupo Domain admins e tem acesso ao servidor do AGPM (o computador em que a Microsoft Advanced Group Policy Management-Server está instalado) é necessária para concluir este procedimento.

**Para modificar o caminho do arquivo morto**

1.  No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor está instalado, clique em **Iniciar**, **painel de controle**, clique em **Adicionar ou remover programas**.

2.  Clique em **gerenciamento avançado de política de grupo da Microsoft-servidor**e, em seguida, clique em **alterar**.

3.  Clique em **Avançar**e, em seguida, clique em **Modificar**.

4.  Siga as instruções na tela para definir as configurações do serviço do AGPM:

    1.  Para o caminho do arquivo morto, insira um novo local para o arquivo morto relativo ao servidor do AGPM. O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas o local deve ter espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.

    2.  Insira as credenciais para a conta de serviço do AGPM.

        **Importante**  Modificar a instalação limpa as credenciais da conta de serviço do AGPM. Você deve inserir as credenciais novamente, mas elas não precisam corresponder às credenciais usadas durante a instalação original.

        A conta de serviço do AGPM deve ter acesso total aos GPOs que ele gerenciará. Se você estiver gerenciando GPOs em um único domínio, poderá tornar a conta do sistema local para o controlador de domínio primário a conta do serviço do AGPM.

        Se você estiver gerenciando GPOs em vários domínios ou se um servidor membro for o servidor do AGPM, você deve configurar uma conta diferente como a conta de serviço do AGPM porque a conta do sistema local para um controlador de domínio não pode acessar GPOs em outros domínios.

         

    3.  Para o proprietário do arquivo morto, insira as credenciais de um administrador do AGPM (controle total).

5.  Clique em **alterar**e, quando a instalação estiver concluída, clique em **concluir**.

### Referências adicionais

-   [Gerenciamento do serviço AGPM](managing-the-agpm-service.md)

 

 





