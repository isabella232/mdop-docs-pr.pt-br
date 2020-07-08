---
title: Planejando a implantação do cliente do MBAM 2.5
description: Planejando a implantação do cliente do MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799783"
---
# Planejando a implantação do cliente do MBAM 2.5


Dependendo de quando você implantar o software cliente do Microsoft BitLocker Administration and Monitoring (MBAM), você pode habilitar a criptografia de unidade de disco BitLocker em um computador em sua organização antes de o usuário final receber o computador ou mais tarde. Para as topologias de integração do MBAM autônomo e do System Center Configuration Manager, você precisa definir configurações de política de grupo para MBAM.

Se você estiver usando a topologia autônoma do MBAM, recomendamos que use um sistema de implantação de software corporativo para implantar o software cliente do MBAM em computadores de usuário final.

Se você implantar o MBAM com a topologia de integração do Configuration Manager, poderá usar o Configuration Manager para implantar o software cliente do MBAM em computadores de usuário final. No Configuration Manager, a instalação do MBAM cria um conjunto de computadores que MBAM pode gerenciar. Esta coleção inclui estações de trabalho e dispositivos que não têm um Trusted Platform Module (TPM), mas que estão executando o Windows 8, o Windows 8,1 ou o Windows 10.

**Observação**  Não há suporte para o Windows to go para a instalação de topologia de integração do Configuration Manager quando você está usando o Configuration Manager 2007.

 

## Implantando o cliente MBAM para habilitar a criptografia de unidade de disco BitLocker após a distribuição de computador para usuários finais


Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager ou os serviços de domínio Active Directory (AD DS), para implantar os arquivos do Windows Installer da instalação do cliente do MBAM em computadores de destino. Para implantar o cliente do MBAM, você pode usar os arquivos 32 de MbamClientSetup.exe bits ou 64 bits ou arquivos MBAMClient.msi, que são fornecidos com o software cliente do MBAM.

**Observação**  A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM. No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto.

 

Quando você implanta o cliente MBAM após distribuir computadores para computadores cliente, os usuários finais são solicitados a criptografar o computador. Essa ação permite que o MBAM colete os dados, que inclui o PIN e a senha (se necessário pela política) e, em seguida, iniciar o processo de criptografia.

**Observação**  Nessa abordagem, os usuários finais que tiverem computadores com um chip TPM serão solicitados a ativar e inicializar o chip TPM se o chip não tiver sido ativado anteriormente.

 

## Usando o cliente MBAM para habilitar a criptografia de unidade de disco BitLocker antes da distribuição de computador para usuários finais


Nas organizações em que os computadores são recebidos e configurados de forma centralizada, e onde os computadores têm um chip TPM compatível, você pode usar o cliente MBAM para gerenciar a criptografia de unidade de disco BitLocker em cada computador antes que os dados do usuário sejam gravados nele. A vantagem desse processo é que todos os computadores são compatíveis. Esse método não depende da ação do usuário final porque o administrador já criptografou o computador. Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário final.

Se a sua organização quiser usar o chip TPM para criptografar computadores, o administrador adicionará o protetor TPM para criptografar o volume do sistema operacional do computador. Se a sua organização quiser usar o chip TPM e um protetor de PIN, o administrador criptografará o volume do sistema operacional com o protetor TPM e, em seguida, os usuários finais selecionarão um PIN quando fizerem logon pela primeira vez. Se a sua organização decidir usar apenas o protetor de PIN, o administrador não precisará criptografar o volume primeiro. Quando os usuários finais se conectam, o monitoramento e a administração do Microsoft BitLocker pedem que eles forneçam um PIN, ou um PIN e uma senha a serem usados em reinícios posteriores do computador.

**Observação**  A opção de protetor TPM exige que o administrador aceite o prompt do BIOS para ativar e inicializar o TPM antes que o computador seja entregue ao usuário final.

 

## Suporte do cliente MBAM para discos rígidos criptografados


O MBAM dá suporte ao BitLocker em discos rígidos criptografados que atendem aos requisitos de especificação do TCG para o Opal e com os padrões IEEE 1667. Quando o BitLocker estiver habilitado nesses dispositivos, ele irá gerar chaves e executar funções de gerenciamento na unidade criptografada. Para obter mais informações, consulte [unidade de disco rígido criptografado](https://technet.microsoft.com/library/hh831627.aspx) .


## Tópicos relacionados


[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

[Implantando o cliente do MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




