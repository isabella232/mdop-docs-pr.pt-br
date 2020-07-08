---
title: Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software
description: Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796809"
---
# Planejamento da solução de streaming em uma implementação de Distribuição Eletrônica de Software


Se você decidir usar os servidores de streaming em conjunto com o seu sistema ESD para disponibilizar o conteúdo do aplicativo para os computadores dos usuários finais, poderá escolher entre várias alternativas, tirando proveito de qualquer infraestrutura que já esteja no lugar. Por exemplo, se o seu sistema ESD tiver compartilhamentos de distribuição de software nos servidores nas filiais do campo, você poderá colocar o compartilhamento de \\CONTENT do Application Virtualization nesses servidores e, em seguida, configurar os clientes para usar esse compartilhamento de conteúdo como fonte de conteúdo do aplicativo. As opções com suporte incluem o uso de um servidor de arquivos ou um servidor IIS. Você também pode instalar o servidor de streaming do Application Virtualization em um servidor de arquivos ou servidor IIS existente.

O servidor de streaming do Application Virtualization oferece suporte para o recurso atualização ativa na virtualização do aplicativo. O recurso atualização ativa permite que uma nova versão de um aplicativo seja adicionada a um servidor de gerenciamento do App-V ou servidor de fluxo contínuo sem afetar os usuários que atualmente executam o aplicativo. Os clientes App-V receberão automaticamente a versão mais recente do aplicativo do servidor de gerenciamento do App-V ou do servidor de streaming na próxima vez em que o usuário iniciar o aplicativo. O uso do protocolo RTSP (S) é necessário para este recurso. Se você optar por não usar o servidor de streaming do Application Virtualization, será necessário gerenciar explicitamente as atualizações dos pacotes de aplicativos usando o sistema ESD.

**Observação**  O acesso aos aplicativos é controlado por meio de grupos de segurança nos serviços de domínio Active Directory, portanto, você precisará planejar um processo para configurar um grupo de segurança para cada aplicativo virtual e para gerenciar quais usuários serão adicionados a cada grupo. O administrador do sistema do Application Virtualization configura cada servidor de streaming para usar esses grupos do Active Directory aplicando ACLs aos diretórios de aplicativos no compartilhamento de conteúdo, que controla o acesso aos pacotes com base em associações de grupo do Active Directory.

 

As características das opções de streaming disponíveis são resumidas na tabela a seguir.

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Como configurar os Application Virtualization Management Servers</a></p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Como configurar servidores para a implantação baseada em ESD](how-to-configure-servers-for-esd-based-deployment.md)

[Visão geral de segurança e proteção](security-and-protection-overview.md)

[Publicação de aplicativos virtuais usando a Distribuição Eletrônica de Software](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





