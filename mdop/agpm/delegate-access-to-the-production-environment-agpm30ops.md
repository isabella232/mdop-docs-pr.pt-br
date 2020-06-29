---
title: Delegar acesso ao ambiente de produção
description: Delegar acesso ao ambiente de produção
author: dansimp
ms.assetid: c1ebae2e-909b-4e64-b368-b7d3cc67b1eb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4667a23f1584d7aab6143860721e326da6407afb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797840"
---
# Delegar acesso ao ambiente de produção


Você pode alterar o acesso aos objetos de política de grupo (GPOs) no ambiente de produção, substituindo as permissões existentes nesses GPOs. Você pode configurar permissões no nível do domínio para permitir ou impedir que os usuários editem, excluam ou modifiquem a segurança de GPOs no ambiente de produção quando não estiverem usando a pasta de **controle de alterações** no GPMC (console de gerenciamento de política de grupo).

**Observação**  
-   Delegar o acesso ao ambiente de produção não afeta a capacidade dos usuários de vincular GPOs.

-   Quando os GPOs são controlados ou implantados, o acesso a todas as outras contas, exceto aquelas com permissões de **leitura** e **aplicação** , é removido.

 

Uma conta de usuário que tenha as permissões necessárias no AGPM (gerenciamento avançado de política de grupo) ou a função do administrador do AGPM (controle total) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para alterar o acesso a GPOs no ambiente de produção**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Clique na guia **delegação de produção** .

3.  Para adicionar permissões para um usuário ou grupo que não tenha acesso ao ambiente de produção ou para substituir as permissões de um usuário ou grupo que tem acesso:

    1.  Clique em **Adicionar**, selecione um usuário ou grupo e, em seguida, clique em **OK**.

    2.  Selecione permissões para delegar a esse usuário ou grupo para o ambiente de produção e clique em **OK**.

4.  Para remover todas as permissões para o ambiente de produção de um usuário ou grupo, selecione o usuário ou grupo, clique em **remover**e, em seguida, clique em **OK**.

### Considerações adicionais

-   Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissão de **modificação de segurança** para o domínio.

-   As permissões para a conta de serviço do AGPM não podem ser alteradas na guia de **delegação de produção** .

-   Por padrão, as contas a seguir têm permissões para GPOs no ambiente de produção:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Account</th>
    <th align="left">Permissões padrão para GPOs</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>&lt;Conta de serviço do AGPM&gt;</p></td>
    <td align="left"><p>Editar configurações, excluir, modificar segurança</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Usuários autenticados</p></td>
    <td align="left"><p>Ler, aplicar</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administradores de domínio</p></td>
    <td align="left"><p>Editar configurações, excluir, modificar segurança</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administradores de empresas</p></td>
    <td align="left"><p>Editar configurações, excluir, modificar segurança</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Controladores de domínio da empresa</p></td>
    <td align="left"><p>Leitura</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sistema</p></td>
    <td align="left"><p>Editar configurações, excluir, modificar segurança</p></td>
    </tr>
    </tbody>
    </table>

     

-   A associação no grupo proprietários criadores de política de grupo deve ser restrita, o soit não é usado para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

### Referências adicionais

-   [Configuração do Gerenciamento Avançado de Política de Grupo](configuring-advanced-group-policy-management.md)

 

 





