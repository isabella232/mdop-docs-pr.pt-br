---
title: Visão geral de segurança e proteção
description: Visão geral de segurança e proteção
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796769"
---
# Visão geral de segurança e proteção


O Microsoft Application Virtualization 4.5 oferece os seguintes recursos de segurança aprimorados para ajudar você a planejar e implementar uma estratégia de implantação mais segura:

-   A virtualização de aplicativos agora oferece suporte a TLS (Transport Layer Security) usando certificados do X. 509 v3. Desde que um certificado do servidor tenha sido provisionado para o gerenciamento de aplicativo de aplicativos ou o servidor de streaming planejado, a instalação padrão será segura, usando o protocolo RTSP na porta 322. Usar RTSPs garante que a comunicação entre os servidores de virtualização de aplicativos e os clientes de virtualização de aplicativos seja assinada e criptografada. Se nenhum certificado for atribuído ao servidor durante a instalação do servidor do Application Virtualization, a comunicação será definida como RTSP na porta 554.

    **Observação de segurança:**

    Para ajudar a oferecer uma configuração de segurança do servidor, você deve verificar se as portas RTSP estão desativadas, mesmo que você tenha todos os pacotes configurados para usar RTSPs.

    Se você adicionar certificados de segurança ao servidor após a instalação do servidor, o servidor talvez não detecte os certificados. Para ajudar a garantir a detecção do certificado de segurança, reinicie o servidor após adicionar os certificados.

-   O cliente deve ser configurado para usar o mesmo protocolo e a mesma porta do servidor ou não poderá se comunicar com o servidor. O cliente também deve confiar no emissor do certificado e vem com vários dos provedores primários em seu armazenamento raiz confiável. Você pode usar certificados autoassinados, mas será necessário atualizar os clientes.

-   Ao configurar os servidores IIS para usar o protocolo HTTPS para streaming, você precisará configurar o Secure Sockets Layer (SSL) no servidor IIS e provisionar o certificado para o servidor. Além disso, os clientes precisarão ser configurados para confiar na autoridade de certificação raiz que emitiu o certificado do servidor.

-   A autenticação Kerberos foi adicionada ao Microsoft Application Virtualization como o mecanismo de autenticação padrão. Versões anteriores dependentes do NTLM v2 para autenticação. Usar a autenticação Kerberos reforça a segurança da comunicação entre o cliente e o servidor do Application Virtualization. Quando uma conexão é iniciada do cliente, o servidor de virtualização de aplicativos verifica a permissão de sessão com o centro de distribuição de chaves (KDC).

-   Devido ao suporte para o uso de certificados de servidor e o uso de protocolos HTTPS ou HTTPS, agora você pode oferecer suporte a clientes fora da rede corporativa. Isso pode ajudar a eliminar a necessidade de usuários móveis de configurar uma conexão segura com a rede corporativa (VPN, RAS e assim por diante) antes de iniciar aplicativos provisionados do Application Virtualization.

Outras importantes considerações de segurança a serem consideradas incluem o seguinte:

-   Sempre mantenha os servidores totalmente atualizados e protegidos.

-   Para adicionar um certificado para permitir comunicações mais seguras com o servidor de gerenciamento do Application Virtualization, os seguintes critérios devem ser atendidos:

    -   O usuário que adicionará o certificado deve ser um administrador no servidor em que o repositório de certificados está localizado.

    -   O serviço do servidor deve ser iniciado.

    -   A porta 139 do servidor de gerenciamento deve estar aberta para o serviço Web server'sIP.

-   Use as listas de controle de acesso (ACLs) para garantir que os pacotes de aplicativos e todos os arquivos de pacote sejam protegidos e não possam ser adulterados. ACLs restringem o acesso ao local ou à pasta onde você armazena os pacotes, permitindo o acesso somente a determinadas contas.

-   Certifique-se de que o canal entre o servidor de gerenciamento do Application Virtualization e o banco de dados seja protegido — por exemplo, usando IPsec.

-   Se os pacotes estiverem armazenados em uma SAN ou NAS, verifique se a conexão entre o dispositivo de armazenamento central e os servidores de virtualização de aplicativo está protegida.

-   Todos os canais de comunicação para o cliente devem ser protegidos, incluindo as conexões com o servidor de publicação, o servidor do Application Virtualization e o caminho para os arquivos OSD e ICO, usando um protocolo como HTTPS ou IPsec. 

-   As permissões de cliente devem ser configuradas para ajudar a garantir que os pacotes não possam ser adulterados por usuários. É especialmente importante que você não conceda aos usuários permissão para adicionar ou atualizar pacotes em sistemas, como servidores host de sessão de área de trabalho remota (host RDSession) que são compartilhados com vários usuários.

-   A autenticação Kerberos deve ser permitida em ambientes de floresta ou domínio para que o console de gerenciamento do servidor funcione corretamente.

-   Esta versão do software não oferece suporte à Hospedagem de um servidor RTSP baseado em Kerberos e a um servidor IIS baseado em Microsoft NTLM somente no mesmo computador. Para hospedar um servidor RTSP e um servidor IIS no mesmo computador, remova o SPN do servidor IIS e use a autenticação NTLM.

## Tópicos relacionados


[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





