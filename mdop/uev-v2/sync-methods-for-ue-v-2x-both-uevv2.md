---
title: Métodos de sincronização para a UE-V 2.x
description: Métodos de sincronização para a UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799300"
---
# Métodos de sincronização para a UE-V 2.x


O agente do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 permite que você sincronize as configurações do aplicativo e do Windows do usuário com o local de armazenamento de configurações. A configuração do *método Sync* define como o agente UE-V carrega e baixa essas configurações para o local de armazenamento de configurações. O UE-V 2. x introduz um novo SyncMethod chamado de *SyncProvider*. Para obter mais informações sobre eventos de gatilho que iniciam a sincronização das configurações do aplicativo e do Windows, confira [sincronizar eventos de gatilho para UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).

## Configuração do SyncMethod


Esta tabela explica as alterações no SyncMethod do UE-V v 1.0 para o v 2.0 para o v 2.1, bem como as configurações para cada configuração:

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configuração do SyncMethod</strong></p></td>
<td align="left"><p><strong>V 1.0</strong></p></td>
<td align="left"><p><strong>V 2.0</strong></p></td>
<td align="left"><p><strong>V 2.1 e V 2.1 SP1</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncProvider</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>Padrão</p></td>
<td align="left"><p>Padrão</p></td>
<td align="left"><p>As alterações de configurações para um aplicativo específico ou configurações da área de trabalho global do Windows são salvas localmente em uma pasta de cache. Essas alterações são sincronizadas com o local de armazenamento de configurações quando ocorre um evento de gatilho de sincronização. Ao enviar alterações, você salvará as alterações locais no caminho de armazenamento de configurações.</p>
<p>Essa configuração padrão é o padrão ouro para computadores. Essa opção tenta sincronizar a configuração e expira após um pequeno atraso para garantir que a inicialização do aplicativo ou do sistema operacional não seja adiada por um longo período de tempo.</p>
<p>Essa funcionalidade também está vinculada à tarefa agendada – aplicativo do controlador de sincronização. O administrador controla a frequência da tarefa agendada. Por padrão, os computadores sincronizam as configurações a cada 30 min após o logon.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OfflineFiles</p></td>
<td align="left"><p>Padrão</p></td>
<td align="left"><p>Preterido</p></td>
<td align="left"><p>Preterido</p></td>
<td align="left"><p>Comporta-se da mesma forma que o SyncProvider em V 2.0.</p>
<p>Se os arquivos offline estiverem habilitados e a pasta estiver fixada, o UE-V desafixará essa pasta e será sincronizado diretamente com o diretório SMB central.</p>
<p><strong>Observação: </strong> em V 1.0 se você quisesse usar o UE-V em uma CorpNet desconectada (conhecida pela viagem com um laptop), a orientação é usar arquivos offline para garantir que as configurações sejam móveis.Recebemos comentários suficientes do cliente que a ativação de arquivos offline é um bloqueador corporativo não trivial. Portanto, na UE-V 2, criamos um mecanismo de sincronização rigidamente acoplado para armazenar seus dados localmente em cache e sincronizar as configurações para o servidor central. Esta área de recursos não substitui os arquivos offline ou o redirecionamento de pastas.</p>
<p>O UE-V 2 não funciona bem com pastas offline, portanto, as orientações não definem o caminho de armazenamento de configurações para uma pasta fixa offline ou CSC.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Externo</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>Com suporte</p></td>
<td align="left"><p>Novo no UE-V 2,1, esse método de configuração especifica que se as configurações de UE-V são gravadas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como o OneDrive for Business, as pastas de trabalho, o SharePoint ou o Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Essa configuração de configuração foi projetada para a VDI (Virtual Desktop Infrastructure) e a experiência do aplicativo em fluxo principalmente. Essa configuração deve ser usada em caixas do Windows Server usadas em um datacenter, onde a conexão sempre estará disponível.</p>
<p>Todas as alterações de configurações são salvas diretamente no servidor. Se a conexão de rede com o caminho de armazenamento de configurações não estiver disponível, as alterações de configurações serão armazenadas em cache no dispositivo e sincronizadas na próxima vez que o provedor de sincronização for executado. Se o caminho de armazenamento de configurações não for encontrado e o perfil do usuário for removido de um ambiente de VDI em pool no logoff, essas alterações serão perdidas, e o usuário deverá reaplicar a alteração quando o computador puder alcançar novamente o caminho de armazenamento de configurações.</p>
<p>Os aplicativos e o sistema operacional aguardarão indefinidamente o local a ser apresentado. Isso pode causar a carga do aplicativo ou o tempo de logon do sistema operacional para aumentar drasticamente se o local não for encontrado.</p></td>
</tr>
</tbody>
</table>

 

Você pode configurar o método de sincronização das seguintes maneiras:

-   Ao [implantar o UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) por meio de um parâmetro de linha de comando ou em um script em lotes

-   Por meio das configurações de [política de grupo](https://technet.microsoft.com/library/dn458893.aspx)

-   Com o [pacote de configuração do System Center](https://technet.microsoft.com/library/dn458917.aspx) para UE-V

-   Após a instalação do UE-V Agent, usando o [Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows)](https://technet.microsoft.com/library/dn458937.aspx)






## Tópicos relacionados


[Implantar os recursos necessários na UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[Implantar os recursos necessários na UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





