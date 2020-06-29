---
title: Planejando o uso do redirecionamento de pastas com o App-V
description: Planejando o uso do redirecionamento de pastas com o App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796236"
---
# Planejando o uso do redirecionamento de pastas com o App-V


O Microsoft Application Virtualization (App-V) 5,1 oferece suporte ao uso de redirecionamento de pastas, um recurso que permite aos usuários e administradores redirecionar o caminho de uma pasta para um novo local.

Este tópico contém as seguintes seções:

-   [Requisitos para usar o redirecionamento de pastas](#bkmk-folder-redir-reqs)

-   [Como configurar o redirecionamento de pastas para uso com o App-V](#bkmk-folder-redir-cfg)

-   [Como o redirecionamento de pastas funciona com o App-V](#bkmk-folder-redir-works)

-   [Visão geral do redirecionamento de pastas](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>Requisitos e cenários sem suporte para o uso do redirecionamento de pastas


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Requisitos</p></td>
<td align="left"><p>Para usar o redirecionamento de pastas% AppData%, você deve:</p>
<ul>
<li><p>Ter um pacote App-V que tenha uma pasta de sistema de arquivos virtual do AppData (VFS).</p></li>
<li><p>Habilite o redirecionamento de pastas e redirecione as pastas dos usuários para uma pasta compartilhada, geralmente uma pasta de rede.</p></li>
<li><p>Faça o roaming ou nenhum dos seguintes:</p>
<ul>
<li><p>Arquivos em%appdata%\Microsoft\AppV\Client\Catalog</p></li>
<li><p>Configurações do registro em HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</p>
<p>Para obter mais detalhes, consulte <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> publicação de aplicativos e interação do cliente </a> .</p></li>
</ul></li>
<li><p>Verifique se as seguintes pastas estão disponíveis para cada usuário que faz logon no computador que está executando o aplicativo App-V 5,0 SP2 ou posterior:</p>
<ul>
<li><p>% AppData% está configurado para o local de rede desejado (com ou sem <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> suporte a arquivos offline </a> ).</p></li>
<li><p>% LocalAppData% está configurado para a pasta local desejada.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cenários sem suporte</p></td>
<td align="left"><ul>
<li><p>Configurando o% LocalAppData% como uma unidade de rede.</p></li>
<li><p>Redirecionar o menu Iniciar para uma única pasta para vários usuários.</p></li>
<li><p>Se o roaming AppData (% AppData%) for Redirecionado para um compartilhamento de rede que não está disponível, aplicativos App-V falharão ao iniciarão da seguinte maneira:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do App-V</th>
<th align="left">Descrição do cenário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nos hotfixes do App-V 5,0 a App-V 5,0 SP2 Plus</p></td>
<td align="left"><p>Essa falha ocorrerá independentemente de os arquivos offline estarem habilitados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>No App-V 5,0 SP3 e posterior</p></td>
<td align="left"><p>Se o compartilhamento de rede não disponível tiver sido habilitado para arquivos offline, o aplicativo App-V será iniciado com êxito.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>Como configurar o redirecionamento de pastas para uso com o App-V


O redirecionamento de pastas pode ser aplicado a diferentes pastas, como área de trabalho, meus documentos, minhas imagens, etc. No entanto, a única pasta que impacta o uso de aplicativos App-V é a pasta Roaming do usuário do usuário (% AppData%). Você pode aplicar o redirecionamento de pastas a qualquer outra pasta com suporte sem afetar o App-V.

## <a href="" id="bkmk-folder-redir-works"></a>Como o redirecionamento de pastas funciona com o App-V


A tabela a seguir descreve como o redirecionamento de pastas funciona quando% AppData% é redirecionado para uma rede e quando você atende aos requisitos listados anteriormente neste artigo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estado do ambiente virtual</th>
<th align="left">Ação que ocorre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Quando o ambiente virtual é iniciado</p></td>
<td align="left"><p>A pasta de AppData do sistema de arquivos virtual (VFS) é mapeada para a pasta local AppData (% LocalAppData%) em vez de na pasta Roaming AppData do usuário (% AppData%).</p>
<ul>
<li><p>LocalAppData contém um cache local da pasta de AppData do roaming do usuário para o pacote em uso. O cache local está localizado em:</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>Os dados mais recentes da pasta roaming de AppData do usuário são copiados para e substituem os dados atualmente no cache local.</p></li>
<li><p>Enquanto o ambiente virtual está em execução, os dados continuam a ser salvos no cache local. Os dados são servidos somente a partir de% LocalAppData% e não são movidos ou sincronizados com% AppData% até o usuário final desligar o computador.</p></li>
<li><p>As entradas na pasta AppData são feitas usando o contexto do usuário, e não o contexto do sistema.</p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>Às vezes, o redirecionamento de pastas do cliente App-V falha ao mover arquivos de% AppData% para% LocalAppData%. Confira <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> notas de versão do App-V 5,0 SP2 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Quando o ambiente virtual é encerrado</p></td>
<td align="left"><p>Os dados armazenados em cache locais em AppData (roaming) são compactados e copiados para a pasta "real" de AppData em roaming em% AppData%. Um carimbo de data/hora, que indica o último carregamento conhecido, é salvo simultaneamente como uma chave do registro em:</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>Para fornecer redundância, o App-V mantém as três cópias mais recentes dos dados compactados em% AppData%.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>Visão geral do redirecionamento de pastas


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Finalidade</p></td>
<td align="left"><p>Permite que os usuários finais trabalhem com arquivos, que foram redirecionados para outra pasta, como se os arquivos ainda existissem na unidade local.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>O redirecionamento de pastas permite aos usuários e administradores redirecionar o caminho de uma pasta para um local de rede. Os documentos na pasta estão disponíveis para o usuário em qualquer computador na rede.</p>
<ul>
<li><p>O redirecionamento de pastas permite aos usuários e administradores redirecionar o caminho de uma pasta para um local de rede. Os documentos na pasta estão disponíveis para o usuário em qualquer computador na rede.</p></li>
<li><p>O novo local pode ser uma pasta no computador local ou em uma pasta em uma rede compartilhada.</p></li>
<li><p>O redirecionamento de pastas atualiza os arquivos imediatamente, enquanto os dados de roaming geralmente são sincronizados quando o usuário faz logon ou logoff.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Exemplo de uso</p></td>
<td align="left"><p>Você pode redirecionar a pasta documentos, que geralmente é armazenada no computador&#39;s local disco rígido, em um local de rede. O usuário pode acessar os documentos na pasta de qualquer computador na rede.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mais recursos</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">Visão geral do redirecionamento de pasta</a></p></td>
</tr>
</tbody>
</table>
















