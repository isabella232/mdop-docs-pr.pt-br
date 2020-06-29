---
title: Modificar o serviço AGPM
description: Modificar o serviço AGPM
author: dansimp
ms.assetid: 3239d088-bb86-4ec4-bc56-dbe8f1c710f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: be39b170ef4cdc14c0f447bb6bd09a4ea92c82fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797737"
---
# Modificar o serviço AGPM


O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção do domínio. Se esse serviço for interrompido ou desabilitado, os clientes do AGPM não poderão realizar operações por meio do servidor. Você pode modificar o caminho de arquivo morto, a conta de serviço do AGPM e a porta que o serviço do AGPM escuta.

**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional. Isso pode impedir que o serviço do AGPM seja iniciado.

 

Uma conta de usuário que é membro do grupo Domain admins e tem acesso ao servidor do AGPM (o computador em que a Microsoft Advanced Group Policy Management-Server está instalado) é necessária para concluir este procedimento. Além disso, você deve fornecer credenciais para a conta de serviço do AGPM para concluir este procedimento.

**Para modificar o serviço do AGPM**

1.  No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor está instalado, clique em **Iniciar**, **painel de controle**, **programas**e **programas e recursos**.

2.  Clique com o botão direito do mouse em **gerenciamento avançado de política de grupo da Microsoft-servidor**e clique em **alterar**.

3.  Clique em **Avançar**e, em seguida, clique em **Modificar**.

4.  Siga as instruções para configurar o serviço do AGPM:

    1.  Na caixa de diálogo **caminho do arquivo morto** , insira um novo local para o arquivo morto relativo ao servidor do AGPM ou confirme o caminho do arquivo morto atual e clique em **Avançar**.

        **Importante**  O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas o local deve ter espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.

         

    2.  Na caixa de diálogo **conta de serviço do AGPM** , insira as credenciais de uma conta de serviço sob a qual o serviço do AGPM será executado e clique em **Avançar**.

        **Importante**  Modificar a instalação limpa as credenciais da conta de serviço do AGPM. Você deve inserir as credenciais novamente, mas elas não precisam corresponder às credenciais usadas durante a instalação original.

        A conta de serviço do AGPM deve ter acesso total aos GPOs que ele gerenciará e receberá a concessão de **logon como permissão de serviço** . Se você estiver gerenciando GPOs em um único domínio, poderá tornar a conta do sistema local para o controlador de domínio primário a conta do serviço do AGPM.

        Se você estiver gerenciando GPOs em vários domínios ou se um servidor membro for o servidor do AGPM, você deve configurar uma conta diferente como a conta de serviço do AGPM porque a conta do sistema local para um controlador de domínio não pode acessar GPOs em outros domínios.

         

    3.  Na caixa de diálogo **proprietário do arquivo morto** , insira o nome de usuário de um administrador do AGPM (controle total) ou grupo de administradores do AGPM e clique em **Avançar**.

        **Observação**  Modificar a instalação limpa as credenciais do proprietário do arquivo. Você deve inserir as credenciais novamente, mas elas não precisam corresponder às credenciais usadas durante a instalação original.

         

    4.  Na caixa de diálogo **configuração de porta** , digite uma nova porta na qual o serviço do AGPM deve ouvir ou confirmar a porta selecionada no momento e clique em **Avançar**.

        **Observação**  Por padrão, o serviço do AGPM escuta na porta 4600.

        Se você configurar exceções de porta manualmente ou tiver regras Configurando exceções de porta, você pode desmarcar a caixa de seleção **Adicionar exceção de porta ao firewall** .

         

5.  Clique em **alterar**e, quando a instalação estiver concluída, clique em **concluir**.

6.  Se você tiver alterado a porta na qual o serviço do AGPM escuta, modifique a porta na conexão do servidor do AGPM para cada administrador de política de grupo. (Para obter mais informações, consulte [Configurar conexões do servidor de AGPM](configure-agpm-server-connections-agpm40.md).)

7.  Repita para cada servidor do AGPM ao qual as alterações de configuração devem ser aplicadas.

### Referências adicionais

-   [Gerenciamento do serviço AGPM](managing-the-agpm-service-agpm40.md)

 

 





