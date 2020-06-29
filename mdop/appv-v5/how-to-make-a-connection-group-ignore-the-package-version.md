---
title: Como criar um grupo de conexão para ignorar a versão do pacote
description: Como criar um grupo de conexão para ignorar a versão do pacote
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796380"
---
# Como criar um grupo de conexão para ignorar a versão do pacote


O Microsoft Application Virtualization (App-V) 5,0 SP3 permite que você configure um grupo de conexão para usar qualquer versão de um pacote, que simplifica as atualizações do pacote e reduz o número de grupos de conexão que você precisa criar.

Para atualizar um pacote nas versões anteriores do App-V, você precisava executar várias etapas, incluindo a desabilitação do grupo de conexão e a modificação do arquivo de definição XML do grupo de conexão.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrição da tarefa com o App-V 5,0 SP3</th>
<th align="left">Como executar a tarefa com o App-V 5,0 SP3</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Você pode configurar um grupo de conexão para aceitar qualquer versão de um pacote, o que permite que você atualize o pacote sem precisar desabilitar o grupo de conexão.</p>
<p><strong>Como funciona o recurso:</strong></p>
<ul>
<li><p>Se o grupo de conexão tiver acesso a várias versões de um pacote, a versão mais recente será usada.</p></li>
<li><p>Se o grupo de conexão contiver um pacote opcional com uma versão incorreta, o pacote será ignorado e não bloqueará a criação do ambiente virtual do grupo de conexão.</p></li>
<li><p>Se o grupo de conexão contém um pacote não opcional com uma versão incorreta, o ambiente virtual do grupo de conexão não pode ser criado.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Etapas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor App-V – console de gerenciamento</p></td>
<td align="left"><ol>
<li><p>No console de gerenciamento, selecione <strong> pacotes de conexão de pacotes </strong> &gt; <strong> </strong> .</p></li>
<li><p>Selecione o grupo de conexões correto da biblioteca de grupos de conexão.</p></li>
<li><p>Clique em <strong> Editar </strong> no painel pacotes conectados.</p></li>
<li><p>Marque <strong> </strong> a caixa de seleção usar qualquer versão ao lado do nome do pacote e clique em <strong> aplicar </strong> .</p></li>
</ol>
<p>Para saber mais sobre como adicionar ou atualizar pacotes, consulte <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> como adicionar ou atualizar pacotes usando o console de gerenciamento </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente App-V em um computador autônomo</p></td>
<td align="left"><ol>
<li><p>Crie o documento XML do grupo de conexão.</p></li>
<li><p>Para que o pacote seja atualizado, defina o <strong> atributo de marca do pacote </strong> <strong> VersionId </strong> como um asterisco ( <strong>*</strong> ).</p></li>
<li><p>Use o cmdlet a seguir para adicionar o grupo de conexão e incluir o caminho para o documento XML do grupo de conexões:</p>
<p><strong>Add-AppvClientConnectionGroup</strong></p></li>
<li><p>Ao atualizar um pacote, use os seguintes cmdlets para remover o pacote antigo, adicionar o pacote atualizado e publicar o pacote atualizado:</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Publicar-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>Para obter mais informações, consulte:</p>
<ul>
<li><p>O arquivo XML de exemplo, o <strong> arquivo XML do grupo de conexão com pacotes opcionais </strong> , nesta seção: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> como usar pacotes opcionais em grupos de conexão</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## Tópicos relacionados


[Gerenciando grupos de conexão](managing-connection-groups.md)

 

 





