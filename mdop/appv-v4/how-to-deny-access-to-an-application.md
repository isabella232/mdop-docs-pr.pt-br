---
title: Como negar acesso a um aplicativo
description: Como negar acesso a um aplicativo
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797141"
---
# Como negar acesso a um aplicativo


Os usuários devem estar na lista de **permissões de acesso** do aplicativo para carregar e usar o aplicativo. Embora o console de gerenciamento do aplicativo virtualização do aplicativo não dê suporte à negação explícita de um acesso a um grupo de usuários a um aplicativo, você pode remover os grupos de usuários das propriedades de um aplicativo para conseguir isso.

**Para negar acesso a um aplicativo**

1.  Para um aplicativo existente, clique no nó **aplicativos** no painel esquerdo.

2.  Clique com o botão direito do mouse em um aplicativo no painel direito e escolha **Propriedades**. Em seguida, selecione a guia **permissões de acesso** .

3.  Para remover o acesso de um grupo de usuários, realce o grupo de usuários e clique em **remover**.

4.  Clique em **OK**.

    **Observação**  Para controlar o acesso aos aplicativos, você também pode limitar as licenças do aplicativo. A configuração dos grupos de usuários adequados nos serviços de domínio Active Directory fornece a maneira mais fácil de conceder e negar acesso a conjuntos de usuários específicos.

     

## Tópicos relacionados


[Como conceder acesso a um aplicativo](how-to-grant-access-to-an-application.md)

[Como gerenciar licenças de aplicativos no Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Como gerenciar aplicativos no Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





