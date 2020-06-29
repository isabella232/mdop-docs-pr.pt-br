---
title: Como configurar servidores de publicação
description: Como configurar servidores de publicação
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796943"
---
# Como configurar servidores de publicação


Você pode usar os procedimentos a seguir para adicionar e configurar servidores de virtualização de aplicativos diretamente do console de gerenciamento de cliente.

**Para adicionar um servidor de publicação de aplicativos**

1.  No painel de **resultados** , clique com o botão direito do mouse e selecione **novo servidor** no menu pop-up-menu para iniciar o novo assistente de servidor de virtualização de aplicativos ou, como alternativa, clique com o botão direito do mouse no nó do **servidor de publicação** e selecione **novo servidor** no menu pop-up-up.

2.  Na página um do assistente, insira o nome do servidor no campo nome para **exibição** e selecione o tipo de servidor na lista suspensa **tipo** . Você pode escolher o servidor de **virtualização de aplicativos**, o **servidor de virtualização de aplicativo de segurança avançada**, o **servidor HTTP padrão**ou o **servidor http de segurança avançada** na lista suspensa de tipos de servidor.

3.  Clique em **Avançar**.

4.  Na página 2 do assistente, digite as informações apropriadas nos campos **nome do host** e **porta** . O campo **caminho** não é editável para servidores do Application Virtualization. Você deve digitar um caminho para o servidor HTTP padrão ou o servidor HTTP de segurança avançada.

5.  Clique em **concluir** para adicionar o servidor.

**Para configurar um servidor de publicação de aplicativos**

1.  No painel de **resultados** , clique com o botão direito do mouse no servidor desejado e selecione **Propriedades** no menu pop-up.

2.  Clique na guia **geral** , na qual você pode alterar o nome do servidor, selecione um tipo na lista suspensa de tipos de servidor e especifique o nome e a porta do host. Quando o tipo de servidor é um servidor HTTP padrão ou um servidor HTTP de segurança avançada, o campo **caminho** também é editável.

3.  Clique na guia **Atualizar** , na qual a caixa de seleção **Atualizar publicação no logon do usuário** está marcada por padrão. Para alterar a taxa de atualização, marque a caixa de seleção **atualizar a publicação a cada** e insira um número que represente a frequência no campo. Em seguida, selecione **minutos**, **horas**, **dias** no menu suspenso. (A quantidade mínima de tempo que você pode inserir é de 30 minutos.)

4.  Clique em **aplicar** para alterar a configuração.

5.  Quando terminar de publicar, clique em **OK** para sair da caixa de diálogo e retornar ao console de gerenciamento de cliente.

## Tópicos relacionados


[Como desabilitar ou Modificar as configurações de Modo de Operação Desconectada](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





