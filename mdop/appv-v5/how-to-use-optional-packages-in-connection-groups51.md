---
title: Como usar pacotes opcionais em grupos de conexão
description: Como usar pacotes opcionais em grupos de conexão
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796297"
---
# Como usar pacotes opcionais em grupos de conexão


A partir do Microsoft Application Virtualization (App-V) 5,0 SP3, você pode adicionar pacotes opcionais a seus grupos de conexão para simplificar o gerenciamento de grupo de conexão. A tabela a seguir resume as tarefas que você pode realizar com mais facilidade usando pacotes opcionais e fornece links para instruções para cada tarefa.

**Observação** 
 **Não há suporte para pacotes opcionais nas versões anteriores ao App-V 5,0 SP3.**

 

Antes de usar pacotes opcionais, consulte [requisitos para usar pacotes opcionais em grupos de conexão](#bkmk-reqs-using-cg).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Link para instruções</th>
<th align="left">Tarefa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">Use um grupo de conexão, com pacotes opcionais, para vários usuários com diferentes pacotes qualificados para eles</a></p></td>
<td align="left"><p>Use um único grupo de conexão para disponibilizar diferentes grupos de aplicativos e plug-ins disponíveis para usuários finais diferentes.</p>
<p>Por exemplo, você deseja distribuir o Microsoft Office para todos os usuários finais, mas distribuir plug-ins diferentes para subconjuntos diferentes de usuários.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">Cancelar a publicação ou excluir um pacote opcional ou cancelar a publicação de um pacote opcional e republicá-lo mais tarde sem alterar o grupo de conexões</a></p></td>
<td align="left"><p>Cancele a publicação, exclua ou publique novamente um pacote opcional sem precisar desabilitar, remover, editar, adicionar e habilitar novamente o grupo de conexão no cliente App-V.</p>
<p>Você também pode cancelar a publicação do pacote opcional e republicá-lo mais tarde sem precisar desabilitar ou republicar o grupo de conexão.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>Use um grupo de conexão, com pacotes opcionais, para vários usuários com diferentes pacotes qualificados para eles


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrição da tarefa</th>
<th align="left">Como executar a tarefa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Com o App-V 5,0 SP3 e o App-V 5,1</strong></p>
<p>Você pode adicionar pacotes opcionais a grupos de conexão, o que permite fornecer diferentes combinações de aplicativos e plug-ins para usuários finais diferentes.</p>
<p><strong>Exemplo </strong> : você deseja distribuir o Microsoft Office para seus usuários finais, mas habilitou um determinado plug-in para apenas um subconjunto de usuários.</p>
<p>Para fazer isso, crie um grupo de conexão que contenha um pacote com o Office e outro pacote com plug-ins do Office e, em seguida, torne opcional o pacote de plug-ins.</p>
<p>Os usuários finais que não estão habilitados para o pacote de plug-in ainda poderão executar o Office.</p></td>
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
<li><p>No console de gerenciamento, selecione <strong> grupos </strong> de conexão para exibir a biblioteca de grupos de conexão.</p></li>
<li><p>Selecione o grupo de conexões correto da biblioteca de grupos de conexão.</p></li>
<li><p>Clique em <strong> Editar </strong> no painel pacotes conectados.</p></li>
<li><p>Selecione <strong> opcional </strong> ao lado do nome do pacote.</p></li>
<li><p>Marque a <strong> caixa de seleção Adicionar acesso ao pacote ao acesso ao grupo </strong> . Esta etapa necessária adiciona ao grupo de conexão os direitos do pacote que você configurou anteriormente ao atribuir pacotes a grupos do Active Directory.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Server-cmdlet do PowerShell</p></td>
<td align="left"><p>Use o cmdlet a seguir e especifique o <strong> parâmetro-Optional </strong> :</p>
<p><strong>Add-AppvServerConnectionGroupPackage</strong></p>
<p><strong>Syntax</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>Exemplo:</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente App-V em um computador autônomo</p></td>
<td align="left"><ol>
<li><p>Crie o documento XML do grupo de conexão e defina o <strong> atributo de marca do pacote </strong> <strong> como isoption </strong> para <strong> "true".</strong></p></li>
<li><p>Use os seguintes cmdlets para adicionar e habilitar o grupo de conexão:</p>
<ul>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>Exemplo de documento XML do grupo de conexão com pacotes opcionais:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Com versões anteriores ao App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Você precisou criar vários grupos de conexão para fazer combinações de aplicativos e plug-in específicos disponíveis para usuários específicos.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>Cancelar a publicação ou excluir um pacote opcional ou cancelar a publicação de um pacote opcional e republicá-lo mais tarde sem alterar o grupo de conexões


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descrição da tarefa</th>
<th align="left">Como executar a tarefa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Com o App-V 5,0 SP3 e o App-V 5,1</strong></p>
<p>Você pode cancelar a publicação, excluir ou publicar novamente um pacote opcional, que está em um grupo de conexão, sem ter que desabilitar ou habilitar novamente o grupo de conexão no cliente App-V.</p>
<p>Você também pode cancelar a publicação de um pacote opcional e republicá-lo mais tarde sem precisar desabilitar ou republicar o grupo de conexão.</p>
<p><strong>Exemplo </strong> : se você publicar um pacote opcional que contém um plug-in do Microsoft Office e deseja remover o plug-in, poderá cancelar a publicação do pacote sem ter que desabilitar o grupo de conexão.</p></td>
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
<td align="left"><ul>
<li><p>Para cancelar a publicação do pacote: no console de gerenciamento, selecione eleger a <strong> </strong> página pacotes, clique ou clique com o botão direito do mouse no pacote que você deseja cancelar a publicação e clique em <strong> Cancelar publicação </strong> .</p></li>
<li><p>Para remover um pacote opcional de um grupo de conexão: na <strong> página grupos de conexão </strong> , selecione o pacote que você deseja remover e clique na seta para a direita para remover o pacote do painel de grupo de conexão na parte inferior esquerda.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente App-V em um computador autônomo</p></td>
<td align="left"><p>Use os seguintes cmdlets existentes:</p>
<ul>
<li><p>Cancelar publicação-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
</ul>
<p>Para obter mais informações, consulte <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> como gerenciar pacotes do App-V 5,1 em execução em um computador autônomo usando o PowerShell </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Com versões anteriores ao App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Você precisou:</p>
<ol>
<li><p>Remova o grupo de conexão de cada computador cliente App-V em que ele foi habilitado.</p></li>
<li><p>Cancele a publicação do pacote.</p></li>
<li><p>Remova o pacote da definição do grupo de conexão.</p></li>
<li><p>Republicar o grupo de conexão.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>Requisitos para usar pacotes opcionais em grupos de conexão


Revise os seguintes requisitos antes de usar pacotes opcionais em grupos de conexão:

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
<td align="left"><p>Os grupos de conexão devem conter pelo menos um pacote não opcional.</p></td>
<td align="left"><ul>
<li><p>Verifique atentamente que você atende a este requisito, pois o servidor do App-V e o cmdlet do PowerShell não validam que a necessidade foi atendida.</p></li>
<li><p>Se você acidentalmente criar um grupo de conexão que não contenha pelo menos um pacote não opcional, e o usuário final tentar abrir um aplicativo empacotado nesse grupo de conexão, o grupo de conexão falhará.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>Os grupos de conexão publicados pelo usuário podem conter pacotes que são publicados globalmente ou para o usuário.</p></li>
<li><p>Os grupos de conexão publicados globalmente devem conter apenas pacotes publicados globalmente.</p></li>
</ul></td>
<td align="left"><p>Os grupos de conexão publicados globalmente devem conter pacotes que são publicados globalmente para garantir que os pacotes estarão disponíveis ao iniciar o ambiente virtual do grupo de conexão.</p>
<p>Se você tentar adicionar ou habilitar os grupos de conexão globalmente publicados que contêm pacotes publicados pelo usuário, o grupo de conexão falhará.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Você deve publicar todos os pacotes não opcionais antes de publicar o grupo de conexão que contém esses pacotes.</p></td>
<td align="left"><p>Um ambiente virtual do grupo de conexão não pode iniciar se houver pacotes não opcionais ausentes.</p>
<p>O cliente App-V falha ao adicionar ou habilitar um grupo de conexão se algum pacote não opcional não tiver sido publicado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Antes de cancelar a publicação de um pacote publicado globalmente, certifique-se de que os grupos de conexão que são habilitados para todos os usuários desse computador não precisem mais do pacote.</p></td>
<td align="left"><p>O sistema não verifica se o pacote faz parte do grupo de conexões de outro usuário. Ao cancelar a publicação de um pacote global, ele não estará disponível para todos os usuários desse computador, portanto certifique-se de que os grupos de conexão de cada usuário não contenham mais o pacote ou que também torne o pacote opcional.</p></td>
</tr>
</tbody>
</table>

 






## Tópicos relacionados


[Gerenciando grupos de conexão](managing-connection-groups51.md)

 

 





