---
title: Planejar implantação de cliente MBAM 1.0
description: Planejar implantação de cliente MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799760"
---
# Planejar implantação de cliente MBAM 1.0


Dependendo de quando você implantar o cliente Microsoft BitLocker Administration and Monitoring (MBAM), você pode habilitar a criptografia do BitLocker em um computador em sua organização antes de o usuário final receber o computador ou depois. Para habilitar a criptografia BitLocker após o usuário final receber o computador, configure a política de grupo. Para habilitar a criptografia do BitLocker antes de o usuário final receber o computador, implante o software cliente do MBAM usando um sistema de implantação de software corporativo.

Você pode usar um ou os dois métodos em sua organização. Se você usa os dois métodos, pode melhorar a conformidade, o relatório e o suporte à recuperação de chave.

**Observação**  Para verificar os requisitos do sistema do cliente do MBAM, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).

 

## Implantando o cliente do MBAM para habilitar a criptografia do BitLocker após a distribuição do computador para usuários finais


Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager 2012 ou os serviços de domínio do Active Directory, para implantar os arquivos do Windows Installer da instalação do cliente do MBAM para os computadores de destino. Os dois arquivos de instalação do cliente MBAM do Windows Installer são MBAMClient-64bit.msi e MBAMClient-32bit.msi, que são fornecidos com o software do MBAM. Para obter mais informações sobre como implantar objetos de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

Quando você implanta o cliente MBAM, depois de distribuir os computadores para os usuários finais, os usuários finais são solicitados a criptografar seus computadores. Isso permite que o MBAM colete os dados para incluir o PIN e a senha e, em seguida, iniciar o processo de criptografia.

**Observação**  Nessa abordagem, os usuários são solicitados a ativar e inicializar o chip Trusted Platform Module (TPM), se ele não tiver sido ativado anteriormente.

 

## Usando o cliente MBAM para habilitar a criptografia do BitLocker antes da distribuição do computador para usuários finais


Nas organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia do BitLocker em cada computador antes que os dados do usuário sejam gravados nele. A vantagem desse processo é que cada computador será compatível com a criptografia do BitLocker. Esse método não depende da ação do usuário porque o administrador já criptografou o computador. Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.

Se a sua organização deseja usar (TPM) para criptografar computadores, o administrador deve criptografar o volume do sistema operacional do computador com o protetor TPM. Se a sua organização quiser usar o chip TPM e um protetor de PIN, o administrador deve criptografar o volume do sistema com o protetor TPM e, em seguida, os usuários selecionam um PIN na primeira vez em que fazem logon. Se a sua organização decidir usar apenas o protetor de PIN, o administrador não precisará criptografar o volume primeiro. Quando os usuários fazem logon em seus computadores, o MBAM solicita que forneçam um PIN ou um PIN e uma senha que eles usarão quando reinicializarem o computador mais tarde.

**Observação**  A opção de protetor TPM exige que o administrador aceite o prompt do BIOS para ativar e inicializar o TPM antes de entregar o computador ao usuário.

 

## Tópicos relacionados


[Planejar a implantação do MBAM 1.0](planning-to-deploy-mbam-10.md)

[Implantando o Cliente do MBAM 1.0](deploying-the-mbam-10-client.md)

 

 





