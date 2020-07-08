---
title: Visão geral do Cenário baseado no Application Virtualization Server
description: Visão geral do Cenário baseado no Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799003"
---
# Visão geral do Cenário baseado no Application Virtualization Server


Se você pretende usar um cenário de implantação baseado em servidor para o seu ambiente do Microsoft Application Virtualization, é importante entender as diferenças entre o *servidor de gerenciamento do Application Virtualization* e o *servidor de streaming do Application Virtualization*. Este tópico descreve essas diferenças e também fornece informações sobre métodos de entrega de pacote, protocolos de transmissão e componentes externos que você precisará considerar enquanto prossegue com a implantação.

## Servidor de gerenciamento do Application Virtualization


O servidor de gerenciamento do Application Virtualization executa a função de publicação e a função streaming. O servidor publica os ícones de aplicativos, atalhos e associações de tipo de arquivo para os clientes do App-V para usuários autorizados. Quando solicitações de usuário para aplicativos são recebidas, o servidor transmite os dados sob demanda para usuários autorizados usando protocolos RTSP ou RTSP. Na maioria das configurações usando este servidor, um ou mais servidores de gerenciamento compartilham um repositório de dados comum para informações de configuração e pacote.

Os servidores de gerenciamento do Application Virtualization usam grupos do Active Directory para gerenciar a autorização do usuário. Além dos serviços de domínio Active Directory, esses servidores têm o SQL Server instalado para gerenciar o banco de dados e o repositório de dados. O servidor de gerenciamento é controlado por meio do console de gerenciamento do Application Virtualization, um snap-in para o console de gerenciamento da Microsoft.

Como os servidores de gerenciamento do Application Virtualization transmitem aplicativos para usuários finais sob demanda, esses servidores são adequados para configurações de sistema que têm LANs confiáveis e de alta largura de banda.

## Servidor de streaming do Application Virtualization


O servidor de streaming do Application Virtualization oferece os mesmos recursos de streaming e atualização de pacote fornecidos pelo servidor de gerenciamento, mas sem seus requisitos do Active Directory ou do SQL Server. No entanto, o servidor de streaming não tem um serviço de publicação, nem tem recursos de licenciamento ou medição. O serviço de publicação de um servidor de gerenciamento do App-V separado é usado em conjunto com o servidor de streaming do App-V. O servidor de streaming App-V atende às necessidades de empresas que desejam usar a virtualização de aplicativos em vários locais com os recursos de streaming da configuração do servidor clássico, mas talvez não tenham a infraestrutura para dar suporte a servidores de gerenciamento do App-V em todos os locais.

O servidor de streaming do Application Virtualization também pode ser usado em ambientes com um ESD (sistema de distribuição de software eletrônico) existente. Use o ESD para gerenciar os aplicativos de streaming. Ao contrário do servidor de gerenciamento do Application Virtualization, o servidor de streaming não usa SQL ou um console de gerenciamento. Esses servidores usam listas de controle de acesso (ACLs) para conceder autorização ao usuário.

## Métodos de entrega de pacote


Se você planeja usar um servidor de virtualização de aplicativos como o método de entrega de publicação, será necessário determinar qual dos seguintes métodos de entrega de pacote o seu cenário emprega:

-   *Entrega de pacote dinâmico*

-   *Carregar de entrega de pacote de arquivo*

### Entrega de pacote dinâmico

Durante a distribuição de pacote dinâmico, o servidor (servidor de gerenciamento do Application Virtualization, o servidor de streaming do Application Virtualization ou o servidor IIS) fornece os aplicativos virtualizados aos usuários finais por meio da implantação sob demanda. O servidor fornece os aplicativos e pacotes virtualizados para um computador cliente somente quando um usuário tenta iniciar um aplicativo pela primeira vez (sob demanda). O servidor transmite apenas os blocos necessários para iniciar o aplicativo (bloco de recursos primário). Depois que o bloco de recursos principal é entregue ao cliente, o aplicativo é executado; o cliente não recebe o aplicativo completo (implantação incremental) a menos que o cliente precise acessar uma parte do aplicativo que não está incluída no bloco de recursos principal. Quando isso ocorre, o cliente executa uma solicitação fora de sequência e o bloco de recursos secundário é transmitido para o cliente. A entrega de pacote dinâmico permite um início rápido do aplicativo.

### Carregar de entrega de pacote de arquivo

