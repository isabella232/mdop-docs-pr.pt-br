---
title: Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming
description: Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797043"
---
# Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming


Para dar suporte a uma instalação mais segura do App-V, você pode usar os procedimentos a seguir para modificar as chaves privadas no Windows Server2003 ou no Windows Server2008. Para modificar as permissões da chave privada, você pode usar a ferramenta Windows Server2003 Resource Kit `WinHttpCertCfg.exe` .

Para o Windows Server2003, o procedimento requer que um certificado que atenda aos pré-requisitos listados neste documento seja instalado no computador ou nos computadores nos quais você vai instalar o gerenciamento do App-V ou o Streaming Server. Informações adicionais sobre como usar a `WinHttpCertCfg.exe` ferramenta estão disponíveis em <https://go.microsoft.com/fwlink/?LinkId=151981> .

No Windows Server2008, o processo de alteração das ACLs na chave privada é muito mais simples. A interface do usuário do certificado pode ser usada para gerenciar permissões de chave privada.

**Observação**  O contexto de segurança padrão é serviço de rede; no entanto, uma conta de domínio pode ser usada em vez disso.

 

**Para gerenciar chaves privadas no Windows Server2003**

1.  No computador que se tornará o servidor de gerenciamento ou de streaming do App-V, digite o seguinte comando em um prompt de comando para listar as permissões atuais atribuídas a um certificado específico:

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  Se necessário, modifique as permissões do certificado para fornecer acesso de leitura ao contexto de segurança que será usado para o serviço de gerenciamento ou streaming:

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  Verifique se o contexto de segurança foi adicionado corretamente listando as permissões no certificado:

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**Para gerenciar chaves privadas no Windows Server2008**

1.  Crie um MMC (console de gerenciamento Microsoft) com o snap-in de *certificados* que direciona o repositório de certificados do *computador local* .

2.  Expanda o MMC e selecione **gerenciar chaves privadas**.

3.  Na guia **segurança** , adicione a conta de **serviço de rede** com acesso de **leitura** .

## Tópicos relacionados


[Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[Configuração de certificados para dar suporte ao streaming seguro](configuring-certificates-to-support-secure-streaming.md)

 

 





