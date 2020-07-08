---
title: Atualizando do MBAM 2.5 para o MBAM 2.5 SP1
description: Atualizando do MBAM 2.5 para o MBAM 2.5 SP1
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796076"
---
# Atualizando do MBAM 2.5 para o MBAM 2.5 SP1
Este tópico descreve o processo de atualização do servidor de administração e monitoramento do Microsoft BitLocker (MBAM) 2,5 e do cliente MBAM do 2,5 para o MBAM 2,5 SP1.

### Antes de começar
#### Baixe o lançamento de manutenção de maio de 2019
[Desktop Optimization Pack](https://www.microsoft.com/download/details.aspx?id=58345)

#### Verificar a instalação do documentaion
Verifique se você tem uma documentação atual do seu ambiente MBAM, incluindo todos os nomes de servidor, nomes de banco de dados, contas de serviço e suas senhas.

### Etapas de atualização
#### Etapas para atualizar o banco de dados do MBAM (SQL Server)
1. Usando o configurador MBAM; Remova a função relatórios do SQL Server ou onde o banco de dados do SSRS estiver hospedado. Dependendo do seu ambiente, ele pode ser o mesmo servidor ou um separado.
  > [!NOTE]
  > Você não verá uma opção para remover os bancos de dados; Isso é esperado.  
2. Instale o 2,5 SP1 (localizado com o MDOP-Microsoft Desktop Optimization Pack 2015 do site do centro de serviços de licenciamento por volume:  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. Não configurar no momento 
4. Usando o configurador MBAM; Adicionar novamente a função relatórios
5. Usando o configurador MBAM; Adicionar novamente a função de banco de dados SQL ao SQL Server
6. No final, você será avisado de que os bancos de bancos já existem e não foram criados, mas isso é esperado
7. Esse processo atualiza os bancos de dados existentes para a versão atual que está sendo instalada.              

#### Etapas para atualizar o servidor MBAM (executando MBAM e IIS)
1. Usando o configurador MBAM; remover os portais de administração e de autoatendimento do servidor IIS
2. Instalar o MBAM 2,5 SP1
3. Não configurar no momento  
4. Usando o configurador MBAM; Adicionar novamente os portais de administração e de autoatendimento ao servidor IIS 
5. Abra um prompt de comando elevado, digite **iisreset**e pressione Enter.
 
#### Etapas para atualizar os clientes do MBAM/pontos de extremidade
1. Desinstalar o agente do 2,5 dos pontos de extremidade do cliente
2. Instalar o agente do 2,5 SP1 nos pontos de extremidade do cliente
3. Empurre a atualização de cliente de pacote de maio de 2019 para clientes que executam o agente do 2,5 SP1 
4. Não é necessário desinstalar o cliente existente antes de instalar o pacote de maio de 2019.  
