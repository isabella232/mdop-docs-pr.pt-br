---
title: Preparando seu ambiente para o MBAM 1.0
description: Preparando seu ambiente para o MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799223"
---
# Preparando seu ambiente para o MBAM 1.0


Antes de começar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), certifique-se de que você atendeu aos pré-requisitos necessários para instalar o produto. Se você souber os pré-requisitos antecipadamente, poderá implantar eficientemente o produto e habilitar seus recursos, o que pode dar suporte a objetivos comerciais da sua organização com mais eficiência.

## Revisar os pré-requisitos de implantação do MBAM 1,0


O cliente MBAM e cada um dos recursos do servidor MBAM têm pré-requisitos específicos que devem ser atendidos para que possam ser instalados com êxito.

Para garantir a instalação bem-sucedida dos clientes do MBAM e dos recursos do MBAM Server, você deve planejar a garantia de que os computadores especificados para MBAM cliente ou MBAM instalação de recursos de servidor estejam adequadamente preparados para a instalação do MBAM.

**Observação**  A instalação do MBAM verifica se todos os pré-requisitos são atendidos antes do início da instalação. Se não forem atendidas, a instalação falhará.

 

[Pré-requisitos para implantação do MBAM 1.0](mbam-10-deployment-prerequisites.md)

## Plano para requisitos de política de grupo do MBAM 1,0


Antes que o MBAM possa gerenciar clientes na empresa, você deve definir a política de grupo para os requisitos de criptografia do seu ambiente.

**Importante**  O MBAM não funcionará com políticas para criptografia de unidade de disco BitLocker autônoma. A política de grupo deve ser definida para MBAM; caso contrário, haverá falha na criptografia e na imposição do BitLocker.

 

[Planejar Requisitos de Política de Grupo do MBAM 1.0](planning-for-mbam-10-group-policy-requirements.md)

## Planejar as funções de administrador do MBAM 1,0


As funções de administrador do MBAM são gerenciadas por grupos locais criados pela configuração do MBAM quando você instala o seguinte: servidor de administração e monitoramento do BitLocker, recurso de relatórios de auditoria e conformidade e banco de dados de status de auditoria e conformidade.

A associação de funções de MBAM pode ser gerenciada com mais eficiência se você criar grupos de segurança no ActiveDirectoryDomainServices, adicionar as contas de administrador apropriadas a esses grupos e, em seguida, adicionar esses grupos de segurança aos grupos locais do MBAM. Para obter mais informações, consulte [como gerenciar as funções de administrador do MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).

[Planejamento para Funções de Administrador do MBAM 1.0](planning-for-mbam-10-administrator-roles.md)

## Outros recursos para o planejamento do MBAM


[Planejamento para o MBAM 1.0](planning-for-mbam-10.md)

 

 





