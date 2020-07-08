---
title: Configurar conexões de servidor do AGPM
description: Configurar conexões de servidor do AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797452"
---
# Configurar conexões de servidor do AGPM


Todas as versões de cada objeto de política de grupo controlado (GPO) são armazenadas em um arquivo morto central para que os administradores de política de grupo possam exibir e modificar os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo (AGPM) é necessária para concluir esses procedimentos para configurar centralmente locais de arquivamento para todos os administradores de política de grupo. Examine os detalhes em "considerações adicionais" neste tópico.

## Configurando conexões do servidor do AGPM


Como administrador do AGPM, você pode garantir que todos os administradores de política de grupo se conectem ao mesmo servidor de AGPM, definindo centralmente a configuração associada. Se o ambiente exigir servidores de AGPM separados para alguns ou todos os domínios, configure esses servidores do AGPM adicionais como exceções para o padrão. Se você não configurar as conexões do servidor do AGPM de forma centralizada, cada administrador da política de grupo deve configurar manualmente o servidor do AGPM para ser exibido para cada domínio.

-   [Configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo](#bkmk-defaultarchiveloc)

-   [Configurar conexões do servidor do AGPM adicionais para todos os administradores de política de grupo](#bkmk-additionalarchiveloc)

-   [Configurar manualmente uma conexão com o servidor do AGPM para a sua conta](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Para configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo**

1.  Na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo. (Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)

2.  Na janela **Editor de gerenciamento de política de grupo** , clique em **configuração do usuário**, **políticas**, **modelos administrativos**, **componentes do Windows**e **AGPM**.

3.  No painel detalhes, clique duas vezes em **AGPM: especifique o servidor do AGPM padrão (todos os domínios)**.

4.  Na janela **Propriedades** , marque a caixa de seleção **habilitado** e digite o nome do computador e a porta totalmente qualificados (por exemplo, Server.contoso.com:4600).

5.  Clique em **OK**. A menos que você queira configurar outras conexões do servidor do AGPM, feche a janela do **Editor de gerenciamento de política de grupo** e implante o GPO. (Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).) Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para todos os administradores de política de grupo.

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Para configurar conexões do servidor do AGPM adicionais para todos os administradores de política de grupo**

1.  Se nenhuma conexão do servidor do AGPM tiver sido configurada, siga o procedimento anterior para configurar um servidor do AGPM padrão para todos os domínios.

2.  Para configurar servidores de AGPM separados para alguns ou todos os domínios (substituindo o servidor do AGPM padrão), na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo. (Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)

3.  Na janela **Editor de gerenciamento de política de grupo** , clique em **configuração do usuário**, **políticas**, **modelos administrativos**, **componentes do Windows**e, em seguida, **AGPM**.

4.  No painel de detalhes, clique duas vezes em **AGPM: especificar servidores de AGPM**.

5.  Na janela **Propriedades** , marque a caixa de seleção **habilitado** e clique em **Mostrar**.

6.  Na janela **Mostrar conteúdo** :

    1.  Clique em **Adicionar**.

    2.  Para **nome do valor**, digite o nome do domínio (por exemplo, server1.contoso.com).

    3.  Para **valor**, digite o nome e a porta do servidor de AGPM a ser usado para esse domínio (por exemplo, server2.contoso.com:4600) e clique em **OK**. (Por padrão, o serviço do AGPM escuta na porta 4600. Para usar uma porta diferente, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).)

    4.  Repita para cada domínio que não use o servidor do AGPM padrão.

7.  Clique em **OK** para fechar as janelas **Mostrar conteúdo** e **Propriedades** .

8.  Feche a janela do **Editor de gerenciamento de política de grupo** . (Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).) Quando a política de grupo é atualizada, as novas conexões do servidor do AGPM são configuradas para todos os administradores de política de grupo.

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Se você configurou a conexão do servidor do AGPM de forma centralizada, a opção de configurá-lo manualmente não está disponível para todos os administradores de política de grupo.

**Para configurar manualmente o servidor de AGPM a ser exibido para a sua conta**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  No painel detalhes, clique na guia **servidor do AGPM** .

3.  Digite o nome do computador totalmente qualificado para o servidor do AGPM que gerencia o arquivo morto usado para esse domínio (por exemplo, server.contoso.com) e a porta na qual o serviço do AGPM escuta (por padrão, a porta 4600).

4.  Clique em **aplicar**e, em seguida, clique em **Sim** para confirmar.

### Considerações adicionais

-   Você deve ser capaz de editar e implantar um GPO para executar os procedimentos de configuração centralizada das conexões do servidor do AGPM para todos os administradores de política de grupo. Consulte [editando um GPO](editing-a-gpo-agpm40.md) e [implante um GPO](deploy-a-gpo-agpm40.md) para obter detalhes adicionais.

-   O servidor do AGPM selecionado determina quais GPOs são exibidos na guia **conteúdo** e para qual local as configurações da guia de **delegação de domínio** são aplicadas. Se não for gerenciado centralmente por meio do modelo administrativo, cada administrador da política de grupo deve definir essa configuração para apontar para o servidor do AGPM do domínio.

-   A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

### Referências adicionais

-   [Configuração do Gerenciamento Avançado de Política de Grupo](configuring-advanced-group-policy-management-agpm40.md)

 

 





