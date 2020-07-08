---
title: Configurar log e rastreamento
description: Configurar log e rastreamento
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797432"
---
# Configurar log e rastreamento


Você pode configurar centralmente o log e o rastreamento opcionais para gerenciamento avançado de política de grupo (AGPM) usando modelos administrativos.

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir esses procedimentos. Além disso, uma conta de usuário com acesso ao servidor do AGPM é necessária para iniciar o registro em log no servidor do AGPM. Examine os detalhes em "considerações adicionais" neste tópico.

**Para configurar o registro em log e rastreamento do AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo para os quais você deseja ativar o log e o rastreamento. (Para obter mais informações, consulte [editando um GPO](editing-a-gpo.md).)

2.  No **Editor de objeto de política de grupo**, clique em configuração do **computador**, **modelos administrativos**e **componentes do Windows**.

3.  Se o **AGPM** não estiver listado em **componentes do Windows**:

    1.  Clique com o botão direito do mouse em **modelos administrativos** e clique em **Adicionar/remover modelos**.

    2.  Clique **em Adicionar**, selecione **AGPM. admx** ou **AGPM. adm**, clique em **abrir**e, em seguida, clique em **fechar**.

4.  Em **componentes do Windows**, clique duas vezes em **AGPM**.

5.  No painel de detalhes, clique duas vezes em **log do AGPM**.

6.  Na janela **Propriedades de log do AGPM** , clique em **habilitado**e configure o nível de detalhes a serem registrados nos logs.

7.  Clique em **OK**.

8.  Feche o **Editor de objeto de política de grupo**. (Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo.md).) Após a atualização da política de grupo, você deve reiniciar o serviço do AGPM para começar a fazer logon no servidor do AGPM. Os administradores de política de grupo devem fechar e reiniciar o GPMC para começar a fazer logon em seus computadores.

    **Rastrear locais de arquivos**:

    -   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Considerações adicionais

-   Você deve ser capaz de editar e implantar um GPO para configurar o rastreamento e o log do AGPM. Consulte [editando um GPO](editing-a-gpo.md) e [implante um GPO](deploy-a-gpo.md) para obter detalhes adicionais.

### Referências adicionais

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks.md)

 

 





