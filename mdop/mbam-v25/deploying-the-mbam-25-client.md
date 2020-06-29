---
title: Implantando o cliente do MBAM 2.5
description: Implantando o cliente do MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799840"
---
# Implantando o cliente do MBAM 2.5


O software cliente de administração e monitoramento do Microsoft BitLocker (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory, ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.

Dependendo de quando você implantar o software cliente de administração e monitoramento do Microsoft BitLocker, é possível habilitar a criptografia de unidade de disco BitLocker em um computador em sua organização antes de o usuário final receber o computador ou depois de configurar a política de grupo e implantar o software cliente do MBAM usando um sistema de implantação de software corporativo.

## Implantar o cliente do MBAM em computadores desktop ou laptop


Depois de definir as configurações da política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o MicrosoftSystemCenter2012 ConfigurationManager ou os serviços de domínio do Active Directory, para implantar os arquivos de instalação do cliente do MBAM no computador de destino. Você pode usar os arquivos 32 de MbamClientSetup.exe bits ou 64 bits ou os arquivos de 32 bits ou 64 bits MBAMClient.msi, que são fornecidos com o software cliente MBAM. Para obter mais informações sobre a implantação de configurações de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 2,5](deploying-mbam-25-group-policy-objects.md).

**Observação**  A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM. No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto.

 

[Como implantar o cliente do MBAM em computadores desktop ou notebooks](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## Implantar o cliente MBAM como parte de uma implantação do Windows


Nas organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia de unidade de disco BitLocker em cada computador antes que os dados do usuário sejam gravados nele. A vantagem desse processo é que todos os computadores, em conformidade com a criptografia de unidade de disco BitLocker. Esse método não depende da ação do usuário porque o administrador já criptografou o computador. Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário. Se as configurações de política de grupo tiverem sido configuradas para exigir um PIN, os usuários serão solicitados a definir um PIN depois de receberem a política.

[Como habilitar o BitLocker por meio do MBAM como parte de uma implantação do Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## Como implantar o cliente MBAM usando uma linha de comando


Esta seção explica como instalar o cliente MBAM usando uma linha de comando.

[Como implantar o cliente do MBAM usando uma linha de comando](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## Outros recursos para a implantação do cliente MBAM


[Implantando o MBAM 2.5](deploying-mbam-25.md)



## Tópicos relacionados


[Implantando o MBAM 2.5](deploying-mbam-25.md)

[Planejamento do MBAM 2.5](planning-for-mbam-25.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





