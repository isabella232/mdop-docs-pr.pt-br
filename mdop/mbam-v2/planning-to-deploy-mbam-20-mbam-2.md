---
title: Planejar a implantação do MBAM 2.0
description: Planejar a implantação do MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799711"
---
# Planejar a implantação do MBAM 2.0


Você deve considerar várias configurações de implantação e pré-requisitos diferentes antes de criar seu plano de implantação do Microsoft BitLocker Administration and Monitoring (MBAM). Esta seção inclui informações que podem ajudá-lo a coletar as informações necessárias para formular um plano de implantação que melhor atenda às suas necessidades de negócios. Se você estiver instalando o MBAM com a topologia do Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) para obter informações adicionais sobre o planejamento.

## Examine as configurações compatíveis do MBAM 2,0


Depois de preparar seu ambiente de computação para a instalação de recursos do cliente e do servidor do MBAM, verifique se você revisar as configurações compatíveis para confirmar se os computadores nos quais está instalando o MBAM atendem aos requisitos mínimos de hardware e sistema operacional. Para obter mais informações sobre os pré-requisitos de implantação do MBAM, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).

[Configurações com suporte no MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)

## Plano para a implantação do servidor e do cliente do MBAM 2,0


A infraestrutura do MBAM Server depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa. Esses recursos podem ser instalados em uma configuração distribuída em vários servidores.

**Observação**  Uma instalação do MBAM em um único servidor é recomendada apenas para ambientes de laboratório.

 

O cliente MBAM permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software corporativo ou instalando o agente do cliente em computadores cliente como parte do processo de imagem inicial.

Com o MBAM, você pode criptografar um computador em sua organização antes de o usuário final receber o computador ou depois de usar a política de grupo.

[Planejar implantação de servidor MBAM 2.0](planning-for-mbam-20-server-deployment-mbam-2.md)

[Planejar implantação de cliente MBAM 2.0](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Outros recursos para o planejamento do MBAM


[Planejamento para o MBAM 2.0](planning-for-mbam-20-mbam-2.md)

 

 





