---
title: Arquitetura de alto nível para o App-V 5.1
description: Arquitetura de alto nível para o App-V 5.1
author: dansimp
ms.assetid: 90406361-55b8-40b7-85c0-449436789d4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8044c6ae9af4673ec12b47cf3b8fa73a134d9cca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796520"
---
# Arquitetura de alto nível para o App-V 5.1


Use as informações a seguir para ajudar a simplificar a implantação do Microsoft Application Virtualization (App-V) 5,1.

## Visão geral da arquitetura


Uma implementação típica do App-V 5,1 consiste nos elementos a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de gerenciamento do App-V 5,1</p></td>
<td align="left"><p>O servidor de gerenciamento do App-V 5,1 oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,1. Além disso, você pode instalar mais de uma instância do servidor de gerenciamento em seu ambiente, que oferece os seguintes benefícios:</p>
<ul>
<li><p>Tolerância a falhas e alta disponibilidade – instalar e configurar o servidor de gerenciamento do App-V 5,1 em dois computadores separados pode ajudar em situações em que um dos servidores está indisponível ou offline.</p>
<p>Você também pode ajudar a aumentar a disponibilidade do App-V 5,1 Instalando o servidor de gerenciamento em vários computadores. Nesse cenário, um balanceador de carga de rede também deve ser considerado para que as solicitações do servidor sejam balanceadas.</p></li>
<li><p>Escalabilidade – você pode adicionar mais servidores de gerenciamento conforme necessário para dar suporte a uma alta carga, por exemplo, você pode instalar vários servidores atrás de um balanceador de carga.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de publicação do App-V 5,1</p></td>
<td align="left"><p>O servidor de publicação do App-V 5,1 fornece funcionalidade para hospedagem e streaming de aplicativos virtual. O servidor de publicação não requer uma conexão de banco de dados e é compatível com os seguintes protocolos:</p>
<ul>
<li><p>HTTP e HTTPS</p></li>
</ul>
<p>Você também pode ajudar a aumentar a disponibilidade do App-V 5,1 Instalando o servidor de publicação em vários computadores. Um balanceador de carga de rede também deve ser considerado para que as solicitações do servidor sejam balanceadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servidor de relatórios do App-V 5,1</p></td>
<td align="left"><p>O servidor de relatórios do App-V 5,1 permite que os usuários autorizados executem e visualizem relatórios ad hoc e relatórios ad hoc existentes do 5,1 app-v e possam ajudá-los a gerenciar a infraestrutura do App-V 5,1. O servidor de relatório requer uma conexão com o banco de dados de relatórios do App-V 5,1. Você também pode ajudar a aumentar a disponibilidade do App-V 5,1 Instalando o servidor de relatórios em vários computadores. Um balanceador de carga de rede também deve ser considerado para que as solicitações do servidor sejam balanceadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente do App-V 5,1</p></td>
<td align="left"><p>O cliente App-V 5,1 permite que pacotes criados usando o App-V 5,1 sejam executados em computadores de destino.</p></td>
</tr>
</tbody>
</table>

 

**Observação**  Se você estiver usando o App-V 5,1 com ESD (Electronic Software Distribution), não será necessário usar o servidor de gerenciamento do App-V 5,1, mas ainda poderá usar a funcionalidade de relatório e de streaming do App-V 5,1.

 






## Tópicos relacionados


[Introdução ao App-V 5.1](getting-started-with-app-v-51.md)

 

 





