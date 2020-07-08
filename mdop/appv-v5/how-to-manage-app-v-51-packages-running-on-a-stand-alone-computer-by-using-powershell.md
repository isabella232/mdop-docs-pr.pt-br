---
title: Como gerenciar pacotes do App-V 5.1 em execução em um computador autônomo usando o PowerShell
description: Como gerenciar pacotes do App-V 5.1 em execução em um computador autônomo usando o PowerShell
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796369"
---
# Como gerenciar pacotes do App-V 5.1 em execução em um computador autônomo usando o PowerShell


As seções a seguir explicam como executar várias tarefas de gerenciamento em um computador cliente autônomo usando o PowerShell:

-   [Para retornar uma lista de pacotes](#bkmk-return-pkgs-standalone-posh)

-   [Para adicionar um pacote](#bkmk-add-pkgs-standalone-posh)

-   [Para publicar um pacote](#bkmk-pub-pkg-standalone-posh)

-   [Para publicar um pacote para um usuário específico](#bkmk-pub-pkg-a-user-standalone-posh)

-   [Para adicionar e publicar um pacote](#bkmk-add-pub-pkg-standalone-posh)

-   [Para cancelar a publicação de um pacote existente](#bkmk-unpub-pkg-standalone-posh)

-   [Para cancelar a publicação de um pacote para um usuário específico](#bkmk-unpub-pkg-specfc-use)

-   [Para remover um pacote existente](#bkmk-remove-pkg-standalone-posh)

-   [Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes](#bkmk-admins-pub-pkgs)

-   [Noções básicas sobre pacotes pendentes (userpending e GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>Para retornar uma lista de pacotes


Use as informações a seguir para retornar uma lista de pacotes que têm direito a um usuário específico:

**Cmdlet**: Get-AppvClientPackage

**Parâmetros**:-Name-Version-PackageID-VersionId

**Exemplo**: Get-AppvClientPackage-Name "ContosoApplication"-versão 2

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>Para adicionar um pacote


Use as informações a seguir para adicionar um pacote a um computador.

**Importante**  Este exemplo adiciona apenas um pacote. Ele não publica o pacote no usuário ou no computador.

 

**Cmdlet**: Add-AppvClientPackage

**Exemplo**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>Para publicar um pacote


Use as informações a seguir para publicar um pacote que foi adicionado a um usuário específico ou globalmente para qualquer usuário do computador.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método de publicação</th>
<th align="left">Cmdlet e exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publicação para o usuário</p></td>
<td align="left"><p><strong>Cmdlet </strong> : publish-AppvClientPackage</p>
<p><strong>Exemplo </strong> : publish-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicação global</p></td>
<td align="left"><p><strong>Cmdlet </strong> : publish-AppvClientPackage</p>
<p><strong>Exemplo </strong> : publish-AppvClientPackage "ContosoApplication"-global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>Para publicar um pacote para um usuário específico


**Observação**  Você deve usar o pacote de hotfix do App-V 5,0 SP2 5 ou posterior para usar esse parâmetro.

 

Um administrador pode publicar um pacote para um usuário específico especificando o parâmetro opcional **– userid** com o cmdlet **Publish-AppvClientPackage** , em que **-userid** representa o Sid (identificador de segurança) do usuário final.

Para usar esse parâmetro:

-   Você pode executar esse cmdlet a partir da sessão de usuário ou de administrador.

-   Você deve estar conectado com credenciais administrativas para usar o parâmetro.

-   O usuário final deve estar conectado.

-   Você deve fornecer o SID (identificador de segurança) do usuário final.

**Cmdlet**: publish-AppvClientPackage

**Exemplo**: publish-AppvClientPackage "ContosoApplication"-usuáriosid S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>Para adicionar e publicar um pacote


Use as informações a seguir para adicionar um pacote a um computador e publicá-lo para o usuário.

**Cmdlet**: Add-AppvClientPackage

**Exemplo**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publicar-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>Para cancelar a publicação de um pacote existente


Use as informações a seguir para cancelar a publicação de um pacote que tenha sido qualificado para um usuário, mas não remova o pacote do computador.

**Cmdlet**: cancelar publicação-AppvClientPackage

**Exemplo**: cancelar publicação-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>Para cancelar a publicação de um pacote para um usuário específico


**Observação**  Você deve usar o pacote de hotfix do App-V 5,0 SP2 5 ou posterior para usar esse parâmetro.

 

Um administrador pode cancelar a publicação de um pacote para um usuário específico usando o parâmetro opcional **– userid** com o cmdlet **UNPUBLISH-AppvClientPackage** , em que **-userid** representa o Sid (identificador de segurança) do usuário final.

Para usar esse parâmetro:

-   Você pode executar esse cmdlet a partir da sessão de usuário ou de administrador.

-   Você deve estar conectado com credenciais administrativas para usar o parâmetro.

-   O usuário final deve estar conectado.

-   Você deve fornecer o SID (identificador de segurança) do usuário final.

**Cmdlet**: cancelar publicação-AppvClientPackage

**Exemplo**: cancelar publicação-AppvClientPackage "ContosoApplication"-usuáriosid S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>Para remover um pacote existente


Use as informações a seguir para remover um pacote do computador.

**Cmdlet**: Remove-AppvClientPackage

**Exemplo**: Remove-AppvClientPackage "ContosoApplication"

**Observação**  Cmdlets do App-V foram atribuídos a variáveis para os exemplos anteriores somente para fins de esclarecimento; a atribuição não é um requisito. A maioria dos cmdlets pode ser combinada conforme exibido em [para adicionar e publicar um pacote](#bkmk-add-pub-pkg-standalone-posh). Para obter um tutorial detalhado, consulte o [App-V 5,0 Client do PowerShell DeepShip](https://go.microsoft.com/fwlink/?LinkId=324466).

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes


**Observação** 
 **Este recurso tem suporte a partir do App-V 5,0 SP3.**

 

Use o cmdlet e o parâmetro a seguir para habilitar somente administradores (não usuários finais) para publicar ou cancelar a publicação de pacotes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cmdlet</strong></p></td>
<td align="left"><p>Set-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Parâmetro</strong></p></td>
<td align="left"><p>-RequirePublishAsAdmin</p>
<p>Valores de parâmetro:</p>
<ul>
<li><p>0-falso</p></li>
<li><p>1-verdadeiro</p></li>
</ul>
<p><strong>Exemplo: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Para usar o console de gerenciamento do App-V para definir essa configuração, consulte [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-51.md).

## <a href="" id="bkmk-understd-pend-pkgs"></a>Noções básicas sobre pacotes pendentes (userpending e GlobalPending)


A **partir do App-V 5,0 SP2**: se você executar um cmdlet do PowerShell que afeta um pacote que está em uso no momento, a tarefa que você está tentando executar é colocada em um estado pendente. Por exemplo, se você tentar publicar um pacote quando um aplicativo nesse pacote estiver sendo usado e executar **Get-AppvClientPackage**, o status pendente será exibido na saída do cmdlet da seguinte maneira:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item de saída do cmdlet</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Userpending</p></td>
<td align="left"><p>Indica se o pacote listado tem uma tarefa pendente que está sendo aplicada ao usuário:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>Indica se o pacote listado tem uma tarefa pendente que está sendo aplicada globalmente ao computador:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

A tarefa pendente será executada mais tarde, de acordo com as seguintes regras:

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

 

Para obter mais informações sobre tarefas pendentes, consulte [sobre o App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).

**Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

[Administração do App-V 5.1 usando o PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





