---
title: Sincronizar eventos de disparo para a UE-V 2.x
description: Sincronizar eventos de disparo para a UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799944"
---
# Sincronizar eventos de disparo para a UE-V 2.x


O Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 permite sincronizar seu aplicativo e as configurações do Windows em todos os seus dispositivos ingressados no domínio. Os *eventos de gatilho de sincronização* definem quando o UE-V Agent sincroniza essas configurações com o local de armazenamento de configurações. O UE-V 2 introduz um novo *método de sincronização* chamado *SyncProvider*. Para obter mais informações sobre a configuração do método de sincronização, consulte [métodos de sincronização para UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

## Eventos do gatilho de sincronização do UE-V 2


A tabela a seguir explica os eventos de gatilho para aplicativos clássicos e configurações do Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Evento de gatilho UE-V 2</strong></p></td>
<td align="left"><p><strong>SyncMethod = SyncProvider</strong></p></td>
<td align="left"><p><strong>SyncMethod = nenhum</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Logon do Windows</strong></p></td>
<td align="left"><ul>
<li><p>As configurações do aplicativo e do Windows são importadas para o cache local do local de armazenamento de configurações.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">As configurações assíncronas do Windows </a> são aplicadas.</p></li>
<li><p>As configurações síncronas do Windows serão aplicadas durante o próximo logon do Windows.</p></li>
<li><p>As configurações do aplicativo serão aplicadas quando o aplicativo for iniciado.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>As configurações do aplicativo e do Windows são lidas diretamente do local de armazenamento de configurações.</p></li>
<li><p>As configurações assíncronas e assíncronas do Windows são aplicadas.</p></li>
<li><p>As configurações do aplicativo serão aplicadas quando o aplicativo for iniciado.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Logoff do Windows</strong></p></td>
<td align="left"><p>Armazenar alterações localmente e armazenar em cache e copiar configurações assíncronas e assíncronas do Windows para o servidor de localização de armazenamento de configurações, se disponível</p></td>
<td align="left"><p>Armazenar alterações no local de armazenamento de configurações assíncronas e assíncronas do Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Connect (RDP)/desbloquear</strong></p></td>
<td align="left"><p>Sincronize as configurações assíncronas do Windows do local de armazenamento de configurações para o cache local, se disponível.</p>
<p>Aplicar configurações do Windows armazenadas em cache</p></td>
<td align="left"><p>Baixar e aplicar configurações assíncronas do Windows do local de armazenamento de configurações</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Desconexão do Windows (RDP)/bloqueio</strong></p></td>
<td align="left"><p>Armazene as alterações de configurações assíncronas do Windows no cache local.</p>
<p>Sincronizar qualquer configuração assíncrona do Windows do cache local para o local de armazenamento configurações, se disponível</p></td>
<td align="left"><p>Armazenar alterações de configurações assíncronas do Windows no local de armazenamento de configurações</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Início do aplicativo</strong></p></td>
<td align="left"><p>Aplicar configurações de aplicativo do cache local conforme o aplicativo é iniciado</p></td>
<td align="left"><p>Aplicar configurações do aplicativo do local de armazenamento de configurações à medida que o aplicativo for iniciado</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Aplicativo é fechado</strong></p></td>
<td align="left"><p>Armazenar as alterações de configurações do aplicativo nas configurações de cache local e copiar para o local de armazenamento de configurações, se disponíveis</p></td>
<td align="left"><p>Armazenar as alterações de configurações do aplicativo em local de armazenamento de configurações</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>A tarefa agendada do controlador de sincronização ou "sincronizar agora" é executada no centro de configurações da empresa</strong></p>
<p></p></td>
<td align="left"><p>As configurações do aplicativo e do Windows são sincronizadas entre o local de armazenamento de configurações e o cache local.</p>
<div class="alert">
<strong>Observação</strong><br/><p>As alterações de configurações não são armazenadas em cache localmente até que o aplicativo seja fechado. Este gatilho não importará alterações feitas em um aplicativo em execução no momento.</p>
<p>Para configurações do Windows, isso significa que todas as alterações não serão armazenadas em cache localmente e exportadas até o próximo bloqueio (assíncrono) ou logoff (assíncrono e síncrono).</p>
</div>
<div>

</div>
<p>As configurações são aplicadas nestes casos:</p>
<ul>
<li><p>As configurações assíncronas do Windows são aplicadas diretamente.</p></li>
<li><p>As configurações do aplicativo são aplicadas quando o aplicativo é iniciado.</p></li>
<li><p>As configurações assíncronas e assíncronas do Windows são aplicadas durante o próximo logon do Windows.</p></li>
<li><p>As configurações do aplicativo do Windows (AppX) são aplicadas durante a próxima atualização. Consulte <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)"> monitorar configurações </a> do aplicativo para obter mais informações.</p></li>
</ul></td>
<td align="left"><p>NA</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Configurações assíncronas atualizadas na loja remota *</strong></p></td>
<td align="left"><p>Carregar e aplicar novas configurações assíncronas do cache.</p></td>
<td align="left"><p>Carregar e aplicar configurações do servidor central</p></td>
</tr>
</tbody>
</table>








## Tópicos relacionados


[Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

[Alterar a frequência das tarefas agendadas do UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[Escolha o método de configuração para UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#config)









