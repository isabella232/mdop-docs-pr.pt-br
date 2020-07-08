---
title: Determinar o método de streaming
description: Determinar o método de streaming
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797971"
---
# Determinar o método de streaming


Na primeira vez que um usuário clica duas vezes no ícone que foi colocado em um computador por meio do processo de publicação, o cliente de virtualização do aplicativo obtém o conteúdo do pacote do aplicativo virtual de um local de origem de streaming.

**Observação** 
 *Streaming* é o termo usado para descrever o processo de obter conteúdo de um pacote de aplicativo sequenciado, começando com o bloco de recursos principal e, em seguida, obtendo blocos adicionais conforme necessário.

 

O local de origem de streaming é geralmente um servidor acessível pelo computador do usuário; no entanto, alguns sistemas de distribuição eletrônicos, como o Microsoft Endpoint Configuration Manager, podem distribuir o arquivo SFT para o computador do usuário e, em seguida, transmitir o pacote de aplicativo virtual localmente do cache do computador.

**Observação**  Um local de origem de streaming para pacotes virtuais pode ser configurado em um computador que não seja um servidor. Isso é especialmente útil em um escritório de filial pequeno que não tem servidor.

 

As fontes de streaming que podem ser usadas para armazenar aplicativos sequenciados são descritas na tabela a seguir.

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
<th align="left">Protocolo</th>
<th align="left">Vantagens</th>
<th align="left">Desvantagens</th>
<th align="left">Links</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de arquivos</p></td>
<td align="left"><p>Arquivo</p></td>
<td align="left"><ul>
<li><p>Solução simples de baixo custo para configurar o servidor de arquivos existente com o \CONTENT share</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Sem atualização ativa</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Como configurar o Servidor de Arquivos</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor IIS</p></td>
<td align="left"><p>HTTP/HTTPS</p></td>
<td align="left"><ul>
<li><p>Dá suporte à segurança aprimorada usando o protocolo HTTPS.</p></li>
<li><p>Suporte a streaming para computadores remotos pela Internet</p></li>
<li><p>Apenas uma porta em Firewall para abrir</p></li>
<li><p>Altamente dimensionável</p></li>
<li><p>Protocolo familiar</p></li>
</ul></td>
<td align="left"><ul>
<li><p>É necessário gerenciar o IIS</p></li>
<li><p>Sem atualização ativa</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Como configurar o servidor para o IIS</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servidor de streaming do Application Virtualization</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Atualização ativa</p></li>
<li><p>Suporta a segurança aprimorada usando o protocolo RTSP</p></li>
<li><p>Somente uma porta em Firewall para abrir (somente RTSP)</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Duas infra-estruturas</p></li>
<li><p>Requisito de administração do servidor</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Como configurar os Application Virtualization Management Servers</a></p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Visão geral de cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario-overview.md)

[Determinar o método de publicação](determine-your-publishing-method.md)

 

 





