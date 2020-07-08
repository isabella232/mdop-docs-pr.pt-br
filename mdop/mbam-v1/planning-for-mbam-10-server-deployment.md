---
title: Planejar implantação de servidor MBAM 1.0
description: Planejar implantação de servidor MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795997"
---
# Planejar implantação de servidor MBAM 1.0


A infraestrutura de servidor de administração e monitoramento do Microsoft BitLocker (MBAM) depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da sua empresa.

## Planejando a implantação do MBAM Server


Os seguintes recursos de MBAM representam a infraestrutura de servidor para a implantação de servidor MBAM:

-   Recuperação e banco de dados de hardware

-   Banco de dados de auditoria e conformidade

-   Relatórios de conformidade e auditoria

-   Servidor de administração e monitoramento

Os bancos de dados e recursos do MBAM Server podem ser instalados em configurações diferentes, dependendo das suas necessidades de escalabilidade. Todos os recursos do MBAM Server podem ser instalados em um único servidor ou distribuídos entre vários servidores. Geralmente, recomendamos que você use uma configuração de três servidores ou cinco servidores para ambientes de produção, embora configurações de dois ou quatro servidores também possam ser usadas, dependendo das suas necessidades de computação.

**Observação**  Para obter mais informações sobre a escalabilidade de desempenho de MBAM e as topologias de implantação recomendadas, consulte o White Paper MBAM redimensionation and High-Availability Guide at <https://go.microsoft.com/fwlink/p/?LinkId=258314> .

 

Cada recurso MBAM tem pré-requisitos específicos. Para obter uma lista completa de pré-requisitos de recursos de servidor e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).

Além dos recursos do MBAM relacionados ao servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM. Este modelo pode ser instalado em qualquer computador que possa executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).

## Ordem de implantação de recursos do MBAM Server


Ao implantar os recursos do MBAM Server, instale os recursos na seguinte ordem:

1.  Recuperação e banco de dados de hardware

2.  Banco de dados de auditoria e conformidade

3.  Auditoria e relatórios de conformidade

4.  Servidor de administração e monitoramento

5.  Modelo de política

**Observação**  Mantenha o controle dos nomes dos computadores nos quais você instala cada recurso. Você usará essas informações durante todo o processo de instalação. Você pode imprimir e usar uma lista de verificação de implantação para ajudá-lo no processo de instalação. Para obter mais informações sobre a lista de verificação de implantação do MBAM, consulte [lista de verificação de implantação do MBAM 1,0](mbam-10-deployment-checklist.md).

 

## Tópicos relacionados


[Planejar a implantação do MBAM 1.0](planning-to-deploy-mbam-10.md)

[Implantando a infraestrutura do Servidor do MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





