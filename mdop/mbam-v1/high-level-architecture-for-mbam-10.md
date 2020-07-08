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
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799632"
---
# Arquitetura de alto nível para o MBAM 1.0


O Microsoft BitLocker Administration and Monitoring (MBAM) é uma solução de criptografia de dados cliente/servidor que pode ajudá-lo a simplificar a implantação e o provisionamento de BitLocker, melhorar a conformidade e os relatórios do BitLocker, além de reduzir os custos de suporte. O MBAM inclui os recursos descritos neste tópico.

Além disso, há um vídeo que fornece uma visão geral da arquitetura MBAM e da configuração do MBAM. Para obter mais informações, consulte [visão geral da arquitetura e implantação do MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## Visão geral da arquitetura


O diagrama a seguir exibe a arquitetura MBAM. A topologia de implantação do MBAM do servidor único é mostrada para apresentar os recursos do MBAM. No entanto, essa topologia de implantação do MBAM é recomendada apenas para ambientes de laboratório.

**Observação**  Pelo menos uma topologia de implantação do MBAM de três computadores é recomendada para uma implantação de produção. Para obter mais informações sobre topologias de implantação do MBAM, consulte [implantando a infraestrutura de servidor do MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

![topologia de implantação de servidor único do MBAM](images/mbam-1-server.jpg)

1.  **Servidor de administração e monitoramento**. O servidor de administração e monitoramento do MBAM é instalado em um servidor Windows e hospeda o site de administração e gerenciamento do MBAM e os serviços Web de monitoramento. O site de administração e gerenciamento do MBAM é usado para determinar o status de conformidade empresarial, para a atividade de auditoria, para gerenciar o recurso de hardware e para acessar dados de recuperação, como as chaves de recuperação do BitLocker. O servidor de administração e monitoramento se conecta aos seguintes bancos de dados e serviços:

    -   Recuperação e banco de dados de hardware. O banco de dados de recuperação e de hardware é instalado em um servidor baseado no Windows e na instância do SQLServer com suporte. Esse banco de dados armazena dados de recuperação e informações de hardware coletados de computadores cliente do MBAM.

    -   Banco de dados de auditoria e conformidade. O banco de dados de conformidade e auditoria está instalado em um servidor Windows e na instância do SQLServer com suporte. Esse banco de dados armazena dados de conformidade para computadores cliente do MBAM. Esses dados são usados principalmente para relatórios que são hospedados pelo SQL Server Reporting Services (SSRS).

    -   Relatórios de conformidade e auditoria. Os relatórios de conformidade e auditoria são instalados em um servidor baseado no Windows e na instância do SQLServer com suporte que tem o recurso SSRS instalado. Esses relatórios fornecem relatórios de administração e monitoramento do Microsoft BitLocker. Esses relatórios podem ser acessados a partir do site de administração e gerenciamento do MBAM ou diretamente do servidor SSRS.

2.  **Cliente MBAM**. O cliente de administração e monitoramento do Microsoft BitLocker executa as seguintes tarefas:

    -   Usa a política de grupo para impor a criptografia do BitLocker dos computadores cliente da empresa.

    -   Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

    -   Coleta informações de recuperação e informações de hardware sobre os computadores cliente.

    -   Coleta dados de conformidade do computador e passa os dados para o sistema de relatórios.

3.  **Modelo de política**. O modelo de política de grupo do MBAM é instalado em um servidor ou computador cliente compatível com Windows. Este modelo é usado para especificar as configurações de implementação do MBAM para a criptografia de unidade de disco BitLocker.

## Tópicos relacionados


[Introdução ao MBAM 1.0](getting-started-with-mbam-10.md)

 

 





