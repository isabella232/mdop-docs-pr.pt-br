---
title: Como configurar a segurança do servidor de gerenciamento após a instalação
description: Como configurar a segurança do servidor de gerenciamento após a instalação
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797225"
---
# Como configurar a segurança do servidor de gerenciamento após a instalação


Use o console de gerenciamento do App-V para adicionar o certificado e configurar o servidor de gerenciamento do App-V para segurança aprimorada. Você pode usar o procedimento a seguir para configurar a pós-instalação de segurança.

**Para configurar a instalação de segurança do servidor de gerenciamento após a instalação**

1.  Abra o console de gerenciamento do App-V e conecte-se ao **serviço de gerenciamento** com privilégios de administrador do App-v.

2.  Expanda o servidor, expanda **grupos de servidores**e selecione o grupo de servidores apropriado com o qual o servidor de gerenciamento foi registrado.

3.  Clique com o botão direito do mouse no objeto do servidor de gerenciamento e selecione **Propriedades**.

4.  Na guia **portas** , clique em **certificado de servidor** e conclua o assistente para selecionar o certificado provisionado corretamente.

    **Observação**  Se nenhum certificado for exibido no assistente, um certificado não foi provisionado ou o certificado atende aos requisitos do App-V.

     

5.  Clique em **Avançar** para continuar na página **Bem-vindo ao assistente de certificado** .

6.  Selecione o certificado correto na tela **certificados disponíveis** .

7.  Clique em **concluir**.

8.  Depois de concluir o assistente, limpe **RTSP** como uma porta de escuta disponível. Isso impede que as conexões sejam feitas em um canal de comunicação não seguro.

9.  Clique em **aplicar**e reinicie o serviço **Microsoft Virtual Application Server** . Use o snap-in do MMC do serviço para realizar essa tarefa.

## Tópicos relacionados


[Como configurar a segurança do servidor de streaming após a instalação](how-to-configure-streaming-server-security-post-installation.md)

[Solução de problemas de permissão de certificado](troubleshooting-certificate-permission-issues.md)

 

 





