---
title: Como mover os sites do MBAM 2.5
description: Como mover os sites do MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799734"
---
# Como mover os sites do MBAM 2.5


Use estes procedimentos para mover os seguintes sites do MBAM de um computador para outro, ou seja, para mover os seguintes recursos do servidor a para o servidor B:

-   Site de administração e monitoramento

-   Portal de autoatendimento

**Importante**  Durante a configuração dos dois websites, você deve fornecer a mesma cadeia de conexão, a URL de relatórios, as contas de grupo e a conta de domínio do pool de aplicativos de serviço Web como aquelas que você está usando no momento. Se você não usar os mesmos valores, não será possível acessar alguns dos servidores. Para obter os valores atuais, use o cmdlet **Get-MbamWebApplication** do Windows PowerShell.

 

**Para mover o site de administração e monitoramento para outro servidor**

1.  No servidor B, instale o software do servidor MBAM 2,5. Para obter instruções, confira [instalar o software de servidor MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso de **site Administração e monitoramento** .

    Você também pode usar o cmdlet **Enable-MbamWebApplication** do Windows PowerShell para configurar o site de administração e monitoramento.

    Para obter instruções sobre como configurar o site de administração e monitoramento, consulte [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

**Para mover o portal de autoatendimento para outro servidor**

1.  No servidor B, instale o software do servidor MBAM 2,5. Para obter instruções, confira [instalar o software de servidor MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso do **portal de autoatendimento** .

    Você também pode usar o cmdlet **Enable-MbamWebApplication** do Windows PowerShell para configurar o portal de autoatendimento.

    Para obter instruções sobre como configurar o site de administração e monitoramento, consulte [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

3.  Se os computadores cliente da sua organização não tiverem acesso à rede de entrega de conteúdo da Microsoft, também será necessário mover os arquivos JavaScript. Veja [como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a rede de entrega de conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) para obter mais informações.

4.  Personalize o portal de autoatendimento da sua organização. Use as instruções em [Personalizando o portal de autoatendimento da sua organização](customizing-the-self-service-portal-for-your-organization.md) para analisar suas personalizações atuais e para definir configurações personalizadas no portal de autoservidor no servidor B.



## Tópicos relacionados


[Como configurar os aplicativos Web do MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Movendo os recursos do MBAM 2.5 para outro servidor](moving-mbam-25-features-to-another-server.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





