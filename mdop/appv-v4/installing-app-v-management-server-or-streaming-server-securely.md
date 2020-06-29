---
title: Como instalar um servidor de gerenciamento do App-V ou um servidor de streaming com segurança
description: Como instalar um servidor de gerenciamento do App-V ou um servidor de streaming com segurança
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796903"
---
# Como instalar um servidor de gerenciamento do App-V ou um servidor de streaming com segurança


Os tópicos desta seção fornecem informações para instalar uma versão de segurança aprimorada do servidor de gerenciamento do App-V ou do servidor de streaming do App-V.

**Observação**  A instalação ou configuração de um servidor de fluxo ou de gerenciamento do App-V para usar a segurança aprimorada (por exemplo, Transport Layer Security ou TLS) requer que um certificado X. 509 v3 seja provisionado para o App-V Server.

 

Ao se preparar para instalar ou configurar um servidor de fluxo e gerenciamento seguro, considere os seguintes requisitos técnicos:

-   O certificado deve ser válido. Se o certificado não for válido, o cliente encerrará a conexão.

-   O certificado deve conter o *uso de chave avançada* (EKU) correto, autenticação do servidor (OID 1.3.6.1.5.5.7.3.1). Se o certificado não contiver esse EKU, o cliente encerrará a conexão.

-   O nome de domínio totalmente qualificado (FQDN) do certificado deve corresponder ao servidor no qual ele está instalado. Por exemplo, se o cliente estiver chamando `RTSPS://Myserver.mycompany.com/content/MyApp.sft` e o campo certificado **emitido para** está definido como `Server1.mycompany.com` , o cliente não se conectará ao servidor e a sessão será encerrada. A falha é reportada para o usuário.

    **Observação**  Se você estiver usando o App-V em um cluster de balanceamento de carga de rede, será preciso configurar o certificado com nomes alternativos de assunto (SANs) para dar suporte a RTSPs. Para obter informações sobre como configurar a CA (autoridade de certificação) e criar certificados com SANs, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .

     

-   O cliente e o servidor precisam confiar na CA raiz – a autoridade de certificação que emite o certificado para o servidor App-V deve ser confiável para o cliente se conectando ao servidor. Caso contrário, o cliente finalizará a conexão.

-   A chave privada do certificado deve ter permissões alteradas para permitir que a conta de serviço do App-V acesse o certificado. Por padrão, o App-V usa a conta de serviço de rede e, por padrão, a conta de serviço de rede não tem permissão para acessar a chave privada, o que impedirá conexões seguras.

## Nesta seção


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[Configuração de certificados para dar suporte ao streaming seguro](configuring-certificates-to-support-secure-streaming.md)  
Fornece informações sobre como obter, configurar e instalar certificados para dar suporte ao streaming seguro.

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
Fornece procedimentos que você pode usar para modificar as chaves no Windows Server2003 e no Windows Server2008.

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
Fornece informações sobre como configurar certificados para os servidores de gerenciamento ou de fluxo do App-V, incluindo informações sobre como configurar certificados para ambientes de balanceamento de carga de rede.

 

 