Para carregar a entrega de pacotes de arquivos, o servidor entrega todo o pacote de aplicativos virtualizados para um computador cliente antes de o usuário iniciar o aplicativo. Nesse cenário, os aplicativos virtualizados são entregues como um pacote completo, em vez de usar o método dinâmico e incremental usado pelo modelo de entrega dinâmico.

**Observação**  Para cada método de entrega, o processo inicial de entrega do aplicativo virtual e o processo de atualização de aplicativo virtual são iguais. o pacote de aplicativo virtual atualizado substitui o pacote do aplicativo original.

 

A tabela a seguir compara as vantagens e desvantagens de cada método de entrega de pacote.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Vantagens</th>
<th align="left">Desvantagens</th>
<th align="left">Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Entrega de pacote dinâmico</p></td>
<td align="left"><p>Os aplicativos são entregues e atualizados sob demanda.</p>
<p>Os aplicativos são entregues e atualizados de forma incremental para otimizar o tempo de inicialização.</p>
<p>As atualizações são entregues automaticamente na área de trabalho do cliente.</p></td>
<td align="left"><p>Maior base na topologia empresarial devido aos requisitos do servidor.</p>
<p>O streaming de aplicativos deve ser de uma LAN; cenários de implantação em uma WAN ou que usam uma conexão não confiável ou intermitente entre o servidor e o cliente podem ser inutilizáveis.</p></td>
<td align="left"><p>Requer uma infraestrutura de streaming.</p>
<p>Windows Installer usado para implantar o software cliente da área de trabalho do Application Virtualization em computadores de usuários finais.</p>
<p>Grandes empresas devem usar os servidores de streaming do Application Virtualization como pontos de distribuição.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Carregar de entrega de pacote de arquivo</p></td>
<td align="left"><p>Consistente com práticas comuns de gerenciamento corporativo.</p>
<p>Compatível com o cenário de configuração autônomo.</p>
<p>Fornece a solução para o micro – problema com o Branch Office.</p></td>
<td align="left"><p>A entrega e a atualização de aplicativos não é possível sob demanda.</p>
<p>A entrega e a atualização de aplicativos não é incremental; Ele aumenta o consumo de recursos em relação à entrega dinâmica.</p></td>
<td align="left"><p>A organização de ti geralmente é responsável por gerenciar licenças de aplicativos, autorização de usuário e autenticação.</p></td>
</tr>
</tbody>
</table>

 

## Protocolos relacionados a servidor e componentes externos


A tabela a seguir lista os tipos de servidor que podem ser usados em cenários baseados em servidor do Application Virtualization, juntamente com seus protocolos de transmissão correspondentes e os componentes externos necessários para dar suporte à configuração do servidor específico. A tabela também inclui o mecanismo de relatório e o mecanismo de atualização ativa para cada tipo de servidor. Como esses cenários usam o servidor de gerenciamento do Application Virtualization, você pode usar a funcionalidade de relatório interna interna do sistema. Se você usa um servidor de gerenciamento do Application Virtualization ou um servidor de streaming do Application Virtualization para entregar pacotes ao cliente, os pacotes no servidor são atualizados automaticamente quando um usuário faz logon no cliente; Se você usar servidores IIS ou um arquivo para entregar os pacotes ao cliente, os pacotes no cliente deverão ser atualizados manualmente.

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
<th align="left">Componentes externos necessários</th>
<th align="left">Relatórios</th>
<th align="left">Atualização ativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de gerenciamento do Application Virtualization</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPs</p></td>
<td align="left"><p>Ao usar HTTPS, use um servidor IIS para baixar arquivos ICO e OSD e um firewall para proteger o servidor de exposição à Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de streaming do Application Virtualization</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPs</p></td>
<td align="left"><p>Use um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming. Ao usar HTTPS, use um servidor IIS para baixar arquivos ICO e OSD e use um firewall para proteger o servidor de exposição à Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servidor IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Use um mecanismo para sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming. Ao usar HTTP ou HTTPS, use um servidor IIS para baixar arquivos ICO e OSD e um firewall para proteger o servidor de exposição à Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arquivo</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Você precisa de uma maneira de sincronizar o conteúdo entre o servidor de gerenciamento e o servidor de streaming. Você precisa de um computador cliente com compartilhamento de arquivos ou recurso de streaming.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)

[Como configurar os servidores para a implantação baseada em servidor](how-to-configure-servers-for-server-based-deployment.md)

[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)

 

 





