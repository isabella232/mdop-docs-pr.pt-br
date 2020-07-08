---
title: Planejamento da segurança do servidor
description: Planejamento da segurança do servidor
author: dansimp
ms.assetid: c7cd8227-b359-41e7-a8ae-d0d5718a76a2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bea1bd8287a15385200bbfb425ed8e00fbcdb02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796818"
---
# Planejamento da segurança do servidor


Para aprimorar a segurança de um ambiente, você deve observar a exposição a qualquer possível ameaça no ambiente. O fornecimento de segurança para uma infraestrutura do App-V requer o uso dos recursos de segurança específicos do App-V, bem como as práticas de segurança e os recursos da infraestrutura subjacente. A proteção da infraestrutura subjacente para serviços como serviços de informações da Internet (IIS), dos serviços de domínio Active Directory e do SQL Server irá melhorar a segurança geral do seu sistema App-V.

As configurações padrão para a instalação do servidor fornecem os níveis mais altos de segurança. No entanto, alguns dos componentes dependem da infraestrutura subjacente que não está configurada como parte da instalação. Acompanhar as etapas pós-instalação aprimorará a segurança da infraestrutura do App-V.

O diretório de conteúdo contém todos os pacotes que devem ser transmitidos para os clientes. Esses recursos precisam ser o mais seguros possível para eliminar muitas possíveis ameaças de segurança. A lista a seguir oferece algumas orientações adicionais:

-   Publicação com base em UNC e/ou streaming — as permissões para esse item devem ser as mais restritivas no ambiente. Use as permissões de NTFS para implementar as listas de controle de acesso (ACLs) mais restritivas do diretório de conteúdo (usuários = ler, administradores = ler e gravar).

-   IIS usado para publicação e/ou streaming — configure o IIS para dar suporte apenas à autenticação integrada do Windows. Remova o acesso anônimo ao servidor IIS e restrinja o acesso ao diretório com permissões NTFS.

-   RTSP/RTSP para transmitir pacotes de aplicativos — configure a política do provedor do App-V para exigir autenticação, impor permissões de acesso e habilitar somente grupos obrigatórios para ter acesso à política do provedor. Configurar aplicativos com as permissões apropriadas no banco de dados.

Mantenha o número de usuários com privilégios administrativos a um mínimo para reduzir possíveis ameaças aos dados no repositório de dados e para evitar a publicação de aplicativos mal-intencionados na infra-estrutura.

## Segurança da virtualização de aplicativos


O App-V usa vários métodos de comunicação entre os vários componentes da infraestrutura. Quando você planeja sua infraestrutura do App-V, a proteção das comunicações entre servidores pode reduzir os riscos de segurança que já podem estar presentes na rede existente.

### Repositório de dados

O servidor de gerenciamento do Application Virtualization e o serviço de gerenciamento de virtualização de aplicativos se comunicam com o repositório de dados usando uma conexão SQL na porta TCP 1433. O servidor de gerenciamento usa o repositório de dados para recuperar dados de aplicativos e de configuração, além de gravar as informações de uso no banco de dados. O serviço de gerenciamento comunica-se com o repositório de dados em nome de um administrador que está configurando a infraestrutura do App-V. Como o repositório de dados contém informações críticas, é importante minimizar as ameaças a esses dados.

É recomendável que as comunicações entre o servidor de gerenciamento do App-V, o serviço de gerenciamento e o repositório de dados sejam protegidas com a segurança do protocolo Internet (IPsec). Especificamente, crie políticas que protejam o canal de comunicação entre o repositório de dados (SQL) e o servidor de gerenciamento e o repositório de dados e o serviço de gerenciamento. Você também pode implantar o isolamento de servidor e domínio com IPsec, garantindo que todos os componentes da infraestrutura do App-V se comuniquem somente com canais seguros. Para obter informações sobre como implementar o IPsec, consulte a seguinte documentação:

-   Para o Windows Server2003, consulte <https://go.microsoft.com/fwlink/?LinkId=133226> ( https://go.microsoft.com/fwlink/?LinkId=133226) .

-   Para o Windows Server2008, consulte <https://go.microsoft.com/fwlink/?LinkId=133227> ( https://go.microsoft.com/fwlink/?LinkId=133227) .

### Diretório de conteúdo

A instalação do App-V Management Server configura um local para o diretório de conteúdo. Esse diretório é o local de armazenamento para pacotes de aplicativos virtualizados. Esse local pode ser local para o servidor ou pode ser colocado em um compartilhamento de rede remoto. Portanto, implemente o IPsec para ajudar a proteger a comunicação com um local remoto para o diretório de conteúdo.

Você também pode usar um diretório virtual em um servidor IIS para transmitir pacotes para os clientes. Se o diretório virtual criado para conteúdo estiver localizado em uma fonte remota, use o IPsec para ajudar a proteger a comunicação entre o servidor IIS e o local de armazenamento remoto.

O diretório de conteúdo contém todos os pacotes que são transmitidos para os clientes. Esses recursos precisam ser o mais seguros possível para eliminar muitas possíveis ameaças de segurança.

