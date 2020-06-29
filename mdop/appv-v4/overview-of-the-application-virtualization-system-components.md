---
title: Visão geral dos Componentes do Application Virtualization System
description: Visão geral dos Componentes do Application Virtualization System
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796848"
---
# Visão geral dos Componentes do Application Virtualization System


A tabela a seguir descreve os componentes principais do sistema de gerenciamento do Microsoft Application Virtualization. Para obter mais informações sobre como implantar esses componentes do sistema, consulte [cenário baseado em servidor do Application Virtualization](application-virtualization-server-based-scenario.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">Função</th>
<th align="left">Informações adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de gerenciamento do Microsoft Application Virtualization</p></td>
<td align="left"><p>O componente responsável por transmitir o conteúdo do pacote e publicar os atalhos e associações de tipo de arquivo para o cliente do Application Virtualization.</p></td>
<td align="left"><p>O servidor de gerenciamento do Application Virtualization dá suporte à atualização ativa, ao gerenciamento de licenças e a um banco de dados que pode ser usado para relatórios.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Pasta de conteúdo </strong></p></td>
<td align="left"><p>O local dos pacotes do Application Virtualization para streaming.</p></td>
<td align="left"><p>Essa pasta pode ser localizada em um compartilhamento ou em um servidor de gerenciamento do Application Virtualization. A pasta também pode estar localizada em uma rede de área de armazenamento (SAN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Console de gerenciamento do Microsoft Application Virtualization</p></td>
<td align="left"><p>Um utilitário de gerenciamento de snap-in do MMC 3,0 para administração do Microsoft Application Virtualization Server.</p></td>
<td align="left"><p>Esse componente pode ser instalado no servidor do Microsoft Application Virtualization ou localizado em uma estação de trabalho separada que tenha o MMC 3.0 e. .NET 2.0 instalado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serviço Web de gerenciamento do aplicativo Microsoft Application Virtualization</p></td>
<td align="left"><p>O componente responsável pela comunicação de qualquer solicitação de leitura/gravação ao repositório de dados do Application Virtualization.</p></td>
<td align="left"><p>Esse componente pode ser instalado no servidor do Microsoft Application Virtualization ou em um computador separado com o IIS instalado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Repositório de dados do Microsoft Application Virtualization</p></td>
<td align="left"><p>O componente armazenado no banco de dados SQL e responsável por armazenar todas as informações relacionadas à infraestrutura de virtualização de aplicativo.</p></td>
<td align="left"><p>Essas informações incluem todos os registros de aplicativos, atribuições de aplicativos e quais grupos têm responsabilidade por gerenciar o ambiente de virtualização de aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de streaming do Microsoft Application Virtualization</p></td>
<td align="left"><p>O componente responsável pela hospedagem dos pacotes do Application Virtualization para o streaming para clientes em uma filial, em que o link de volta para o servidor de gerenciamento do Application Virtualization é considerado uma WAN.</p></td>
<td align="left"><p>Esse servidor contém somente a funcionalidade de streaming e não fornece o console de gerenciamento do Application Virtualization nem o serviço Web de gerenciamento da virtualização de aplicativos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenciador do Microsoft Application Virtualization</p></td>
<td align="left"><p>O componente usado para monitorar e capturar a instalação de aplicativos para criar pacotes de aplicativos virtuais.</p></td>
<td align="left"><p>A saída consiste nos ícones do aplicativo, um arquivo OSD contendo informações de definição do pacote, um arquivo de manifesto do pacote e o arquivo SFT que contém os arquivos de conteúdo do programa aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente do Microsoft Application Virtualization</p></td>
<td align="left"><p>O componente instalado no cliente da área de trabalho do Application Virtualization ou no cliente do Application Virtualization para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal) e que fornece o ambiente virtual para aplicativos virtualizados.</p></td>
<td align="left"><p>O cliente do Microsoft Application Virtualization gerencia o fluxo de pacote no cache, a atualização de publicação, o transporte e todas as interações com os servidores do Application Virtualization.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Publicação de aplicativos virtuais usando os Application Virtualization Management Servers](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





