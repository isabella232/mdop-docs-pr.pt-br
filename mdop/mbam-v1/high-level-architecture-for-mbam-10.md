---
title: Arquitetura de alto nível para o MBAM 1.0
description: Arquitetura de alto nível para o MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d06c7bd801a9dd63916d310af75e88a307e7226a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910406"
---
# <a name="high-level-architecture-for-mbam-10"></a>Arquitetura de alto nível para o MBAM 1.0


O Microsoft BitLocker Administration and Monitoring (MBAM) é uma solução de criptografia de dados de cliente/servidor que pode ajudá-lo a simplificar o provisionamento e a implantação do BitLocker, melhorar a conformidade e o relatório do BitLocker e reduzir os custos de suporte. O MBAM inclui os recursos descritos neste tópico.

Além disso, há um vídeo que fornece uma visão geral da arquitetura do MBAM e da Instalação do MBAM. Para obter mais informações, [consulte MbaM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## <a name="architecture-overview"></a>Visão geral da arquitetura


O diagrama a seguir exibe a arquitetura MBAM. A topologia de implantação do MBAM de servidor único é mostrada para introduzir os recursos do MBAM. No entanto, essa topologia de implantação do MBAM é recomendada apenas para ambientes de laboratório.

**Observação**  
Pelo menos uma topologia de implantação de MBAM de três computadores é recomendada para uma implantação de produção. Para obter mais informações sobre topologias de implantação do MBAM, consulte [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).

 

![topologia de implantação de servidor único do mbam.](images/mbam-1-server.jpg)

1.  **Servidor de Administração e Monitoramento.** O MbaM Administration and Monitoring Server é instalado em um servidor Windows e hospeda o site de Administração e Gerenciamento do MBAM e os serviços Web de monitoramento. O site administração e gerenciamento do MBAM é usado para determinar o status de conformidade da empresa, para auditar a atividade, para gerenciar a funcionalidade de hardware e para acessar dados de recuperação, como as chaves de recuperação do BitLocker. O Servidor de Administração e Monitoramento se conecta aos seguintes bancos de dados e serviços:

    -   Banco de dados de recuperação e hardware. O banco de dados de Recuperação e Hardware é instalado em um servidor baseado em Windows e tem suporte SQL Server instância. Esse banco de dados armazena dados de recuperação e informações de hardware coletados de computadores cliente MBAM.

    -   Banco de dados de conformidade e auditoria. O Banco de Dados de Conformidade e Auditoria é instalado em um servidor Windows e tem suporte SQL Server instância. Esse banco de dados armazena dados de conformidade para computadores cliente MBAM. Esses dados são usados principalmente para relatórios hospedados pelo SQL Server Reporting Services (SSRS).

    -   Relatórios de conformidade e auditoria. Os Relatórios de Conformidade e Auditoria são instalados em um servidor Windows com suporte SQL Server instância que tem o recurso SSRS instalado. Esses relatórios fornecem relatórios de Administração e Monitoramento do Microsoft BitLocker. Esses relatórios podem ser acessados no site administração e gerenciamento do MBAM ou diretamente do Servidor SSRS.

2.  **Cliente MBAM**. O Microsoft BitLocker Administration and Monitoring Client executa as seguintes tarefas:

    -   Usa a Política de Grupo para impor a criptografia BitLocker de computadores cliente na empresa.

    -   Coleta a chave de recuperação para os três tipos de unidade de dados do BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades USB (dados removíveis).

    -   Coleta informações de recuperação e informações de hardware sobre os computadores cliente.

    -   Coleta dados de conformidade para o computador e passa os dados para o sistema de relatórios.

3.  **Modelo de Política**. O modelo de Política de Grupo do MBAM é instalado em um servidor Windows ou computador cliente com suporte. Este modelo é usado para especificar as configurações de implementação do MBAM para criptografia de unidade BitLocker.

## <a name="related-topics"></a>Tópicos relacionados


[Introdução ao MBAM 1.0](getting-started-with-mbam-10.md)

 

 





