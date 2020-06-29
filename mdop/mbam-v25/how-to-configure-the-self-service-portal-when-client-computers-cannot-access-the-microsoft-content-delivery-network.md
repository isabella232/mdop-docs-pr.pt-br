---
title: Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft
description: Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799483"
---
# Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft


Siga estas instruções se os computadores cliente da sua organização não tiverem acesso à rede de distribuição de conteúdo (CDN) do Microsoft Ajax.

**Por que você precisa configurar isto:**

Seus computadores cliente precisam ter acesso à CDN, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript. Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, somente o nome da empresa e a conta sob a qual o usuário final será efetuado será exibido. Nenhuma mensagem de erro será mostrada.

**Observação**  No MBAM 2,5 SP1, os arquivos JavaScript são incluídos no produto, e você não precisa seguir as instruções nesta seção para configurar o SSP para dar suporte a clientes que não podem acessar a Internet.

 

**Como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN**

1. Baixe os seguintes arquivos JavaScript da CDN:

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. Copie os arquivos JavaScript para o diretório **scripts** do portal de autoatendimento. Esse diretório está localizado no <em> &lt; MBAM Self-Service &gt; \\ </em> Website\\Scripts. Self-Service Directory

3. Abra o Gerenciador dos serviços de informações da Internet (IIS).

4. Expanda **sites** &gt; **Administração e monitoramento do Microsoft BitLocker**e realce **SelfService**.

   **Observação**  
   *SelfService* é o nome do diretório virtual padrão. Se você escolheu um nome diferente para esse diretório durante a configuração, lembre-se de substituir *SelfService* nessas instruções pelo nome escolhido.

     

5. No painel do meio, clique duas vezes em **configurações do aplicativo**.

6. Para cada item na lista a seguir, edite as configurações do aplicativo para referenciar o novo local substituindo/ &lt; *diretório virtual* &gt; /com/SelfService/(ou qualquer nome que você tenha escolhido durante a configuração). Por exemplo, o caminho do diretório virtual será semelhante a jQuery-1.10.2.min.js/selfservice/Scripts/.

   -   jQueryPath:/ &lt; *diretório virtual* &gt; /scripts/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *diretório virtual* &gt; /scripts/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *diretório virtual* &gt; /scripts/jQuery.validate.unobtrusive.min.js



## Tópicos relacionados


[Como configurar os aplicativos Web do MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





