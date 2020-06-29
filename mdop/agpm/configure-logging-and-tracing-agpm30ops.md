---
title: Configurar log e rastreamento
description: Configurar log e rastreamento
author: dansimp
ms.assetid: 4f89552f-e949-48b0-9325-23746034eaa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6edcb643dd34a20a845cb3d44a0fe8b353a6291
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797434"
---
# Configurar log e rastreamento


Você pode configurar centralmente o rastreamento e o log opcionais usando modelos administrativos. Isso pode ser útil ao diagnosticar problemas relacionados ao gerenciamento avançado de política de grupo (AGPM).

Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o objeto de política de grupo (GPO) usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no AGPM é necessária para concluir esses procedimentos. Além disso, uma conta de usuário com acesso ao servidor do AGPM é necessária para iniciar o registro em log no servidor do AGPM. Examine os detalhes em "considerações adicionais" neste tópico.

**Para configurar o registro em log e rastreamento do AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo para os quais você deseja ativar o log e o rastreamento. (Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm30ops.md).)

2.  Na janela **Editor de gerenciamento de política de grupo** , clique em **configuração do computador**, **políticas**, **modelos administrativos**, **componentes do Windows**e **AGPM**.

3.  No painel de detalhes, clique duas vezes em **AGPM: configurar o registro em log**.

4.  Na janela **Propriedades** , clique em **habilitado**e configure o nível de detalhes a serem registrados nos logs.

5.  Clique em **OK**.

6.  Feche a janela do **Editor de gerenciamento de política de grupo** . (Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm30ops.md).) Após a atualização da política de grupo, você deve reiniciar o serviço do AGPM para iniciar, modificar ou parar o registro em log no servidor do AGPM. Os administradores de política de grupo devem fechar e reiniciar o GPMC para iniciar, modificar ou interromper o registro em seus computadores.

    **Rastrear locais de arquivos**:

    -   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Considerações adicionais

-   Você deve ser capaz de editar e implantar um GPO para configurar o rastreamento e o log do AGPM. Consulte [editando um GPO](editing-a-gpo-agpm30ops.md) e [implante um GPO](deploy-a-gpo-agpm30ops.md) para obter detalhes adicionais.

### Referências adicionais

-   [Configuração do Gerenciamento Avançado de Política de Grupo](configuring-advanced-group-policy-management.md)

 

 





