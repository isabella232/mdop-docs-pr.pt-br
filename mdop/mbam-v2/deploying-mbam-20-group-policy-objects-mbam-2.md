---
title: Implantar Objetos de Política de Grupo no MBAM 2.0
description: Implantar Objetos de Política de Grupo no MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799283"
---
# Implantar Objetos de Política de Grupo no MBAM 2.0


Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), primeiro você precisa determinar as políticas de grupo que usará na implementação da administração e do monitoramento do Microsoft BitLocker. Consulte [planejando os requisitos da política de grupo do MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obter mais informações sobre as diferentes políticas disponíveis. Depois de determinar as políticas que você vai usar, você deve criar e implantar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política para o MBAM usando o modelo de política de grupo MBAM 2,0.

## Instalar o modelo de política de grupo do MBAM 2,0


Além dos recursos de administração e monitoramento do Microsoft BitLocker relacionados a servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM. Este modelo pode ser instalado em qualquer computador capaz de executar o GPMC (console de gerenciamento de política de grupo) ou no AGPM (gerenciamento avançado de política de grupo).

[Como instalar o Modelo de Política de Grupo do MBAM 2.0](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## Implantar configurações de política de grupo do MBAM 2,0


Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização.

[Como editar Configurações GPO do MBAM 2.0](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## Exibir o painel de controle do MBAM no Windows


Como o MBAM oferece um painel de controle personalizado do MBAM que pode substituir o painel de controle padrão do Windows BitLocker, você também pode optar por ocultar o painel de controle padrão do BitLocker dos usuários finais usando a política de grupo.

[Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## Outros recursos para a implantação de objetos de política de grupo do MBAM 2,0


[Implantando o MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





