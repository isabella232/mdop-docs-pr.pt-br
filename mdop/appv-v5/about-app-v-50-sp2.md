---
title: Sobre o App-V 5.0 SP2
description: Sobre o App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796635"
---
# Sobre o App-V 5.0 SP2


O App-V 5.0 SP2 fornece uma plataforma integrada aprimorada, virtualização mais flexível e gerenciamento eficiente para aplicativos virtualizados. Para obter mais informações, consulte [visão geral do App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .

## Alterações na funcionalidade padrão do SP2 do App-V 5.0


As seções a seguir contêm informações sobre as alterações na funcionalidade padrão do App-V 5.0 SP2.

### <a href="" id="bkmk-sp2-supported-cfg"></a>Suporte para Windows Server 2012 R2 e Windows 8,1

O App-V 5,0 inclui suporte para Windows Server 2012 R2 e Windows 8,1

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> O App-V 5.0 SP2 agora oferece suporte ao redirecionamento de pastas para o diretório roaming de AppData do usuário

O aplicativo do App-V 5.0 SP2 dá suporte a roaming AppData (% AppData%) redirecionamento de pastas. Para obter mais informações, consulte o [planejamento para usar o redirecionamento de pastas com o App-V](planning-to-use-folder-redirection-with-app-v.md).

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a>Melhorias na atualização do pacote e tarefas pendentes

No App-V 5.0 SP2, você não é mais solicitado a fechar um aplicativo virtual em execução quando uma versão mais recente do grupo ou do grupo de conexão é publicada. Se um pacote ou grupo de conexão estiver em uso quando você tentar executar uma tarefa relacionada, uma mensagem será exibida para indicar que o objeto está em uso e que a operação será tentada posteriormente.

As tarefas que foram colocadas em um estado pendente serão realizadas de acordo com as seguintes regras:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de tarefa</th>
<th align="left">Regra aplicável</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarefa baseada em usuário, por exemplo, publicar um pacote para um usuário</p></td>
<td align="left"><p>A tarefa pendente será executada após o usuário fazer logoff e, em seguida, fazer logon novamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarefa com base global, por exemplo, habilitar um grupo de conexão globalmente</p></td>
<td align="left"><p>A tarefa pendente será executada quando o computador for desligado e reiniciado.</p></td>
</tr>
</tbody>
</table>

 

Quando uma tarefa é colocada em um estado pendente, o cliente App-V também gera uma chave do registro para a tarefa pendente, da seguinte maneira:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa baseada em usuário ou globalmente</th>
<th align="left">Onde a chave do registro é gerada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarefas baseadas em usuário</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarefas com base global</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

### Virtualizando o Microsoft Office 2013 e o Microsoft Office 2010 usando o App-V 5,0

Use o link a seguir para obter mais informações sobre os cenários do Microsoft Office com suporte para o App-V 5,0.

[Virtualização do Microsoft Office 2013 para Application Virtualization (App-V) 5.0](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

**Observação**  Este documento enfoca a criação de um pacote do Microsoft Office 2013 App-V 5,0. No entanto, ele também fornece informações sobre cenários do Microsoft Office 2010 com o App-V 5,0.

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> Aplicativo da interface de usuário do gerenciamento de cliente do App-V 5,0

Em versões anteriores do App-V 5,0, a interface do usuário de gerenciamento do cliente (UI) foi fornecida com a instalação do aplicativo do aplicativo-V 5,0 Client. Com o App-V 5.0 SP2, isso não é mais o caso. Os administradores agora têm a opção de implantar a interface do usuário do cliente do App-V 5,0 como um aplicativo virtual (usando todas as configurações de implantação do App-V com suporte) ou como um aplicativo instalado.

Para obter mais informações, consulte [aplicativo da interface do usuário do cliente do Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .

### Empacotamento e implantação automáticos do assembly lado a lado (SxS)

O App-V 5.0 SP2 agora detecta automaticamente assemblies lado a lado (SxS) e a implantação no computador que executa o cliente App-V 5.0 SP2. Um assembly SxS consiste principalmente em dependências do tempo de execução do VC + + Runtime ou MSXML. Em versões anteriores do App-V, os aplicativos virtuais que tinham dependências em tempo de execução do VC exigiam que essas dependências fossem localmente no computador executando o cliente App-V 5.0 SP2.

Agora há suporte para a seguinte funcionalidade:

-   O sequenciador do App-V 5,0 captura automaticamente o assembly SxS no pacote, independentemente de o tempo de execução do VC já ter sido instalado no computador que está executando o sequenciador.

-   O cliente App-V 5,0 instala automaticamente o assembly SxS obrigatório para o computador que está executando o cliente, conforme necessário no momento da publicação.

-   O sequenciador do App-V 5,0 relata a dependência do tempo de execução do VC usando o mecanismo de relatório do sequenciador.

-   O sequenciador do App-V 5,0 agora permite que você exclua a dependência do tempo de execução do VC no caso de que a dependência já esteja disponível no computador que executa o sequenciador.

### Melhorias na atualização de publicação

O App-V 5,0 dá suporte a vários recursos foram adicionados para melhorar a experiência geral da atualização de um conjunto de aplicativos para um usuário específico.

A lista a seguir mostra os aprimoramentos de atualização de publicação:

A lista a seguir contém mais informações sobre como habilitar os novos aprimoramentos de atualização de publicação.

-   **EnablePublishingRefreshUI** -habilita a barra de progresso de atualização de publicação do computador que está executando o cliente App-V 5,0.

-   **HideUI** -oculta a barra de progresso de atualização de publicação durante uma sincronização manual.

### Configuração do novo cliente

A configuração do novo cliente a seguir está disponível com o App-V 5,0 SP2:

**EnableDynamicVirtualization** -habilita as extensões do shell com suporte, objetos auxiliares do navegador e controles ActiveX para serem virtualizados e executados com aplicativos virtuais.

Para obter mais informações, consulte [sobre as definições de configuração do cliente](about-client-configuration-settings.md).

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> Extensões do shell do App-V 5,0

O App-V 5,0 SP2 agora oferece suporte a extensões do Shell.

Para obter mais informações, consulte a seção **suporte para extensão do shell do App-v 5.0 SP2** de [criação e gerenciamento de aplicativos virtualizados do app-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).

## <a href="" id="---------app-v-5-0-documentation-updates"></a> Atualizações da documentação do App-V 5,0


O App-V 5,0 SP2 fornece documentação atualizada para os seguintes cenários:

-   [Migração de uma versão anterior](migrating-from-a-previous-version-app-v-50.md)

-   [Sobre o App-V 5.0](about-app-v-50.md)

-   [Sobre relatórios do App-V 5,0](about-app-v-50-reporting.md) (seção de perguntas frequentes)

## Como obter tecnologias do MDOP


O App-V 5,0 é parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .






## Tópicos relacionados


[Notas de versão do App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md)

 

 





