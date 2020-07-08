---
title: Planejamento da segurança do cliente
description: Planejamento da segurança do cliente
author: dansimp
ms.assetid: 4840a60f-4c91-489c-ad0b-6671882abf9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0038f7cbc8592d6c7fcdfa485111da88c17791d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796824"
---
# Planejamento da segurança do cliente


O cliente App-V fornece vários aprimoramentos de segurança que não estavam presentes nas versões anteriores do produto. Essas alterações fornecem segurança aprimorada após a instalação e, por meio da configuração mais recente das configurações do cliente. Este tópico descreve algumas dessas melhorias e identifica várias configurações importantes relacionadas à segurança que você deve considerar durante o processo de planejamento. É importante lembrar que os aplicativos virtuais ainda são executáveis, portanto, você deve garantir que esses ativos não sejam adulterados por pessoas não autorizadas. Por esse motivo, o cache de arquivos Open Software Descriptor (OSD) é protegido conforme descrito posteriormente neste tópico, e recomendamos que você use RTSPs, HTTPS e IPsec para proteger a publicação e streaming.

## Segurança do cliente do App-V


Por padrão, na instalação, o cliente App-V é configurado com as permissões mínimas necessárias para permitir que um usuário execute uma atualização de publicação e inicie aplicativos. Outros aprimoramentos de segurança fornecidos no cliente App-V incluem o seguinte:

-   Por padrão, o cache de arquivos OSD pode ser atualizado apenas por administradores e usando o processo de atualização de publicação.

-   O arquivo de log (sftlog.txt) só pode ser acessado por contas com acesso administrativo local ao cliente.

-   O arquivo de log agora tem um tamanho máximo.

### Associações de tipo de arquivo

Por padrão, a instalação do cliente registra associações de tipo de arquivo (FTAs) para arquivos OSD, o que permite que os usuários iniciem aplicativos diretamente de arquivos OSD em vez dos atalhos publicados. Se um usuário com direitos de administrador local receber um arquivo OSD contendo código mal-intencionado, seja por email ou baixado de um site, o usuário poderá abrir o arquivo OSD e iniciar o aplicativo, mesmo que o cliente tenha sido definido para restringir a permissão **Adicionar aplicativo** . Você pode cancelar o registro do FTAs para o OSD reduzir esse risco. Além disso, considere bloquear essa extensão no sistema de email e no firewall. Para obter mais informações sobre como configurar o Outlook para bloquear extensões, consulte <https://go.microsoft.com/fwlink/?LinkId=133278> .

**Observação de segurança:**

A partir da versão 4.6 do App-V, a associação de tipo de arquivo não é mais criada para arquivos OSD durante uma nova instalação do cliente, embora as configurações existentes sejam mantidas durante uma atualização da versão 4,2 ou 4,5 do App-V Client. Se, por qualquer motivo, for essencial criar a associação de tipo de arquivo, você poderá criar as seguintes chaves do registro e definir seus valores conforme mostrado:

    Create HKEY\_CLASSES\_ROOT\\.osd with a default value of SoftGrid.osd.File

    Under HKEY\_LOCAL\_MACHINE\\software\\classes\\Softgrid.osd.file, create a string value named AppUserModelID with a data value of Microsoft.AppV.Client.Tray

### Autorização

Durante a instalação, você pode usar o parâmetro **RequireAuthorizationIfCached** para configurar o cliente para exigir autorização do servidor quando o usuário tentar iniciar um aplicativo. Considere cuidadosamente como definir esse parâmetro. Se o servidor App-V estiver indisponível por algum motivo, o aplicativo usará o estado armazenado mais recente desse parâmetro para controlar o acesso do usuário ao aplicativo. Se o usuário não tiver iniciado o aplicativo com êxito antes de o servidor do App-V ficar indisponível, ele não poderá iniciar o aplicativo até que ele possa se comunicar com o servidor e receber a autorização. No entanto, se você definir o parâmetro para que o cliente não exija autorização e se o servidor não estiver disponível, todos os aplicativos armazenados anteriormente em cache poderão ser iniciados, seja autorizado ou não. Além disso, se o usuário tiver permissão para alterar o cliente para trabalhar no modo offline por meio de permissões ou se o usuário for um administrador local, o usuário poderá abrir todos os pacotes em cache como se a infraestrutura do App-V estivesse indisponível.

### Verificação de antivírus

