---
title: Planejamento da implantação do servidor App-V 5.0
description: Planejamento da implantação do servidor App-V 5.0
author: dansimp
ms.assetid: fd89b324-3961-471a-ad90-c8f9ae7a8155
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06c7c17fd081b89337bbecd31f20f6796338f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796254"
---
# Planejamento da implantação do servidor App-V 5.0


A infraestrutura de servidor do Microsoft Application Virtualization (App-V) 5,0 consiste em um conjunto de recursos especializados que podem ser instalados em um ou mais computadores servidor, de acordo com os requisitos da empresa.

## Planejando a implantação do App-V 5,0 Server


O servidor do App-V 5,0 consiste nos seguintes recursos:

-   Servidor de gerenciamento – oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,0.

-   Banco de dados de gerenciamento – facilita as implantações de banco de dados do gerenciamento do App-V 5,0.

-   Publishing Server – fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.

-   Servidor de relatórios – fornece o App-V 5,0 Reporting Services.

-   Banco de dados de relatórios – facilita a implantação de bancos de dados para relatórios do App-V 5,0.

A lista a seguir exibe os métodos recomendados para a instalação da infraestrutura de servidor do App-V 5,0:

-   Instale o servidor do App-V 5,0. Para obter mais informações, consulte [como implantar o servidor do App-V 5,0](how-to-deploy-the-app-v-50-server-50sp3.md).

-   Instale os recursos de banco de dados, relatórios e gerenciamento em computadores separados. Para obter mais informações, consulte [como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).

-   Use a ESD (Electronic Software Distribution). Para obter mais informações, consulte [como implantar pacotes do App-V 5,0 usando a distribuição de software eletrônico](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).

-   Instale todos os recursos do servidor em um único computador.

## <a href="" id="---------app-v-5-0-server-interaction"></a> Interação do servidor do App-V 5,0


Esta seção contém informações sobre como as várias funções de servidor do App-V 5,0 interagem umas com as outras.

O servidor de gerenciamento do App-V 5,0 contém o repositório de pacotes e suas configurações atribuídas. Para servidores de publicação registrados com o servidor de gerenciamento, os metadados associados são fornecidos aos servidores de publicação para serem usados quando as solicitações de atualização de publicação são recebidas de computadores que executam o cliente do App-V 5,0. Os servidores de publicação do App-V 5,0 gerenciados por um único servidor de gerenciamento podem servir para clientes diferentes e podem ter nomes de site e associações de porta diferentes. Além disso, todos os servidores de publicação gerenciados pelo mesmo servidor de gerenciamento são réplicas uns dos outros.

**Observação**  O servidor de gerenciamento não executa balanceamento de carga. Os metadados associados são simplesmente passados para o Publishing Server para uso durante o processamento de solicitações do cliente.

 

## Protocolos relacionados a servidor e recursos externos


As informações a seguir exibem informações sobre protocolos relacionados a servidor usados pelos servidores App-V 5,0. A tabela também inclui o mecanismo de relatório para cada tipo de servidor.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de servidor</th>
<th align="left">Protocolos</th>
<th align="left">Recursos externos necessários</th>
<th align="left">Relatórios</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Essa combinação de protocolo de servidor requer um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming. Ao usar HTTP ou HTTPS, use um servidor IIS e um firewall para proteger o servidor de exposição à Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p>Arquivo</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Essa combinação de protocolo de servidor requer suporte para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming. Use um computador cliente com o compartilhamento de arquivos ou o recurso de streaming.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## Tópicos relacionados


[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

[Implantação do servidor App-V 5.0](deploying-the-app-v-50-server.md)

 

 





