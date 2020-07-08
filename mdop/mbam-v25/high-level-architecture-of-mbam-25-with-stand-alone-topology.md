---
title: Arquitetura de alto nível do MBAM 2.5 com topologia autônoma
description: Arquitetura de alto nível do MBAM 2.5 com topologia autônoma
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799896"
---
# Arquitetura de alto nível do MBAM 2.5 com topologia autônoma


Este tópico descreve a arquitetura recomendada para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia autônoma do Configuration Manager. Nessa topologia, o MBAM é implantado como um produto autônomo. Você também pode implantar o MBAM com a topologia de integração do Configuration Manager, que integra o MBAM com o Configuration Manager. Para obter mais informações, consulte [arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Para obter uma lista das versões com suporte do software mencionadas neste tópico, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).

**Observação**  Recomendamos que você use uma arquitetura de servidor único somente em ambientes de teste.

 

## Número recomendado de servidores e número de clientes com suporte


O número recomendado de servidores e o número de clientes com suporte em um ambiente de produção é o seguinte:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquitetura recomendada em um ambiente de produção</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Número de servidores e outros computadores</p></td>
<td align="left"><p>Dois servidores</p>
<p>Uma estação de trabalho</p></td>
</tr>
<tr class="even">
<td align="left"><p>Número de computadores cliente com suporte</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Arquitetura de alto nível MBAM recomendada com a topologia autônoma


O diagrama e a tabela a seguir descrevem a arquitetura recomendada de dois níveis e dois servidores para o MBAM com a topologia autônoma. MBAM implantações de várias florestas exigem confiança unidirecional ou bidirecional. As relações de confiança unidirecionais exigem que o domínio do servidor confie no domínio do cliente.

![mbam2](images/mbam2-5-2servers.png)

Recursos de servidor a serem configurados neste servidor de banco de dados de descrição do servidor

Banco de dados de auditoria e conformidade

Esse recurso está configurado em um servidor que executa o Windows Server e a instância do SQL Server com suporte.

O banco de dados de **conformidade e auditoria** armazena dados de conformidade, que são usados principalmente para relatórios que o SQL Server Reporting Services hospeda.

Banco de dados de recuperação

Esse recurso está configurado em um servidor que executa o Windows Server e a instância do SQL Server com suporte.

O **banco** de dados de recuperação armazena dados de recuperação coletados de computadores cliente do MBAM.

Relatórios

Esse recurso está configurado em um servidor que executa o Windows Server e a instância do SQL Server com suporte.

Os **relatórios** fornecem dados de status de conformidade e auditoria de recuperação sobre os computadores cliente da sua empresa. Você pode acessar os relatórios do site Administração e monitoramento ou diretamente do SQL Server Reporting Services.

Servidor de administração e monitoramento

Site de administração e monitoramento

Esse recurso é configurado em um computador que executa o Windows Server.

O **site de administração e monitoramento** é usado para:

-   Ajude os usuários finais a recuperarem o acesso aos seus computadores quando estiverem bloqueados. (Essa área do site geralmente é chamada de suporte técnico).

-   Exiba relatórios que mostram o status de conformidade e a atividade de recuperação para computadores cliente.

Portal de autoatendimento

Esse recurso é configurado em um computador que executa o Windows Server.

O **portal de autoatendimento** é um site que permite aos usuários finais nos computadores cliente fazerem logon independentemente em um site para obter uma chave de recuperação caso percam ou esqueçam a senha do BitLocker.

Monitorando serviços Web para este site

Esse recurso é configurado em um computador que executa o Windows Server.

Os **Serviços Web de monitoramento** são usados pelo cliente MBAM e pelos websites para se comunicar ao banco de dados.

**Importante**  O serviço Web de monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, pois os sites do MBAM se comunicam diretamente com o banco de dados de recuperação.

 

Estação de trabalho de gerenciamento

Modelos de política de grupo MBAM

-   Os modelos de política de grupo do MBAM são configurações de política de grupo que definem configurações de implementação para MBAM, que permitem que você gerencie a criptografia de unidade de disco BitLocker.

-   Antes de executar o MBAM, você deve baixar os modelos de política de grupo de [como obter modelos de política de grupo do MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou estação de trabalho que esteja executando um servidor Windows ou sistema operacional Windows com suporte.

-   A estação de trabalho não precisa ser um computador dedicado.

Cliente MBAM e computador cliente do Configuration Manager

Software cliente MBAM

O cliente MBAM:

-   Usa objetos de política de grupo para impor a criptografia de unidade de disco BitLocker em computadores cliente da empresa.

-   Coleta a chave de recuperação do BitLocker para três tipos de unidade de dados: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

-   Coleta informações de recuperação e informações do computador dos computadores cliente.



## Tópicos relacionados


[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

[Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Recursos ilustrados de uma implantação do MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





