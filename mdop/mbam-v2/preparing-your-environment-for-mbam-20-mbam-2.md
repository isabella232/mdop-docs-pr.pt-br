---
title: Como preparar seu ambiente para o MBAM 2.0
description: Como preparar seu ambiente para o MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799706"
---
# Como preparar seu ambiente para o MBAM 2.0


Antes de iniciar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), você deve verificar se atendeu os pré-requisitos para instalar o produto. Quando você sabe o que os pré-requisitos estão antecipadamente, você pode implantar o produto com eficiência e habilitar seus recursos para que ele dê suporte aos objetivos de negócios da sua organização de forma mais eficiente.

Se você estiver implantando a administração e o monitoramento do Microsoft BitLocker com o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

## Revisar os pré-requisitos de implantação do MBAM 2,0


O cliente MBAM e cada um dos recursos do servidor MBAM têm pré-requisitos específicos que devem ser atendidos para que possam ser instalados com êxito.

Para garantir a instalação bem-sucedida de clientes do MBAM e recursos do MBAM Server, certifique-se de que os computadores especificados para a instalação do MBAM cliente ou do MBAM Server estejam adequadamente preparados para a instalação do MBAM.

**Observação**  MBAM a instalação verifica se todos os pré-requisitos são atendidos antes do início da instalação. Se todos os pré-requisitos não forem atendidos, a instalação não será bem-sucedida.

 

[Pré-requisitos para implantação do MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

## Plano para requisitos de política de grupo do MBAM 2,0


Antes que o MBAM possa gerenciar clientes na empresa, você deve definir a política de grupo para os requisitos de criptografia do seu ambiente.

**Importante**  O MBAM não funcionará com políticas para criptografia de unidade de disco BitLocker autônoma. As configurações de política de grupo devem ser definidas para MBAM, ou a criptografia e a imposição do BitLocker falharão.

 

[Planejar Requisitos de Política de Grupo do MBAM 2.0](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## Planejar as funções de administrador do MBAM 2,0


As funções de administrador do MBAM são gerenciadas por grupos locais criados pela configuração do MBAM ao instalar o servidor de administração e monitoramento do BitLocker, o recurso de relatórios de auditoria e conformidade e o banco de dados de status de conformidade e auditoria.

A Associação das funções de administração e administração do Microsoft BitLocker pode ser gerenciada pela criação de grupos de segurança no ActiveDirectoryDomainServices, adição das contas de administrador apropriadas a esses grupos e, em seguida, adição desses grupos de segurança aos grupos locais de administração e monitoramento do BitLocker. Para obter mais informações, consulte [como gerenciar as funções de administrador do MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).

## Outros recursos para o planejamento do MBAM


[Planejamento para o MBAM 2.0](planning-for-mbam-20-mbam-2.md)

[Configurações com suporte no MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)

 

 





