---
title: Planejar implantação de servidor MBAM 2.0
description: Planejar implantação de servidor MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796043"
---
# Planejar implantação de servidor MBAM 2.0


A infraestrutura de servidor de administração e monitoramento do Microsoft BitLocker (MBAM) depende de um conjunto de recursos do servidor que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa. Se você estiver instalando a administração e o monitoramento do Microsoft BitLocker com a topologia do Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

**Observação**  As instalações do Microsoft BitLocker Administration and Monitoring em um único servidor são recomendadas apenas para ambientes de teste.

 

## Planejando a implantação do MBAM Server


A infraestrutura para uma implantação do MBAM Server inclui os seguintes recursos:

-   Banco de dados de recuperação

-   Banco de dados de auditoria e conformidade

-   Relatórios de conformidade e auditoria

-   Portal de autoatendimento

-   Servidor de administração e monitoramento

-   Modelo de política de grupo MBAM

Os bancos de dados e recursos do MBAM Server podem ser instalados em configurações diferentes, dependendo dos requisitos de redimensionamento. Todos os recursos do MBAM Server podem ser instalados em um único servidor ou distribuídos entre vários servidores. Recomendamos que você use uma configuração de dois servidores para ambientes de produção, embora configurações de dois a quatro servidores também possam ser usadas, dependendo de suas necessidades de computação.

Cada recurso MBAM tem pré-requisitos específicos. Para obter uma lista completa de pré-requisitos de recursos de servidor e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md).

Além dos recursos do MBAM relacionados ao servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM. O modelo contém configurações de objeto de política de grupo (GPO) que você configura para gerenciar a criptografia de unidade de disco BitLocker na empresa. Você pode instalar esse modelo em qualquer computador que possa executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).

Ao planejar a implantação do MBAM Server, considere que as chaves de recuperação do BitLocker no MBAM devem ser somente para uso único, após o vencimento das chaves de recuperação. Para que as chaves expirem após o uso, elas devem ser recuperadas por meio do portal de suporte técnico ou do portal de autoatendimento.

## Ordem de implantação de recursos do MBAM Server


Para implantar recursos do MBAM em vários servidores, você precisa instalar os recursos na seguinte ordem:

1.  Banco de dados de recuperação

2.  Banco de dados de auditoria e conformidade

3.  Auditoria e relatórios de conformidade

4.  Portal de autoatendimento

5.  Servidor de administração e monitoramento

6.  Modelo de política de grupo MBAM

**Observação**  Mantenha o controle dos nomes dos computadores nos quais você instala cada recurso. Você precisa usar essas informações em todo o processo de instalação. Você pode imprimir e usar uma lista de verificação de implantação para ajudar nesse esforço. Para obter mais informações sobre a lista de verificação de implantação do MBAM, consulte [lista de verificação de implantação do MBAM 2,0](mbam-20-deployment-checklist-mbam-2.md).

 

## Tópicos relacionados


[Planejar a implantação do MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Implantação da infraestrutura de servidor do MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





