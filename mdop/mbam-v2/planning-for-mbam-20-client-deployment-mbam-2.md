---
title: Planejar implantação de cliente MBAM 2.0
description: Planejar implantação de cliente MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796045"
---
# Planejar implantação de cliente MBAM 2.0


Dependendo de quando você implantar o cliente Microsoft BitLocker Administration and Monitoring (MBAM), você pode habilitar a criptografia de unidade de disco BitLocker em um computador em sua organização antes de o usuário final receber o computador ou mais tarde. Para as topologias autônomas do MBAM e do Configuration Manager, você precisa definir configurações de política de grupo para MBAM.

Se você estiver usando a topologia autônoma do MBAM, é recomendável usar um sistema de implantação de software corporativo para implantar o software cliente do MBAM em computadores de usuário final.

Se você implantar o MBAM com a topologia do Configuration Manager, poderá usar o Configuration Manager para implantar o software cliente do MBAM em computadores de usuário final. No Configuration Manager, a instalação do MBAM cria um conjunto de computadores que MBAM pode gerenciar. Esta coleção inclui estações de trabalho e dispositivos que não têm um Trusted Platform Module (TPM), mas que executam o Windows 8.

**Observação**  Não há suporte para o Windows to go para instalações do Gerenciador de configurações integradas do MBAM se você estiver usando o Configuration Manager 2007.

 

## Implantando o cliente do MBAM para habilitar a criptografia do BitLocker após a distribuição do computador para usuários finais


Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager ou os serviços de domínio Active Directory (AD DS), para implantar os arquivos do Windows Installer da instalação do cliente do MBAM em computadores de destino. Para implantar o cliente do MBAM, você pode usar os arquivos 32 de MbamClientSetup.exe bits ou 64 bits ou arquivos MBAMClient.msi, que são fornecidos com o software do MBAM.

Quando você implanta o cliente MBAM após distribuir computadores para computadores cliente, os usuários finais são solicitados a criptografar o computador. Isso permite que o MBAM colete os dados, que incluem o PIN e a senha, e, em seguida, iniciar o processo de criptografia.

**Observação**  Nessa abordagem, os usuários que tiverem computadores com um chip TPM serão solicitados a ativar e inicializar o chip TPM se o chip não tiver sido ativado anteriormente.

 

## Usando o cliente MBAM para habilitar a criptografia do BitLocker antes da distribuição do computador para usuários finais


Nas organizações em que os computadores são recebidos e configurados de forma centralizada, e onde os computadores têm um chip TPM compatível, você pode instalar o cliente MBAM para gerenciar a criptografia do BitLocker em cada computador antes que os dados do usuário sejam gravados nele. A vantagem desse processo é que cada computador será compatível com a criptografia BitLocker. Esse método não depende da ação do usuário porque o administrador já criptografou o computador. Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.

Se a sua organização quiser usar o chip TPM para criptografar computadores, o administrador adicionará o protetor TPM para criptografar o volume do sistema operacional do computador. Se a sua organização quiser usar o chip TPM e um protetor de PIN, o administrador criptografará o volume do sistema operacional com o protetor TPM e os usuários selecionarão um PIN quando fizerem logon pela primeira vez. Se a sua organização decidir usar apenas o protetor de PIN, o administrador não precisará criptografar o volume primeiro. Quando os usuários fazem logon, o monitoramento e a administração do Microsoft BitLocker pedem que eles forneçam um PIN, ou um PIN e uma senha a serem usados em reinícios posteriores do computador.

**Observação**  A opção de protetor TPM exige que o administrador aceite o prompt do BIOS para ativar e inicializar o TPM antes que o computador seja entregue ao usuário.

 

## Tópicos relacionados


[Planejar a implantação do MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Implantando o Cliente do MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