### Protocolos de segurança

Você pode usar RTSPs ou HTTPS para comunicações seguras aprimoradas. RTSPs é o protocolo usado por servidores App-V, e HTTPS é o protocolo usado pelos servidores IIS. Esses protocolos são usados ao publicar aplicativos do servidor para o cliente da área de trabalho do Application Virtualization. Depois de determinar o protocolo desejado, adicione um servidor de publicação que use esse protocolo.

### <a href="" id="configuring-app-v-servers-for-rtsps-"></a>Configurando servidores App-V para RTSPs

A instalação ou configuração de um servidor de gerenciamento do App-V ou do servidor de streaming para usar a segurança aprimorada (por exemplo, TLS) requer que um certificado X. 509 v3 seja provisionado para o App-V Server. Ao se preparar para instalar ou configurar a segurança para um servidor, você deve atender a alguns requisitos específicos. Os requisitos técnicos para a implantação e a configuração de certificados para um servidor de gerenciamento do App-V mais seguro ou servidor de fluxo contínuo incluem o seguinte:

-   O certificado deve ser válido. Caso contrário, o cliente encerrará a conexão.

-   O certificado deve conter a correção de uso avançado de chave (EKU)-autenticação do servidor (OID 1.3.6.1.5.5.7.3.1) correta. Caso contrário, o cliente encerrará a conexão.

-   O nome de domínio totalmente qualificado (FQDN) do certificado deve corresponder ao servidor no qual ele está instalado. Por exemplo, se o cliente estiver chamando `RTSPS://Myserver.mycompany.com/content/MyApp.sft` , mas o certificado **emitido para** o campo contiver `Myserver1.mycompany.com` , o cliente não se conectará ao servidor e a sessão será encerrada, mesmo se `Myserver.mycompany.com` e `Myserver1.mycompany.com` resolvida para o mesmo endereço IP.

    **Observação**  Se você usa o App-V em um cluster de carga balanceada de rede, o certificado deve ser configurado com *nomes alternativos de assunto* (SANs) para dar suporte a RTSPS. Para obter informações sobre como configurar a CA (autoridade de certificação) e criar certificados com SANs, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> ( https://go.microsoft.com/fwlink/?LinkId=133228) .

     

-   A autoridade de certificação que emite o certificado para o servidor App-V deve ser confiável para o cliente se conectando ao servidor. Caso contrário, o cliente encerrará a conexão.

-   Você deve alterar as permissões da *chave privada do certificado* para habilitar o acesso pelo serviço App-V do servidor. Por padrão, os serviços do App-V Management Server e do Streaming Server são executados na conta de serviço de rede. Quando um #10 PKCS \ é gerado no servidor, uma chave privada é criada. Somente os grupos sistema local e administradores têm acesso a essa chave. Essas ACLs padrão impedem que o servidor App-V aceite conexões seguras.

    **Observação**  Para obter informações sobre como configurar uma PKI (infraestrutura de chave pública), consulte <https://go.microsoft.com/fwlink/?LinkId=133229> ( https://go.microsoft.com/fwlink/?LinkId=133229) .

     

### Configurando servidores IIS com HTTPS

O App-V pode usar servidores IIS em determinadas configurações de infraestrutura. Para obter mais informações sobre a configuração de servidores IIS, consulte <https://go.microsoft.com/fwlink/?LinkId=133230> ( https://go.microsoft.com/fwlink/?LinkId=133230) .

**Observação**  Se você estiver usando o IIS para publicar os arquivos ICO e OSD, configure um tipo MIME para OSD = TXT; caso contrário, o IIS se recusará a atender os arquivos ICO e OSD aos clientes.

 

### Segurança em nível de aplicativo

Você pode configurar os servidores para transmitir aplicativos específicos para a área de trabalho de um usuário. No entanto, a permissão de acesso na verdade é concedida no nível do pacote, e não no nível do aplicativo. Embora um aplicativo específico não possa ser publicado na área de trabalho do usuário, se o usuário tiver permissão para adicionar aplicativos ou se for um administrador no computador cliente, o usuário poderá criar e usar um atalho no cliente para executar todos os aplicativos em um pacote.

## Configuração da administração do App-V para um ambiente distribuído


Ao projetar a infraestrutura de sua organização específica, você pode instalar o serviço Web de gerenciamento do App-V em um computador diferente do computador em que você instala o servidor de gerenciamento do App-V. Os motivos comuns para separar esses componentes do App-V incluem o seguinte:

-   Desempenho

-   Confiabilidade

-   Disponibilidade

-   Escalabilidade

Para que a infraestrutura opere corretamente, separar o console de gerenciamento do App-V, servidor de gerenciamento e serviço Web de gerenciamento requer configuração adicional. Para obter informações detalhadas sobre como configurar o servidor, consulte [como configurar o servidor para ser confiável para delegação](how-to-configure-the-server-to-be-trusted-for-delegation.md).

## Tópicos relacionados


[Planejamento de segurança e proteção](planning-for-security-and-protection.md)

 

 





