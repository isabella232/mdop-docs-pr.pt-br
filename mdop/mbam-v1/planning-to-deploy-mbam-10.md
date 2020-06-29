---
title: Planejar a implantação do MBAM 1.0
description: Planejar a implantação do MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799222"
---
# Planejar a implantação do MBAM 1.0


Você deve considerar várias configurações e pré-requisitos de implantação diferentes antes de criar seu plano de implantação do Microsoft BitLocker Administration and Monitoring (MBAM) 1,0. Esta seção inclui informações que podem ajudá-lo a obter as informações que você precisa ter para formular um plano de implantação que melhor atenda às suas necessidades de negócios.

## Examine as configurações compatíveis do MBAM 1,0


Depois de preparar o ambiente de computação para a instalação de recursos cliente e servidor do MBAM, verifique se você revisar as informações de configuração com suporte para o MBAM para confirmar se os computadores nos quais você instala MBAM atendem aos requisitos mínimos de hardware e sistema operacional. Para obter mais informações sobre os pré-requisitos de implantação do MBAM, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md).

[Configurações com suporte no MBAM 1.0](mbam-10-supported-configurations.md)

## Plano para a implantação do servidor e do cliente do MBAM 1,0


A infraestrutura do MBAM Server depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa. Esses recursos podem ser instalados em um único servidor ou distribuídos entre vários servidores.

O cliente MBAM permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de ferramentas como os serviços de domínio do Active Directory ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.

Com o MBAM, você pode criptografar um computador em sua organização antes de o usuário final receber o computador ou depois, usando a política de grupo. Você pode usar um ou os dois métodos em sua organização. Se optar por usar os dois métodos, você poderá melhorar a conformidade, o relatório e o suporte à recuperação de chave.

[Planejar implantação de servidor MBAM 1.0](planning-for-mbam-10-server-deployment.md)

[Planejar implantação de cliente MBAM 1.0](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Outros recursos para o planejamento do MBAM


-   [Planejamento para o MBAM 1.0](planning-for-mbam-10.md)

 

 





