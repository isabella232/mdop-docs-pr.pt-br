---
title: Configurar notificações por email
description: Configurar notificações por email
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797438"
---
# Configurar notificações por email


Quando um editor ou um revisor tenta criar, implantar ou excluir um objeto de política de grupo (GPO), uma solicitação para esta ação é enviada a um endereço de email ou a endereços designados para que um Aprovador possa avaliar a solicitação e implementá-la ou Deny-la. Você determina o endereço de email ou endereços para os quais as notificações são enviadas, bem como o alias do qual as notificações são enviadas.

Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento. Examine os detalhes em "considerações adicionais" neste tópico.

**Para configurar a notificação por email para o AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  No painel de detalhes, clique na guia de **delegação de domínio** .

3.  No campo **do endereço de email** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.

4.  No campo **endereço de email para** , digite uma lista delimitada por vírgulas de endereços de email de aprovadores que devem receber solicitações de aprovação.

5.  No campo **servidor SMTP** , digite um servidor de email SMTP válido.

6.  Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário com acesso ao serviço SMTP.

7.  Clique em **Aplicar**.

### Considerações adicionais

-   Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento. Especificamente, você deve ter permissões de **lista de conteúdo** e **Opções de modificação** para o domínio.

-   A notificação por email para o AGPM é uma configuração no nível do domínio. Você pode fornecer diferentes endereços de email do aprovador ou aliases de email do AGPM na guia de **delegação de domínio** de cada domínio ou usar os mesmos endereços de email em todo o ambiente.

-   Por padrão, as mensagens de email enviadas como resultado de ações no gerenciamento avançado de política de grupo (AGPM) não são criptografadas. No entanto, você pode configurar a segurança de email para o AGPM usando configurações do registro para especificar se deseja usar a criptografia SSL (Secure Sockets Layer) e qual porta SMTP usar. Para obter mais informações, consulte [Configurar a segurança de email para o AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)

### Referências adicionais

-   [Configuração do Gerenciamento Avançado de Política de Grupo](configuring-advanced-group-policy-management.md)

 

 





