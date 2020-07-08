---
title: Notas de versão do App-V 5.0 SP3
description: Notas de versão do App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796221"
---
# Notas de versão do App-V 5.0 SP3


Estes são problemas conhecidos do Microsoft Application Virtualization (App-V) 5,0 SP3.

## Arquivos de servidor falha ao ser excluído após uma nova instalação do App-V 5,0 SP3 Server


Se você desinstalar o servidor App-V 5,0 SP1 e instalar o aplicativo App-V 5,0 SP3, a instalação falhará e a versão errada do servidor de gerenciamento será instalada. Os seguintes erros são exibidos:

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

O problema ocorre porque os arquivos do servidor não estão sendo excluídos ao desinstalar o App-V 5,0 SP1, portanto, o processo de instalação do App-V 5,0 SP3 emite erroneamente uma atualização em vez de uma nova instalação.

**Solução alternativa**: exclua a seguinte chave do registro antes de começar a instalar o App-V 5,0 SP3:

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## Consultar o AD DS pode fazer com que alguns aplicativos funcionem incorretamente


Quando você recebe pacotes atualizados consultando os serviços de domínio do Active Directory para associações de grupo atualizadas, isso pode fazer com que alguns aplicativos funcionem incorretamente se os aplicativos dependerem do token de acesso do usuário. Além disso, consultas frequentes em associação a grupos podem causar sobrecarregar o controlador de domínio. Para obter mais informações sobre os tokens de acesso do usuário, consulte [tokens do Access](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).

**Solução alternativa**: Aguarde até que o usuário faça logoff e logon novamente antes de consultar associações de grupo atualizadas. Não use a chave do registro, descrita em [pacote de hotfix 2 para Microsoft Application Virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087), para consultar associações de grupo atualizadas.






## Tópicos relacionados


[Sobre o App-V 5.0 SP3](about-app-v-50-sp3.md)

 

 





