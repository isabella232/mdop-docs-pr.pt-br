---
title: Como implantar o cliente do MBAM em computadores desktop ou notebooks
description: Como implantar o cliente do MBAM em computadores desktop ou notebooks
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796142"
---
# Como implantar o cliente do MBAM em computadores desktop ou notebooks


O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory ou o MicrosoftSystemCenterConfigurationManager.

**Observação**  Para verificar os requisitos do sistema do cliente de administração e administração do Microsoft BitLocker, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).

 

**Para implantar o cliente do MBAM em computadores desktop ou laptop**

1.  Localize os arquivos de instalação do cliente do MBAM fornecidos com o software do MBAM.

2.  Use os serviços de domínio do Active Directory ou uma ferramenta de implantação de software corporativo como o MicrosoftSystemCenterConfigurationManager para implantar o pacote do Windows Installer nos computadores de destino.

3.  Configurar as configurações de distribuição ou a política de grupo para executar o arquivo de instalação do cliente MBAM. Após a instalação bem-sucedida, o cliente MBAM aplica as configurações de política de grupo que são recebidas de um controlador de domínio para iniciar as funções de gerenciamento e criptografia do BitLocker. Para obter mais informações sobre configurações de política de grupo do MBAM, consulte [planejando requisitos de política de grupo do MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).

    **Importante**  O cliente MBAM não iniciará as ações de criptografia BitLocker se uma conexão de protocolo de área de trabalho remota estiver ativa. Todas as conexões de console remoto devem ser fechadas antes que a criptografia do BitLocker seja iniciada.

     

## Tópicos relacionados


[Implantando o Cliente do MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





