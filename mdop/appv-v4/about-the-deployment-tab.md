---
title: Sobre a guia Implantação
description: Sobre a guia Implantação
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797630"
---
# Sobre a guia Implantação


Use a guia **implantação** no console do sequenciador do Application Virtualization para alterar as informações de um aplicativo que você está prestes a sequenciar. Esta guia contém os elementos a seguir.

## URL do servidor


Use os controles de **URL do servidor** para especificar as definições de configuração do servidor de aplicativos virtual.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controle</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Protocolo</strong></p></td>
<td align="left"><p>Permite que você selecione o protocolo que irá transmitir o pacote do aplicativo sequenciado de um servidor de aplicativos virtual a um cliente de desktop do Application Virtualization. Os seguintes protocolos estão disponíveis:</p>
<ul>
<li><p><strong>RTSP </strong> — o padrão, especifica que o protocolo de streaming em tempo real controla a troca de aplicativos habilitados para virtualização.</p></li>
<li><p><strong>RTSPs </strong> — especifica que o protocolo de streaming em tempo real com segurança da camada de transporte controla a troca de um pacote de aplicativo sequenciado.</p></li>
<li><p><strong>Arquivo </strong> — especifica que o aplicativo sequenciado será transmitido de um compartilhamento de arquivos.</p></li>
<li><p><strong>HTTPS </strong> — especifica que o protocolo de transporte de hipertexto seguro controla a troca de um pacote.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Hostname</strong></p></td>
<td align="left"><p>Permite que você selecione o servidor de aplicativos virtual ou o balanceador de carga na frente de um grupo de servidores de aplicativos virtuais que transmitirá o pacote de software a um cliente de desktop de virtualização de aplicativo. Você deve concluir esse item para criar um pacote de aplicativo sequenciado, mas você pode alterar a variável de ambiente% SFT_SOFTGRIDSERVER% padrão para o nome de host ou endereço IP real de um servidor de aplicativos virtual.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você optar por não especificar um nome de host estático ou endereço IP, em cada cliente de desktop virtualização de aplicativos, será necessário configurar uma variável de ambiente chamada SFT_SOFTGRIDSERVER. O valor deve ser o nome do host ou endereço IP do servidor de aplicativos virtual ou o balanceador de carga que é este cliente&#39;s fonte de aplicativos. Você deve transformar essa variável de ambiente em uma variável de sistema, em vez de uma variável de usuário. Qualquer sessão de cliente da área de trabalho do Application Virtualization que esteja em execução neste computador durante a atribuição dessa variável deve ser fechada e, em seguida, aberta para que a sessão retomada saiba qual é a sua nova fonte de aplicativo.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Port</strong></p></td>
<td align="left"><p>Permite que você especifique a porta na qual o servidor de aplicativos virtual ou o balanceador de carga escutará uma solicitação de cliente de desktop virtualização de aplicativos&#39;s para o pacote. Essas informações são necessárias para criar um pacote, mas você pode alterá-lo. A porta padrão é 554.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Caminho</strong></p></td>
<td align="left"><p>Permite que você especifique o caminho relativo no servidor de aplicativos virtual em que o pacote do software está armazenado e do qual ele será transmitido. Essas informações são necessárias para criar um pacote se o arquivo SFT for armazenado em um subdiretório de conteúdo; caso contrário, essas informações não são necessárias.</p></td>
</tr>
</tbody>
</table>



## Sistemas operacionais


Use os controles de **sistemas operacionais** para especificar os requisitos do sistema operacional do aplicativo. Se um cliente da área de trabalho do Application Virtualization não puder dar suporte a nenhum dos sistemas operacionais selecionados, o aplicativo não será iniciado.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controles</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Sistemas operacionais disponíveis</strong></p></td>
<td align="left"><p>Exibe uma lista de sistemas operacionais que podem dar suporte aos aplicativos no pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sistemas operacionais selecionados</strong></p></td>
<td align="left"><p>Exibe uma lista de sistemas operacionais selecionados que dão suporte aos aplicativos no pacote.</p></td>
</tr>
</tbody>
</table>



## Opções de saída


Use os controles de **Opções de saída** para especificar as opções de saída para o aplicativo a ser instalado.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controle</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Algoritmo de compactação</strong></p></td>
<td align="left"><p>Use para selecionar o método para compactar o arquivo SFT para streaming em uma rede. Selecione um dos seguintes métodos de compactação:</p>
<ul>
<li><p><strong>Compactado </strong> — especifica que o arquivo SFT seja compactado <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> no </a> formato zlib.</p></li>
<li><p><strong>Não compactado </strong> — o padrão; especifica que o arquivo SFT não seja compactado.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Impor descritores de segurança</strong></p></td>
<td align="left"><p>Selecione para impor os descritores de segurança dos aplicativos no pacote após a implantação no cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Gerar pacote MSI (Microsoft Windows Installer)</strong></p></td>
<td align="left"><p>Selecione para instalar ou implantar um pacote de aplicativo sequenciado com o Windows Installer. Se você tiver feito alterações usando o sequenciador, as alterações não serão incluídas com o arquivo do Windows Installer. O arquivo do Windows Installer sempre será criado usando o arquivo. sft salvo no disco rígido.</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Como alterar as propriedades da implantação](how-to-change-deployment-properties.md)

[Console do Sequencer](sequencer-console.md)









