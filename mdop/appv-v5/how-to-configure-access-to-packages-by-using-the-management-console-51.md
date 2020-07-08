---
title: Como configurar o acesso a pacotes usando o Console de Gerenciamento
description: Como configurar o acesso a pacotes usando o Console de Gerenciamento
author: dansimp
ms.assetid: 4fd39bc2-d814-46de-a108-1c21fa404e8a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c6c8f930fb1fbd82432f6d43dae8b9bed7a563c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796494"
---
# Como configurar o acesso a pacotes usando o Console de Gerenciamento


Antes de implantar um pacote virtualizado do App-V 5,1, você deve configurar os grupos de segurança dos serviços de domínio Active Directory (AD DS) que terão permissão para acessar e executar os aplicativos. Os grupos de segurança podem conter computadores ou usuários. Entitling um pacote a um grupo de computador publica o pacote globalmente em todos os computadores do grupo.

Use o procedimento a seguir para configurar o acesso a pacotes virtualizados.

**Para conceder acesso a um pacote do App-V 5,1**

1.  Localize o pacote que você deseja configurar:

    1.  Abra o console de gerenciamento do App-V 5,1.

    2.  Para exibir a página de **acesso do AD** , clique com o botão direito do mouse no pacote a ser configurado e selecione **Editar acesso ao Active Directory**. Ou, se preferir, selecione o pacote e clique em **Editar** no painel **acesso ao anúncio** .

2.  Provisionar um grupo de segurança para o pacote:

    1.  Vá para a página **localizar nomes válidos do Active Directory e conceder acesso** .

    2.  Usando o formato **mydomain**  \\  **GroupName**, digite o nome ou parte do nome de um objeto de grupo do Active Directory e clique em **verificar**.

        **Observação**  Certifique-se de fornecer um nome de domínio associado para o grupo que você está procurando.

         

3.  Para conceder acesso ao pacote, selecione o grupo desejado e clique em **conceder acesso**. O grupo recém-adicionado é exibido no painel **entidades do anúncio com acesso** .

4.  

    Para aceitar as configurações padrão e fechar a página de **acesso do AD** , clique em **fechar**.

    Para personalizar as configurações de um grupo específico, clique no menu suspenso **configurações atribuídas** e selecione **personalizado**. Para definir as configurações personalizadas, clique em **Editar**. Após conceder o acesso, clique em **fechar**.

**Para remover o acesso a um pacote do App-V 5,1**

1.  Localize o pacote que você deseja configurar:

    1.  Abra o console de gerenciamento do App-V 5,1.

    2.  Para exibir a página de **acesso do AD** , clique com o botão direito do mouse no pacote a ser configurado e selecione **Editar acesso ao Active Directory**. Ou, se preferir, selecione o pacote e clique em **Editar** no painel **acesso ao anúncio** .

2.  Selecione o grupo que você deseja remover e clique em **excluir**.

3.  Para fechar a página de **acesso do AD** , clique em **fechar**.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





