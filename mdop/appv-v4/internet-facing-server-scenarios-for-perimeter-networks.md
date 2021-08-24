---
title: Cenários de servidor voltado para a Internet para redes de perímetro
description: Cenários de servidor voltado para a Internet para redes de perímetro
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7415cf7a97edc646653df552723667bac8d25fdc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910686"
---
# <a name="internet-facing-server-scenarios-for-perimeter-networks"></a>Cenários de servidor voltado para a Internet para redes de perímetro


O App-V 4.5 dá suporte a cenários de servidor voltados para a Internet, nos quais os usuários que não estão conectados à rede corporativa ou que se desconectam da rede ainda podem usar o App-V. Conforme mostrado na ilustração a seguir, há suporte apenas para o uso de protocolos seguros na Internet (RTSPS e HTTPS).

![Diagrama de posicionamento do firewall do app-v.](images/appvfirewalls.gif)

Você pode configurar uma solução voltada para a Internet usando um SERVIDOR ISA, onde a infraestrutura do App-V está na rede interna das seguintes maneiras:

-   Crie uma regra de Publicação da Web para o servidor IIS que está hospedando os arquivos ICO e OSD e, opcionalmente, os pacotes para streaming localizados na rede interna. As etapas detalhadas são fornecidas em <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Crie uma regra de Publicação do Servidor para o Servidor de Gerenciamento da Web (RTSPS) do App-V. As etapas detalhadas são fornecidas em [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Conforme mostrado na ilustração a seguir, se a infraestrutura tiver implementado outros firewalls entre o cliente e o SERVIDOR ISA ou entre o SERVIDOR ISA e a rede interna, as regras de firewall RTSPS (TCP 322) e HTTPS (TCP 443) devem ser criadas para dar suporte ao fluxo de tráfego. Além disso, se firewalls foram implementados entre o ISA Server e a rede interna, o tráfego padrão necessário para membros do domínio deve ser permitido para túnel através do firewall (DNS, LDAP, Kerberos, SMB/CIFS).

![Diagrama de firewall de rede de perímetro do app-v.](images/appvperimeternetworkfirewall.gif)

Como as soluções de firewall variam de ambiente para ambiente, as diretrizes fornecidas neste tópico descrevem o tráfego necessário para configurar um ambiente App-V voltado para a Internet na rede de perímetro. Essas informações também incluem os servidores de rede internos recomendados.

Coloque os seguintes servidores na rede de perímetro:

-   Servidor de Gerenciamento do App-V

-   Servidor IIS para publicação e streaming

**Observação**  
É uma prática prática melhor colocar o servidor de gerenciamento e o servidor IIS em computadores separados.

 

Coloque os seguintes servidores na rede interna:

-   Servidor de conteúdo

-   Armazenamento de dados (SQL Server)

-   Controlador de Domínio do Active Directory

## <a name="traffic-requirements"></a>Requisitos de Tráfego


As tabelas a seguir listam os requisitos de tráfego para comunicação da Internet e da rede de perímetro e da rede de perímetro para a rede interna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos de Tráfego da Internet para a Rede de Perímetro</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS (pacotes de atualização e streaming de publicação)</p></td>
<td align="left"><p>TCP 322 por padrão; isso pode ser alterado no Servidor de Gerenciamento do App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (publicação de arquivos ICO e OSD e pacotes de streaming)</p></td>
<td align="left"><p>TCP 443 por padrão; isso pode ser alterado na configuração do IIS.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos de Tráfego da Rede de Perímetro para a Rede Interna</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>O TCP 1433 é o padrão, mas pode ser configurado SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Se o diretório de conteúdo estiver localizado remotamente a partir dos Servidores de Gerenciamento ou servidor IIS (recomendado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP e UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP e UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>Para a resolução de nomes de recursos internos (pode ser eliminado com o uso do arquivo do host em servidores de rede de perímetro)</p></td>
</tr>
</tbody>
</table>

 

 

 





