---
title: Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager
description: Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796031"
---
# Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager


Se você estiver instalando o recurso de integração do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando o recurso de integração do System Center Configuration Manager, será necessário concluir os pré-requisitos descritos neste tópico, além daqueles dos [pré-requisitos do MBAM 2,5 Server para topologias autônomas e de integração do Configuration Manager](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md). Você também deve criar ou modificar arquivos. mof necessários para a topologia de integração do Configuration Manager.

## Pré-requisitos para o recurso de integração do Configuration Manager


Se você estiver configurando o MBAM com a topologia de integração do System Center Configuration Manager, será necessário concluir pré-requisitos adicionais necessários para o Configuration Manager.

[Pré-requisitos para o recurso de integração do Configuration Manager](prerequisites-for-the-configuration-manager-integration-feature.md)

## Editar o arquivo Configuration. mof


Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo Configuration. MOF para SystemCenter2012 ConfigurationManager e o Microsoft System Center Configuration Manager 2007.

[Edite o arquivo Configuration.mof](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Criar ou editar o arquivo SMS \ _def. mof


Para permitir que os computadores cliente relatem os detalhes de conformidade do BitLocker nos relatórios do Gerenciador de configuração do MBAM, você precisa criar ou editar o arquivo SMS \ _def. mof. Se estiver usando o SystemCenter2012 ConfigurationManager, você deve criar o arquivo. No Configuration Manager 2007, o arquivo já existe, portanto, você precisa editar, mas não substituir, o arquivo existente.

[Criar ou editar o arquivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file-mbam-25.md)


## Tópicos relacionados


[Preparando seu ambiente para o MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Configurações com suporte no MBAM 2.5](mbam-25-supported-configurations.md)

[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




