---
title: Implantar Objetos de Política de Grupo no MBAM 1.0
description: Implantar Objetos de Política de Grupo no MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797881"
---
# Implantar Objetos de Política de Grupo no MBAM 1.0


Para implantar com êxito a administração e o monitoramento do Microsoft BitLocker (MBAM), você deve primeiro determinar as políticas de grupo que usará na implementação do MBAM. Para obter mais informações sobre as várias políticas disponíveis, consulte [planejando os requisitos da política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Depois de determinar as políticas que você vai usar, você deve usar o modelo de política de grupo do MBAM 1,0 para criar e implantar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política de MBAM.

## Instalar o modelo de política de grupo do MBAM 1,0


Além de fornecer recursos relacionados ao servidor do MBAM, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM. Você pode instalar esse modelo em qualquer computador que possa executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).

[Como instalar o Modelo de Política de Grupo do MBAM 1.0](how-to-install-the-mbam-10-group-policy-template.md)

## Implantar configurações de política de grupo do MBAM 1,0


Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização.

[Como editar Configurações GPO do MBAM 1.0](how-to-edit-mbam-10-gpo-settings.md)

## Exibir o painel de controle do MBAM no Windows


Como o MBAM oferece um painel de controle personalizado do MBAM que pode substituir o painel de controle padrão do Windows BitLocker, você também pode optar por ocultar o painel de controle padrão do BitLocker dos usuários finais usando a política de grupo.

[Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## Outros recursos para a implantação de objetos de política de grupo do MBAM 1,0


[Implantando o MBAM 1.0](deploying-mbam-10.md)

 

 





