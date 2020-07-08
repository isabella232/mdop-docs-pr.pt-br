---
title: Como configurar o Firewall do Windows Server 2003 para App-V
description: Como configurar o Firewall do Windows Server 2003 para App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797183"
---
# Como configurar o Firewall do Windows Server 2003 para App-V


Use o procedimento a seguir para configurar o Firewall do WindowsServer 2003 para o App-V.

**Para configurar o WindowsServer 2003 firewall para o App-V**

1.  No **painel de controle**, abra o **Firewall do Windows**.

    **Observação**  Se o servidor não tiver sido configurado para executar o serviço de firewall antes desta etapa, você será solicitado a iniciar o serviço de firewall.

     

2.  Se os arquivos ICO e OSD forem publicados por SMB, verifique se o **compartilhamento de arquivos e impressoras** está habilitado na guia **exceções** .

    **Observação**  Se os arquivos ICO e OSD forem publicados por HTTP/HTTPS no servidor de gerenciamento, talvez seja necessário adicionar uma exceção para HTTP ou HTTPS. Se o servidor IIS que hospeda os arquivos ICO e OSD estiver hospedado em um computador separado do servidor de gerenciamento, você precisará adicionar a exceção a esse computador. Para maximizar o desempenho, é recomendável que você hospede os arquivos ICO e OSD em um servidor separado do servidor de gerenciamento.

     

3.  Adicione uma exceção do programa para `sghwdsptr.exe` , que é o executável do serviço de servidor de gerenciamento. O caminho padrão para esse executável é `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

    **Observação**  Se o servidor de gerenciamento usar RTSP para comunicação, você também deverá adicionar uma exceção do programa `sghwsvr.exe` .

    O servidor de streaming App-V requer uma exceção `sglwdsptr.exe` do programa para comunicação entre RTSPS. O servidor de streaming App-V que usa RTSP para comunicação também exige uma exceção do programa para `sglwsvr.exe` .

     

4.  Verifique se o escopo correto está configurado para cada exceção. Para reduzir o risco, remova qualquer computador e limite estritamente os endereços IP aos quais o servidor irá responder.

## Tópicos relacionados


[Como configurar o Firewall do Windows Server 2008 para App-V](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





