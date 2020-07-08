---
title: Monitorando os contadores de desempenho das solicitações de serviço Web
description: Monitorando os contadores de desempenho das solicitações de serviço Web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799360"
---
# Monitorando os contadores de desempenho das solicitações de serviço Web


O monitoramento e a administração do Microsoft BitLocker (MBAM) fornecem contadores de desempenho que registram o desempenho de solicitações que são enviadas para os seguintes serviços Web:

-   **StatusReportingService. svc** – serviço que recebe solicitações de status de conformidade

-   **CoreService. svc** – serviço que recebe solicitações para tentativas de recuperação de chave

## Contadores de desempenho que o MBAM fornece


O MBAM fornece os seguintes contadores de desempenho para cada um dos métodos públicos implementados por seus serviços Web do StatusReportingService e do CoreService:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de contador de desempenho</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Número total de solicitações</p></td>
<td align="left"><p>Fornece uma contagem de incremento que começa do zero quando o servidor é iniciado ou reiniciado.</p>
<p>Fornece uma visão geral da atividade do sistema. Pode ser monitorado por ferramentas automatizadas para garantir a integridade do servidor e validar que o contador é incrementado continuamente durante um período de tempo especificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Solicitações por segundo</p></td>
<td align="left"><p>Indica a taxa de transferência atual do servidor MBAM, pois ele dá suporte à base de clientes do MBAM.</p>
<p>Permite que os administradores de sites:</p>
<ul>
<li><p>Calcular o número médio de solicitações por segundo, com base no número de clientes do MBAM e na sua frequência de relatórios.</p></li>
<li><p>Valide se o número de solicitações por segundo correlaciona-se amplamente com o número médio de solicitações calculadas por segundo. Uma variação significativa pode indicar que o cliente MBAM não está instalado em uma porcentagem da base do cliente ou que um objeto de política de grupo do MBAM não foi implantado com êxito.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Duração da solicitação</p></td>
<td align="left"><p>Registra a duração de solicitações em milissegundos.</p>
<p>Embora esse contador seja atualizado com a duração de cada solicitação, o monitor de desempenho do Windows o amostra apenas periodicamente (geralmente a cada segundo), para que você possa ver uma variabilidade no valor. Por esse motivo, considere usar o valor médio exibido pelo monitor de desempenho.</p></td>
</tr>
</tbody>
</table>

 

## Resultados e recomendações do contador de desempenho


À medida que você adicionar novos clientes do MBAM a um servidor MBAM com capacidade de sobra, espera ver um aumento no número de solicitações por segundo. Esse aumento será proporcional ao número de novos computadores cliente. A duração média da solicitação permanecerá relativamente estática. Como o servidor se aproxima da capacidade máxima, as solicitações por segundo começam a se redistribuirem e a média da duração da solicitação começa a ser mais longa.

Se você se preocupa se seus servidores do MBAM podem dar suporte à base de clientes, considere a implantação de MBAM em fases em diferentes conjuntos de computadores cliente. Ao implantar o MBAM em cada conjunto de computadores cliente, recomendamos que você faça instantâneos dos contadores de desempenho para ver o impacto relativo da implantação em cada novo conjunto de clientes. Se o número de solicitações por segundo começar a redistribuir e a média da duração da solicitação aumentar, considere aprimorar sua infraestrutura de servidor do MBAM seguindo um destes procedimentos:

-   Mover o banco de dados do MBAM para um cluster exclusivo do Microsoft SQL Server ou SQL Server

-   Balanceamento de carga MBAM em vários servidores Web dos serviços de informações da Internet (IIS)

-   Implantando o MBAM em um hardware de servidor mais potente

## Exibindo contadores de desempenho


A ferramenta recomendada para exibir os contadores de desempenho do MBAM é o monitor de desempenho do Windows, que vem com o Windows. Se você estiver usando o Windows PowerShell, não será necessário habilitar os contadores antes de exibi-los, pois eles são automaticamente registrados pelo cmdlet **Enable-WebApplication** do Windows PowerShell.

Para obter instruções detalhadas sobre como exibir contadores de desempenho, consulte [como exibir contadores de desempenho do MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).



## Tópicos relacionados


[Manutenção do MBAM 2.5](maintaining-mbam-25.md)

 

 


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).


