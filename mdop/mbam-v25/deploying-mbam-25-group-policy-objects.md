---
title: Implantando objetos de Política de Grupo do MBAM 2.5
description: Implantando objetos de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799462"
---
# Implantando objetos de Política de Grupo do MBAM 2.5


Para implantar o MBAM, você precisa definir configurações de política de grupo que definem as configurações de implementação de MBAM para a criptografia de unidade de disco BitLocker. Para concluir essa tarefa, você deve copiar os modelos de política de grupo do MBAM para um servidor ou uma estação de trabalho que sejam capazes de executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) e, em seguida, editar as configurações.

**Importante**  Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente. Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.

 

## Copiando os modelos de Política de Grupo do MBAM 2.5


Antes de instalar o cliente do MBAM, você deve copiar objetos de política de grupo (GPOs) específicos do MBAM para a estação de trabalho de gerenciamento. Esses GPOs definem as configurações de implementação do MBAM para a criptografia de unidade de disco BitLocker. Você pode copiar os modelos de política de grupo para qualquer servidor ou estação de trabalho que seja compatível com Windows Server ou computador cliente e que possa executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM).

[Copiando os modelos de Política de Grupo do MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

## Editando MBAM 2,0 configurações do GPO


Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização. Para exibir e criar GPOs, você deve ter o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) instalado.

[Editando as configurações de Política de Grupo do MBAM 2.5](editing-the-mbam-25-group-policy-settings.md)

## Mostrar ou ocultar o painel de controle do MBAM no painel de controle do Windows


Como o MBAM oferece um painel de controle personalizado do MBAM que pode substituir o painel de controle padrão do Windows BitLocker, você também pode optar por mostrar ou ocultar o painel de controle padrão do BitLocker dos usuários finais usando as configurações de política de grupo.

[Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## Outros recursos para a implantação de objetos de política de grupo do MBAM 2,0


[Implantando o MBAM 2.5](deploying-mbam-25.md)

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





