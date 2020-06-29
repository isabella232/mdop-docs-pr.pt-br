---
title: Planejando a implantação do MBAM 2.5
description: Planejando a implantação do MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799923"
---
# Planejando a implantação do MBAM 2.5


Você deve considerar várias configurações de implantação e pré-requisitos diferentes antes de criar seu plano de implantação do Microsoft BitLocker Administration and Monitoring (MBAM). Esta seção inclui informações que podem ajudá-lo a coletar as informações necessárias para formular um plano de implantação que melhor atenda às suas necessidades de negócios.

## Examine as configurações compatíveis do MBAM 2,5


Depois de preparar seu ambiente de computação para a implantação de recursos do cliente e do servidor do MBAM, verifique se você revisar as configurações compatíveis para confirmar se os computadores nos quais está instalando o MBAM atendem aos requisitos mínimos de hardware e sistema operacional. Para obter mais informações sobre os pré-requisitos de implantação do MBAM, consulte [pré-requisitos de implantação do MBAM 2,5](mbam-25-deployment-prerequisites.md).

[Configurações com suporte no MBAM 2.5](mbam-25-supported-configurations.md)

## Plano para a implantação do servidor e do cliente do MBAM 2,5


A infraestrutura do MBAM Server depende de um conjunto de recursos do servidor que podem ser configurados em um ou mais computadores servidor, de acordo com os requisitos da empresa. Esses recursos podem ser configurados em uma configuração distribuída em vários servidores.

**Observação**  Uma instalação do MBAM em um único servidor é recomendada apenas para ambientes de laboratório.

 

O cliente MBAM permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software corporativo ou instalando o cliente em computadores cliente como parte do processo de imagem inicial.

Com o MBAM, você pode criptografar um computador em sua organização antes de o usuário final receber o computador ou depois de usar a política de grupo.

[Planejando a implantação de servidor do MBAM 2.5](planning-for-mbam-25-server-deployment.md)

[Planejando a implantação do cliente do MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Outros recursos para o planejamento do MBAM


[Planejamento do MBAM 2.5](planning-for-mbam-25.md)

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





