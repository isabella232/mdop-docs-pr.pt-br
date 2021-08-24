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
ms.openlocfilehash: 9ec9b1e4391fde3083564f34b5f89d1c5bd174f7
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910666"
---
# <a name="high-level-architecture-of-mbam-25-with-stand-alone-topology"></a>Arquitetura de alto nível do MBAM 2.5 com topologia autônoma


Este tópico descreve a arquitetura recomendada para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia autônomo do Configuration Manager. Nesta topologia, o MBAM é implantado como um produto autônomo. Você também pode implantar o MBAM com a topologia integração do Configuration Manager, que integra o MBAM ao Configuration Manager. Para obter mais informações, consulte [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Para ver uma lista das versões com suporte do software mencionado neste tópico, consulte CONFIGURAções com suporte do [MBAM 2.5](mbam-25-supported-configurations.md).

**Observação**  
Recomendamos que você use uma arquitetura de servidor único somente em ambientes de teste.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Número recomendado de servidores e número de clientes com suporte


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
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="recommended-mbam-high-level-architecture-with-the-stand-alone-topology"></a>Arquitetura de alto nível do MBAM recomendada com a topologia autônomo


O diagrama e a tabela a seguir descrevem a arquitetura de dois servidores de alto nível recomendada para MBAM com a topologia autônomo. As implantações de várias florestas do MBAM exigem uma confiança única ou de duas vias. As confianças de ida exigem que o domínio do servidor confie no domínio do cliente.

![mbam2.](images/mbam2-5-2servers.png)

Recursos do servidor para configurar neste servidor de Banco de Dados de Descrição do servidor

Banco de dados de conformidade e auditoria

Esse recurso é configurado em um servidor que executa Windows Server e tem suporte SQL Server instância.

O **Banco de Dados de** Conformidade e Auditoria armazena dados de conformidade, que são usados principalmente para relatórios que SQL Server Reporting Services hosts.

Banco de Dados de Recuperação

Esse recurso é configurado em um servidor que executa Windows Server e tem suporte SQL Server instância.

O **Banco de Dados de** Recuperação armazena dados de recuperação coletados de computadores clientes do MBAM.

Relatórios

Esse recurso é configurado em um servidor que executa Windows Server e tem suporte SQL Server instância.

Os **Relatórios fornecem** dados de status de auditoria e conformidade de recuperação sobre os computadores cliente em sua empresa. Você pode acessar os relatórios do Site de Administração e Monitoramento ou diretamente do SQL Server Reporting Services.

Servidor de Administração e Monitoramento

Site de Administração e Monitoramento

Esse recurso é configurado em um computador que executa Windows Server.

O **Site de Administração e Monitoramento** é usado para:

-   Ajude os usuários finais a recuperar o acesso aos computadores quando estão bloqueados. (Essa área do site é comumente chamada de Help Desk.)

-   Exibir relatórios que mostram o status de conformidade e a atividade de recuperação para computadores cliente.

Self-Service Portal

Esse recurso é configurado em um computador que executa Windows Server.

O **Portal de** Autoatendenciamento é um site que permite que os usuários finais em computadores clientes faça logoff independentemente em um site para obter uma chave de recuperação se perderem ou esquecerem a senha do BitLocker.

Monitorando serviços Web para este site

Esse recurso é configurado em um computador que executa Windows Server.

Os **serviços Web de monitoramento** são usados pelo Cliente MBAM e pelos sites para se comunicar com o banco de dados.

**Importante**  
O Serviço Web de Monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, já que os sites do MBAM se comunicam diretamente com o Banco de Dados de Recuperação.

 

Estação de trabalho de gerenciamento

Modelos de Política de Grupo do MBAM

-   Os Modelos de Política de Grupo do MBAM são configurações de Política de Grupo que definem configurações de implementação para MBAM, que permitem gerenciar a Criptografia de Unidade do BitLocker.

-   Antes de executar o MBAM, você deve baixar os Modelos de Política de Grupo de Modelos de Como Obter Modelos de Política de Grupo [MDOP (.admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou estação de trabalho que está executando um servidor Windows ou um sistema operacional Windows com suporte.

-   A estação de trabalho não precisa ser um computador dedicado.

Computador cliente do MBAM Client and Configuration Manager

Software cliente MBAM

O cliente MBAM:

-   Usa objetos de política de grupo para impor a Criptografia de Unidade do BitLocker em computadores cliente na empresa.

-   Coleta a chave de recuperação do Bitlocker para três tipos de unidade de dados: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

-   Coleta informações de recuperação e informações do computador sobre os computadores cliente.



## <a name="related-topics"></a>Tópicos relacionados


[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

[Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Recursos ilustrados de uma implantação do MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## <a name="got-a-suggestion-for-mbam"></a>Tem uma sugestão para MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, use o [Fórum technet do MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam) 





