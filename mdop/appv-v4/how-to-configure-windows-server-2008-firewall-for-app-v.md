---
title: Como configurar o Firewall do Windows Server 2008 para App-V
description: Como configurar o Firewall do Windows Server 2008 para App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797181"
---
# Como configurar o Firewall do Windows Server 2008 para App-V


Com a introdução do Windows Server2008, os componentes de firewall e IPsec foram mesclados em um serviço, e os recursos desse serviço foram aprimorados. O novo serviço de firewall dá suporte à inspeção de entrada e de saída de estado. Além disso, você pode configurar regras de firewall específicas e diretivas IPsec por meio de políticas de grupo. Para obter informações adicionais sobre o Firewall do Windows no Windows Server2008, consulte <https://go.microsoft.com/fwlink/?LinkId=151980> .

O procedimento a seguir não inclui a adição de uma exceção para a publicação por ICO e OSD por SMB ou HTTP/HTTPS. Essas exceções são adicionadas automaticamente com base no perfil de rede e nas funções instaladas no firewall do Windows Server 2008.

**Observação**  Se o servidor de gerenciamento estiver configurado para usar RTSP, repita este procedimento para adicionar o `sghwsvr.exe` programa como uma exceção.

O servidor de streaming do App-V requer a exceção do programa `sglwdsptr.exe` para comunicação entre RTSPS. Um servidor de streaming do App-V que usa RTSP para comunicação também exige uma exceção do programa para `sglwsvr.exe` .

 

**Para configurar o Windows Server2008 firewall para App-V**

1.  Abra o console **Firewall do Windows com gerenciamento de segurança avançada** por meio do painel de controle ou digite `wf.msc` na linha executar.

2.  Crie uma nova regra de entrada e selecione **programa**.

3.  Selecione o caminho do programa e navegue até `sghwdsptr.exe` , que está localizado por padrão em `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

4.  Clique em **Avançar**.

5.  Na página **ação** , selecione **permitir a conexão**e, em seguida, clique em **Avançar**.

6.  Selecione os **perfis** apropriados para aplicar à regra de entrada.

7.  Forneça um nome e uma descrição para a regra e clique em **concluir**.

## Tópicos relacionados


[Como configurar o Firewall do Windows Server 2003 para App-V](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





