---
title: Como configurar atualização periódica de publicação
description: Como configurar atualização periódica de publicação
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796948"
---
# Como configurar atualização periódica de publicação


Você pode usar o procedimento a seguir para configurar o cliente para atualizar periodicamente as informações de publicação dos servidores App-V. Após a configuração do cliente, a operação de atualização é automática. Essas configurações definem as configurações padrão do cliente para que todos os usuários deste computador vejam as mesmas configurações.

**Observação**  Depois que você executar esse procedimento, as informações de publicação serão atualizadas de acordo com as novas configurações após a primeira atualização ao fazer logon. Quando essa primeira atualização ocorre, o servidor pode substituir as configurações do computador por configurações diferentes, dependendo de como ela está configurada. A guia **Atualizar** na caixa de diálogo **Propriedades** mostra as configurações do computador cliente configurado localmente e as configurações que podem ter sido configuradas para o usuário pelo servidor de publicação.

 

**Para atualizar periodicamente as informações de publicação dos servidores de virtualização de aplicativos**

1.  Clique em **servidores de publicação** no painel **escopo** .

2.  No painel de **resultados** , clique com o botão direito do mouse no servidor desejado e selecione **Propriedades** no menu pop-up-.

3.  Na caixa de diálogo **Propriedades** , na guia **Atualizar** , marque a caixa de seleção **Atualizar configuração a cada** e insira um número que represente a frequência no campo. Em seguida, selecione **minutos**, **horas**, **dias** no menu suspenso.

    **Observação**  Essa configuração fará com que o cliente atualize as informações de publicação toda vez que o período configurado for ultrapassado. Se o usuário não estiver conectado quando for hora de fazer uma atualização, a atualização ocorrerá quando o usuário fizer logon. Em seguida, o temporizador é iniciado novamente para o próximo período.

     

4.  Clique em **aplicar** para alterar a configuração.

5.  Quando terminar de configurar o servidor, clique em **OK** para sair da caixa de diálogo e retornar ao console de gerenciamento de cliente do Application Virtualization.

## Tópicos relacionados


[Como configurar o Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





