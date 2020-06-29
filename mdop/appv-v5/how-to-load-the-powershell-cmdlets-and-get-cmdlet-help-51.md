---
title: Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets
description: Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796377"
---
# <span data-ttu-id="cb00f-103">Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets</span><span class="sxs-lookup"><span data-stu-id="cb00f-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="cb00f-104">O que este tópico aborda:</span><span class="sxs-lookup"><span data-stu-id="cb00f-104">What this topic covers:</span></span>

-   [<span data-ttu-id="cb00f-105">Requisitos para usar cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="cb00f-106">Carregando os cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="cb00f-107">Obtendo ajuda para os cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="cb00f-108">Exibindo a ajuda para um cmdlet do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="cb00f-109">Requisitos para usar cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="cb00f-110">Examine os seguintes requisitos para usar os cmdlets do PowerShell do App-V:</span><span class="sxs-lookup"><span data-stu-id="cb00f-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb00f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb00f-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="cb00f-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="cb00f-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-113">Os usuários podem executar cmdlets do App-V Server somente se você conceder acesso a eles usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="cb00f-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="cb00f-114">Ao implantar e configurar o servidor App-V </strong> :</span><span class="sxs-lookup"><span data-stu-id="cb00f-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="cb00f-115">Especifique um grupo do Active Directory ou um usuário individual que tenha permissões para gerenciar o ambiente do App-V.</span><span class="sxs-lookup"><span data-stu-id="cb00f-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="cb00f-116">Veja <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> como implantar o servidor do App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb00f-116">See <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="cb00f-117">Depois de implantar o App-V Server </strong> :</span><span class="sxs-lookup"><span data-stu-id="cb00f-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="cb00f-118">Use o console de gerenciamento do App-V para adicionar um usuário ou grupo do Active Directory adicional.</span><span class="sxs-lookup"><span data-stu-id="cb00f-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="cb00f-119">Veja <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> como adicionar ou remover um administrador usando o console de gerenciamento </a> .</span><span class="sxs-lookup"><span data-stu-id="cb00f-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb00f-120">Cmdlets que exigem um prompt de comando elevado</span><span class="sxs-lookup"><span data-stu-id="cb00f-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="cb00f-121">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb00f-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="cb00f-122">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb00f-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="cb00f-123">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb00f-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="cb00f-124">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="cb00f-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="cb00f-125">Remove-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="cb00f-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="cb00f-126">Add-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="cb00f-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="cb00f-127">Remove-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="cb00f-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="cb00f-128">Send-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="cb00f-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="cb00f-129">Set-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="cb00f-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="cb00f-130">Set-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb00f-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="cb00f-131">Set-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="cb00f-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-132">Cmdlets que os usuários finais podem executar, a menos que você os configure para exigir um prompt de comando elevado</span><span class="sxs-lookup"><span data-stu-id="cb00f-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="cb00f-133">Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb00f-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="cb00f-134">Cancelar publicação-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb00f-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="cb00f-135">Para configurar esses cmdlets para exigir um prompt de comando elevado, use um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="cb00f-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb00f-136">Método</span><span class="sxs-lookup"><span data-stu-id="cb00f-136">Method</span></span></th>
<th align="left"><span data-ttu-id="cb00f-137">Mais recursos</span><span class="sxs-lookup"><span data-stu-id="cb00f-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-138">Execute o <strong> cmdlet Set-AppvClientConfiguration </strong> com o <strong> parâmetro-RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="cb00f-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="cb00f-139">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="cb00f-140">Como gerenciar pacotes do App-V 5.1 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-140">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb00f-141">Habilite a configuração da política de grupo "exigir publicação como administrador" para clientes App-V.</span><span class="sxs-lookup"><span data-stu-id="cb00f-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)"><span data-ttu-id="cb00f-142">Como publicar um pacote usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cb00f-142">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="cb00f-143">Carregando os cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-143">Loading the PowerShell cmdlets</span></span>

<span data-ttu-id="cb00f-144">Para carregar os módulos cmdlet do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cb00f-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="cb00f-145">Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="cb00f-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="cb00f-146">Digite um dos seguintes comandos para carregar os cmdlets do módulo que você deseja:</span><span class="sxs-lookup"><span data-stu-id="cb00f-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb00f-147">Componente App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="cb00f-148">Comando para digitar</span><span class="sxs-lookup"><span data-stu-id="cb00f-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-149">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-150">Import-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="cb00f-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb00f-151">Sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-152">Import-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="cb00f-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-153">Cliente App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-154">Import-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="cb00f-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="cb00f-155">Obtendo ajuda para os cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="cb00f-156">A partir do App-V 5,0 SP3, a ajuda do cmdlet está disponível em dois formatos:</span><span class="sxs-lookup"><span data-stu-id="cb00f-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb00f-157">Formato</span><span class="sxs-lookup"><span data-stu-id="cb00f-157">Format</span></span></th>
<th align="left"><span data-ttu-id="cb00f-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb00f-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-159">Como um módulo para download</span><span class="sxs-lookup"><span data-stu-id="cb00f-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-160">Para baixar a ajuda mais recente após o download do módulo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb00f-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="cb00f-161">Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="cb00f-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="cb00f-162">Digite um dos seguintes comandos para carregar os cmdlets do módulo que você deseja:</span><span class="sxs-lookup"><span data-stu-id="cb00f-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb00f-163">Componente App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="cb00f-164">Comando para digitar</span><span class="sxs-lookup"><span data-stu-id="cb00f-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-165">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-166">Update-Help-AppvServer do módulo</span><span class="sxs-lookup"><span data-stu-id="cb00f-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb00f-167">Sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-168">Update-Help-AppvSequencer do módulo</span><span class="sxs-lookup"><span data-stu-id="cb00f-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb00f-169">Cliente App-V</span><span class="sxs-lookup"><span data-stu-id="cb00f-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-170">Update-Help-AppvClient do módulo</span><span class="sxs-lookup"><span data-stu-id="cb00f-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb00f-171">No TechNet como páginas da Web</span><span class="sxs-lookup"><span data-stu-id="cb00f-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb00f-172">Consulte o nó App-V em <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automação do Microsoft Desktop Optimization Pack with Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="cb00f-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="cb00f-173">Exibindo a ajuda para um cmdlet do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb00f-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="cb00f-174">Para exibir a ajuda para um cmdlet específico do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cb00f-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="cb00f-175">Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="cb00f-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="cb00f-176">Cmdlet **Get-Help** &lt; *cmdlet* &gt; do tipo, por exemplo, **Get-Help Publish-AppvClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="cb00f-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="cb00f-177">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="cb00f-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cb00f-178">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="cb00f-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cb00f-179">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="cb00f-179">Got an App-V issue?</span></span>** <span data-ttu-id="cb00f-180">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cb00f-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





