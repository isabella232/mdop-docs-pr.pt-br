---
title: Como criar um grupo de conexão
description: Como criar um grupo de conexão
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796475"
---
# Como criar um grupo de conexão


Use estas etapas para criar um grupo de conexão usando o console de gerenciamento do App-V. Para usar o PowerShell para criar grupos de conexão, consulte [como gerenciar grupos de conexão em um computador autônomo usando o PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).

Quando você coloca pacotes em um grupo de conexão, os caminhos raiz do pacote são mesclados. Se você remover pacotes, somente os pacotes restantes mantêm a raiz mesclada.

**Para criar um grupo de conexões**

1.  No console de gerenciamento do App-V 5,0, selecione **pacotes**.

2.  Selecione **grupos de conexão** para exibir a biblioteca de grupos de conexão.

3.  Selecione **Adicionar grupo de conexão** para criar um novo grupo de conexão.

4.  No painel **novo grupo de conexão** , digite uma descrição para o grupo.

5.  Clique em **Editar** no painel **pacotes conectados** para adicionar um novo aplicativo ao grupo de conexão.

6.  No painel **pacotes e biblioteca inteira** , selecione o aplicativo a ser adicionado e clique na seta para adicionar o aplicativo.

    Para remover um aplicativo, selecione o aplicativo a ser removido no painel **pacotes** e clique na seta.

    Para repriorizar os aplicativos no seu grupo de conexão, use as setas no painel **pacotes no** painel.

    **Importante**  Por padrão, as configurações de acesso dos serviços de domínio Active Directory associadas a um aplicativo específico não são adicionadas ao grupo de conexão. Para transferir a configuração do acesso ao Active Directory, selecione **Adicionar acesso ao pacote ao acesso a grupo**, localizado no painel **pacotes no** painel.

     

7.  Após adicionar todos os aplicativos e configurar o acesso ao Active Directory, clique em **aplicar**.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

[Gerenciando grupos de conexão](managing-connection-groups.md)

 

 





