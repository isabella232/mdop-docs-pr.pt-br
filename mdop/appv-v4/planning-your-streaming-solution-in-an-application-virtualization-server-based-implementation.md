---
title: Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server
description: Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796811"
---
# Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server


Se você quiser usar os servidores de streaming do Application Virtualization em conjunto com a implementação baseada em servidor de gerenciamento do Application Virtualization, poderá escolher entre várias alternativas, tirando proveito de qualquer infraestrutura que já esteja no lugar. Por exemplo, se você já tem servidores em suas filiais de campo, pode colocar o compartilhamento do \\CONTENT do Application Virtualization nesses servidores e, em seguida, configurar os clientes para usar esse compartilhamento de conteúdo como fonte de conteúdo do aplicativo. Se você optar por usar somente servidores de gerenciamento do Application Virtualization — por exemplo, se tiver apenas um único escritório, os clientes podem transmitir conteúdo desse servidor.

As opções com suporte incluem o uso de um servidor de arquivos, um servidor IIS ou um servidor de streaming do Application Virtualization. Você também pode instalar o servidor de streaming do Application Virtualization em um servidor de arquivos ou servidor IIS existente. As características dessas diferentes opções são resumidas na tabela a seguir.

**Observação**  O recurso atualização ativa permite que uma nova versão de um aplicativo seja adicionada a um servidor de gerenciamento do App-V ou servidor de fluxo contínuo sem afetar os usuários que atualmente executam o aplicativo. Os clientes App-V receberão automaticamente a versão mais recente do aplicativo do servidor de gerenciamento do App-V ou do servidor de streaming na próxima vez em que o usuário iniciar o aplicativo. O uso do protocolo RTSP (S) é necessário para este recurso.

 

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
<td align="left"><p>SMB</p></td>
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
<li><p>Suporte à segurança aprimorada usando o protocolo HTTPS</p></li>
<li><p>Suporte a streaming para computadores remotos pela Internet</p></li>
<li><p>Apenas uma porta em Firewall para abrir</p></li>
<li><p>Escaláveis</p></li>
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
<li><p>Apenas uma porta em Firewall para abrir</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Duas infra-estruturas</p></li>
<li><p>Requisito de administração do servidor</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Como configurar os Application Virtualization Streaming Servers</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de gerenciamento do Application Virtualization</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Atualização ativa</p></li>
<li><p>Suporta a segurança aprimorada usando o protocolo RTSP</p></li>
<li><p>Apenas uma porta em Firewall para abrir</p></li>
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


[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Visão geral dos Componentes do Application Virtualization System](overview-of-the-application-virtualization-system-components.md)

[Publicação de aplicativos virtuais usando os Application Virtualization Management Servers](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





