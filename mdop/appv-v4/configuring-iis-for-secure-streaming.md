---
title: Configuração do IIS para streaming seguro
description: Configuração do IIS para streaming seguro
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798014"
---
# Configuração do IIS para streaming seguro


Com o lançamento do Microsoft Application Virtualization (App-V) versão 4,5, você pode usar HTTP e HTTPS como protocolos para transmitir pacotes de aplicativos para os clientes do App-V. Essa opção permite que as organizações aproveitem a escalabilidade adicional que o IIS geralmente oferece. Ao usar o IIS como um servidor de streaming, você pode ajudar a proteger a comunicação entre o cliente e o servidor usando HTTPS em vez de HTTP.

**Observação**  Se quiser transmitir aplicativos de um servidor de arquivos, você deve melhorar a segurança das comunicações com os pacotes de aplicativos. Isso pode ser conseguido com o IPsec. Para obter mais informações, consulte os seguintes tópicos na biblioteca do TechNet:

-   Para Windows Server2003, <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Para o Windows Server 2008, <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## Tipos de MIME


Quando você usa o IIS para transmitir aplicativos virtuais com HTTP ou HTTPS, para dar suporte ao App-V, os seguintes tipos de MIME devem ser adicionados ao servidor IIS:

-   . OSD = TXT

-   . SFT = binário

Use os seguintes artigos da KB como orientação para adicionar tipos de MIME:

IIS 6,0: <https://go.microsoft.com/fwlink/?LinkId=151973>

IIS 7,0: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Autenticação Kerberos


Ao usar a autenticação HTTP ou HTTPS e Kerberos para transmitir arquivos ICO, OSD ou SFT, você está aprimorando a segurança do seu ambiente. No entanto, para que o IIS ofereça suporte à autenticação Kerberos, você deve configurar um SPN (nome da entidade de serviço) adequado. A `setspn.exe` ferramenta está disponível para Windows Server2003 nas ferramentas de suporte no CD de instalação e está integrada ao Windows Server2008.

Para criar um SPN, execute `setspn.exe` a partir de um prompt de comando enquanto estiver conectado como membro de administradores de domínio, por exemplo, `setspn.exe –A HTTP/FQDN of Server ServerName` .

## Tópicos relacionados


[Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





