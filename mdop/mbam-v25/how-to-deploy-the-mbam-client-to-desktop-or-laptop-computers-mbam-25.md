---
title: Como implantar o cliente do MBAM em computadores desktop ou notebooks
description: Como implantar o cliente do MBAM em computadores desktop ou notebooks
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799480"
---
# Como implantar o cliente do MBAM em computadores desktop ou notebooks


Este tópico explica como implantar o cliente MBAM para os computadores dos usuários finais. Você pode implantar o cliente MBAM por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory ou o Gerenciador de MicrosoftSystemCenterConfiguration.

Para implantar o cliente MBAM como parte de uma implantação do Windows, consulte [como habilitar o BitLocker usando o MBAM como parte de uma implantação do Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).

Antes de iniciar a implantação do cliente MBAM, examine as [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).

**Para implantar o cliente do MBAM em computadores desktop ou laptop**

1.  Localize os arquivos de instalação do cliente do MBAM fornecidos com o software do MBAM.

2.  Use os serviços de domínio do Active Directory ou uma ferramenta de implantação de software corporativo, como o MicrosoftSystemCenterConfiguration Manager, para implantar o pacote do Windows Installer em computadores de destino.

3.  Defina as configurações de distribuição ou as configurações de política de grupo para executar o arquivo de instalação do cliente MBAM.

    Após a instalação bem-sucedida, o cliente MBAM aplica as configurações de política de grupo que são recebidas de um controlador de domínio para iniciar as funções de gerenciamento e criptografia de unidade de disco BitLocker.

    **Importante**  O cliente MBAM não iniciará as ações de criptografia de unidade de disco BitLocker se uma conexão de protocolo de área de trabalho remota estiver ativa. Todas as conexões de console remoto devem ser fechadas e um usuário deve estar conectado a uma sessão de console físico antes do início da criptografia de unidade de disco BitLocker.

     


## Tópicos relacionados
[Implantando o cliente do MBAM 2.5](deploying-the-mbam-25-client.md)

[Planejando a implantação do cliente do MBAM 2.5](planning-for-mbam-25-client-deployment.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