O software antivírus em execução em um computador cliente App-V pode detectar e relatar um arquivo infectado no ambiente virtual. No entanto, ele não pode disinfectr o arquivo. Se um vírus for detectado no ambiente virtual, o software antivírus executaria a operação de quarentena ou reparo configurada no cache, e não no pacote real. Configure o software antivírus com uma exceção para o arquivo Sftfs. FSD. Esse arquivo é o arquivo de cache que armazena pacotes no cliente App-V.

**Observação de segurança:**

Se um vírus for detectado em um aplicativo ou pacote implantado no ambiente de produção, substitua o aplicativo ou o pacote por uma versão sem vírus.

## Comunicação entre cliente e servidor


As atualizações de publicação e o streaming de pacote também são áreas nas quais considerações de segurança relacionadas à comunicação cliente/servidor são importantes.

### Atualização de publicação

Quando o cliente se comunica com o servidor para executar uma atualização de publicação, ele usa as credenciais do usuário conectado para solicitar informações sobre os pacotes de aplicativos. Você deve proteger a comunicação que ocorre entre o cliente App-V e o App-V Management Server para garantir que nenhuma das informações de publicação possa ser adulterada em trânsito. Isso é feito usando-se a opção de segurança aprimorada, que usará RTSPs/HTTPS. A comunicação entre o cliente e o local em que os arquivos ICO e OSD são armazenados deve usar IPsec para compartilhamentos SMB/CIFS e HTTPS para um servidor IIS.

**Observação**  Se você estiver usando o IIS para publicar os arquivos ICO e OSD, configure um tipo MIME para OSD = TXT; caso contrário, o IIS se recusará a atender os arquivos ICO e OSD aos clientes.

 

### Streaming de pacote

Quando um usuário inicia um aplicativo pela primeira vez, ou se os parâmetros de carregamento automático são definidos no cliente, o pacote do aplicativo é transmitido de um servidor para o cache do cliente. Esse processo dá suporte a protocolos RTSP/RTSP, HTTP/HTTPS e SMB/CIFS. Os arquivos OSD controlam quais protocolos são usados, a menos que a configuração **APPLICATIONSOURCEROOT** ou **OVERRIDEURL** tenha sido configurada nos clientes. Você deve configurar a comunicação para ocorrer em RTSPs, HTTPS ou IPsec para SMB/CIFS para obter níveis mais altos de segurança. Para obter mais informações sobre como escolher o método de comunicação a ser usado, consulte o guia de planejamento e implantação do App-V em <https://go.microsoft.com/fwlink/?LinkId=122063> .

**Observação**  Se você estiver usando o IIS para publicar pacotes (arquivos SFT), configure um tipo MIME para SFT = Binary; caso contrário, o IIS se recusará a atender os arquivos SFT aos clientes.

 

### Perfis de roaming e redirecionamento de pastas

O sistema App-V armazena alterações específicas do usuário em pacotes no arquivo usrvol \ _sftfs \ _v1. pkg. Esse arquivo está localizado na pasta dados do aplicativo do perfil de um usuário. Como o perfil ou uma pasta de dados de aplicativo redirecionada é transferida entre o cliente e o servidor, use IPsec para proteger a comunicação.

## Considerações para clientes voltados para a Internet


Para clientes voltados para a Internet, é importante considerar se o cliente é membro do domínio ou não ingressado no domínio.

### Cliente ingressado no domínio

Por padrão, os clientes do App-V usam tíquetes Kerberos que foram emitidos pelos serviços de domínio Active Directory para autenticação e autorização na intranet. Esses tíquetes Kerberos são válidos por 10 horas por padrão. O cliente usará esse tíquete para acessar o App-V Server enquanto o tíquete for válido, mesmo se o computador não conseguir se conectar ao controlador de domínio para atualizar a permissão. Se o tíquete Kerberos expirar, o cliente App-V irá reverter para a autenticação NTLM e usará as credenciais do usuário armazenadas em cache.

### Cliente não associado a um domínio

Se um usuário for baseado em casa e o computador não estiver associado ao domínio da empresa, o App-V ainda poderá oferecer suporte ao fornecimento de aplicativos. Para autenticar e autorizar um usuário para executar uma atualização de publicação e iniciar aplicativos, configure a conta de usuário no computador cliente para armazenar o nome de usuário e a senha que têm acesso ao ambiente do App-V e para fornecer as permissões apropriadas para os aplicativos.

## Tópicos relacionados


[Planejamento de segurança e proteção](planning-for-security-and-protection.md)

 

 





