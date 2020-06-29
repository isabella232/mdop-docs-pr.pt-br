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
# <span data-ttu-id="470c0-103">Como usar pacotes opcionais em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="470c0-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="470c0-104">A partir do Microsoft Application Virtualization (App-V) 5,0 SP3, você pode adicionar pacotes opcionais a seus grupos de conexão para simplificar o gerenciamento de grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="470c0-105">A tabela a seguir resume as tarefas que você pode realizar com mais facilidade usando pacotes opcionais e fornece links para instruções para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="470c0-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="470c0-106">**Observação** 
 **Não há suporte para pacotes opcionais nas versões anteriores ao App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="470c0-106">**Note**
**Optional packages are not supported in releases prior to App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="470c0-107">Antes de usar pacotes opcionais, consulte [requisitos para usar pacotes opcionais em grupos de conexão](#bkmk-reqs-using-cg).</span><span class="sxs-lookup"><span data-stu-id="470c0-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="470c0-108">Link para instruções</span><span class="sxs-lookup"><span data-stu-id="470c0-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="470c0-109">Tarefa</span><span class="sxs-lookup"><span data-stu-id="470c0-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="470c0-110">Use um grupo de conexão, com pacotes opcionais, para vários usuários com diferentes pacotes qualificados para eles</span><span class="sxs-lookup"><span data-stu-id="470c0-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="470c0-111">Use um único grupo de conexão para disponibilizar diferentes grupos de aplicativos e plug-ins disponíveis para usuários finais diferentes.</span><span class="sxs-lookup"><span data-stu-id="470c0-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="470c0-112">Por exemplo, você deseja distribuir o Microsoft Office para todos os usuários finais, mas distribuir plug-ins diferentes para subconjuntos diferentes de usuários.</span><span class="sxs-lookup"><span data-stu-id="470c0-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="470c0-113">Cancelar a publicação ou excluir um pacote opcional ou cancelar a publicação de um pacote opcional e republicá-lo mais tarde sem alterar o grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="470c0-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="470c0-114">Cancele a publicação, exclua ou publique novamente um pacote opcional sem precisar desabilitar, remover, editar, adicionar e habilitar novamente o grupo de conexão no cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="470c0-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="470c0-115">Você também pode cancelar a publicação do pacote opcional e republicá-lo mais tarde sem precisar desabilitar ou republicar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="470c0-116">Use um grupo de conexão, com pacotes opcionais, para vários usuários com diferentes pacotes qualificados para eles</span><span class="sxs-lookup"><span data-stu-id="470c0-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="470c0-117">Descrição da tarefa</span><span class="sxs-lookup"><span data-stu-id="470c0-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="470c0-118">Como executar a tarefa</span><span class="sxs-lookup"><span data-stu-id="470c0-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="470c0-119">Com o App-V 5,0 SP3 e o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="470c0-119">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="470c0-120">Você pode adicionar pacotes opcionais a grupos de conexão, o que permite fornecer diferentes combinações de aplicativos e plug-ins para usuários finais diferentes.</span><span class="sxs-lookup"><span data-stu-id="470c0-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="470c0-121">Exemplo </strong> : você deseja distribuir o Microsoft Office para seus usuários finais, mas habilitou um determinado plug-in para apenas um subconjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="470c0-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="470c0-122">Para fazer isso, crie um grupo de conexão que contenha um pacote com o Office e outro pacote com plug-ins do Office e, em seguida, torne opcional o pacote de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="470c0-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="470c0-123">Os usuários finais que não estão habilitados para o pacote de plug-in ainda poderão executar o Office.</span><span class="sxs-lookup"><span data-stu-id="470c0-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="470c0-124">Método</span><span class="sxs-lookup"><span data-stu-id="470c0-124">Method</span></span></th>
<th align="left"><span data-ttu-id="470c0-125">Etapas</span><span class="sxs-lookup"><span data-stu-id="470c0-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470c0-126">Servidor App-V – console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="470c0-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="470c0-127">No console de gerenciamento, selecione <strong> grupos </strong> de conexão para exibir a biblioteca de grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-127">In the Management Console, select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="470c0-128">Selecione o grupo de conexões correto da biblioteca de grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-128">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="470c0-129">Clique em <strong> Editar </strong> no painel pacotes conectados.</span><span class="sxs-lookup"><span data-stu-id="470c0-129">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="470c0-130">Selecione <strong> opcional </strong> ao lado do nome do pacote.</span><span class="sxs-lookup"><span data-stu-id="470c0-130">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="470c0-131">Marque a <strong> caixa de seleção Adicionar acesso ao pacote ao acesso ao grupo </strong> .</span><span class="sxs-lookup"><span data-stu-id="470c0-131">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="470c0-132">Esta etapa necessária adiciona ao grupo de conexão os direitos do pacote que você configurou anteriormente ao atribuir pacotes a grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="470c0-132">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="470c0-133">App-V Server-cmdlet do PowerShell</span><span class="sxs-lookup"><span data-stu-id="470c0-133">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="470c0-134">Use o cmdlet a seguir e especifique o <strong> parâmetro-Optional </strong> :</span><span class="sxs-lookup"><span data-stu-id="470c0-134">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="470c0-135">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="470c0-135">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="470c0-136">Syntax</span><span class="sxs-lookup"><span data-stu-id="470c0-136">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="470c0-137">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="470c0-137">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470c0-138">Cliente App-V em um computador autônomo</span><span class="sxs-lookup"><span data-stu-id="470c0-138">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="470c0-139">Crie o documento XML do grupo de conexão e defina o <strong> atributo de marca do pacote </strong> <strong> como isoption </strong> para <strong> "true".</span><span class="sxs-lookup"><span data-stu-id="470c0-139">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="470c0-140">Use os seguintes cmdlets para adicionar e habilitar o grupo de conexão:</span><span class="sxs-lookup"><span data-stu-id="470c0-140">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="470c0-141">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="470c0-141">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="470c0-142">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="470c0-142">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="470c0-143">Exemplo de documento XML do grupo de conexão com pacotes opcionais:</span><span class="sxs-lookup"><span data-stu-id="470c0-143">Example connection group XML document with optional packages:</span></span></strong></p>
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
<td align="left"><p><strong><span data-ttu-id="470c0-144">Com versões anteriores ao App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="470c0-144">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="470c0-145">Você precisou criar vários grupos de conexão para fazer combinações de aplicativos e plug-in específicos disponíveis para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="470c0-145">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="470c0-146">Cancelar a publicação ou excluir um pacote opcional ou cancelar a publicação de um pacote opcional e republicá-lo mais tarde sem alterar o grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="470c0-146">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="470c0-147">Descrição da tarefa</span><span class="sxs-lookup"><span data-stu-id="470c0-147">Task description</span></span></th>
<th align="left"><span data-ttu-id="470c0-148">Como executar a tarefa</span><span class="sxs-lookup"><span data-stu-id="470c0-148">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="470c0-149">Com o App-V 5,0 SP3 e o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="470c0-149">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="470c0-150">Você pode cancelar a publicação, excluir ou publicar novamente um pacote opcional, que está em um grupo de conexão, sem ter que desabilitar ou habilitar novamente o grupo de conexão no cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="470c0-150">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="470c0-151">Você também pode cancelar a publicação de um pacote opcional e republicá-lo mais tarde sem precisar desabilitar ou republicar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-151">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="470c0-152">Exemplo </strong> : se você publicar um pacote opcional que contém um plug-in do Microsoft Office e deseja remover o plug-in, poderá cancelar a publicação do pacote sem ter que desabilitar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-152">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="470c0-153">Método</span><span class="sxs-lookup"><span data-stu-id="470c0-153">Method</span></span></th>
<th align="left"><span data-ttu-id="470c0-154">Etapas</span><span class="sxs-lookup"><span data-stu-id="470c0-154">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470c0-155">Servidor App-V – console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="470c0-155">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="470c0-156">Para cancelar a publicação do pacote: no console de gerenciamento, selecione eleger a <strong> </strong> página pacotes, clique ou clique com o botão direito do mouse no pacote que você deseja cancelar a publicação e clique em <strong> Cancelar publicação </strong> .</span><span class="sxs-lookup"><span data-stu-id="470c0-156">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, click or right-click the package that you want to unpublish, and click <strong>Unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="470c0-157">Para remover um pacote opcional de um grupo de conexão: na <strong> página grupos de conexão </strong> , selecione o pacote que você deseja remover e clique na seta para a direita para remover o pacote do painel de grupo de conexão na parte inferior esquerda.</span><span class="sxs-lookup"><span data-stu-id="470c0-157">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="470c0-158">Cliente App-V em um computador autônomo</span><span class="sxs-lookup"><span data-stu-id="470c0-158">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="470c0-159">Use os seguintes cmdlets existentes:</span><span class="sxs-lookup"><span data-stu-id="470c0-159">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="470c0-160">Cancelar publicação-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="470c0-160">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="470c0-161">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="470c0-161">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="470c0-162">Para obter mais informações, consulte <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> como gerenciar pacotes do App-V 5,1 em execução em um computador autônomo usando o PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="470c0-162">For more information, see <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="470c0-163">Com versões anteriores ao App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="470c0-163">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="470c0-164">Você precisou:</span><span class="sxs-lookup"><span data-stu-id="470c0-164">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="470c0-165">Remova o grupo de conexão de cada computador cliente App-V em que ele foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="470c0-165">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="470c0-166">Cancele a publicação do pacote.</span><span class="sxs-lookup"><span data-stu-id="470c0-166">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="470c0-167">Remova o pacote da definição do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-167">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="470c0-168">Republicar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-168">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="470c0-169">Requisitos para usar pacotes opcionais em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="470c0-169">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="470c0-170">Revise os seguintes requisitos antes de usar pacotes opcionais em grupos de conexão:</span><span class="sxs-lookup"><span data-stu-id="470c0-170">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="470c0-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="470c0-171">Requirement</span></span></th>
<th align="left"><span data-ttu-id="470c0-172">Detalhes</span><span class="sxs-lookup"><span data-stu-id="470c0-172">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470c0-173">Os grupos de conexão devem conter pelo menos um pacote não opcional.</span><span class="sxs-lookup"><span data-stu-id="470c0-173">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="470c0-174">Verifique atentamente que você atende a este requisito, pois o servidor do App-V e o cmdlet do PowerShell não validam que a necessidade foi atendida.</span><span class="sxs-lookup"><span data-stu-id="470c0-174">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="470c0-175">Se você acidentalmente criar um grupo de conexão que não contenha pelo menos um pacote não opcional, e o usuário final tentar abrir um aplicativo empacotado nesse grupo de conexão, o grupo de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="470c0-175">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="470c0-176">Os grupos de conexão publicados pelo usuário podem conter pacotes que são publicados globalmente ou para o usuário.</span><span class="sxs-lookup"><span data-stu-id="470c0-176">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="470c0-177">Os grupos de conexão publicados globalmente devem conter apenas pacotes publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="470c0-177">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="470c0-178">Os grupos de conexão publicados globalmente devem conter pacotes que são publicados globalmente para garantir que os pacotes estarão disponíveis ao iniciar o ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="470c0-178">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="470c0-179">Se você tentar adicionar ou habilitar os grupos de conexão globalmente publicados que contêm pacotes publicados pelo usuário, o grupo de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="470c0-179">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470c0-180">Você deve publicar todos os pacotes não opcionais antes de publicar o grupo de conexão que contém esses pacotes.</span><span class="sxs-lookup"><span data-stu-id="470c0-180">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="470c0-181">Um ambiente virtual do grupo de conexão não pode iniciar se houver pacotes não opcionais ausentes.</span><span class="sxs-lookup"><span data-stu-id="470c0-181">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="470c0-182">O cliente App-V falha ao adicionar ou habilitar um grupo de conexão se algum pacote não opcional não tiver sido publicado.</span><span class="sxs-lookup"><span data-stu-id="470c0-182">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="470c0-183">Antes de cancelar a publicação de um pacote publicado globalmente, certifique-se de que os grupos de conexão que são habilitados para todos os usuários desse computador não precisem mais do pacote.</span><span class="sxs-lookup"><span data-stu-id="470c0-183">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="470c0-184">O sistema não verifica se o pacote faz parte do grupo de conexões de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="470c0-184">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="470c0-185">Ao cancelar a publicação de um pacote global, ele não estará disponível para todos os usuários desse computador, portanto certifique-se de que os grupos de conexão de cada usuário não contenham mais o pacote ou que também torne o pacote opcional.</span><span class="sxs-lookup"><span data-stu-id="470c0-185">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="470c0-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="470c0-186">Related topics</span></span>


[<span data-ttu-id="470c0-187">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="470c0-187">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





