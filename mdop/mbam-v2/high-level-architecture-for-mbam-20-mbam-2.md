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
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799525"
---
# Arquitetura de alto nível para o MBAM 2.0


O Microsoft BitLocker Administration and Monitoring (MBAM) é uma solução cliente/servidor que pode ajudá-lo a simplificar o provisionamento e a implantação do BitLocker, melhorar a conformidade e os relatórios sobre o BitLocker e reduzir os custos de suporte. A administração e o monitoramento do Microsoft BitLocker incluem os recursos descritos neste tópico.

A administração e o monitoramento do Microsoft BitLocker podem ser implantados na topologia autônoma ou em uma topologia integrada ao Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012 ConfigurationManager. Este tópico descreve a arquitetura para a topologia autônoma. Para obter informações sobre a implantação na topologia do Gerenciador de configurações integradas, consulte [usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md).

O diagrama a seguir mostra a arquitetura recomendada MBAM para um ambiente de produção, que consiste em dois servidores e uma estação de trabalho de gerenciamento. Essa arquitetura dá suporte a até 200.000 clientes MBAM. Os recursos do servidor e os bancos de dados na imagem da arquitetura são descritos na seção a seguir e estão listados no computador ou servidor onde recomendamos que você os instale.

**Observação**  Uma arquitetura de servidor único deve ser usada somente em ambientes de teste.

 

![MBAM 2 2-topologia de implantação do servidor](images/mbam2-3-servers.gif)

## Servidor de administração e monitoramento


Os recursos a seguir estão instalados neste servidor:

-   **Servidor de administração e monitoramento**. O recurso servidor de administração e monitoramento é instalado em um servidor Windows e consiste no site de administração e monitoramento, que inclui os relatórios e o portal de suporte técnico e os serviços Web de monitoramento.

-   **Portal de autoatendimento**. O portal de autoatendimento está instalado em um servidor Windows. O portal de autoatendimento permite que os usuários finais em computadores cliente façam logon independentemente em um site, onde eles podem obter uma chave de recuperação para recuperar um volume do BitLocker bloqueado.

## Servidor de banco de dados


Os recursos a seguir estão instalados neste servidor:

-   **Banco de dados de recuperação**. O banco de dados de recuperação está instalado em um servidor Windows e uma instância com suporte do Microsoft SQLServer. Esse banco de dados armazena dados de recuperação coletados de computadores cliente do MBAM.

-   **Banco de dados de auditoria e conformidade**. O banco de dados de conformidade e auditoria está instalado em um servidor Windows e uma instância com suporte do SQLServer. Esse banco de dados armazena dados de conformidade para computadores cliente do MBAM. Esses dados são usados principalmente para relatórios que os SQL Server Reporting Services (SSRS) hospedam.

-   **Relatórios de conformidade e auditoria**. Os relatórios de conformidade e auditoria são instalados em um servidor Windows e uma instância com suporte do SQLServer que tem o recurso do SQL Server Reporting Services (SSRS) instalado. Esses relatórios fornecem relatórios do MBAM que você pode acessar a partir do site de administração e monitoramento ou diretamente do servidor SSRS.

## Estação de trabalho de gerenciamento


O recurso a seguir está instalado na estação de trabalho de gerenciamento, que pode ser um servidor Windows ou um computador cliente.

-   **Modelo de política**. O modelo de política consiste em configurações de política de grupo que definem as configurações de implementação MBAM para a criptografia de unidade de disco BitLocker. Você pode instalar o modelo de política em qualquer servidor ou estação de trabalho, mas ele geralmente está instalado em uma estação de trabalho de gerenciamento, que é um computador cliente ou servidor com suporte. A estação de trabalho não precisa ser um computador dedicado.

## <a href="" id="---------mbam-client"></a> Cliente MBAM


O cliente do MBAM está instalado em um computador com Windows e tem as seguintes características:

-   Usa a política de grupo para impor a criptografia de unidade de disco BitLocker dos computadores cliente da empresa.

-   Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

-   Coleta dados de conformidade do computador e passa os dados para o sistema de relatórios.

## Tópicos relacionados


[Introdução ao MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





