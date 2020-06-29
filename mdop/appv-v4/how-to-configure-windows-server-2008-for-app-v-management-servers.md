---
title: Como configurar o Windows Server 2008 paro App-V Management Servers
description: Como configurar o Windows Server 2008 paro App-V Management Servers
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797182"
---
# Como configurar o Windows Server 2008 paro App-V Management Servers


O servidor do Windows Server 2008 no qual você instala o serviço Web de gerenciamento do Microsoft Application Virtualization (App-V) requer que os serviços de informações da Internet (IIS) sejam instalados como uma função no servidor. Use o procedimento a seguir para configurar o Windows Server 2008 para dar suporte à instalação do App-vserver.

**Para instalar o IIS em um computador com Windows Server2008**

1.  No computador Windows Server2008, clique em **Iniciar**, clique em **todos os programas**, clique em **Ferramentas administrativas**e clique em **Gerenciador de servidores** para iniciar o Gerenciador de servidores. No Gerenciador de servidores, clique com o botão direito do mouse no nó **funções** e clique em **adicionar funções** para iniciar o **Assistente para adicionar funções**.

2.  No **Assistente para adicionar funções**, na página **selecionar funções do servidor** , selecione **servidor Web (IIS)**. Quando solicitado, clique em **Adicionar recursos necessários** para adicionar os recursos dependentes.

3.  Na página **selecionar funções de servidor** , clique em **Avançar**e, em seguida, clique em **Avançar** novamente.

4.  No **Assistente para adicionar funções**, na página **selecionar serviços de função** :

    1.  Em **desenvolvimento de aplicativos**, selecione **ASP.net** e, quando solicitado, clique em **Adicionar serviços de função necessários** para adicionar os serviços e recursos de funções dependentes.

    2.  Em **segurança**, selecione **autenticação do Windows**.

    3.  No nó **ferramentas de gerenciamento** , selecione **scripts e ferramentas de gerenciamento do IIS**. Em **compatibilidade com gerenciamento do IIS6**, verifique se a **compatibilidade da metabase do Iis6** e a compatibilidade do WMI do **IIS6** estão selecionadas e clique em **Avançar**.

5.  Na página **confirmar seleções de instalação** , clique em **instalar**e, em seguida, conclua o restante do assistente.

6.  Clique em **fechar** para sair do **Assistente para adicionar funções**e feche o Gerenciador de servidores.

## Tópicos relacionados


[Requisitos para implantação do Application Virtualization](application-virtualization-deployment-requirements.md)

[Listas de verificação de atualização e implantação do Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





