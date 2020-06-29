---
title: Determinar o método de publicação
description: Determinar o método de publicação
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797973"
---
# Determinar o método de publicação


Depois de sequenciar um aplicativo usando o sequenciador do Application Virtualization, você precisará *publicar* esse aplicativo para seus usuários. Publicar o aplicativo consiste em fornecer os ícones, as informações de definição do pacote e o local da fonte de conteúdo para cada computador em que o cliente do Application Virtualization foi instalado. A tabela a seguir descreve os métodos de publicação com suporte ao implantar o Application Virtualization usando um sistema ESD (Electronic Software Distribution).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Vantagens</th>
<th align="left">Desvantagens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gerar um arquivo do Windows Installer durante o sequenciamento, como uma solução autônoma.</p></td>
<td align="left"><ul>
<li><p>Muito simples de usar.</p></li>
<li><p>Pacote carregado no cache localmente em cada computador.</p></li>
<li><p>Ícones exibidos para o usuário.</p></li>
<li><p>Semelhante à implantação de software tradicional.</p></li>
<li><p>Não é preciso ter servidores de streaming.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Não há flexibilidade na localização do conteúdo do pacote em computadores, no mesmo local em todos os computadores.</p></li>
<li><p>Deve usar somente adicionar/remover programas ou msiexec para remover aplicativos.</p></li>
<li><p>Remoção e substituição pela nova versão necessária para atualização do pacote.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Gerar um arquivo do Windows Installer durante o sequenciamento, usado com as propriedades de linha de comando MODE, LOAD e OVERRIDEURL e o manifesto do pacote.</p></td>
<td align="left"><ul>
<li><p>Simples de usar, mas com flexibilidade adicional.</p></li>
<li><p>Ícones exibidos para o usuário.</p></li>
<li><p>O arquivo SFT que contém os aplicativos pode ser colocado em um local de origem de streaming, com clientes configurados para usar esse local.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Flexibilidade limitada — apenas o local do conteúdo do pacote pode ser controlado no tempo de execução.</p></li>
<li><p>Deve usar somente adicionar/remover programas ou msiexec para remover o aplicativo.</p></li>
<li><p>Remoção e substituição pela nova versão necessária para a atualização do pacote, a menos que você use o Streaming Server.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Executar comandos SFTMIME.</p></td>
<td align="left"><ul>
<li><p>Flexibilidade completa: controle total de todas as funções de gerenciamento de pacotes.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Os comandos devem ser scripdos para serem usados com o sistema ESD.</p></li>
<li><p>Os comandos devem ser executados em cada computador na sequência correta.</p></li>
<li><p>Informações detalhadas sobre a linguagem de comando e o planejamento cuidadoso necessários.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre como usar esses métodos de publicação, consulte [como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md).

## Tópicos relacionados


[Determinar o método de streaming](determine-your-streaming-method.md)

[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Visão geral de cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario-overview.md)

[Como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Referência de comando SFTMIME](sftmime--command-reference.md)

 

 





