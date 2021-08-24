---
title: Arquitetura de alto nível para o MBAM 2.0
description: Arquitetura de alto nível para o MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19480b5797362e6e4119fff9a14afd9d5a74d98
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910496"
---
# <a name="high-level-architecture-for-mbam-20"></a>Arquitetura de alto nível para o MBAM 2.0


O Microsoft BitLocker Administration and Monitoring (MBAM) é uma solução de cliente/servidor que pode ajudá-lo a simplificar o provisionamento e a implantação do BitLocker, melhorar a conformidade e o relatório sobre o BitLocker e reduzir os custos de suporte. O Microsoft BitLocker Administration and Monitoring inclui os recursos descritos neste tópico.

A Administração e o Monitoramento do Microsoft BitLocker podem ser implantados na topologia autônomo ou em uma topologia integrada ao Microsoft System Center Configuration Manager 2007 ou ao Microsoft System Center 2012 Configuration Manager. Este tópico descreve a arquitetura da topologia autônomo. Para obter informações sobre como implantar na topologia integrada do Configuration Manager, consulte [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).

O diagrama a seguir mostra a arquitetura recomendada do MBAM para um ambiente de produção, que consiste em dois servidores e uma estação de trabalho de gerenciamento. Essa arquitetura dá suporte a até 200.000 clientes MBAM. Os recursos e bancos de dados do servidor na imagem da arquitetura são descritos na seção a seguir e estão listados no computador ou servidor em que recomendamos instalá-los.

**Observação**  
Uma arquitetura de servidor único deve ser usada somente em ambientes de teste.

 

![topologia de implantação de dois servidores do mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Servidor de Administração e Monitoramento


Os seguintes recursos são instalados neste servidor:

-   **Servidor de Administração e Monitoramento.** O recurso Servidor de Administração e Monitoramento é instalado em um servidor Windows e consiste no site de Administração e Monitoramento, que inclui os relatórios e o Portal do Help Desk e os serviços Web de monitoramento.

-   **Portal de Autoatendneto**. O Self-Service Portal é instalado em um servidor Windows servidor. O Self-Service Portal permite que os usuários finais em computadores clientes faça logoff independentemente em um site, onde eles podem obter uma chave de recuperação para recuperar um volume bloqueado do BitLocker.

## <a name="database-server"></a>Servidor de Banco de Dados


Os seguintes recursos são instalados neste servidor:

-   **Banco de Dados de Recuperação**. O Banco de Dados de Recuperação é instalado em um servidor Windows e uma instância de Microsoft SQL Server. Esse banco de dados armazena dados de recuperação coletados de computadores clientes do MBAM.

-   **Banco de Dados de Conformidade e Auditoria.** O Banco de Dados de Conformidade e Auditoria é instalado em um servidor Windows e uma instância de SQL Server. Esse banco de dados armazena dados de conformidade para computadores cliente MBAM. Esses dados são usados principalmente para relatórios que SQL Server Reporting Services hosts (SSRS).

-   **Relatórios de conformidade e auditoria.** Os Relatórios de Conformidade e Auditoria são instalados em um servidor Windows e uma instância de SQL Server com suporte que tem o recurso SQL Server Reporting Services (SSRS) instalado. Esses relatórios fornecem relatórios mbam que você pode acessar a partir do site de Administração e Monitoramento ou diretamente do servidor SSRS.

## <a name="management-workstation"></a>Estação de Trabalho de Gerenciamento


O recurso a seguir é instalado na estação de trabalho Gerenciamento, que pode ser um servidor Windows ou um computador cliente.

-   **Modelo de Política**. O Modelo de Política consiste em configurações de Política de Grupo que definem as configurações de implementação do MBAM para criptografia de unidade BitLocker. Você pode instalar o modelo de Política em qualquer servidor ou estação de trabalho, mas ele é comumente instalado em uma estação de trabalho de gerenciamento, que é um servidor Windows servidor ou computador cliente com suporte. A estação de trabalho não precisa ser um computador dedicado.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> Cliente MBAM


O Cliente MBAM é instalado em um computador Windows e tem as seguintes características:

-   Usa a Política de Grupo para impor a criptografia de unidade do BitLocker de computadores cliente na empresa.

-   Coleta a chave de recuperação para os três tipos de unidade de dados do BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades USB (dados removíveis).

-   Coleta dados de conformidade para o computador e passa os dados para o sistema de relatórios.

## <a name="related-topics"></a>Tópicos relacionados


[Introdução ao MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





