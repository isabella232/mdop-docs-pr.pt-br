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
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796894"
---
# Cenários de servidor voltado para a Internet para redes de perímetro


O App-V 4.5 é compatível com cenários de servidor voltados para a Internet, em que os usuários que não estão conectados à rede corporativa ou que desconectam-se da rede ainda podem usar o App-V. Conforme mostrado na ilustração a seguir, só há suporte para o uso de protocolos seguros na Internet (RTSPs e HTTPS).

![diagrama de posicionamento do firewall do App-v](images/appvfirewalls.gif)

Você pode configurar uma solução voltada à Internet usando um ISA Server, no qual a infraestrutura do App-V está na rede interna das seguintes maneiras:

-   Crie uma regra de publicação na Web para o servidor IIS que hospeda os arquivos ICO e OSD, e, opcionalmente, os pacotes para transmissão, localizado na rede interna. As etapas detalhadas são fornecidas em <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Crie uma regra de publicação de servidor para o servidor de gerenciamento da Web do App-V (RTSPs). As etapas detalhadas são fornecidas em [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Conforme mostrado na ilustração a seguir, se a infraestrutura tiver implementado outros firewalls entre o cliente e o servidor ISA ou entre o ISA Server e a rede interna, as regras de firewall RTSP (TCP 322) e HTTPS (TCP 443) devem ser criadas para dar suporte ao fluxo de tráfego. Além disso, se os firewalls foram implementados entre o ISA Server e a rede interna, o tráfego padrão necessário para os membros do domínio deve ser permitido para o encapsulamento por meio do firewall (DNS, LDAP, Kerberos, SMB/CIFS).

![diagrama de firewall de rede de perímetro do App-v](images/appvperimeternetworkfirewall.gif)

Como as soluções de firewall variam de um ambiente para o ambiente, as orientações fornecidas neste tópico descrevem o tráfego que seria necessário para configurar um ambiente do App-V para a Internet na rede de perímetro. Essas informações também incluem os servidores de rede internos recomendados.

Coloque os seguintes servidores na rede de perímetro:

-   Servidor de gerenciamento do App-V

-   Servidor IIS para publicação e streaming

**Observação**  É uma prática recomendada colocar o servidor de gerenciamento e o servidor IIS em computadores separados.

 

Coloque os seguintes servidores na rede interna:

-   Servidor de conteúdo

-   Repositório de dados (SQL Server)

-   Controlador de domínio do Active Directory

## Requisitos de tráfego


As tabelas a seguir listam os requisitos de tráfego para comunicação da Internet e da rede de perímetro e da rede de perímetro para a rede interna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos de tráfego da Internet para a rede de perímetro</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPs (atualização de publicação e pacotes de streaming)</p></td>
<td align="left"><p>TCP 322 por padrão; Isso pode ser alterado no servidor de gerenciamento do App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (arquivos. ICO e OSD de publicação e pacotes de streaming)</p></td>
<td align="left"><p>TCP 443 por padrão; Isso pode ser alterado na configuração do IIS.</p></td>
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
<th align="left">Requisitos de tráfego da rede de perímetro para a rede interna</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>O TCP 1433 é o padrão, mas pode ser configurado no SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Se o diretório de conteúdo estiver localizado remotamente a partir do (s) servidor (es) de gerenciamento ou do IIS (recomendado).</p></td>
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
<td align="left"><p>Para a resolução de nomes de recursos internos (pode ser eliminada com o uso do arquivo do host em servidores de rede de perímetro)</p></td>
</tr>
</tbody>
</table>

 

 

 





