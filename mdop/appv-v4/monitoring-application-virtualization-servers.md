---
title: Monitorando Application Virtualization Servers
description: Monitorando Application Virtualization Servers
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796866"
---
# Monitorando Application Virtualization Servers


Para simplificar o gerenciamento do servidor do Application Virtualization (App-V), você pode usar o pacote de gerenciamento do Manager2007 de operações do System Center. Este pacote de gerenciamento oferece suporte somente a servidores do Application Virtualization (App-V) 4,5; Ele não é compatível com versões anteriores do servidor. O pacote de gerenciamento maximiza a disponibilidade do App-V Server para manipular solicitações do cliente App-V.

## Indicadores de status


Os indicadores de status de integridade do App-V Server são codificados por cor. As cores representam os seguintes valores de status:

-   Sem cor indica que o servidor está em execução sem erros não recuperáveis.

-   Amarelo indica que um dos componentes não está funcionando corretamente. A funcionalidade geral do servidor está degradada, mas o servidor ainda está disponível.

-   Vermelho indica que o servidor não está disponível e que não pode fornecer serviços essenciais nem comunicar-se com dependências de serviço externo.

## Critérios de monitoramento


O pacote de gerenciamento monitora os seguintes aspectos da integridade do servidor:

-   Status do servidor — monitora eventos do servidor para confirmar se o servidor está fornecendo seus serviços esperados.

-   Acesso ao repositório de dados — controla a capacidade de um ou mais dos servidores de gerenciamento do App-V acessar e se comunicar com o repositório de dados do App-V.

-   Acesso a dados de conteúdo — monitora o acesso ao diretório \\Content, que pode ser um diretório local ou um compartilhamento de rede e a capacidade de ler os arquivos solicitados.

-   Segurança — relata erros com o certificado do servidor App-V e comunicações seguras.

-   Tratamento de solicitação do cliente — monitora a capacidade de um ou mais dos servidores do App-V manipular e responder corretamente a solicitações do cliente. Essas solicitações incluem a publicação de itens como solicitações de configuração, solicitações de carregamento de pacote e solicitações fora de sequência.

-   Configuração do servidor — verifica as configurações do App-V Server. Essas configurações incluem as configurações no registro e no repositório de dados App-V.

## Diferenças do servidor


As principais diferenças entre o servidor de gerenciamento do App-V e do App-V Streaming Server são as seguintes:

-   Os servidores de gerenciamento do App-V podem oferecer serviços de publicação, streaming, gerenciamento e relatórios. Portanto, o pacote de gerenciamento pode gerenciar mais aspectos do servidor de gerenciamento do App-V do que ele pode gerenciar no servidor de streaming do App-V, que fornece apenas streaming de pacote.

-   O servidor de streaming App-V não tem um repositório de dados App-V, portanto, o acesso ao repositório de dados não é monitorado. As informações de configuração do servidor de streaming App-V são gerenciadas no registro.

-   O servidor de streaming do App-V não usa a interface do console de gerenciamento do App-V Server; Use outras ferramentas para gerenciar a configuração.

## Tópicos relacionados


[Application Virtualization Server](application-virtualization-server.md)

 

 





