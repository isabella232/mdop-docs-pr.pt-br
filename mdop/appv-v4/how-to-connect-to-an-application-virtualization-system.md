---
title: Como se Conectar a um Application Virtualization System
description: Como se Conectar a um Application Virtualization System
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797180"
---
# Como se Conectar a um Application Virtualization System


Você deve conectar o console de gerenciamento do servidor do Application Virtualization a um sistema de virtualização de aplicativos antes de poder usar o console de gerenciamento para gerenciar aplicativos, associações de tipo de arquivo, pacotes, licenças de aplicativos, grupos de servidores, políticas e administradores de provedor. O procedimento a seguir descreve as etapas que devem ser seguidas para conectar o console a um sistema de virtualização de aplicativo.

**Para se conectar a um sistema de virtualização de aplicativos**

1. Clique com o botão direito do mouse no nó do sistema do Application Virtualization no painel **escopo** e selecione **conectar ao sistema de virtualização de aplicativos** no menu pop-up.

   **Observação**  
   Há três componentes para o gerenciamento de servidor do Application Virtualization: o console de gerenciamento do Application Virtualization, o serviço de gerenciamento da Web e o SQL Datastore. Se esses componentes forem distribuídos entre máquinas físicas diferentes, você precisará configurar a segurança corretamente para que os componentes se comuniquem pelo sistema. Para obter mais informações, consulte os seguintes artigos e manuais:

   [Como configurar o servidor para ser confiável para delegação](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)

   [Guia de planejamento e implantação para o sistema de virtualização de aplicativos](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)

   [Guia de operações do sistema de virtualização de aplicativos](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)

   [Artigo 930472](https://go.microsoft.com/fwlink/?LinkId=114647) na base de dados de conhecimento Microsoft (https://go.microsoft.com/fwlink/?LinkId=114647)

   [Artigo 930565](https://go.microsoft.com/fwlink/?LinkId=114648) na base de dados de conhecimento Microsoft (https://go.microsoft.com/fwlink/?LinkId=114648)

     

2. Preencha os campos da caixa de diálogo **conectar-se ao sistema do Application Virtualization** :

   1. **Nome do host do serviço Web**— Insira o nome do sistema de virtualização de aplicativos ao qual você deseja se conectar ou digite **localhost** para se conectar ao servidor local.

   2. **Usar conexão segura**-Marque esta caixa de seleção se quiser se conectar ao servidor com uma conexão segura.

   3. **Porta**— Insira o número da porta que você deseja usar para a conexão. o **80** é o número de porta convencional padrão e o **443** é o número da porta segura.

   4. **Usar conta atual do Windows**— Selecione este botão de opção para usar as credenciais atuais da conta do Windows.

   5. **Especificar conta do Windows**— Selecione este botão de opção quando quiser se conectar ao servidor como um usuário diferente.

   6. **Nome**— Insira o nome do novo usuário usando o formato *DOMAIN\\username* ou o <em> username@domain </em> .

   7. **Senha**— Insira a senha que corresponde ao novo usuário.

3. Clique em **OK**.

## Tópicos relacionados


[Como realizar tarefas administrativas no Application Virtualization Server Management Console](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





