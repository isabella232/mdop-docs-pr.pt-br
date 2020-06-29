---
title: Implantação da infraestrutura de servidor do MBAM 2.0
description: Implantação da infraestrutura de servidor do MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799536"
---
# Implantação da infraestrutura de servidor do MBAM 2.0


Os recursos de servidor de administração e monitoramento do Microsoft BitLocker (MBAM) para a topologia autônoma podem ser instalados em diferentes configurações em dois ou mais servidores em um ambiente de produção. A configuração recomendada é de dois servidores para um ambiente de produção, dependendo dos requisitos de escalabilidade. Use um único servidor para uma instalação do MBAM somente em ambientes de teste. Para obter mais informações sobre como planejar a implantação de recursos do servidor MBAM, consulte [planejando a implantação do MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md).

O diagrama a seguir mostra um exemplo de como você pode configurar a implantação de MBAM de dois servidores recomendada. Essa configuração oferece suporte a até 200.000 clientes do MBAM em um ambiente de produção. Os recursos do servidor e os bancos de dados na imagem da arquitetura são descritos na seção a seguir e estão listados no computador ou servidor onde recomendamos que você os instale.

![MBAM 2 2-topologia de implantação do servidor](images/mbam2-3-servers.gif)

## Servidor de administração e monitoramento


Os recursos a seguir estão instalados neste servidor:

-   **Servidor de administração e monitoramento**. O recurso do servidor de administração e monitoramento é instalado em um servidor Windows e consiste no site de suporte técnico e nos serviços Web de monitoramento.

-   **Portal de autoatendimento**. O portal de autoatendimento está instalado em um servidor Windows. O portal de autoatendimento permite que os usuários finais em computadores cliente façam logon independentemente em um site, onde eles podem obter uma chave de recuperação para recuperar um volume do BitLocker bloqueado.

## Servidor de banco de dados


Os recursos a seguir estão instalados neste servidor:

-   **Banco de dados de recuperação**. O banco de dados de recuperação está instalado em um servidor Windows e uma instância com suporte do Microsoft SQLServer. Esse banco de dados armazena dados de recuperação coletados de computadores cliente do MBAM.

-   **Banco de dados de auditoria e conformidade**. O banco de dados de conformidade e auditoria está instalado em um servidor Windows e uma instância com suporte do SQLServer. Esse banco de dados armazena dados de conformidade para computadores cliente do MBAM. Esses dados são usados principalmente para relatórios que os SQL Server Reporting Services (SSRS) hospedam.

-   **Relatórios de conformidade e auditoria**. Os relatórios de conformidade e auditoria são instalados em um servidor Windows e uma instância com suporte do SQLServer que tem o recurso do SQL Server Reporting Services (SSRS) instalado. Esses relatórios fornecem relatórios do MBAM que você pode acessar a partir do site do suporte técnico ou diretamente do servidor do SSRS.

## Estação de trabalho de gerenciamento


O recurso a seguir está instalado na estação de trabalho de gerenciamento, que pode ser um servidor Windows ou um computador cliente.

-   **Modelo de política**. O modelo de política consiste em políticas de grupo que definem as configurações de implementação de MBAM para a criptografia de unidade de disco BitLocker. Você pode instalar o modelo de política em qualquer servidor ou estação de trabalho, mas ele geralmente está instalado em uma estação de trabalho de gerenciamento, que é um computador cliente ou servidor com suporte. A estação de trabalho não precisa ser um computador dedicado.

## <a href="" id="---------mbam-client"></a> Cliente MBAM


O cliente do MBAM está instalado em um computador com Windows e tem as seguintes características:

-   Usa a política de grupo para impor a criptografia de unidade de disco BitLocker dos computadores cliente da empresa.

-   Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

-   Coleta dados de conformidade do computador e passa os dados para o sistema de relatórios.

## Outros recursos para a implantação de recursos do MBAM 2,0 Server


[Implantando o MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





