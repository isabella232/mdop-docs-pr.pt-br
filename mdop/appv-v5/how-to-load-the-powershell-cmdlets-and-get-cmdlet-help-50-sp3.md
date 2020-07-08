---
title: Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets
description: Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets
author: dansimp
ms.assetid: 0624495b-943e-485b-9e54-b50e4ee6591c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 7692d3e36aabc4f3142f664e94d9d71b2cfc1bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796379"
---
# Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets


O que este tópico aborda:

-   [Requisitos para usar cmdlets do PowerShell](#bkmk-reqs-using-posh)

-   [Carregando os cmdlets do PowerShell](#bkmk-load-cmdlets)

-   [Obtendo ajuda para os cmdlets do PowerShell](#bkmk-get-cmdlet-help)

-   [Exibindo a ajuda para um cmdlet do PowerShell](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>Requisitos para usar cmdlets do PowerShell


Examine os seguintes requisitos para usar os cmdlets do PowerShell do App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Os usuários podem executar cmdlets do App-V Server somente se você conceder acesso a eles usando um dos seguintes métodos:</p></td>
<td align="left"><ul>
<li><p><strong>Ao implantar e configurar o servidor App-V </strong> :</p>
<p>Especifique um grupo do Active Directory ou um usuário individual que tenha permissões para gerenciar o ambiente do App-V. Veja <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> como implantar o servidor do App-V 5,0 </a> .</p></li>
<li><p><strong>Depois de implantar o App-V Server </strong> :</p>
<p>Use o console de gerenciamento do App-V para adicionar um usuário ou grupo do Active Directory adicional. Veja <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)"> como adicionar ou remover um administrador usando o console de gerenciamento </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlets que exigem um prompt de comando elevado</p></td>
<td align="left"><ul>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
<li><p>Set-AppvClientConfiguration</p></li>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Remove-AppvClientConnectionGroup</p></li>
<li><p>Add-AppvPublishingServer</p></li>
<li><p>Remove-AppvPublishingServer</p></li>
<li><p>Send-AppvClientReport</p></li>
<li><p>Set-AppvClientMode</p></li>
<li><p>Set-AppvClientPackage</p></li>
<li><p>Set-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Cmdlets que os usuários finais podem executar, a menos que você os configure para exigir um prompt de comando elevado</p></td>
<td align="left"><ul>
<li><p>Publicar-AppvClientPackage</p></li>
<li><p>Cancelar publicação-AppvClientPackage</p></li>
</ul>
<p>Para configurar esses cmdlets para exigir um prompt de comando elevado, use um dos seguintes métodos:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Mais recursos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Execute o <strong> cmdlet Set-AppvClientConfiguration </strong> com o <strong> parâmetro-RequirePublishAsAdmin </strong> .</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Habilite a configuração da política de grupo "exigir publicação como administrador" para clientes App-V.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Como publicar um pacote usando o Console de Gerenciamento</a> </p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>Carregando os cmdlets do PowerShell
Para carregar os módulos cmdlet do PowerShell:

1.  Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).

2.  Digite um dos seguintes comandos para carregar os cmdlets do módulo que você deseja:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente App-V</th>
<th align="left">Comando para digitar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor do App-V</p></td>
<td align="left"><p>Import-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sequenciador App-V</p></td>
<td align="left"><p>Import-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente App-V</p></td>
<td align="left"><p>Import-Module AppvClient</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-get-cmdlet-help"></a>Obtendo ajuda para os cmdlets do PowerShell
A partir do App-V 5,0 SP3, a ajuda do cmdlet está disponível em dois formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Como um módulo para download</p></td>
<td align="left"><p>Para baixar a ajuda mais recente após o download do módulo cmdlet:</p>
<ol>
<li><p>Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</p></li>
<li><p>Digite um dos seguintes comandos para carregar os cmdlets do módulo que você deseja:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente App-V</th>
<th align="left">Comando para digitar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor do App-V</p></td>
<td align="left"><p>Update-Help-AppvServer do módulo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sequenciador App-V</p></td>
<td align="left"><p>Update-Help-AppvSequencer do módulo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente App-V</p></td>
<td align="left"><p>Update-Help-AppvClient do módulo</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>No TechNet como páginas da Web</p></td>
<td align="left"><p>Consulte o nó App-V em <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automação do Microsoft Desktop Optimization Pack with Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-display-help-cmdlet"></a>Exibindo a ajuda para um cmdlet do PowerShell
Para exibir a ajuda para um cmdlet específico do PowerShell:

1.  Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).

2.  Cmdlet **Get-Help** &lt; *cmdlet* &gt; do tipo, por exemplo, **Get-Help Publish-AppvClientPackage**.

**Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V**? Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





